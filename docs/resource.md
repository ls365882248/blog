### 资源文章

antd 的故事

> https://zhuanlan.zhihu.com/p/104027273

漫谈 Typescript 研发体系建设
> https://zhuanlan.zhihu.com/p/86276764

恕我直言，你可能连 GitHub 搜索都不会用 - 如何精准搜索的神仙技巧
> https://juejin.im/post/6891056415440535565

不可错过的Webpack核心知识点
> https://mp.weixin.qq.com/s/8De2fcrrj_ZwP5ov5ZVDnA

手写Express.js源码
> https://segmentfault.com/a/1190000037690135

如何突破自己的技术瓶颈期
> https://juejin.im/post/6892315162657685518



## Less

#### extend

```less
h2 {
  &:extend(.style);
  font-style: italic;
}
.style {
  background: green;
}
```
```css
h2 {
  font-style: italic;
}
.style,
h2 {
  background: green;
}
```