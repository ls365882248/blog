### 记录每日 ugly

#### onScrollToview

> 当内容不足以撑出滚动条时，调用 onScrollToView 页面会调一下

#### 图片加载会导致页面跳动

> 为保证图片的比例，并支持响应式布局，所以初次加载图片页面都会跳动，解决思路使用 image preload

#### react-router

> 在使用 script 标签预加载图片时，如果切换路由到相应的图片。依旧会被 react 加载一遍。达不到预加载的效果。