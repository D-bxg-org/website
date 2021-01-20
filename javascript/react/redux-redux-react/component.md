---
description: 一般组件如何调用store
---

# component

```javascript
import {fun_one} from 'action'

class A extends component{
    
    
    
    fun=()=>{
        const {data} = this.data
        store.dispatch({type:'type_one',data})// 自己手动传入action
        store.dispatch({fun_one})
    }
    
    render(){
        return(
            <div>
                <input ref={c=>this.data=c}>{store.getState()}</input>
            </div>
        )
    }
}
```

