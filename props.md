### Remember

Answer these on your own, then compare answers as a group

1.  What are props?
  - Props is an object of key/value data pairs accessible to a child component of another parent component. The props object with those key/value pairs is passed down by the parent 

2.  How do you pass props from a parent to a child?
  - In our return/render on our parent component, we attach a key/value pair within a specific JSX tag: "<Child myValue={this.state.myvalue} />"

3.  How do you access props from a class-based child component?
  - Within the child class component we accept props into our constructor as and argument, then we invoke the super method passing in props "super(props);" within our constructor. This will ensure that this.props is available to our entire component as well as our constructor!
    ```
    class MyComp extends Component {
      constructor(props){
        super(props)
      }
      render(){
        return (
          <h1>{this.props.title}</h1>
        )
      }
    }
    ```

4.  How do you access props from a functional component?
  - Within the functional component declaration we accept props in as an argument, after that, the props object is now available to use in the component with "props.myPropName" 
    ```
    function MyComp(props){
      return (
          <h1>{props.title}</h1>
      )
    }
    ```

5.  How do you bind a function to a parent component so that it can be passed to a child?
 - this.function = this.function.bind(this) inside the constructor for a class component.
 

### Understand

Discuss this question in pairs if you have a 4-person group

6.  What's happening in this component?

```jsx
import React, { Component } from "react";

class Queue extends Component {
  constructor() {
    super();

    this.state = {
      questions: []
    };

    this.askQuestion = this.askQuestion.bind(this);
    this.answerQuestion = this.answerQuestion.bind(this);
  }
  askQuestion(newQuestion) {
    const questions = [...this.state.questions, newQuestion];
    this.setState({ questions });
  }
  answerQuestion(index) {
    const questions = [...this.state.questions];
    questions.splice(index, 1);
    this.setState({ questions });
  }
  render() {
    <div className="queue-container">
      <h1>The Queue</h1>
      <h3>{this.state.questions.length}</h3>
      <h3>questions need answers</h3>
      <Student askQuestion={this.askQuestion} />
      <Mentor answerQuestion={this.answerQuestion} />
    </div>;
  }
}
```

### Apply

Try these on your own, but work together if you start to get stuck.

7.  Using the `Queue` component above, create a `Student` component that can add a question as a string and a `Mentor` component that can remove a question from the array.

### Analyze, Evaluate, Create

Discuss these questions as a group

8.  In the Queue component above, why are we holding state in the Queue component instead of Mentor or Student?
