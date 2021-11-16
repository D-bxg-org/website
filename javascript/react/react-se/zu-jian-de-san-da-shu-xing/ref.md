# ref

## 1. 字符串

```javascript
// 过时，不推荐使用
import React from 'react';

class Example{
    func = ()=>{
        const {div} = this.refs; // 此时获取的是真实dom
    }
    render(){
        return(
            <div>
                <div id="div" ref="div">value</div>
            </div>
        )
    }
}
```

## 2. 回调形式

ref所处的结点的ref属性，里面写的回调函数会受到整个结点传入的参数，就是这个结点本身。

```javascript
class A extends component{
    fun=()=>{
    const {input} = this;
        console.log(input.value)
    }
    
    render(){
        return(
            <div>
                <input ref={Node=>this.input = Node} 
                        type="text"
                        placeholder="默认显示"></input>
            </div>
        )
    }
}
```

```javascript
class A extends component{
    fun=(Node)=>{
    this.input = Node;
    const {input} = this;
        console.log(input.value)
        console.log(Node.value)
    }
    
    render(){
        return(
            <div>
                <input ref={this.fun} 
                        type="text"
                        placeholder="默认显示"></input>
            </div>
        )
    }
}
```

## 3. createRef()

```javascript
import React from 'react';

class test{
    myRef = React.createRef();
    
    fun=()=>{
        alert(this.myRef.current.value);
    }
    
    render(){
        return(
            <div ref = {this.myRef}>
                aa
            </div>
        )
    }
}
```

## 函数组件

```javascript
function test(){
    const myRef = React.useRef().current;// 此处myRef就是div这个DOM对象
    /** 
     * 此处把一个数组存储到了nameRef变量中
     * 因为每次state发生变化都会导致函数组件再次执行
     * 所以我们需要一个只执行一次的变量去存储不会发生变化的变量
     * 该组件的state发生变化时不会导致nameRef这个函数再次执行
     */
    const nameRef = React.useRef([]).current;
    React.useEffect(()=>{
        console.log(myRef.current.style.width)
    },[])// 此处[]请查看useEffect
    return(
        <>
            <div ref={myRef}></div>
        </>
    )
}
```

## 双向绑定

```javascript
import React from 'react';

class Example{
    constructor(props) {
        super(props);
        this.state = {data:0};
    }
    testChange = ()=>{
        const {input} = this.refs;
        this.setState({
            data = input.value;
        })
    }
    render(){
        return(
            <div>
                <input ref="input" onChange = {this.testChange} type = "text">
                <div id="div" ref="div"></div>
            </div>
        )
    }
}
```
