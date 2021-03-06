
关于前端
----

先描述一下前端开发者写 React Native 的感受, 有点心理准备.

熟悉 React 可以帮助了解 React Native(后面简写 RN), 然而要完成整个应用是不够的.
从应用开始开发, 到能做发布, 还需要了解比较多的移动平台的知识:

* 了解移动平台布局的细节
* 性能优化
* 设备使用和打包
* 证书和商店

首先 RN 的样式细节和 DOM 有细微差别. 加上前端的路由在移动端用 Navigator 差别较大.
估计在实际开发当中界面部分比较快, 但可能遇到奇怪的坑, 注意移动端的差异.

移动平台首先芯片架构 ARM 就和 X86 不同, 导致后面的参数也无法弥补的性能差距.
同时考虑电池考虑发热 CPU 的运行会受到一些限制.
内存管理方面同时开启大量的应用都会占用内存, 实际上内存还比较吃紧.
(需要补充)
以 Web 开发的经验很难了解移动平台那么多细节, 然而性能优化特别需要做.

开发过程主要是 `adb` `Xcode` 等工具的上手比较麻烦, 有很多琐碎的功能.
React Native 有些步骤涉及到修改 Gradle 配置和 Xcode 中的依赖等等, 需要时间熟悉.

Android 打包相对方便, 然而需要配置秘钥. iOS 也需要证书, 了解 Xcode 的操作等等.
(需要补充)

如果要开发完整的 Native App, 需要的 API 也是 RN 没有充分提供的,
RN 的代码主要提供了 View 层开发的方便.

另外由于 RN 应用几乎和 Redux 做了捆绑, 实际开发需要引入 Redux 的.
虽然不用 Redux 方案上可行, 但是教程稀缺, 会造成非常多的不便.
