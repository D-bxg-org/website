---
description: 错误边界
---

# Error boundary

父组件中的子组件出了问题，不影响父组件渲染，就是“错误边界”的作用。

适用于生产环境（部署后，或者说打包后），开发环境还是会继续报错，这是没问题的。

使用下面的的方法

```jsx
state={
    hasError:false
}
//当parent的子组件出现报错，触发该方法，并携带错误信息参数。
static getDerivedStateFromError(error){
    return {hasError:error}
}
componentDidCatch(){
    //在此处统计出错次数，返回给后台
}
render(){
    const {hasError} = this.state
    return (
        {hasError ? <h1>有错</h1> : <Child></Child>}
    )
}
```

