### 记录每日 ugly

#### onScrollToview

> 当内容不足以撑出滚动条时，调用 onScrollToView 页面会调一下

#### 图片加载会导致页面跳动

> 为保证图片的比例，并支持响应式布局，所以初次加载图片页面都会跳动，解决思路使用 image preload

#### react-router

> 在使用 script 标签预加载图片时，如果切换路由到相应的图片。依旧会被 react 加载一遍。达不到预加载的效果。

#### flex 

> flex 布局是使得滚动条无法触顶
为什么 flex 会影响滚动条的行为

#### 实现一个运行时的数据校验
  > typescript-is typescript-json-schema ajv jsonschema yup runtypes

#### 实现一个宽高等比例元素(16:9)的 div 元素

  > https://www.w3schools.com/howto/howto_css_aspect_ratio.asp

#### windows 模态框内部点击失效
  > 主页面元素设置了 -webkit-app-regin: drag;

#### 前端模块化
  CommonJS 模块输出的是一个值的拷贝，ES6 模块输出的是值的引用。

#### bash command  
  在 **package.json** 中添加配置
  ```
  "bin": {
    "cut-yml": "index.ts"
  }

  ```
  > cut-yml 为 command index.ts 为命令执行的文件， 另外在 index.ts 需要加上一个声明

  ``` 
  #! /usr/bin/env ts-node
  ...
  ```