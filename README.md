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

위 이미지와 같이 `google.com`의 주소는 `172.217.175.14` 임을 확인할 수 있으며 DNS는 IP로 변환될 뿐 본질은 같다고 볼 수 있다.

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

### 😃도메인 이름이란?

> 해당 내용은 <a href="https://velog.io/@m-vault/%EB%8F%84%EB%A9%94%EC%9D%B8-%EB%84%A4%EC%9E%84%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80%EC%9A%94">brogod님의 Velog</a>를 참고하여 만들어졌음을 밝힙니다.

<img src="https://user-images.githubusercontent.com/46777310/187675328-6d610f6f-4ad3-44f5-b4d1-1008ad0a9c82.png">

### 👨‍💻호스팅이란?

> 해당 내용은 <a href="https://m.blog.naver.com/lhhoo1717/221365274221">DD님의 Blog</a>를 참고하여 만들어졌음

호스팅은 제작한 웹에 접근할 수 있도록 전문 호스팅사의 서버를 빌려 24시간 방문이 가능하도록 요청하는것이다.

크게 `웹호스팅`, `서버 호스팅`, `클라우드호스팅` 으로 나뉜다.

> 웹호스팅

<img src="https://user-images.githubusercontent.com/46777310/187682519-02103780-43f0-4d46-ba0e-627a3cf8c8e0.png">

`웹호스팅`은 하나의 서버장비를 여러명이 공유하여 사용한다.

장점: `저렴함`

단점: `트래픽 적음`

> 서버호스팅

<img src="https://user-images.githubusercontent.com/46777310/187682549-50787405-a7f3-4f24-8d09-215ec2c7494f.png">

`서버호스팅`은 한명의 고객이 하나의 서버를 임대하는 것

장점: `많은 트래픽`

단점: `비싸다`

> 클라우드호스팅

<img src="https://user-images.githubusercontent.com/46777310/187682574-61c9b04d-d8ee-44d7-bcd2-0ca898258de6.png">

`클라우드호스팅`은 가상서버를 임대해서 자유롭게 스펙을 조절할 수 있고 이용한 만큼의 가격만을 지불할 수 있습니다.

장점: `자유로운 트래픽`, `합리적 가격`

### 🥇HTML, CSS, JavaScript

`프런트엔드 기본지식`은 생략

### 🚍터미널 사용법

`Terminal`사용법은 추상적인 의미이며 많은 종류와 더욱 많은 명령어가 있기에 자세한 설명을 생략

### 💤OS의 작동원리

> 해당 내용은 <a href="https://velog.io/@codemcd/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9COS-5.-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4-%EA%B4%80%EB%A6%AC">SungBum Park님의 velog</a>를 참고하여 작성되었음을 미리 밝힙니다.

<img src="https://user-images.githubusercontent.com/46777310/187696045-e9236e95-68c7-4c16-a377-617b8c2ecff4.png">

`Operating System`

사용자와 하드웨어 사이의 인터페이스

- `프로세스 관리`
- `메모리 관리`
- `저장소 관리`
- `보안`

사용자 요청이(`Event`) 발생하면 적절한곳에 일을 분배(`CPU`, `I/O`, `메모리`)하여 처리한다.

### 🚯프로세스 관리

<img src="https://user-images.githubusercontent.com/46777310/187696292-fc67bffb-3277-44bf-9f5d-4a08de9c996c.png">

`프로세스`는 `실행중인 상태`의 프로그램을 말한다.

`프로세스 상태 전이도`에서는 이러한 프로세스를

`New`: 프로그램이 메모리에 할당
`Ready`: 할당 조건을 충족
`Running`: CPU가 해당 프로세스 실행
`Waiting`: 프로세스가 끝나기 다른 작업을 수행 (끝나면 Ready상태로)
`Terminated`: 프로세스가 종료된다.

<img src="https://user-images.githubusercontent.com/46777310/187697267-39d11e3e-52de-44c4-9943-1af9767b9624.png">

`PCB`: 프로세스에 대한 모든 정보가 모여있음

`프로세스`는 `프로세스 큐(Queue)` 라는 곳에 모여서 순서를 대기하게 되는데 이렇게 순서를 정해주는 알고리즘을 `스케줄링(Scheduling)`이라 한다.

