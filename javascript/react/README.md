# react

react也应当算作js库，是一个UI库，但因为它的生态很大，变成了一个围绕着这个库的框架，但其实框架并不是指react本身，而是围绕react、额外添加了很多库的最后的一个大文件，是框架。

因此我们称react是框架，单独拿出来讲，而不放在js库内。

{% embed url="https://www.bilibili.com/video/BV1wy4y1D7JT" %}

一个完整的react项目，通常使用的依赖，或其他相似依赖。（2021年1月18日16:10:42）

```javascript
"@apollo/client": "^3.3.7",//apollo，中间件，graphql的一种实现
"@testing-library/jest-dom": "^5.11.4",//create-react-app脚手架自带
"@testing-library/react": "^11.1.0", //create-react-app脚手架自带
"@testing-library/user-event": "^12.1.10",//create-react-app脚手架自带
"antd": "^4.10.2",//组件库
"axios": "^0.21.1", //ajax的一种实现
"graphql": "^15.4.0", //
"pubsub-js": "^1.9.2", //两个组件之间传递状态值
"react": "^17.0.1",
"react-dom": "^17.0.1", 
"react-router-dom": "^5.2.0",//react-router的web版
"react-scripts": "4.0.1", //create-react-app脚手架自带
"redux": "^4.0.5",//管理状态用
"redux-thunk": "^2.3.0",//redux的action中异步方法支持
"web-vitals": "^0.2.4"//create-react-app脚手架自带
```

