# props

额外库

```javascript
yarn add prop-types
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

## class组件使用

```javascript
<A name='aaaaaaaa'></A>

class A extends component{
 PropTypes{
  name:PropTypes.string
 }
 render(){
  const {name,age,sex}=this.props
  return(
   <></>
  )
 }
}
```

