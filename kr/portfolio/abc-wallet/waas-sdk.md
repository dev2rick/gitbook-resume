---
description: Readme file for WaaS SDK
---

# WaaS SDK

## WaaS SDK for iOS

* iOS 용 ABC WaaS SDK

***

## Requirements

* iOS 13

***

## Installation

### Swift Package Manager

Add .package(url:\_:) to your Package.swift:

```swift
dependencies: [
	.package(url: "https://github.com/ahnlabio/waas-ios-sdk.git",
	.branch("main"))
]
```

***

## SDK 초기화

_**URL, clientId, clientSecret 은 ABC WaaS Console 에서 확인하실 수 있습니다.**_

```swift
// url: https://docs.waas.myabcwallet.com/getting-started/guide/support/
// abcAccessKey: client id
// abcAccessSecret: client secret

Waas.config(    
		url: "",    
		abcAccessKey: "",    
		abcAccessSecret: "",    
		csURL: "",    
		csPort: ""
)
```

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>[WaaS Admin]</p></figcaption></figure>

***

## Usage

### 1.  ABC 로그인

#### 1-1. 로그인 이메일 보내기

```swift
// email: 로그인 코드를 받을 이메일
// language: 전송할 이메일 언어 (한국어, 영어, 인도네시아어, 베트남어, 태국어, 일본어) 지원
// completion: 완료 콜백 (Void / Error)

public func sendLoginCode(    
	email: String,    
	language: Language = .current,    
	completion: @escaping (Result<Void, Error>) -> Void
)
```

{% code title="Example" %}
```swift
let client = WaasClient()    
client.sendLoginCode(        
	email: testEmail,        
	language: .current
) { result in        
	if case .failure = result {            
		// handle Error        
	}    
}
```
{% endcode %}

#### 1-2. 이메일 코드로 로그인하기

```swift
// email: 로그인할 이메일
// code: 이메일에 적혀있는 6자리 코드
// completion: 완료 콜백 (OauthToken / Error)

public func login(    
	email: String,    
	code: String,    
	completion: @escaping (Result<OauthToken, Error>) -> Void
)
```

{% code title="Example" %}
```swift
client.login(        
	email: testEmail,        
	code: "961210" // email code you received    
) { result in        
	switch result {        
	case .success(let authToken):            
		// save abc oauth token        
	case .failure(let error):            
		// handle Error        
	}
}
```
{% endcode %}

#### 1-3. 토큰 리프레시

```swift
// token: 리프레시 토큰
// completion: 완료 콜백 (OauthToken / Error)

public func refreshToken(    
	token: String,    
	completion: @escaping (Result<OauthToken, Error>) -> Void
)
```

{% code title="Example" %}
```swift

client.refreshToken(        
	token: refreshToken
) { result in        
	switch result {        
	case .success(let authToken):            
		// save abc oauth token        
	case .failure(let error):            
		// handle Error        
	}
}
```
{% endcode %}

### 2. WaaS 로 서명하기

#### 2-1. EVM Transaction 서명

```swift
// accessToken: 로그인 후 발급받은 AccessToken
// keyPassword: 사용자가 입력한 비밀번호
// transaction: 서명할 EVM Transaction 형식
// network: 서명할 네트워크 (ethereum, polygon, klaytn ...)

public func signTransaction(    
	accessToken: String,
	keyPassword: String,    
	transaction: EVMTransaction,    
	network: EVMNetwork
) async throws -> String
```

{% code title="Example" %}
```swift
// keyshare 를 저장할 저장소

let storage = MemorySignerStorage()
let signer = EVMSignClient(storage: storage)
let signature = try await signer.signTransaction(    
	accessToken: accessToken,    
	keyPassword: keyPassword,    
	transaction: .init(        
		to: "0xFF5f861bed0dfB81aC389aD88d956fE4653cf5D7",        
		value: "0x0"    
	),
	network: .ethereumTestnet
)
```
{% endcode %}

### 3. SDK 에서 지원하지 않는 Method 사용예

#### WaaS 에는 있지만, SDK 에서 지원하지 않는 API에 대한 사용방법입니다.

> 아래의 예시는 EVM 의 eth\_estimateGas 를 호출하는 방법입니다.
>
> [ABC WaaS (eth\_estimateGas)](https://docs.waas.myabcwallet.com/api/evm/gas/#legacy)

```swift
// accessToken 만 있으면 WaaS에서 지원하는 다양한 API를 사용하실 수 있습니다.

func testEstimatedGas() async throws {    
	let urlString = "\(Waas.config.url.absoluteString)/wapi/v2/gas/estimate/legacy"    
	let url = URL(string: urlString)    
	let request = URLRequest(        
		url: url,        
		method: .post,        
		contentType: .urlEncoded,        
		headers: ["Authorization": "Bearer \(accessToken)"],        
		body: [            
			"network": EVMNetwork.ethereumTestnet.pathName,            
			"to": "0xFF5f861bed0dfB81aC389aD88d956fE4653cf5D7",            
			"from": "0xFF5f861bed0dfB81aC389aD88d956fE4653cf5D7",            
			"value": "0x0"        
		]    
	)!    
	
	let (data, response) = try await URLSession.shared.data(for: request)    
	let text = String(data: data, encoding: .utf8)    
	print(text)
}
```
