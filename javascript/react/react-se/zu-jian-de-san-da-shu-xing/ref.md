# ref

## 1. 字符串

```javascript
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
        const {div} = this
        console.log(div.value)
    }
    
    render(){
        return(
            <div>
                <input ref={currentNode => this.div = currentNode} 
                        type="text"
                        placeholder="默认显示"></input>
            </div>
        )
    }
}
```

## 3. createRef()

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
