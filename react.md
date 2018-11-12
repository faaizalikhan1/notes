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