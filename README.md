# React Idle Timer
> React.js port of jQuery.idleTimer with some extras.

:rocket: **Now  with [Babel 6](https://github.com/babel/babel) and [react-transform](https://github.com/gaearon/babel-plugin-react-transform) support**

[![NPM](https://nodei.co/npm/react-idle-timer.png?downloads=true&stars=true)](https://npmjs.org/package/react-idle-timer/)

# Installation
`npm install react-idle-timer`

# Usage

> check the examples directory for a working example

```javascript
import React from 'react'
import IdleTimer from 'react-idle-timer';

class YourApp extends React.Component {
  constructor(props) {
    super(props)
  }

  render() {
    return (
      <IdleTimer
        ref="idleTimer"
        element={document}
        activeAction={this._onActive}
        idleAction={this._onIdle}
        timeout={this.state.timeout}
        format="MM-DD-YYYY HH:MM:ss.SSS">

        <h1>All your children</h1>

      </IdleTimer>
    )
  }
}
module.exports = YourApp

```

# Documentation

## Props

- **timeout** {*Number*} - Idle timeout in milliseconds
- **events** {*Array*} - Events to bind
- **idleAction** {*Function*} - Function to call on idle
- **activeAction** {*Function*} - Function to call on active
- **element** {*Object*} - Defaults to document, may pass a ref to another element
- **format** {*String*} - moment.js format string applied to `lastActiveTime`

## Methods

- **reset()** *{Void}* - Resets the idleTimer
- **pause()** *{Void}* - Pauses the idleTimer
- **resume()** *{Void}* - Resumes a paused idleTimer
- **getRemainingTime()** *{Number}* - Returns the remaining time in milliseconds
- **getElapsedTime()** *{Number}* - Returns the elapsed time in milliseconds
- **lastActiveTime()** *{String}* - Returns the last active time as a number or a formatted string if the `format` prop is defined
- **isIdle()** {*Boolean*} - Returns whether or not user is idle


