<p align="center">
	<img alt="logo" src="https://smart-input.oss-cn-hangzhou.aliyuncs.com/logo/smartinputprologo.png" width="150" height="150">
</p>
<h1 align="center" style="margin: 10px 0 10px; font-weight: bold; font-size: 40px">Smart Input Pro​</h1>
<h5 align="center">프로그래머의 코딩 효율성을 높이는 도구로, 특정 시나리오에서 원하는 입력법으로 자동 전환됩니다</h5>


---


## 어떤 문제를 해결하는가

한국 개발자들은 코딩 과정에서 자주 한국어/영어 입력법 간에 전환해야 하는데, 현재 어떤 입력 상태인지 모를 때가 있어 반 중간에 입력법이 잘못된 걸 발견하고 삭제한 후 다시 입력해야 해서 코딩 효율이 크게 떨어진다.

사실, 많은 특정 시나리오에서 어떤 입력법을 사용해야 하는지 명확히 할 수 있기 때문에 IDE가 입력법을 자동으로 전환하도록 도울 수 있습니다. **Smart Input Pro**는 커서 위치에 따라 자동으로 입력법을 전환하며, 커서 색상을 통해 현재 입력법 상태를 표시해 입력법 전환으로 인한 입력 오류를 줄이고 코딩의 유연성과 효율성을 높입니다.

## 해결책

**Smart Input Pro**는 플러그인 방식으로 IDE에 통합되어 입력 위치의 상下文에 따라 현재 어떤 시나리오에서 어떤 입력 방식을 사용해야 하는지 지능적으로 분석하고 자동으로 전환할 수 있으며, 커서의 색상으로 사용자에게 현재 어떤 입력 방식과 대소문자 상태인지 알려줄 수 있습니다. 아래는 IntelliJ 플랫폼 IDE의 몇 가지 핵심 시나리오를 나열한 것입니다.

- **기본 시나리오:** 대부분의 주류 프로그래밍 언어는 기본 영역(주석 영역과 문자열 영역을 제외한 영역)에서 ASCII만 입력할 수 있으므로 영어 입력법만 필요합니다. 플러그인이 기본 시나리오로 감지되면 자동으로 영어 입력법으로 전환됩니다. [자세히](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/scene/default).

- **댓글 작성 시:** 한국 사용자는 댓글을 작성할 때 대부분 한글 입력기를 사용하며, 간단한 영어를 입력해야 할 때도 한글 입력기를 통해 입력할 수 있습니다. 플러그인이 댓글 작성 시나리오를 감지하면 자동으로 한글 입력기로 전환합니다 [자세히 알아보기](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/scene/comment).

- **Git 커밋 시나리오:** 한국 사용자는 Git 커밋 시 메모를 입력할 때 대부분 한국어 입력법을 사용하며, 간단한 영어를 입력해야 할 때도 한국어 입력법으로 입력할 수 있습니다. 플러그인이 Git 커밋 시나리오를 감지하면 자동으로 한국어 입력법으로 전환해 줍니다. [자세히 보기](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/scene/commit).

- **도구 창 시나리오:** 많은 도구 창에서는 특정 입력기가 필요합니다. 예를 들어 Project, Terminal 등은 영어 입력기가 필요하며, 플러그인이 특정 도구 창에서 사용하는 경우 해당 입력으로 전환합니다 [자세히](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/scene/toolwindow).

- **IdeaVim 시나리오:** Vim이 NORMAL 모드일 때는 영어 입력 방식을 사용해야 합니다. 그렇지 않으면 입력이 반영되지 않습니다. 플러그인은 NORMAL 모드로 진입할 때 영어 입력 방식으로 전환하고, INSERT 모드로 진입할 때 커서가 위치한 구체적인 시나리오에 따라 입력 방식을 전환합니다. [자세히](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/scene/idea-vim).

- **문자열 시나리오:** 문자열 리터럴은 정의된 이름에 따라 다른 입력법을 사용해야 할 수 있으며, 플러그인은 사용자의 습관을 기록하여 다른 이름의 문자열 리터럴에 대해 자주 사용하는 입력법으로 전환할 수 있습니다 [자세히](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/scene/string).

- **사용자 정의 이벤트 시나리오:** IDE에서 특정 이벤트가 발생하면 사용자 정의 입력기로 전환됩니다. 예를 들어, 번역 플러그인의 번역 창이 열리면 자동으로 한국어 입력기로 전환되어 한국어를 직접 입력하여 영어로 번역할 수 있습니다 [자세히](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/scene/event).

- **커스텀 규칙 시나리오:** 입력 문자열 등 입력 방식이 불확실한 시나리오에서 정규 표현식 매칭 규칙을 사용하여 특정 규칙에 부합할 때 특정 입력 방식으로 전환할 수 있습니다. 예를 들어, 커서가 한글 문자 사이에 있을 때 한글 입력 방식으로 전환됩니다 [자세히](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/scene/regular).

