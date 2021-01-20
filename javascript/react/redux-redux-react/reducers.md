---
description: 这里面定义操作状态的方法
---

# reducers

```javascript
// 类组件状态的初始化
const initState = {
    name:'aaa',
    age:16
}
export default function Reducer(preState=initState,action){
    // 【初始化_1】
    // if(preState === undefined) preState = 0;
    
    
    // 获取action对象的type和data
    const{type,data}=action
    // 根据type决定如何处理data
    switch(type){
        case 'type_one':
        
            return ;
        case 'type_two':
        
            return;
        default:
        // 【初始化】
            return preState;
    }
}
```

