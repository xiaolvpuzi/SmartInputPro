<p align="center">
	<img alt="logo" src="https://smart-input.oss-cn-hangzhou.aliyuncs.com/logo/smartinputprologo.png" width="150" height="150">
</p>
<h1 align="center" style="margin: 10px 0 10px; font-weight: bold; font-size: 40px">Smart Input Pro​</h1>
<h5 align="center">An IntelliJ IDE Plugin to help programmers improve coding efficiency. Automatically switch input method.</h5>

# Abstract

**Jetbrains IntelliJ IDE Plugin** [**Smart Input Pro ​(Japan,​ South Korea,​ Russia & more)​**](https://plugins.jetbrains.com/plugin/25751)

Automatically switch input method according to the position of the cursor. Displays the current language on the cursor. Avoid typos and coding errors caused by language switching. This feature is particularly beneficial for developers whose mother tongue is not English, such as Chinese, Japanese, Korean and Russian, etc. At the same time, it is also a necessary extension of IdeaVim.


## What problems are solved

Many developers in the world are not English. Developers often need to switch between mother tongue and English input method in the process of writing code. Sometimes it is not clear which input method is currently used, which seriously affects coding efficiency.

In fact, in many specific scenarios, which input method needs to be used is very clear. In this way, you can let the IDE help us switch the input method automatically. **Smart Input Pro​** is to help programmers improve coding efficiency. Its core function is to help you switch to the input method you want in the determined scenario. In more aspects, it will help programmers to improve coding efficiency.

## Solution

**Smart Input Pro​** Integrate to the IDE by plug-in. It can intelligently analyze what scenarios are currently in the context of the input position and what input method is needed, and automatically switch to the corresponding input method. It can also remind users which input method to use by cursor color. Next list several core scenarios of the Intellij IDE.

- **Default Scenario:** Most of the mainstream programming languages can only enter ASCII in the default area (except the annotation area and the string area), and the input method is automatically switched to the English input method when the default scenario is recognized [Details](http://xiaolvpuzi.cn/smart-input-pro-doc.html#/en/scene/default).

- **Comment Scenario:** Most developers will choose to use their mother tongue when writing code comments. Even if you need to enter simple English, you can use the mother tongue input method. In this scenario, the input method will be automatically switched to the mother tongue input method [Details](http://xiaolvpuzi.cn/smart-input-pro-doc.html#/en/scene/comment).

- **Git Commit Scenario:** Most developers will choose to use their mother tongue when writing git commit message. Even if you need to enter simple English, you can use the mother tongue input method. In this scenario, the input method will be automatically switched to the mother tongue input method [Details](http://xiaolvpuzi.cn/smart-input-pro-doc.html#/en/scene/commit).

- **Tool Window Scenario:** Many tool windows require specific input methods, such as Project and Terminal requires English input methods. The plug-in can identify the current tool window and switch to the corresponding input method [Details](http://xiaolvpuzi.cn/smart-input-pro-doc.html#/en/scene/toolwindow).

- **Ideavim Scenario:** Vim needs to use the English input method when the Normal mode, otherwise the input will not take effect. When the plug-in recognizes the Normal mode, it will be automatically switched to the English input method. When the plug-in recognizes the INSERT mode, the input method is switched according to the scenario of the cursor [Details](http://xiaolvpuzi.cn/smart-input-pro-doc.html#/en/scene/idea-vim).

- **String Scenario:** When you enter the string word, you need to use different input methods according to the variable names. The plug-in can record your habits and switch to your commonly used input method [Details](http://xiaolvpuzi.cn/smart-input-pro-doc.html#/en/scene/string).

- **Custom Events Scenario:** When an event occurs in the IDE, the plug-in will automatically switch to the corresponding input method. For example, when the window of the translation plugin is opened, the plug-in will be switched to the input method as the mother tongue. You can directly enter the mother tongue [Details](http://xiaolvpuzi.cn/smart-input-pro-doc.html#/en/scene/event).

- **Customized Rules Scenario:** Scenes that are uncertain input method such as input string, etc. You can use custom regular matching rules. When the strings at the cursor meet specific rules, the plug-in will automatically switch the corresponding input method. For example, when the cursor is between Chinese text, the plug-in will be switched to Chinese input method [Details](http://xiaolvpuzi.cn/smart-input-pro-doc.html#/en/scene/regular).

- **Leave the IDE Scenario:** Windows System's input method of each app is independent, switch to a certain app to restore the internal input method status, the MAC system does not have this function, so the plug-in can help you achieve this feature [Details](http://xiaolvpuzi.cn/smart-input-pro-doc.html#/en/scene/leave).

## Support IDE

**Smart Input Pro​** support all IDEs on the Intellij platform and VSCode platform, Such as IDEA, PyCharm, WebStorm, GoLand, PhpStorm, DataGrip, etc. Android Studio and DevEco Studio are also based on the Intellij platform, so it is also supported. The IDE plug-in of other platforms is under development. Each IDE may support a variety of programming languages. We cannot completely cover all the scenes, so when you encounter a bad experience, you can feedback it to us, we will optimize them one by one.

## Support Programming Language

The plug-in supports all programming languages, but the experience of different programming languages may not be the same because different programming language characteristics are different. For example, `Java`, `Kotlin`, `C`, `C++`, `Python`, `Php`, `Golang`, `JavaScript`, `TypeScript`, `Scala`, `Groovy` and other programming languages, Only mother tongue can be used in the comment area and string, and other areas can be used in English; HTML, Markdown and other marking languages do not have a very clear input method. Therefore, automatic switching is not turned on by default, but supports the use of cursor colors to indicate the state of input method.

## Freemium

This product adopts a value-added payment model. It can be tried value-added functions within 30 days. After the trial, you can use basic functions for free. After activation, value-added functions can be used. Later you can also activate through the following path: Main Menu >> Help >> Register. For pricing details, please check [Features & Pricing](/en/start/plans-pricing).

- Automatically switch input method in the **Default Scenario**. (Free)
- Displays the current input method on the cursor. (Free)
- Shows the Caps Lock status on the cursor. (Free)
- Automatically switch input method in the **Comment Scenario**. (Paid)
- Automatically switch input method in the **Git Commit Scenario**. (Paid)
- Automatically switch input method in the **Tool Window Scenario**. (Paid)
- Automatically switch input method in the **Ideavim Scenario**. (Paid)
- Automatically switch input method in the **String Scenario**. (Paid)
- Automatically switch input method in the **Custom Events Scenario**. (Paid)
- All other functions. (Paid)


## Download and Installation

If you are already familiar with how to download and install IntelliJ plugins, you can directly search and install [Smart Input Pro (Japan, South Korea, Russia & more](https://plugins.jetbrains.com/plugin/25751-smart-input-pro-japan-south-korea-russia--more-) in the IntelliJ IDE plugin market. You can also check the detailed instructions [Download and Installation](http://xiaolvpuzi.cn/smart-input-pro-doc.html#/en/start/download).

**Smart Input Pro​** is divided into the Chinese mainland version [Smart Input Pro (Chinese)](https://plugins.jetbrains.com/plugin/25280) and the marketplace version [Smart Input Pro (Japan, South Korea, Russia & more](https://plugins.jetbrains.com/plugin/25751-smart-input-pro-japan-south-korea-russia--more-). The main difference between the two is the authorization method. The Chinese mainland version uses WeChat authorization, and the marketplace version uses the official Jetbrains plugin market authorization method. You can choose according to your needs. Please choose **Smart Input Pro (Chinese)** for mainland China.

## Technical Support

We have written detailed [introduction documentation](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/en) for **Smart Input Pro**. Reading the introduction documentation can solve most problems. You can also submit issues on [GitHub](https://github.com/SmartInput/SmartInput/issues).

## 中文支持

中国大陆区域请下载 **Smart Input Pro (Chinese)** 版本，该版本支持微信登录授权模式，费用更低，我们为 **Smart Input Pro (Chinese)** 写了详细的[介绍文档](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/)，阅读介绍文档可以解决大部分问题。如果您需要技术支持，您可以通过关注微信公众号获取技术支持。

