# state

## 基本状态

* 是否加载
* 是否第一次

一个组件通常有以下几个状态：

* 是否第一次打开：isFirst
* 加载中：loding
* 出错：error
* 。。。

也就是生命周期函数中的那些函数。

## 类组件

```javascript
import React from 'react';

class Example{
    constructor(props) {
        super(props);
        this.state = {data:0};
    }
    func = ()=>{
        this.setState({data:1});
    }
    render(){
        const {data} = this.state;
        return(
            <div>
                <div>{data}</div>
                <button onClick = {this.func}>button</button>
            </div>
        )
    }
}
```

## 函数组件state hooks

```jsx
import React, { useState } from 'react';

function Example() {
  // 声明一个新的叫做 “count” 的 state 变量
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>//使用state
      <button onClick={() => setCount(count + 1)}>//修改state
        Click me
      </button>
    </div>
  );
}
```
