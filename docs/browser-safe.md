### 浏览器安全

> 分为两种 Web 和 二进制

#### Web页面安全

安全策略： 同源策略

localStorage.aaa = 1;

window.open window.opener

同源策略

为什么存在跨域 

js 为什么不能直接操作文件

一哥 sql 二哥 xss

爬虫反爬虫

CORS(跨域资源共享)

JSONP

简单请求/非简单请求

预检， OPTIONS

实现跨域

跨域消息机制（window.postMessage）

#### 浏览器网络安全

#### 浏览器系统安全

1 XSS(Cross-Site Scripting)  CSP 内容安全策略
  CSP 是让服务器决定浏览器能够加载哪些资源，让服务器决定浏览器是否能够执行内联 js 代码。（怎么做）

2 CSRF(Cross Site Request Forgery)

3 点击劫持

4 URL 跳转漏洞

5 SQL 注入

6 OS 命令注入攻击

前端脚本安全

1 浏览器安全
2 xss 跨站脚本攻击
3 csrf 跨站点请求伪造
4 clickjacking 点击劫持


服务器安全

1 sql 注入

2 文件上传漏洞

3 认证与会话管理

4 访问控制

5 加密算法


### 正文

#### 同源策略

Same Origin Policy, 对于开发人员深入理解同源策略是必要的

```html

<script> <img> <iframe> <link>

```
本质上也是发送了一次 get 请求， 不同于 XMLHttpRequest 不被限制罢了

Dom Cookie XMLHttpRequest, 加载一些插件也是受同源策略控制， Flash

同源图片

##### DOM 层面

> window.open

##### 数据层面

> localStorage

##### 网络层面

XMLHttpRequest

#### Question

会引发什么问题

1 页面中嵌入第三方资源

2 跨域资源共享

#### xss

跨站脚本攻击(XSS)


CSP (Content Security Policy)

#### csrf
跨站点请求伪造(CSRF)

session cookie third-party cookie


#### 现在的浏览器对于安全方面做了什么

框架？

Vue/React/Angular

> https://www.zhihu.com/question/338939262

React 漏洞
prerender
ssr
dangerouslySetInnerHTML

#### jsx -> DOM

1。 createDomElement
2、updateDOMProperties
3、setInnerHTML
4、setTextContent


#### angular

为了系统性的防范 XSS 问题，Angular 默认把所有值都当做不可信任的。 当值从模板中以属性（Property）、DOM 元素属性（Attribte)、CSS 类绑定或插值等途径插入到 DOM 中的时候， Angular 将对这些值进行无害化处理（Sanitize），对不可信的值进行编码

安全环境
  HTML/样式/URL/资源 url

> https://angular.cn/guide/security#offline-template-compiler

angular CSP