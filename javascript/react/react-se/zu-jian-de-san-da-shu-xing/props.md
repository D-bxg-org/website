# props

额外库

```javascript
yarn add prop-types
```

## 类组件

```javascript
// Parent.jsx
import React from 'react';
import Son from 'Son';

class Parent{
    constructor(props) {
        super(props);
        this.state = {
            num:1,
            sex:"男"
        }
    }
    render(){
        const p = this.state;
        return(
            <div>
                <Son {...p}></Son>
            </div>
        )
    }
}
```

```javascript
// Son.jsx
import React from 'react';

export default class Son{
    constructor(props) {
        super(props);
    }
    render(){
        const {num,sex} = this.props;
        return(
            <div>
                <div>{num},{sex}</div>
            </div>
        )
    }
}
```

## 函数组件

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return (
    <div>
      <Welcome name="Sara" />
      <Welcome name="Cahal" />
      <Welcome name="Edite" />
    </div>
  );
}

ReactDOM.render(
  <App />,
  document.getElementById('root')
);
```
