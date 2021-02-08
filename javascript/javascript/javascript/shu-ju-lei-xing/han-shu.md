# 函数

高阶函数

> 参考：
>
> [https://juejin.cn/post/6844903892124172301](https://juejin.cn/post/6844903892124172301)

```javascript
function parent(child){
   return child()
}

parent(function(){
   console.log('I am child')
})
```

