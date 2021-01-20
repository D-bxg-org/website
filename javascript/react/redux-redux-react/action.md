# action

```javascript
export const fun_one = data=>({type:'type_one',data})

export const fun_two = (data,time)=>{
    return (dispatch)=>{
        setTimeout(()=>{
            dispatch(fun_one(data))
        },time)
    }
}
```

