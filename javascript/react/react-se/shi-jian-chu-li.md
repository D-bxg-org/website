# 事件处理

事件会传入一个参数，叫event。这个传入的参数的target值是DOM本身。因此我们可以使用这个参数来获取DOM的一些值。

```jsx
import React,{Component} from react

const App = ()=>{
  const onclick = (event)=>{
    let val = event.target.value;
    console.log(val); // 将会输出：I'm value
  }
  return(
    <div>
      <div onClick={onclick}>I'm value</div>
    </div>
  );  
};
export default App;
```

不要过度使用ref是指，如果我们要获取的值，就是触发事件的组件本身，那么我们完全可以用传进来的参数：event.target。

但如果我们要获取的DOM元素的值和触发事件的DOM元素不是同个，我们就需要使用ref来获取到需要获取值的DOM元素。

