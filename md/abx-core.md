生命周期函数

全局级
模块级别
交易级
画面级

onGlobalMessage

// C端
beforeClosePage
afterClosedPage

isPageInsideMsg:此字段为服务端返回，用来区分下发的socket消息是属于渲染画面的，还是仅仅是交易内部的一段数据；此字段的应用仅在交易级别

onSocketMessage：
executeAsync：.js/.ts文件，如果服务端返回的为逻辑文件，则会默认查找当前文件的executeAsync方法，传入参数并执行


// 梳理执行顺序
创建
[hooks] [GlobalHooks][beforeUpdatePage]
[hooks] [TradeHooks][beforeUpdatePage]

[hooks] [BasicPage][beforeCreateFrame]
[hooks] [GlobalFrameHooks][beforeCreateFrame] // 此处的执行顺序有问题

[hooks] [BasicPage][onCreated]
[hooks] [BasicPage][afterCreatedFrame]

[hooks] [GlobalFrameHooks][afterCreatedFrame]
[hooks] [BasicPage][beforeMountFrame]

[hooks] [GlobalFrameHooks][beforeMountFrame]
[hooks] [BasicPage][beforeCreatePage]
[hooks] [GlobalPageHooks][beforeCreatePage]

[hooks] [BasicPage][onCreated]
[hooks] [FramePageHooks][BasicPage][onCreated]
[hooks] [BasicPage][afterCreatedPage]
[hooks] [BasicPage][afterCreatedPage]
[hooks] [BasicPage][beforeMountPage]
[hooks] [GlobalPageHooks][beforeMountPage]
[hooks] [BasicPage][onMounted]

[hooks] [BasicPage][afterMountedPage]
[hooks] [GlobalPageHooks][afterMountedPage]
[hooks] [BasicPage][onMounted]
[模板][onMounted]
[hooks] [BasicPage][afterMountedFrame]
[hooks] [GlobalFrameHooks][afterMountedFrame]
[hooks] [TradeHooks][afterUpdatedPage]
[hooks] [GlobalHooks][afterUpdatedPage]


销毁
[hooks] [BasicPage][beforeDestroyFrame]
[hooks] [GlobalFrameHooks][beforeDestroyFrame]
[hooks] [BasicPage][beforeDestroyPage]
[hooks] [GlobalPageHooks][beforeDestroyPage]
[hooks] [BasicPage][onDestroy]
[hooks] [FramePageHooks][BasicPage][onDestroy]
[hooks] [BasicPage][afterDestroyedPage]
[hooks] [GlobalPageHooks][afterDestroyedPage]
[hooks] [BasicPage][onDestroy]
[模板][页面销毁]
[hooks] [BasicPage][afterDestroyedFrame]
[hooks] [GlobalFrameHooks][afterDestroyedFrame]
[afterAbortedTrade] [frame]


所以钩子函数的执行是异步，到达某个时机就会触发，即使上一个钩子函数没有完成也不关系，只关心当前的时机要确保钩子函数被执行即可

// onCreated onMounted : page frame 以及vue原本的
1 先看下vue本身的执行顺序是否异步 // 异步
2 frame 和 page的顺序：这个顺序不可以修改，确定后就要按照平台提供的顺序执行

frame:onCreated:args: 服务端的参数
page:onCreated: args: 服务端的参数
page:onMounted
frame:onMounted
onDestroy： 先执行page然后执行frame

和vue原生的周期函数相比，执行顺序:
mixins优先执行
// 钩子函数需要的参数
// 平台的默认处理: 不需要处理
错误处理：不用处理，用户自行处理，只需要进行记录即可






