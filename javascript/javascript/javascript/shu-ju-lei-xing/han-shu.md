# 函数

高阶函数

```javascript
function parent(child){
   return child()
}

parent(function(){
   console.log('I am child')
})
```

