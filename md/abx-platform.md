1 abx_libs: sdk库和UI组件库等无法直接通过npm下载的资源
2 node_modules: 第三方依赖
3 abx-module-compile： 模块编译脚本
4 package.json: 下载依赖
5 dist/ABX/: 编译后的目录

升级步骤：
1 先验证本地4.0壳子上可以跑通示例交易
2 保证node的版本
3 重新下载依赖
4 部署资源
5 编译
6 测试访问
7 通知AEC以及ABM更新


// 升级过程中的问题
1 polyfill文件的加载顺序问题
2 如果挂载的交易id不对，
3 错误处理机制
4 监听销毁的问题


// 升级后的语法
1 v-model

交易级
证件/证件信息:证件类型
证件/证件信息:证件.证件类型

全局
@证件/证件信息:证件类型
@证件/证件信息:证件.证件类型











