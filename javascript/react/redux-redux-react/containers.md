---
description: 容器组件
---

# containers

属于react-rodux

```javascript
import {connect} from 'react-redux'
import {fun_one} from '../../redux/action'

class A extends component{

}
/** 
 * redux容器
 * 这个是实际暴露的组件
 */
export default connect(
    /** 
     * mapStateToProps
     * 这里放的是UI能在props里读取的属性
     * 这个state就是store最后传出来的reducers
     */
    (state)=>({}),
    /** 
     * mapDispatchToProps
     * 这里放的是UI能在props里读取的方法
     */
    {
     fun_one_reactRedux:fun_one
    }
)(A)
```

