### Remember

Answer these on your own, then compare answers as a group

1.  What is React?
  - React is a javascript library that uses Component based architecture to structure single-page web applications. 

2.  What is create-react-app?
  - create-react-app is a package that is used to create a boiler plate React application folder. That folder is pre-structured and populated with the necessary dependencies/modules in order for the React application to run.

3.  What is Component Based Architecture?
  - Component Based Architecture is a process in which sections of our code are segmented and compartmentalized into smaller more manageable pieces, this facilitates navigation of our code and increases the efficiency of debugging that code. 

4.  What is JSX?
  - JSX is a mixture of Javascript and XML, JSX uses an almost identical tag structure to html but allows us the possibility to insert javascript within those tags. 

5.  What is the virtual DOM?
  - A lightweight version of the actual DOM which acts as an intermediary between our react components and our actual DOM. The virtual DOM will recognize data changes made to elements in JSX and will only update the actual DOM when needed. This increases performance of our applications to prevent unnecessary rendering of unchanged elements. 

6.  What is unidirectional (one-way) data flow?
  - Unidirectional data flow is a form of data management in which data is stored in it's top most parent component and that data and methods to change that data are only passed downwards to children components as props. Children are able to use the data passed down, as well as the methods to change that data because the context of our methods was bound to the parent component object and it's state. 

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`

8.  Summarize the steps for forking and cloning a repo with an existing React app. How does this process differ from the process of creating a new React app on your laptop?

9.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

10.  Explain how data is passed from a parent component to a child component.

### Apply

Try these on your own, but work together if you start to get stuck.

11.  Use `create-react-app` to create a new React application called `student-directory`

12.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

13. What are the benefits and drawbacks of using a tool like create-react-app?

14. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

15. Compare and contrast one-way data flow with two-way data binding.
