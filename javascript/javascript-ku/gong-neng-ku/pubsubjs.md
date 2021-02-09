---
description: 消息订阅与发布技术
---

# PubSubJS

引入方法

```javascript
yarn add pubsub-js
&
cnpm i --save pubsub-js
```

使用案例

A组件（发布）

```javascript
import PubSub from 'pubsub-js'

class A extends React.PureComponent{
    state={}
    
    fun=()=>{
        PubSub.publish('name',this.state)
    }
    
    render(){
        this.fun()
        return(
            <></>
        )
    }
}
```

B组件（接受）

```javascript
import PubSub from 'pubsub-js'

class B extends React.PureComponent{
    state={}
    componentDidMount(){
        PubSub.subscribe('name',(msg,data)=>{
            //data == A.state
            this.setState(data)
        })
    }
}
```

