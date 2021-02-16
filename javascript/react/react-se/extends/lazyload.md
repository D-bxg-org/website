---
description: 懒加载
---

# lazyLoad

配合路由使用，来达到请求时才加载的作用。

```javascript
const Home = lazy(()=>import('./Home'))

<Suspense fallback={<Loding></Loding>}>
    <Switch>
        <Route></Route>
        <Redirect to="/login" />
    </Switch>
</Suspense>
```



