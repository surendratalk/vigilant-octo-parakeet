Components
import React from 'react'
import ReactDOM from 'react-dom'
class Hello extends React.Component {
  render () {
    return <div className='message-box'>
      Hello {this.props.name}
    </div>
  }
}
const el = document.body
ReactDOM.render(<Hello name='John' />, el)
Use the React.js jsfiddle to start hacking. (or the unofficial jsbin)

Import multiple exports
import React, {Component} from 'react'
import ReactDOM from 'react-dom'
class Hello extends Component {
  ...
}
Properties
<Video fullscreen={true} autoplay={false} />
render () {
  this.props.fullscreen
  const { fullscreen, autoplay } = this.props
  ···
}
 
 
Use this.props to access properties passed to the component.

See: Properties

States
constructor(props) {
  super(props)
  this.state = { username: undefined }
}
this.setState({ username: 'rstacruz' })
render () {
  this.state.username
  const { username } = this.state
  ···
}
 
 
Use states (this.state) to manage dynamic data.

With Babel you can use proposal-class-fields and get rid of constructor

class Hello extends Component {
  state = { username: undefined };
  ...
}
See: States

Nesting
class Info extends Component {
  render () {
    const { avatar, username } = this.props

    return <div>
      <UserAvatar src={avatar} />
      <UserProfile username={username} />
    </div>
  }
}
As of React v16.2.0, fragments can be used to return multiple children without adding extra wrapping nodes to the DOM.

import React, {
  Component,
  Fragment
} from 'react'

class Info extends Component {
  render () {
    const { avatar, username } = this.props

    return (
      <Fragment>
        <UserAvatar src={avatar} />
        <UserProfile username={username} />
      </Fragment>
    )
  }
}
Nest components to separate concerns.

See: Composing Components

Children
<AlertBox>
  <h1>You have pending notifications</h1>
</AlertBox>
 
class AlertBox extends Component {
  render () {
    return <div className='alert-box'>
      {this.props.children}
    </div>
  }
}
 
Children are passed as the children property.

#Defaults
Setting default props
Hello.defaultProps = {
  color: 'blue'
}
 
See: defaultProps

Setting default state
class Hello extends Component {
  constructor (props) {
    super(props)
    this.state = { visible: true }
  }
}
 
Set the default state in the constructor().

And without constructor using Babel with proposal-class-fields.

class Hello extends Component {
  state = { visible: true }
}
 
See: Setting the default state

#Other components
Functional components
function MyComponent ({ name }) {
  return <div className='message-box'>
    Hello {name}
  </div>
}
 
Functional components have no state. Also, their props are passed as the first parameter to a function.

See: Function and Class Components

Pure components
import React, {PureComponent} from 'react'

class MessageBox extends PureComponent {
  ···
}
 
Performance-optimized version of React.Component. Doesn’t rerender if props/state hasn’t changed.

See: Pure components

Component API
this.forceUpdate()
this.setState({ ... })
this.setState(state => { ... })
this.state
this.props
These methods and properties are available for Component instances.

See: Component API

#Lifecycle
Mounting
constructor (props)	Before rendering #
componentWillMount()	Don’t use this #
render()	Render #
componentDidMount()	After rendering (DOM available) #
componentWillUnmount()	Before DOM removal #
componentDidCatch()	Catch errors (16+) #
Set initial the state on constructor(). Add DOM event handlers, timers (etc) on componentDidMount(), then remove them on componentWillUnmount().

Updating
componentDidUpdate (prevProps, prevState, snapshot)	Use setState() here, but remember to compare props
shouldComponentUpdate (newProps, newState)	Skips render() if returns false
render()	Render
componentDidUpdate (prevProps, prevState)	Operate on the DOM here
Called when parents change properties and .setState(). These are not called for initial renders.

See: Component specs
