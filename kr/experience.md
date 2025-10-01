---
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# 경력기술서

### [ABC (AhnLab Blockchain Company)](https://ahnlabblockchain.company)

_iOS App Developers – (2022년 12월 \~ )_

‘[ABC Wallet](https://apps.apple.com/kr/app/id1642837445)’ 앱은 초기에 외주사를 통해 **React Native 기반의 하이브리드 앱**으로 개발되었으며, 저는 Android 개발자와 함께 약 1년간 해당 앱을 유지보수했습니다. 이 경험을 통해 하이브리드 앱의 구조적 장점과 한계를 모두 체감할 수 있었고, 이후 앱의 성능과 확장성을 높이기 위해 Native 전환을 주도했습니다. 약 4개월 만에 기존 기능은 물론 Swap, Aptos 네트워크 등 신규 기능을 포함한 iOS 앱을 완성해 출시하였습니다.

두 플랫폼 간의 구조적 일관성을 유지하기 위해 **Clean Architecture를 도입**하였고, iOS 프로젝트는 추후 **SPM(Swift Package Manager)을 기반으로 Domain, Data, Presentation 모듈로 분리**하여 관리했습니다. Domain과 Data는 **Swift Concurrency를 적극 활용**해 비동기 로직을 간결하고 안정적으로 처리했고, Presentation은 **SwiftUI + Combine 기반의 MVVM 패턴**을 적용했습니다. 또한, 복잡한 Wallet API의 흐름을 클라이언트에 추상화하기 위해 사내 제품인 [**WaaS 의 SDK**](portfolio/abc-wallet/waas-sdk.md)**를 직접 설계**하여, 핵심 기능을 일관되고 안정적으로 사용할 수 있도록 구조화했습니다.

이처럼 구조적으로 분리된 모듈 덕분에, 이후 GX(Ground X)사의 ‘[Klip](https://apps.apple.com/kr/app/id1627665524)’ 앱에 새로운 블록체인 네트워크(비트코인, 솔라나, 트론, 아비트럼 등)를 통합하는 과정에서도 **ABC Wallet에서 개발한 모듈을 안정적으로 이식**할 수 있었고, 최소한의 코드 수정으로 높은 재사용성과 안정성을 확보했습니다.

이 프로젝트를 통해 제가 갖추게 된 가장 큰 강점은 **복잡한 도메인을 설계와 모듈화 관점에서 정리하고, 확장 가능한 구조로 구현하는 역량을 갖추**었습니다.

### [하루하루 (DayDay) / 15만 다운로드, 평점 4.6 & 5000개 리뷰](https://apps.apple.com/kr/app/id1452035712)

‘하루하루’ 앱은 **CoreGraphics와 CoreAnimation을 활용**해 UIView에 직접 선과 면을 그리는 데서 시작된 프로젝트로, 독창적인 UI/UX를 제공하는 시간 계획표 애플리케이션입니다. 특히 방학시간표를 모티브로한 원형 시간표는 한국 사용자를 대상으로 한 차별화된 기능으로 큰 인기를 얻었습니다.

출시 이후에도 CoreData, WidgetKit, WatchKit, StoreKit, CloudKit 등의 Framework 를 추가적으로 사용하였고, SiriKit 과 CoreML 의 활용방안을 검토하며 **사용자 경험을 강화하고자 노력**하였습니다. **이 앱은 국내 생산성 카테고리 유료 앱 1위, 유료 앱 전체 순위 Top 2를 기록했으며, 누적 다운로드 15만 건을 돌파했습니다. 또한, 5000개 이상의 리뷰에서 평균 평점 4.6점을 유지**하며 높은 사용자 만족도를 증명했습니다.

하루하루는 1인 개발자로서 기획부터 운영까지 모든 과정을 맡아, 사용자 중심의 사고를 길렀던 소중한 경험이었습니다.

### Avanssion

_**Full-Stack Dev / Tokyo** – (2020년 9월 - 2022년 6월)_

Avanssion은 일본 도쿄를 본사를 두고 있는 IT기업으로 WMH(World Mode Holdings)와 파트너쉽을 맺고 MyBrands라는 일본, 싱가폴 패션HR 플랫폼을 개발하는 회사입니다.

Avanssion은 개발자 역량을 위하여 **개발자 전원이 풀스택으로 근무하는 시스템으로 저 역시도 풀스택 개발자로 근무**했습니다. 당시 제가 처리했던 업무 비중은 백앤드 작업이 60%, 프론트 20%, 모바일 20% 정도 였습니다.

업무 방식은 다국적 팀원들로 구성되어 **주로 화상회의와 Jira를 이용하여 업무를 분담을 하였고, Jira 보드에 현재 필요한 작업에 배치된 인원이 없다면 팀원중 누구나 할 수 있는 사람이 작업**을 하였습니다. 이러한 조직의 특성과 프로세스 덕에 유연한 사고방식을 배울 수 있었으며, **글로벌 역량을 쌓을 수 있었다는 점**과 다양한 분야에 대한 경험을 할 수 있었다는 점에서 개발자로서 좋은 기회였다고 생각합니다.

이때 인연을 맺은 프랑스 국적의 개발자가 현재는 한국에서 [Seoul iOS Meetup](https://www.meetup.com/seoul-ios-meetup/) 이라는 개발그룹을 주최하고 있어 종종 참여하기도 합니다.

### SoftUs - 창업

_**iOS & Backend / Korea** (2019년 7월 - 2020년 7월)_

창업진흥원 주관 ‘예비창업패키지’ 프로그램에 선발되어 창업에 도전했습니다. 창업 아이템은 ‘**보물섬: 위치기반 AR광고 플랫폼**’ 으로 광고타겟 상점근처에서 앱을 열었을 때 AR광고가 노출되는 서비스입니다. 예를들어 점심밥을 먹는 사람이 을지로 식당가 근처에서 서비스를 열었을때, 해당 지역과 관련된 AR광고가 오픈되는 서비스입니다.

사업을 성공시키겠다는 열정으로 서비스의 개발을 시작하기에 앞서 각 분야에 도움이 되는 공부를 하였습니다. **iOS 앱을 위해선 코드기반 UI 를 작성하여 AutoLayout** 에 대해 깊이 있게 공부하였습니다.

특히 백앤드 개발에 있어서는 단순히 작동하는 코드를 만드는 것을 넘어서, **성능과 확장성을 고려한 구조를 설계하고 싶었습니다.** 그 과정에서 [Inflearn의 REST API 강의](https://www.inflearn.com/course/spring_rest-api)와 함께 네이버 D2 - DEVIEW의 ‘[그런 REST API로 괜찮은가](https://tv.naver.com/v/2292653)’ 발표 영상을 인상 깊게 보았고, **JPA, HATEOAS, REST Docs, TDD, OAuth2 등을 활용한 Spring boot 서버를 개발**하였습니다.

2020년 초 코로나19 바이러스 시작과 함께 오프라인 상권의 상황이 나아지지 않아 사업을 중단하게 되었지만 이때 공부하고 습득한 지식으로 **Web 어플리케이션의 전반적인 시스템을 이해**할 수 있게 되었습니다.

### [Sweettracker](https://apps.apple.com/kr/app/id523045854)

_**iOS Dev / Korea**– (2017년 8월 - 2018년 6월)_

스마트택배는 다양한 택배사의 정보를 취합하여 고객에게 배송정보를 전달하는 서비스로, 월간 평균 5000만건의 택배정보 그리고 **iOS 기준 MAU 20만 / DAU 5만** 정도의 유저에게 서비스되고 있는 앱입니다.

저는 해당 스마트택배의 전체적인 iOS 앱을 담당하였으며, 안정성과 유지보수성의 개선을 위해 **Objective-C를 Swift로 변환하는 작업**을 진행하였습니다. 이외에도 CU택배예약 서비스 신규개발, 디자인 2.0 개편과 같은 작업을 했습니다.

좋은 팀장님과 동료들을 만나 **좋은 개발문화를 배울 수 있었고, 엔터프라이즈 iOS 앱 개발 및 운영자로서 많은 것을 배웠습니다**. 이때 배운 운영 노하우 덕분에 ‘하루하루’ 라는 앱을 2019년 부터 지금까지 운영할 수 있게 되었습니다.
