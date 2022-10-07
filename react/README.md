```
ReactDOM.render(
React.creatElement('h1', null, 'Hello world!'),
document.getElementById('app')
);
```

the first parameter to createElement is the type of element to be created.
the second parameter is an object that specifies any properties
the third parameter defines a child of the component.


```
ReactDOM.render(
<h1 id="my-heading">
 <span>Hello <em>Wonderful</em></span> world!
</h1>, 
document.getElementById('app')
);
```

```
<!DOCTYPE html>
<html>
<head>
</head>
<body>
<div id="app>
</div>
<script src="react/react.js"> </script>
<script src="react/react-dom.js"></script>
<script src="react/babel.js></srcipt>
<script type="text/babel>
// my app's code
</script>
</body>
</html>
```
note how <script> becomes <script type="text/babel"> this is a trick where, by specifying an invalid type, the browse ignores the code.
  this gives Babel a chance to parse and transform the JSX syntax into something the browser can run.
  
  The process of transpilation is a process of taking source code and rewriting it to accomplish the same results but using syntax that's understood by
  older browsers.
  
  New syntax requires a compilation ( transpilation) step so it's transformed before it's served to the browser.
  
  Client-side transforms are not meant for live production sites as they are slower and more resource intensive than serving already transpiled code.
  
  # CHAPTER 2 The Life Of a Component
  
  there are two ways to define a custom component
  * Using a function
  ```
  <script>
  const MyComponent = function () { 
  return React.createElement('span',null,'I am so custom');
  };
   ReactDOM.render(MyComponent(), document.getElementById('app'));
  </script>
  ```
  
  JSX Version
  ```
   <script>
  const MyComponent = function () { 
     return <span>I am so custom</span>;
  };
   ReactDOM.render(<MyComponent/>, document.getElementById('app'));
  </script>
  ```
  
  * Using a clss that extends React.Component
   ```
  <script>
 
   class MyComponent extends React.Component { 
    render() {
     return React.createElement('span',null,'I am so custom');
     // or with JSX:
    // return <span>I am so custom</span>;
    }
    }
   ReactDOM.render(MyComponent(), document.getElementById('app'));
  </script>
  ```
  
  ```
  class MyComponent extends React.Component {
    render() {
  return <span>My name is <em>{this.props.name}</em></span>;
    }
  }
  ```
  
  ```
  ReactDOM.render( 
    <MyComponent name="Bob" />, document.getElementById('app'));
  );
  ```
  
  