### ☯스레드와 동시성

> 해당 내용은 <a href="https://velog.io/@goban/%EC%8A%A4%EB%A0%88%EB%93%9C%EC%99%80-%EB%8F%99%EC%8B%9C%EC%84%B1">이명환 님의 Velog</a> 를 보고 작성되었음을 밝힙니다.

<img src="https://user-images.githubusercontent.com/46777310/187917797-f65f879b-dfcb-483d-93fe-a29bee34aeb0.png">

`스레드`란 한 프로그램 프로세스 내에서 실행되는 흐름의 단위를 말함

`싱글 스레드`는 하나의 프로세스에선 하나의 `스레드`만이 실행되는 것이며

`멀티 스레드`란 하나의 프로세스 내에서 둘 이상의 `스레드`가 동시 작업이 가능한 것을 말한다.

`멀티 스레드`는 `데이터 병렬성(Data parallelism)`, `작업 병렬성(Task parallelism)` 으로 구분된다.

### 💨터미널 기본 명령

`grep`, `awk`, `sed`, `lsof`, `curl`, `wget`, `tail`, `head`, `less`, `find`, `ssh`, `kill`
에 대해서 알아보겠다.

> grep

```linux
grep [옵션][패턴][파일명]

# 특정 파일에서 'error' 문자열 찾기
grep 'error' 파일명

# 여러개의 파일에서 'error' 문자열 찾기
grep 'error' 파일명1 파일명2

# 현재 디렉토리내에 있는 모든 파일에서 'error' 문자열 찾기
grep 'error' *

# 특정 확장자를 가진 모든 파일에서 'error' 문자열 찾기
grep 'error' *.log
```

출처: <a href="https://coding-factory.tistory.com/802">coding-fatory님의 tistory</a>

> awk

```
awk [OPTION...] 'pattern { action }' [ARGUMENT...]
```

<img src="https://user-images.githubusercontent.com/46777310/187921783-da2db0d5-3c88-4734-884a-479c4217752c.png">

출처: <a href="https://recipes4dev.tistory.com/171">recipes4dev님의 tistory</a>

> sed

`ed`와 `grep` 명령어를 합쳐놓은 듯한 명령어로

```
치환(substitute)----------------sed 's/addrass/address/' list.txt : addrass를 address로 바꾼다. 단, 원본파일을 바꾸지 않고 표준출력만 한다.
 
sed 's/\t/\ /' list.txt : 탭문자를 엔터로 변환
 
------------삭제(delete)------------sed '/TD/d' 1.html : TD 문자가 포함된 줄을 삭제하여 출력한다.
sed '/Src/!d' 1.html : Src 문자가 있는 줄만 지우지 않는다.
sed '1,2d' 1.html : 처음 1줄, 2줄을 지운다.
sed '/^$/d 1.html : 공백라인을 삭제하는 명령이다. (★★★)
```

출처: <a href="https://linuxstory1.tistory.com/entry/SED-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%82%AC%EC%9A%A9%EB%B2%95">Linux 세상속으로:티스토리</a>

> lsof

`lsof`는 `list open files`의 약자로 파일 목록을 보여주는 명령어이다.

```
$ lsof
```

위 명령어는 모든 열린 파일 정보를 출력

`-i` 옵션을 주어 특정 포트 프로세스 정보 조회가 가능하며

```
$ lsof -i TCP:22
```

`+D` 옵션을 통해 특정 디렉터리 내 열린 파일 조회도 가능

```
$ lsof +D /test
```

출처: <a href="https://www.lesstif.com/system-admin/lsof-20776078.html">System Administrator님의 게시물</a>

> curl

`curl` 명령어는 url을 통한 웹 페이지의 접근을 담당함

`naver`에 `GET`요청

```
$ curl https://www.naver.com
```

`naver`에 `POST`요청

```
$ curl -d "testParam1=123" www.naver.com
```

이외에도 `PUT`은 `-T`

`DELETE`는 `-X` 명령어로 접근이 가능하다

출처: <a href="https://www.crocus.co.kr/1736">Crocus님의 cURL 개념 및 사용 방법</a>

> wget
