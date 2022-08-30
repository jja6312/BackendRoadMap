# 😏백엔드 로드맵

<img src="https://user-images.githubusercontent.com/46777310/187444773-6f7d1bee-5ace-4439-baa2-a342b0112a10.png">

본 저장소는 2022백엔드 로드맵을 참고해서 풀스택 개발자가 되기위한 김쵸비의 필사적인 발악을 담은 저장소입니다.

### 😚인터넷의 작동 원리

인터넷은 처음 `케이블`로 하나하나의 PC를 연결했었다.
하지만 PC가 늘어나자 연결해야하는 `케이블`의 수는 기하급수적으로 늘어났음

해당 현상을 막기 위해 `IP`주소를 사용하기 시작했고, 이 또한
처음은 안정적으로 보였으나 웹이 발달하며 IP주소를 위우기는 힘들어졌다.

위 상황을 아우러 `도메인`을 사용하기 시작하며 지금의 `google.co.kr`과 같은 주소가 생긴 것이다.

### 😁HTTPS란?

기존 HTTP에 SSL/TLS 보안을 적용한 보안 프로토콜이다. 과거에는 쇼핑몰/은행 등 보안이 필요한 웹에 적용되었지만 현재는 기본적으로 거의 대부분에 웹에서 적용된다.

도메인 검증`DV`, 조직 / 개인 검증 `OV/IV`, 확장 유효성 검사 `EV`

를 시행하며 2020년을 기점으로 HTTPS를 사용하지 않으면 검색능력이 향상되는 `SEO`를 사용할 수 없고 브라우저 보안 경고가 콘솔창에 생깁니다

HTTPS를 등록하려면 `CA` 인증기관에서 SSL.com을 지원하도록 적용해주면 되며 링크는 아래와 같음

<a href="https://www.ssl.com/ko/%EC%95%88%EB%82%B4/SSL-TLS-%EB%B8%8C%EB%9D%BC%EC%9A%B0%EC%A0%80-%EC%98%A4%EB%A5%98-%EB%B0%8F-%EA%B2%BD%EA%B3%A0-%EB%AC%B8%EC%A0%9C-%ED%95%B4%EA%B2%B0/">SSL 문제해결 TLS 브라우저 오류 및 경고</a>

### 😂브라우저 동작원리

브라우저의 핵심 기능은 사용자가 방문하고자 하는 페이지를 서버에 요청하고 응답을 받아 표시하는 것

`script`태그를 만나면 잠시 `DOM`을 중지하고 자바스크립트 엔진으로 제어 권한을 넘긴다.

### 🤣DNS와 그 작동 원리

우리가 자주 접하는 `naver.com`, `google.com` 모두 `DNS`를 가진 `DN(Domain Name)`이라고 할 수 있다.

<img src="https://user-images.githubusercontent.com/46777310/187469280-3976d6ca-fb0f-4b41-baa1-791bd26d866e.png">

위 이미지와 같이 `google.com`의 주소는 `172.217.161.174` 임을 확인할 수 있으며 DNS는 IP로 변환될 뿐 본질은 같다고 볼 수 있다.

1. 도메인 입력시 `Local DNS`에게 전달
2. `Root DNS` 서버에 도메인 질의
3. `Root DNS` 서버로 부터 `TLD(Top-Level Domain)` 이름 서버 정보를 전달 받음 \*`TLD`란 `.com`을 관리하는 서버
4. `TLD`에 도메인 주소 질의
5. `TLD`에서 관리하는 `DNS`정보 전달
6. 해당 도메인을 관리하는 `DNS`서버에 IP주소 질의
7. `Local DNS`서버에 IP주소 전달

의 과정이다.

<a href="https://velog.io/@goban/DNS%EC%99%80-%EC%9E%91%EB%8F%99%EC%9B%90%EB%A6%AC">goban님의 Velog</a>를 참조해보면

```
여담:
velog.io 와 github.io (깃허브 블로그)는 영국령 인도양 지역의 인터넷 국가 코드 최상위 도메인이다. io 도메인을 쓰면 기존 com, net이 점유하고 있던 도메인들을 벗어나 새롭게 도메인을 확보할 수 있다고 한다. 개별국가 NIC이 관리하고 주로 회사들이 이용해서 비싸다고...
```
