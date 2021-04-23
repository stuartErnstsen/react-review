### Remember

Use https://reactjs.org/docs/react-component.html#the-component-lifecycle and http://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/ to answer these on your own then compare answers as a group

1.  Each component has several `lifecycle methods` that you can override to do what?
  - Run some type of logic/function during a specific period of our components being placed into the DOM and the viewport, while the component is being displayed and data is changing for that component, and finally when our component is being removed from the viewport and the DOM. We can run code when a component loads, is updated, or unloads etc. 

2.  What are the 4 categories of lifecycle methods? (these are the headings from the first link)
  constructor, mounting, updating, unmounting

3.  What are the names of the 5 commonly used lifecycle methods? (these are in bold in the first link)
  constructor, render, componentDidMount, componentDidUpdate, componentWillUnmount

### Understand

Discuss this question in pairs if you have a 4-person group

4.  What's going on in this code?

```jsx
import React, { Component } from "react";

class Mentor extends Component {
  componentDidUpdate() {
    console.log("Dwight saved the day!");
  }
  render() {
    return (
      <div>
        <h1>Dwight Schrute</h1>
        <h2>{this.props.questions.length}</h2>
        <h3>questions to answer</h3>
        <button onClick={this.props.answerQuestion}>Answer a question!</button>
      </div>
    );
  }
}
```

### Apply

Try these on your own, but work together if you start to get stuck.

5.  Update the `Mentor` component above so that the message that is currently being console.log'd is displayed below the number of questions to answer instead.
