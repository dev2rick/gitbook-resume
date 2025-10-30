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

### [안랩블록체인컴퍼니](https://ahnlabblockchain.company)

iOS App Developer | 2022.12 \~ 현재

{% hint style="info" %}
[ABCWallet](https://apps.apple.com/kr/app/id1642837445)은 자산관리 및 멀티체인 거래를 지원하는 블록체인 지갑 서비스입니다. 초기 외주사가 React Native로 개발했으나, 패키지 비공개로 인해 유지보수가 어려웠고 성능적인 이점을 위해 Native로 전면 재개발을 진행했습니다. 4개월 만에 **Clean Architecture** 기반의 모듈화 구조로 완성했으며, 안정성과 확장성을 모두 확보했습니다.

이때 구축한 Domain, Data 모듈을 GroundX의 [Klip](https://apps.apple.com/kr/app/id1627665524) 앱에 이식하여 지원하는 네트워크를 4개에서 12개로 확장하는 핵심 기반이 되었습니다.
{% endhint %}

#### 제품명

* [ABC Wallet](https://apps.apple.com/kr/app/id1642837445), [Klip](https://apps.apple.com/kr/app/id1627665524)

#### 주요 역할 및 기여

* **React-Native** 기반 앱을 약 1년간 유지보수하며 구조적 장단점을 직접 체감하고, 네이티브 전환을 주도함
* iOS 리뉴얼 기간 약 4개월 동안 기존 기능과 신규 기능(예: Swap, Aptos 네트워크 지원)을 포함한 네이티브 앱 출시
* 구조적 일관성과 확장성을 확보하기 위해 **Clean Architecture** 도입, Domain / Data / Presentation 모듈로 분리
* **Swift Concurrency**를 활용해 비동기 로직을 간결하고 안전하게 구현
* Presentation 레이어는 **SwiftUI** + **Combine**을 적용한 **MVVM 패턴**을 사용
* [**WaaS SDK**](portfolio/abc-wallet/waas-sdk.md) **설계** 및 통합을 통해 Wallet API 추상화 및 기능 일관성 확보
* 모듈화된 구조 덕분에 **Klip** 앱으로의 코드 이식이 최소 수정으로 가능해짐

#### 성과 및 성취

* **Clean Architecture** 기반 구조 설계 및 모듈화를 통해 확장성과 유지보수성 확보
* 네트워크 추가 시 개발 / 테스트 리드타임 단축
* 앱 전환 과정에서 안정성 및 코드 품질 향상
* Klip 앱에 지원하는 네트워크를 4개 → 12개로 확장

#### 기술 스택

Swift, SwiftUI, Combine, Swift Concurrency, Clean Architecture, SPM(모듈화), MVVM, WaaS SDK, React-Native

***

### Avanssion

Full-Stack Developer | 2020.09 \~ 2022.06

{% hint style="info" %}
일본 도쿄 소재 IT기업에서 패션HR 플랫폼 ‘MyBrands’를 일본·싱가포르 대상 서비스로 개발했습니다.
{% endhint %}

#### 제품명

* Mybrands.jp, Mybrands.sg

#### 주요 역할 및 기여

* 백엔드(60%), 프론트엔드(20%), 모바일(20%) 중심의 풀스택 역할 수행
* 다국적 팀과 Jira, 화상회의 기반 협업
* “필요한 작업에 누구나 참여 가능”한 유연한 조직문화 속에서 개발 프로세스 전반 경험

#### 성과 및 성취

* 글로벌 개발 환경에서 다양한 분야를 경험하며 종합적 시스템 이해도 확보
* 이후 iOS 전문 분야로의 전환 기반 마련

#### 기술 스택

Node.js, NestJS, React, React-Native, Mobile

***

### SoftUs

창업자 | iOS & Backend Developer | 2019.07 \~ 2020.07

{% hint style="info" %}
정부지원 예비창업패키지에 선정되어 진행한 ‘보물섬’은 위치기반 AR 광고 플랫폼으로, 사용자가 상점 근처를 지날 때 AR 형태로 쿠폰이나 광고 오브젝트가 나타나도록 설계된 서비스입니다. 현실 공간에 디지털 오브젝트를 매핑하는 증강현실 광고 네트워크 구축이 목표였습니다.
{% endhint %}

#### 제품명 / 과제명

* 보물섬: 위치기 AR 광고 플랫폼

#### 주요 역할 및 기여

* 제품 기획, iOS 개발, 백엔드 서버 구축까지 전 과정을 주도
* iOS에서는 CoreLocation과 ARKit을 이용해 사용자의 GPS 좌표를 기반으로 가상 광고 오브젝트를 렌더링
* 광고 콘텐츠 관리 및 배포를 위해 Spring Boot 기반 백엔드 구축 (JPA, HATEOAS, REST Docs, TDD, OAuth2 적용)
* 앱 내에서 서버와 실시간 광고 데이터를 주고받기 위한 REST API 설계 및 테스트 자동화
* 초기 스타트업 환경에서 기획자, 디자이너, 외부 협력사 등과 직접 커뮤니케이션하며 제품의 기술적 방향성과 비즈니스 모델을 동시에 설계
* iOS, 서버 개발 외에도 정부지원 과제 수행, 사업계획서 작성, 시연용 데모앱 개발 및 발표를 직접 수행

#### 성과 및 성취

* ARKit, CoreLocation, Swift, Spring Boot를 활용한 엔드투엔드 제품 개발 전 과정 경험
* 실제 서비스 프로토타입을 구축하고 정부기관 데모 심사에서 우수 평가 획득
* 스타트업 환경에서 기획–개발–사업을 잇는 통합적 사고와 **제품 책임감(ownership)**&#xC744; 체득
* 이후 실무에서도 아키텍처 설계 시 '제품 단위 사고(Product-Driven Architecture)'를 적용하는 계기 마련

#### 기술 스택

Swift, UIKit, ARKit, CoreLocation, AutoLayout, Spring Boot, JPA, REST API, OAuth2, TDD, HATEOAS, REST Docs

***

### 사이드 프로젝트

1인 프로젝트 | iOS App Developer | 2019.2 \~ 현재

{% hint style="info" %}
하루하루는 원형 시간표 UI를 중심으로 한 시간 계획·관리 앱으로, “방학시간표”의 아날로그 감성을 디지털로 옮겨 사용자에게 직관적인 하루 구조를 제공합니다.

처음에는 CoreGraphics와 CoreAnimation을 활용해 UIView 위에 선과 면을 직접 그리며 UI를 완성했고, 이후 앱 구조를 지속적으로 개선해 iPad, Apple Watch, Widget, CloudKit 동기화까지 확장했습니다.
{% endhint %}

#### 제품명

* [하루하루](https://apps.apple.com/kr/app/id1627665524)

#### 주요 역할 및 기여

* 1인 개발자로서 **기획, 디자인, 개발, 운영 전 과정을 수행**
* **CoreGraphics** 기반의 원형 시간표 렌더링 로직을 설계하고, 사용자 입력에 따른 실시간 반응형 인터랙션 구현
* CoreData를 활용한 데이터 모델링 및 iCloud 기반 CloudKit 동기화로 멀티디바이스 환경 지원
* WidgetKit과 WatchKit을 통한 위젯 및 워치 앱 확장으로 플랫폼 통합 경험 제공
* SwiftUI 전환 및 StoreKit을 이용한 Plus+ 구독 모델 도입으로 비즈니스 모델 고도화

#### 성과 및 성취

* **'오늘의 앱'** 선정, 생산성 카테고리 유료 앱 1위, 전체 **유료 앱 2위** 달성
* 누적 다운로드 **15만+**, **리뷰 5000+**, **평점 4.6** 유지
* 사용자 피드백 기반으로 지속적인 UX 개선 및 유지보수 문화 확립

#### 기술 스택

Swift, UIKit(CoreGraphics/CoreAnimation), SwiftUI, CoreData, CloudKit, WidgetKit, WatchKit, StoreKit, Combine

***

### 스윗트래커

iOS Developer | 2017.08 \~ 2018.06

{% hint style="info" %}
다양한 택배사의 정보를 통합 제공하는 국내 대표 배송 조회 서비스로, 월 평균 5천만 건 이상의 택배정보를 처리하는 앱입니다.
{% endhint %}

#### 제품명

* [스마트택배](https://apps.apple.com/kr/app/id523045854)

#### 주요 역할 및 기여

* iOS 앱 전체 담당, Objective-C 기반 코드를 Swift로 전환
* CU택배 예약 서비스 신규 개발 및 디자인 2.0 개편 진행

#### 성과 및 성취

* 엔터프라이즈급 iOS 앱 운영 경험 확보
* 코드 품질 향상 및 유지보수성 강화

#### 기술 스택

Objective-C, Swift, UIKit, REST API, MVC, Javascript