- **IDE 장면 떠나기:** Windows 시스템의 각 앱은 입력 상태가 독립적이며, 특정 앱으로 전환하면 내부 입력 상태가 복원됩니다. MAC 시스템에는 이 기능이 없기 때문에 플러그인은 IDE를 떠날 때 입력 방식을 IDE에 들어가기 전 상태로 전환할 수 있습니다 [자세히](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/scene/leave).

지원되는 IDE

현재 **Smart Input Pro​**는 IntelliJ 플랫폼의 모든 IDE(IDEA, PyCharm, WebStorm, GoLand, PhpStorm, DataGrip 등)를 지원하며, Android Studio와 DevEco Studio도 IntelliJ 플랫폼을 기반으로 하기 때문에 지원됩니다. 다른 플랫폼의 IDE 플러그인은 개발 중에 있습니다. 각 IDE는 여러 프로그래밍 언어를 지원할 수 있으며, 모든 시나리오를 완벽하게 테스트하기는 어려우므로 불편한 점이 있을 경우 피드백을 주시면 하나씩 개선해 나갈 예정입니다.

지원하는 프로그래밍 언어

이론적으로 IDE가 지원하는 프로그래밍 언어라면 모두 지원하지만, 프로그래밍 언어마다 특성이 달라 경험은 다를 수 있습니다. 예를 들어 `Java`, `Kotlin`, `C`, `C++`, `Python`, `Php`, `Golang`, `JavaScript`, `TypeScript`, `Scala`, `Groovy` 등은 주석 영역과 문자열 리터럴에서만 한국어를 사용하고 다른 영역에서는 반드시 영어를 사용해야 합니다. HTML, Markdown과 같은 마크업 언어의 경우 특정 입력법을 반드시 사용해야 하는 영역이 명확하지 않아 자동 전환은 현재 지원하지 않지만, 커서 색상으로 입력법 상태를 표시하는 기능은 지원합니다.


 ## 프리미엄

이 제품은 부가가치 결제 모델을 채택했습니다. 30일 동안 부가가치 기능을 체험할 수 있으며, 체험 후 기본 기능은 무료로 사용할 수 있습니다. 활성화 후 부가가치 기능을 이용할 수 있습니다. 나중에 다음 경로를 통해 활성화할 수도 있습니다: 메인 메뉴 >> 도움말 >> 등록. 가격 상세 내역은 [기능 및 가격](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/start/plans-pricing)을 확인해 주세요.

- **기본 시나리오**에서 입력 방식을 자동으로 전환합니다. (무료)
- 커서에 현재 입력 방식을 표시합니다. (무료)
- 커서에 Caps Lock 상태를 표시합니다. (무료)
- **댓글 시나리오**에서 입력 방법을 자동으로 전환합니다. (유료)
- **Git Commit 시나리오**에서 입력 방법을 자동으로 전환합니다. (유료)
- **Tool Window Scenario**에서 입력 방법을 자동으로 전환합니다. (유료)
- **Ideavim 시나리오**에서 입력 방법을 자동으로 전환합니다. (유료)
- **문자 시나리오**에서 입력 방법을 자동으로 전환합니다. (유료)
- **Custom Events Scenario**에서 입력 방법을 자동으로 전환합니다. (유료)
- 기타 모든 기능. (유료)

다운로드 및 설치

이미 IntelliJ 플러그인을 다운로드하고 설치하는 방법에 익숙하시다면, IntelliJ IDE 플러그인 시장에서 [Smart Input Pro (Japan, South Korea, Russia & more)](https://plugins.jetbrains.com/plugin/25751-smart-input-pro-japan-south-korea-russia--more-)를 직접 검색하여 설치할 수 있습니다. 또한 [Download and Installation](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko/start/download)에서 상세한 안내를 확인할 수 있습니다.

**Smart Input Pro**는 중국 본토 버전 [Smart Input Pro (Chinese)](https://plugins.jetbrains.com/plugin/25280)과 마켓플레이스 버전 [Smart Input Pro (Japan, South Korea, Russia & more)](https://plugins.jetbrains.com/plugin/25751-smart-input-pro-japan-south-korea-russia--more-)으로 나뉩니다. 두 버전의 주요 차이점은 인증 방법입니다. 중국 본토 버전은 WeChat 인증을 사용하고, 마켓플레이스 버전은 공식 Jetbrains 플러그인 마켓 인증 방법을 사용합니다. 필요에 따라 선택할 수 있으며, 중국 본토에서는 **Smart Input Pro (Chinese)**을 선택해 주세요.

## 기술 지원

**Smart Input Pro**에 대한 상세한 [입문 문서](https://xiaolvpuzi.cn/docs/smart-input-pro-doc.html#/ko)를 작성했습니다. 입문 문서를 읽으면 대부분의 문제를 해결할 수 있습니다. 또한 [GitHub](https://github.com/SmartInput/SmartInput/issues)에 이슈를 제출할 수도 있습니다.
