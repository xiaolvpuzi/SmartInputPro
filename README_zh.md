<p align="center">
	<img alt="logo" src="https://smart-input.oss-cn-hangzhou.aliyuncs.com/logo/smartinputprologo.png" width="150" height="150">
</p>
<h1 align="center" style="margin: 10px 0 10px; font-weight: bold; font-size: 40px">Smart Input Pro​</h1>
<h5 align="center">一个帮助程序员提升编码效率的工具，在确定的场景自动切换到你想要的输入法</h5>

<div align="center">
	
  [![Chinese](https://img.shields.io/badge/语言-中文-blue)](https://github.com/xiaolvpuzi/SmartInputPro/blob/main/README_zh.md)
  [![English](https://img.shields.io/badge/Language-English-red)](https://github.com/xiaolvpuzi/SmartInputPro/blob/main/README.md)
  [![日本語](https://img.shields.io/badge/言語-日本語-green)](https://github.com/xiaolvpuzi/SmartInputPro/blob/main/README_ja.md)
  [![Korean](https://img.shields.io/badge/언어-한국어-purple)](https://github.com/xiaolvpuzi/SmartInputPro/blob/main/README_ko.md)
  [![Russian](https://img.shields.io/badge/Язык-Русский-orange)](https://github.com/xiaolvpuzi/SmartInputPro/blob/main/README_ru.md)
  
</div>


## 解决什么问题

对于母语为中文的开发者，写代码过程中经常需要在中/英输入法之间进行切换，而且由于不清楚当前处于哪种输入状态，有时输入到一半发现输入法错了，删除后重新输入，严重影响了编码效率。

其实，在很多特定场景需要使用哪种输入法是可以明确的，既然这样那就可以让IDE帮助我们自动切换输入法。**Smart Input Pro**可以根据光标所处位置自动切换输入法，用光标颜色表示当前输入法状态，减少因切换输入法导致的输入错误，提升编码的流畅性和效率。

## 解决方案

**Smart Input Pro**通过插件的方式集成到IDE中，可以根据输入位置的上下文智能分析当前处于什么场景应该使用哪种输入法并自动切换，而且还可以通过光标的颜色来提醒用户当前是什么输入法以及大小写状态。以下列举IntelliJ平台IDE的几个核心场景。

- **默认场景：** 大部分主流编程语言在默认区域（除注释区域和字符串区域之外的区域）只能输入ASCII，因此只需要英文输入法，插件识别到您在默认场景时自动帮您切换为英文输入法 [详情](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/scene/default)。

- **注释场景：** 中文母语用户在注释时大概率使用中文输入法，即使需要输入简单的英文也能通过中文输入法输入，插件识别到您在注释场景时自动帮您切换为中文输入法 [详情](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/scene/comment)。

- **Git提交场景：** 中文母语用户在Git提交输入备注信息时大概率使用中文输入法，即使需要输入简单的英文也能通过中文输入法输入，插件识别到您在Git提交场景时自动帮您切换为中文输入法 [详情](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/scene/commit)。

- **工具窗口场景：** 很多工具窗口内都需要特定的输入法，比如Project、Terminal等都需要英文输入法，插件识别到您在特定工具窗口时切换为特定的输入法 [详情](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/scene/toolwindow)。

- **IdeaVim场景：** Vim在NORMAL模式时需要使用英文输入法，否则输入不生效，插件在识别到您进入NORMAL模式时切换为英文输入法，进入INSERT模式时根据光标具体所处的场景切换输入法 [详情](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/scene/idea-vim)。

- **字符串场景：** 字符串字面量可能根据定义名称不同而需要使用不同输入法，插件可以记录您的习惯，为不同名称的字符串字面量切换到您常用的输入法 [详情](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/scene/string)。

- **自定义事件场景：** IDE中发生某件事件时切换成自定义输入法，比如：Translation插件的翻译窗口打开时自动切换为中文输入法，这样您就可以直接输入中文翻译成英文 [详情](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/scene/event)。

- **自定义规则场景：** 在输入字符串等不确定输入法的场景，可以通过自定义正则匹配规则，符合特定规则时切换为特定输入法，比如：光标处于中文文字之间时切换为中文输入法 [详情](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/scene/regular)。

- **离开IDE场景：** Windows系统每个APP的输入法状态是独立的，切换到某个APP恢复内部的输入法状态，MAC系统没有这个功能，因此插件可以实现离开IDE时切换输入法为进入IDE之前的状态 [详情](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/scene/leave)。

## 支持的IDE

目前**Smart Input Pro**支持IntelliJ平台的所有IDE，如IDEA、PyCharm、WebStorm、GoLand、PhpStorm、DataGrip等等，Android Studio 和 DevEco Studio也是基于IntelliJ平台，所以也是支持的。其他平台的IDE插件正在开发中。每种IDE都可能支持多种编程语言，我们无法完全覆盖测试所有场景，所以当您遇到不好的体验，可以反馈给我们，我们会一一优化。

## 支持的编程语言

理论上只要IDE支持的编程语言都支持，但是不同编程语言体验可能不太一样，因为不同编程语言特点不一样。比如，对于`Java`、`Kotlin`、`C`、`C++`、`Python`、`Php`、`Golang`、`JavaScript`、`TypeScript`、`Scala`、`Groovy`等，它们只有在注释区域和字符串字面量中才会使用中文，其他区域都可以肯定要使用英文；对于HTML、Markdown等标记语言，他们没有非常明确的一定使用某种输入法的区域，因此暂时不支持自动切换，但是支持使用光标颜色表示输入法状态。

## 关于付费

**Smart Input Pro**采用增值付费模式，其中基础功能永久免费，高级功能需要付费使用，您可以试用30天，支持按月/年/永久付费订阅，仅需约两杯星巴克咖啡的价格就可以永久使用，越早越优惠，关于定价详情请查看 [功能&定价](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/start/plans-pricing)。您有任何疑问可以通过“效率铺子”企业微信客服联系我们。

**Smart Input Pro**支持微信登录授权，可随时解换绑定设备。也支持通过IntelliJ官方插件市场订阅和授权的方式，IntelliJ官方插件市场需要支付增值税，因此价格稍高于微信授权方式，建议优先通过微信授权方式。如何微信订阅以及获取授权请查看 [授权说明](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/start/authorize)。

## 下载安装

如果您已经熟悉如何下载安装IntelliJ插件，您可以直接在IntelliJ IDE插件市场搜索安装[Smart Input Pro (Chinese)](https://plugins.jetbrains.com/plugin/25280)。您也可以查看详细说明 [下载安装](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/start/download)。

**Smart Input Pro** 分为中国大陆版 **Smart Input Pro (Chinese)** 和海外版 **Smart Input Pro (Japan, South Korea, Russia & more)**，两者主要的区别在于授权方式不同，中国大陆版采用微信授权方式，海外版采用Jetbrains插件市场官方授权方式，您可以根据您的需求选择。中国大陆地区请选择**Smart Input Pro (Chinese)**，费用相比海外版更低。

## 技术支持

我们为 **Smart Input Pro (Chinese)** 写了详细的[介绍文档](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#?from=HomePage/)，阅读介绍文档可以解决大部分问题，[常见问题](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/other/problem)列举了用户经常遇到的问题。如果您需要技术支持，您可以通过关注微信公众号获取技术支持，也可以直接联系“效率铺子”企业微信客服。我们会不断倾听用户的需求去优化产品，非常欢迎您向我们提产品需求。

<p align="center">
	<img alt="微信公众号" src="https://smart-input.oss-cn-hangzhou.aliyuncs.com/picture/qrcode_wechat.png" width="500">
	<p align="center" style="font-size:14px">微信公众号</p>
</p>

<p align="center">
	<img alt="企业微信客服" src="https://smart-input.oss-cn-hangzhou.aliyuncs.com/picture/xiaoer_wechat.png" width="300">
	<p align="center" style="font-size:14px">企业微信客服</p>
</p>

