# state

## 基本状态

* 是否加载
* 是否第一次

## 函数组件

```jsx
import React, { useState } from 'react';

function Example() {
  // 声明一个新的叫做 “count” 的 state 变量
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>//使用state
      <button onClick={() => setCount(count + 1)}>//修改state
        Click me
      </button>
    </div>
  );
}
```

