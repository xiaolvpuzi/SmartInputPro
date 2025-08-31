<p align="center">
	<img alt="logo" src="https://smart-input.oss-cn-hangzhou.aliyuncs.com/logo/smartinputprologo.png" width="150" height="150">
</p>
<h1 align="center" style="margin: 10px 0 10px; font-weight: bold; font-size: 40px">Smart Input Pro​</h1>
<h4 align="center">プログラマのコード作成効率を向上させるツールで、特定のシーンで自動的に望む入力法に切り替える</h4>


---


## どんな問題を解決するのか

日本語を母語とする開発者は、コードを書く際に頻繁に日本語/英語入力法の切り替えが必要です。また、現在の入力状態がどのようになっているか把握できず、入力中に間違った入力法を使用していることに気づき、削除して再入力しなければならないことがあり、コード作成の効率に深刻な影響を及ぼします。

実は、多くの特定のシーンではどの入力法を使用するかは明確にできます。そうであれば、IDEに入力法の自動切り替えを手伝ってもらうことができます。**Smart Input Pro**は、カーソルの位置に応じて自動的に入力法を切り替え、カーソルの色で現在の入力法状態を表示し、入力法の切り替えによる入力ミスを減らして、コーディングの流暢さと効率を向上させます。

## ソリューション

**Smart Input Pro**はプラグイン形式でIDEに統合され、入力位置のコンテキストに基づいて現在のシーンに応じてどの入力方式を使用すべきかをインテリジェントに分析し自動的に切り替えることができる。また、カーソルの色によって現在の入力方式や大文字/小文字の状態をユーザーに通知することもできる。以下にIntelliJプラットフォームのIDEにおけるいくつかのコアシーンを挙げる。

- **デフォルトシーン：** 大半の主流プログラミング言語では、デフォルト領域（コメント領域と文字列領域を除く領域）ではASCII文字しか入力できないため、英語入力法のみが必要です。プラグインはデフォルトシーンと認識すると、自動的に英語入力法に切り替えてくれます [詳細](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja/scene/default)。

- **コメントシーン：** 日本のプログラマーはコメント時に日本語入力法を使用する確率が高く、簡単な英語の入力が必要な場合でも日本語入力法で入力できます。プラグインはコメントシーンと認識すると自動的に日本語入力法に切り替わります[詳細](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja/scene/comment)。

- **Gitコミットシーン：** 日本のプログラマーはGitコミット時にコメント入力の際、おそらく日本語入力法を使用し、簡単な英語の入力が必要な場合でも日本語入力法で入力できます。プラグインはGitコミットシーンを認識すると自動的に日本語入力法に切り替えてくれます[詳細](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja/scene/commit)。

- **ツールウィンドウシーン：** 複数のツールウィンドウでは特定の入力法が必要です。例えば、Project、Terminalなどはすべて英語入力法を必要とします。プラグインは特定のツールウィンドウ内で動作していることを認識し、対応する入力法に切り替えます[詳細](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja/scene/toolwindow)。

- **IdeaVimシーン：** VimはNORMALモード時に英語入力法を使用する必要があります。それ以外の入力では効果がありません。プラグインは、NORMALモードに入った際に英語入力法に切り替え、INSERTモードに入った際にはカーソルが具体的にいるシーンに応じて入力法を切り替えます[詳細](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja/scene/idea-vim)。

- **文字列シーン：** 文字列リテラルは定義名によって異なる入力方式を必要とする場合があり、プラグインはあなたの習慣を記録し、異なる名前の文字列リテラルにあなたがよく使う入力方式に切り替えることができます[詳細](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja/scene/string)。

- **カスタムイベントシーン：** IDEで特定のイベントが発生した際にカスタム入力法に切り替える、例えば：翻訳プラグインの翻訳ウィンドウが開くと自動的に日本語入力法に切り替わり、日本語を直接入力して英語に翻訳できます [詳細](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja/scene/event)。

- **カスタムルールシーン：** 入力文字列などの入力方法が不確定なシーンでは、カスタム正規表現マッチングルールを使用して、特定のルールに合致した際に特定の入力方法に切り替えることができます。例えば、カーソルが日本文字の間にある場合に日本語入力方法に切り替える [詳細](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja/scene/regular)。

- **IDEシーンから離れること：** Windowsシステムでは各APPの入力メソッド状態が独立しており、あるAPPに切り替える際に入力メソッドの内部状態を復元します。MACシステムにはこの機能がないため、プラグインはIDEから離れたら入力メソッドをIDEに入る前の状態に切り替えることができます[詳細](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja/scene/leave)。

## 対応IDE

現在、**Smart Input Pro​**はIntelliJプラットフォームのすべてのIDE（IDEA、PyCharm、WebStorm、GoLand、PhpStorm、DataGripなど）をサポートしています。Android StudioとDevEco StudioもIntelliJプラットフォームに基づいているため、こちらもサポート対象です。他のプラットフォームのIDEプラグインは現在開発中です。各IDEは複数のプログラミング言語をサポートする可能性があり、すべてのシナリオを完全にカバーしてテストすることはできません。もし不具合や改善点がありましたら、ご報告ください。一つ一つ改善していきます。

## サポートされているプログラミング言語

理論的にはIDEがサポートするプログラミング言語であればすべてサポートしていますが、異なるプログラミング言語では体験が異なる可能性があります。これは異なるプログラミング言語の特徴が異なるためです。例えば、`Java`、`Kotlin`、`C`、`C++`、`Python`、`Php`、`Golang`、`JavaScript`、`TypeScript`、`Scala`、`Groovy`などでは、コメント領域と文字列リテラルのみで日本語を使用し、その他の領域では確実に英語を使用します。HTML、Markdownなどのマークアップ言語では、特定の入力法を使用する明確な領域がないため、現在は自動切り替えをサポートしていませんが、カーソルの色で入力法の状態を表示することをサポートしています。


## ダウンロードとインストール

もしIntelliJプラグインのダウンロードとインストール方法に既に慣れている場合は、IntelliJ IDEプラグインマーケットで直接[Smart Input Pro (Japan, South Korea, Russia & more)](https://plugins.jetbrains.com/plugin/25751-smart-input-pro-japan-south-korea-russia--more-)を検索してインストールできます。また、詳細な手順は[Download and Installation](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja/start/download)で確認できます。

**Smart Input Pro**は中国本土版[Smart Input Pro (Chinese)](https://plugins.jetbrains.com/plugin/25280)とマーケットプレイス版[Smart Input Pro (Japan, South Korea, Russia & more)](https://plugins.jetbrains.com/plugin/25751-smart-input-pro-japan-south-korea-russia--more-)に分かれています。両者の主な違いは認証方法で、中国本土版はWeChat認証を使用し、マーケットプレイス版は公式のJetbrainsプラグインマーケット認証方法を使用しています。ご自身のニーズに応じて選択してください。中国本土の方は**Smart Input Pro (Chinese)**をお選びください。

## 技術サポート

**Smart Input Pro**の詳細な[導入ドキュメント](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ja)を執筆しました。導入ドキュメントを読めば、ほとんどの問題が解決できます。また、[GitHub](https://github.com/SmartInput/SmartInput/issues)に問題を報告することもできます。
