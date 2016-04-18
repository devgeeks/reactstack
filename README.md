# ReactStack

_In the spirit of README Driven Development, this is a work in progress that probably doesn't work yet._

This project is inspired by / cherry picked from [`react-navigation-controller`][1] and [`backstack`][2]

    npm install reactstack --save


## API:

### Functions

- stack.popAll()
- stack.popView()
- stack.pushView()
- stack.replaceAll()
- stack.replaceView()

### Events (?? maybe just react lifecycle?)

- viewChanging
- viewChanged
- viewActivate
- viewDeactivate

### Fields

- viewsStack
- activeView
- defaultPushTransition
- defaultPopTransition

### Component

    import React from 'react';
    import { transitions, stack }, ReactStack from 'reactstack';   

    const App = React.createClass({
      render() {
        const props = {
          // The views to place in the stack
          viewsStack: [
            <Home />,
          ],
          defaultPushTransition: transitions.SLIDE_LEFT,
          defaultPopTransition: transitions.SLIDE_LEFT,
        };
        return (
          <ReactStack { ...props }/>
        );
      }
    };
    
    export default App;




[1]: https://github.com/aputinski/react-navigation-controller
[2]: https://github.com/pwalczyszyn/backstack
