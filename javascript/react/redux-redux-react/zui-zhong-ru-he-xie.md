# 最终如何写

## 如何写

1. 在containers里写容器组件，把UI和容器用react-redux提供的connect\(\)\(\)混成一个。
2. 在index.js中，在App组件外侧包裹一个Provider组件，该组件由react-redux提供，里面传入store。
3. 不必使用store的监测改变方法。react-redux封装了。
4. mapDispatchToProps简写成一个对象
5. 最终版：
   1. 定义UI组件
   2. ```javascript
      export default connect(
          /** 
           * mapStateToProps
           * 这里放的是UI能在props里读取的属性
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
   3. 在UI中使用this.props读取状态和操作

