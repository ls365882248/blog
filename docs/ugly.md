### 记录每日 ugly

#### onScrollToview

> 当内容不足以撑出滚动条时，调用 onScrollToView 页面会调一下

#### 图片加载会导致页面跳动

> 为保证图片的比例，并支持响应式布局，所以初次加载图片页面都会跳动，解决思路使用 image preload

#### react-router

> 在使用 script 标签预加载图片时，如果切换路由到相应的图片。依旧会被 react 加载一遍。达不到预加载的效果。

#### flex

> flex 布局是使得滚动条无法触顶
> 为什么 flex 会影响滚动条的行为

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

#### angular change detection

**ChangeDetectionStrategy.OnPush** 停止变更检测
**detach** 停止变更检测
**reattach** 重启变更检测（仅适用于被禁用分支的顶层组件中，如果父组件禁用变更检测，将不会生效

> this.cd.detach(); ChangeDetectionStrategy.OnPush 功能相似
> 对组件内部数据变更忽略，父组件参数变更依旧会检测

#### angular FormControl setErrors 无效

> 因为 abstrctControl.updateValueAndValidity() 重置了 error 信息

#### 在 select 选择 observable 作为参数时， formControl 无法控制异常状态

> formGroup 使用错误

#### formControl markAsDirty 需要点击两次才会生效

> 需要在 setError 之前 markAsDirty

#### less 中使用 fade 报错

```less
@white: rgb(0, 0, 0); // eorr
color: fade(@white, 60);
```

#### 修改 zorro botton hover

> 需要覆写 antd base.less 下的 a:hover 样式

#### 在 webpack modules rules 使用 exclude 不起作用

> 在 tsconfig.json 中设置 exclude
> [参考](https://jkchao.github.io/typescript-book-chinese/faqs/tsconfig-behavior.html#%E4%B8%BA%E4%BB%80%E4%B9%88%E6%8A%8A%E4%B8%80%E4%B8%AA%E6%96%87%E4%BB%B6%E6%94%BE%E5%85%A5%E3%80%8Cexclude%E3%80%8D%E9%80%89%E9%A1%B9%E4%B8%AD%EF%BC%8C%E5%AE%83%E4%BB%8D%E7%84%B6%E4%BC%9A%E8%A2%AB%E7%BC%96%E8%AF%91%E5%99%A8%E9%80%89%E4%B8%AD%EF%BC%9F)

#### react 定义一个有 children 的类型

> React.PropsWithChildren

#### css 模块化

> https://segmentfault.com/a/1190000016952542

#### antd tab 右侧小蓝条

> .ant-tabs-ink-bar

#### ngc 报 Cannot write file 'xxx.js' because it would overwrite input file

> 在 angular 10 模块模块间的相对引用导致，改为绝对路径即可

#### build 报 The inferred type of 'onResize' cannot be named without a reference to 'lodash.debounce/node_modules/@types/lodash'. This is likely not portable. A type annotation is necessary.

> 类型推断错误， 有可能本地和 Linux 机器的环境的差异导致的类型推断错误！

#### angular 9 -> 10 样式打包后丢失

> encapsulation: ViewEncapsulation.None

#### 词云自定义图形，放大到一定尺寸后，画布变空

#### 修改 less 变量值，热更新会 node 爆栈

> 升级 node 版本 10+ -> 12+

#### 使用 @bixi/label-angular 报 workSrc 找不到

> engine="./bixi-label-engine/index.html?dev=true"

#### Array.fill()

> https://codesandbox.io/s/pedantic-gagarin-l4bse?file=/src/index.js

#### vscode prettier tslint 冲突

```json
{
  "printWidth": 100, // 超过最大值换行
  "overrides": [
    {
      "files": ".prettierrc",
      "options": { "parser": "json" }
    }
  ],
  "tabWidth": 4, // 缩进字节数
  "semi": true, // 句尾添加分号
  "singleQuote": true, // 使用单引号代替双引号
  "proseWrap": "preserve", // 默认值。因为使用了一些折行敏感型的渲染器（如 GitHub comment）而按照 markdown 文本样式进行折行
  "arrowParens": "avoid", // (x) => {} 箭头函数参数只有一个时是否要有小括号。avoid：省略括号
  "bracketSpacing": true, // 在对象，数组括号与文字之间加空格 "{ foo: bar }"
  "disableLanguages": ["vue"], // 不格式化 vue 文件，vue 文件的格式化单独设置
  "endOfLine": "auto", // 结尾是 \n \r \n\r auto
  "eslintIntegration": false, //不让 prettier 使用 eslint 的代码格式进行校验
  "htmlWhitespaceSensitivity": "ignore",
  "ignorePath": ".prettierignore", // 不使用 prettier 格式化的文件填写在项目的.prettierignore 文件中
  "jsxBracketSameLine": false, // 在 jsx 中把'>' 是否单独放一行
  "jsxSingleQuote": false, // 在 jsx 中使用单引号代替双引号 "prettier.parser": "babylon", // 格式化的解析器，默认是 babylon
  "requireConfig": false, // Require a 'prettierconfig' to format prettier
  "stylelintIntegration": false, //不让 prettier 使用 stylelint 的代码格式进行校验
  "trailingComma": "es5", // 在对象或数组最后一个元素后面是否加逗号（在 ES5 中加尾逗号）
  "prettier.tslintIntegration": false // 不让 prettier 使用 tslint 的代码格式进行校验
}
```

#### fix arrow function semicolon

> "semicolon": [true, "always", "ignore-bound-class-methods"]

#### typescript extends

```ts
type A<T> = T extends "x" ? "a" : "b";

type Other = A<"x" | "y">; // 'a' | 'b'
type Merge<T> = T extends "x" ? T : Other;
type Merge2<T> = T extends "x" ? Other : T;

type Values = Merge<"x" | "y">; // 'x' | 'a' | 'b'
type Value2 = Merge<"x" | "y">; // 'y' | 'a' | 'b'

type Filter<T, U> = T extends U ? never : T;
// 类似 Diff
type Value3 = Filter<"x" | "y" | "z", "x">; // 'y' | 'z'
```

> 因为类型的不确定性，做了 **推迟解析条件类型的处理**， 所以返回了一个联合类型（条件不确定时返回所有值）

#### infer

#### git not support password instead token

> https://shliang.blog.csdn.net/article/details/119698015?utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-1.no_search_link&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-1.no_search_link
