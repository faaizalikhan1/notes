- Is a library for creating UI's.

- Does not operate directly on the DOM, but a virtual DOM.
- Divide everything into components.

- To render, it must return a single element, thus nesting everything inside a tag(or div). But this can be avoided with **React.Fragment**

- Instead of a wrapper div, just add <React.Fragment> around the tags, or just <> and </>.

- For adding class names, using for loops, etc, use camel case (className, htmlFor), as class and for are reserved keywords.

- Stateless component can recieve data and render it, but can't track changes to the data. It's just a function.

```
const BlogPostExcerpt = () => {
  return (
    <div>
      <h1>Title</h1>
      <p>Description</p>
    </div>
  )
} 
```

- Stateful component is a class, which manages state(tracks changes to the state).
```
import React, { Component } from 'react'

class BlogPostExcerpt extends Component {
  render() {
    return (
      <div>
        <h1>Title</h1>
        <p>Description</p>
      </div>
    )
  }
}
```

- Main rendering is done through **ReactDom.render()**.

- JSX is transpiled to objects.

- Can be used without JSX too.

- Prop-types library introduces type checking in react.

- Props can become html arrtributes.

- State is an object that records and reacts to user events.

- There can be only one default export per file.

- For multiple exports in the same file, use **export {}** and import with **{}**.

- Initial state can only be set in component's contructor method.

- State's values can be changed in render, before return, can also be passed to a variable, in turn to use in another component.

- No need to import stylesheet for every component(If using a common stylesheet).

- Inline styles can be added as objects ({{style_object-here}}), and in the object -
  
```
let style={'color':'red', 'font-size':'30px'}
```

- JSX prevents injection attacks.

- JSX is compiled to **React.createElement** by Babel.

- No need to import stylesheet in every component declaration, importing the stylesheet in the center where all components are used, works same.

- Element is rendered by ReactDOM (ReactDOM.render(element, html_tag_to_be_rendered_on))

- React elements are immutable (Once created, can't change children or attributes).

- Elements can also be created with function declaration, and passing props as a parameter in it:

```
function Ptst(props){
  return <i>Hello, {props.name}</i>;
}
```

- State is similar to props, but its private and fully controlled by the component. States are available with components defined as classes.

- Mounting- When a component is added to DOM, it's called **mounting**, and when it's removed, it's called **unmounting**.

- Use setState to modify a state:
```
this.setState({});
```

- Remember to bind the function to the state in the construtor (Using **this.name_here = this.name_here.bind(this);**).

- Only bind those, where the state is being changed, if the state is being read, it's not needed to bind that.

- Refs are created to access DOM nodes directly within react. To create a ref, in the constructor:

```
    this.refNameHere = React.createRef()

```

and to add a ref:
```
ref={this.refNameHere}
```

and to access it's value:
```
this.refNameHere.current.value
```


