# useCallback()

```javascript
import React from 'react';

export default function Test(){
    
    let init = React.useCallback(()=>{
    },[])// 这个函数只会在[]内检测的变量发生变化时才再次执行
    
    React.useEffect(){()=>{
        init();
    },[]}
    return(){
        <>
            <div onClick={add}>{count}</div>
        </>    
    }
}
```
