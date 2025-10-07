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

# \[Klip] 지원 네트워크 3배 확대

<figure><img src=".gitbook/assets/3ef8e65c-4206-4cb5-82f6-3e1b0e3094ff.png" alt=""><figcaption></figcaption></figure>

***

## **📌 개요**

* **프로젝트 참여 기간**: 2025년 4월 \~ 현재
* **프로젝트 참여 인원**: iOS 개발 2인 / Android 개발 2인
* **역할**: iOS 앱 개발, 멀티체인 (Bitcoin, Solana, Tron, Arbitrum 등…) 지원
* **앱스토어 링크**: [https://apps.apple.com/kr/app/id1627665524](https://apps.apple.com/kr/app/id1627665524)

***

## **🧩 프로젝트 소개**

'ABCWallet'에서 구축한 모듈을 'Klip' 앱에 이식하며 블록체인 지원 범위를 기존 4개에서 12개로 확장했습니다. Swift Package Manager 기반 모듈화와 클린 아키텍처를 적용해 코드 변경을 최소화하면서도 안정성과 재사용성을 확보했습니다. 이를 통해 다양한 네트워크를 유연하게 통합할 수 있었고, 실제 서비스 운영에서 확장 가능한 아키텍처의 효과를 입증했습니다.

***

## **🔧 기술 스택 및 아키텍처**

* **아키텍처**: Clean Architecture
* **모듈 관리**: Swift Package Manager
* **기술**: SwiftUI, Swift Concurrency, Combine 등

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

***

## **🚀 역할내 구현 사례**

### **1. ABCWallet 모듈 이식**

* Domain / Data 영역에 ABCWallet 에서 사용했던 SPM 을 추가적용
* Bitcoin, Solana, Tron 네트워크의 거래를 위한 추가구현

<div align="left"><figure><img src=".gitbook/assets/image 1 (2).png" alt="" width="295"><figcaption><p>[모듈 적용]</p></figcaption></figure></div>

<div align="left"><figure><img src=".gitbook/assets/image 2 (2).png" alt="" width="284"><figcaption><p>[Solana, Tron 전송 추가구현]</p></figcaption></figure></div>

<div align="left"><figure><img src=".gitbook/assets/9c768ffd-0f03-4199-aa1c-c5f7e754bc91.png" alt="" width="375"><figcaption><p>[Klip 앱내 신규 블록체인 추가]</p></figcaption></figure></div>

### **2. 자산 및 NFT 전송 추상화**

* 전송 다양한 네트워크 및 암호화 알고리즘에 대해 추상화함
* 그 외에도 수수료(가스비) 계산 / WalletConnect / Receipt Polling 등을 추상화함.

<figure><img src=".gitbook/assets/image 3.png" alt=""><figcaption><p>[Native, FT (ERC-20) 토큰의 거래를 지원]</p></figcaption></figure>

<figure><img src=".gitbook/assets/image 4.png" alt=""><figcaption><p>[NFT (ERC-721), MT (ERC-1155) 의 거래를 지원]</p></figcaption></figure>

### **3. Klip 프로젝트 스타일의 모듈 추가**

* ABCDomain / ABCData 모듈을 포함하고 기존 Klip에서 사용하고 있던 모듈중 핵심 로직을 Dependency 로 한 Klip 스타일의 새로운 모듈 추가.
* Presentation Layer 에서 실 사용은 ModuleABC 를 사용.

<div align="left"><figure><img src=".gitbook/assets/image 5.png" alt="" width="284"><figcaption></figcaption></figure></div>

***

## **🎯 성과**

* 기존 4개 → 12 개의 블록체인의 거래를 지원.
* 팀원과의 협업
  * PR 기반 개발 프로세스를 정착시켜 코드 품질을 높이고 커뮤니케이션 효율을 개선.
  * Android 개발팀과 소통을 통해 로직을 교차검증함.

***

## **🧠 회고**

### **1. 모듈화과정**

* 기존 'ABCWallet' 프로젝트는 관심사의 분리가 폴더기반으로 느슨하게 분리가 되어있어서 모듈화 하는데 어려움이 있었음.&#x20;
* 'Klip'에서 재사용할 부분인 Domain, Data 영역을 중점적으로 모듈화 했으며 그중에서도 Crypto, NFT 등의 자산송금, 서명(signTypedDataV4, personalSign) 등을 모듈화했음.
* 동일 도메인의 다른 앱에 사내의 비즈니스 로직을 이식하여 코드의 재활용성을 극대화하는 좋은 경험을 했음.

### **2. 사용자 경험은** ↓

* 'ABCWallet' 의 백앤드를 이용하기 위해서는 ABC의 인증토큰을 발급받아야하는데 이를 'Klip' 유저가 자연스럽게 발급받게 하려면 시간이 조금 더 필요했지만 개발기간이 2주로 너무 촉박했음.
* 기존 'Klip' 은 Crypto, NFT 등을 송금하고 자산의 변경이 즉시 앱에 반영되는데, ABC 의 백앤드는 이 기능이 없어서 사용자가 수동으로 Pull to refresh 를 수행해야함. 또한 노출가능한 거래내역이 200개로 제한되었음. 사용자는 기존 사용성에 익숙하기에 사용자 입장에서 다운그레이드라고 느낄 수 있는 업데이트는 신중할 필요가 있어보임.
