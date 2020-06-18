### 测试工具

#### 集成测试 integration

#### 单元测试 unit

  jest/mocha/chai

#### 自动化测试 e2e

nightwatch/cypress/puppeteer/Selenium/CasperJS/Protractor/TestCafe/CodeceptJS


##### cypress 
特点：不需要复杂配置，直接上手写测试用例，可视化查看测试结果

##### nightwatch
依赖： nodejs/nightwatch/webdriver/selenium server
配置：nightwatch.json/base setting/extended setting/webdriver setting/selenium setting

balabala

##### puppeteer 
puppeteer 是一个 headless 浏览器，可以用最新版本浏览器去跑页面，puppeteer 通过 CDP 获取浏览器数据

创建浏览器实例

**获取页面元素**
- page.$('#uniqueId')：获取某个选择器对应的第一个元素
- page.$$('div')：获取某个选择器对应的所有元素
- page.$x('//img')：获取某个 xPath 对应的所有元素
- page.waitForXPath('//img')：等待某个 xPath 对应的元素出现
- page.waitForSelector('#uniqueId')：等待某个选择器对应的元素出现

**用户行为**
- element.click()
- element.tap() 手指触摸
- element.focus()
- elelment.hover()
- element.type('balabala') 在输入框中输入内容

**请求拦截**

监听页面中的 request 事件, page.on(type)

- close 关闭
- console console API 被调用
- error 页面错误
- load 页面加载完
- request 收到请求
- requestfailed 请求失败
- requestfinished 请求成功
- response 收到响应
- workercreated 创建 webWorker
- workerdestroyed 销毁 webWorkder

**获取 websocket 响应**

**植入 javascript 代码**

**抓取 iframe 中元素**

**页面性能分析**

**文件上传下载**

**tab 页跳转**

**模拟不同设备**

##### puppeteer vs selenium vs phantomjs vs casperjs

stars: 61.8k vs 17.8 vs 27.8k vs 7.3k

**puppeteer vs selenium**

> https://segmentfault.com/a/1190000020081371

**puppeteer vs phantomjs**

放弃维护

phantomjs 环境安装复杂， api 不友好

phantomjs 使用了较老版本的 webkit 作为渲染引擎

puppeteer 会有更好的性能表现

**puppeteer vs casperjs**

casperjs 是基于 phantomjs

##### protractor

protractor 是一个针对 angular 应用的 e2e 测试框架