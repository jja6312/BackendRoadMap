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

`wget`은 인터넷에서 파일을 받는 명령어이다.

```
// 파일 다운로드
$ wget DOWNLOAD-URL

// 백그라운드로 다운로드
$ wget -b DOWNLOAD-URL
```

출처: <a href="https://sisiblog.tistory.com/25">sisiblog님의 tistory</a>

> tail

`tail`명령어는 파일의 마지막 부분을 출력하는 명령어이다.

```
$ tail [옵션][파일명]
```

하나의 파일만을 볼 수 있는것이 아닌 여러 파일을 동시에 표기할 수 있다

출처: <a href="https://coding-factory.tistory.com/801">coding-factory님의 tistory</a>

> head

`head`명령어는 파일의 초반 부분을 출력하는 명령어이다.

`tail`명령어와 상반되며 사용하는 방법또한 동일하다

```
$ head [옵션][파일명]
```

> less

`less`명령어는 파일의 내용을 화면에 보여주나, `vi`명령어와는 상반되는 점으로 전체 파일을 읽지 않기 때문에 빠르다는 장점이 있다.

```
$ less [옵션][파일이름]
```

> find

`find`명령어는 파일을 검색하는데 사용되는 명령어이다.

```
$ find [옵션][경로][표현식]

# 현재 디렉토리에서 test가 포함되는 파일 찾기
find . -name "*test*"

# 현재 디렉토리에서 .txt 확장자 모두 찾기
find . -name "*.txt"

# 현재 디렉토리에서 .txt 확장자 파일 검색 후 모두 삭제
find . -name "*.txt" -delete

# 현재 디렉토리에서 test로 시작되는 파일 찾기
find . -name "test*"

# 현재 디렉토리에서 test로 끝나는 파일 찾기
find . -name "*test"
```

위의 구조로 사용되며, 매우 다양한 종류의 옵션이 존재한다.

- `name` : 해당 이름의 파일을 찾음. 해당 이름에는 정규 표현식을 활용할 수 있음
- `type` : 지정된 파일 타입에 해당하는 파일 검색
- `user` : 해당 유저에게 속한 파일 검색
- `empty` : 빈 디렉토리 혹은 크기가 0인 파일 검색
- `delete` : 검색된 파일 혹은 디렉토리 삭제
- `exec` : 검색된 파일에 대해 지정된 명령 실행
- `path` : 지정된 문자열 패턴에 해당하는 경로에서 검색.
- `print` : 검색 결과를 출력. 검색 항목은 newline으로 구분. (기본 값)
- `print0` : 검색 결과를 출력. 검색 항목은 null로 구분.
- `size` : 파일 크기를 사용하여 파일 검색.
- `mindepth` : 검색을 시작할 하위 디렉토리 최소 깊이 지정.
- `maxdepth` : 검색할 하위 디렉토리의 최대 깊이 지정.
- `atime` : n일 이내에 액세스된 파일을 찾음.
- `ctime` : n일 이내에 만들어진 파일을 찾음.
- `mtime` : n일 이내에 수정된 파일을 찾음.
- `cnewer file` : 해당 파일보다 최근에 수정된 파일을 찾음.

출처: <a href="https://coding-factory.tistory.com/804">coding-factory님의 tistory</a>

> ssh

`ssh`명령어는 리눅스 서버에 원격 접속할 때 사용되는 명령어이다.
기본적으로 `22`번 포트를 사용하며

```
$ ssh root@192.168.159.129
```

위 명령어는 `ssh`로 `192.168.159.129`에 접속하는 것이다.

`exit` 명령어를 입력하여 원격지 접속에 `Logout`이 가능하다

> kill

`kill`명령어는 프로세스를 종료할 때 주로 사용되는 명령어이다.

```
$ kill -(Signal Name) PID
```

위 구조로 사용되는데 아무런 시그널을 지정하지 않게되면 `SIGTERM`이 시그널로 전달되며 `SIGTERM`의 기본 동작인 프로세스 종료가 실행된다.

### 🚲메모리 관리

1. `프로세스`는 `논리적 주소`와 `물리적 주소`로 나뉜다.
2. `메모리`는 크기가 작기 때문에 `프로세스`를 임시로 `디스크`에 보냈다가 다시 `메모리`에 로드해야 하는 상황이 생기는데, 이 때 디스크로 내보내는 것을 `swap out` 다시 들여보내는 것을 `swap in`이라고 한다.
3. 프로세스 영역의 할당 방법으로는 `연속적 할당`과 `비연속적 할당`으로 나뉘는데, `고정 분할`은 분할의 크기가 모두 동일, `가변 분할`은 동적으로 변화 하는 특징이 있다. 관련 지식으로 `First-fit`, `Best-fit`, `Worst-fit`등을 알아보면 좋음
4. `단편화`는 프로세스들이 메모리에 적재/제거 되며 사용하지 못할 공간들이 늘어나는 현상을 말하며, `외부 단편화`와 `내부 단편화`로 나뉜다

출처: <a href="https://rebro.kr/178">rebro님의 게시물</a>

### 🎠프로세스 간 통신

`프로세스`끼리 의사소통하는 것을 `IPC`라 한다.

`프로세스`간의 통신을 위한 별도의 공간을 만들어주어야 하기 때문에 `스레드`간 통신보다 어렵다

> 공유 메모리

<img src="https://user-images.githubusercontent.com/46777310/188258221-bd4f72fb-6183-4e84-8889-15adcf9ef3d4.png" />

`프로세스`간 `메모리 영역을 공유해서 사용`

> 파이프(Pipe)

<img src="https://user-images.githubusercontent.com/46777310/188258258-9dac5b9c-1681-4a99-b4c2-9b042c62ae75.png" />

통신을 위한 `메모리 공간(버퍼)을 생성`

> 소켓(Socket)

<img src="https://user-images.githubusercontent.com/46777310/188258292-dceff12b-31cb-4b5a-b6b3-319cd55fde3e.png" />

각각의 PC의 `프로세스`가 확인 과정을 거쳐 연결을 진행하고 연결 후 마치 `PIPE`와 같이 `1 대 1로 데이터를 주고 받음`

> 메시지 큐(Message Queue)

<img src="https://user-images.githubusercontent.com/46777310/188258383-133dad10-5bbd-4717-bdd6-0211b29e5620.png" />

`메모리를 사용한 PIPE`이며 `다수의 프로세스 간 메시지 전달이 가능`한 점이 있으며 접근을 위해서 `키(key)`가 필요하다.

> 메모리 맵(Memory Map)

<img src="https://user-images.githubusercontent.com/46777310/188258368-e3a36bef-7176-42c1-9edd-1e68edbd79c8.png" />

`열린 파일을 메모리에 맵핑`. `대용량 데이터를 공유해야 할 때 사용`

### 🧨입출력 관리

입출력 관리의 핵심은 `컴퓨터와 하드웨어 장치 사이의 공통된 인터페이스 역할을 수행하는 것이 입출력 관리의 핵심이다.`

> 입출력 하드웨어의 구성

`케이블` 또는 `무선`으로 신호를 보냄으로써 컴퓨터와 통신하는데, 또 다른 구성요소로 `제어기`가 있다

* 제어기: 포트나 입출력 장치를 제어하는 전자회로의 집합체이며 많은 입출력 장치는 제어기를 내장하고 있다.

> 입출력 하드웨어의 동작

`폴링`: `busy bit`를 통해 사용 가능 여부를 확인하며 `1`이라면 불가능 `0`이라면 준비 완료 상태이며 즉 폴링이란 `하드웨어 장치 상태를 체크하여 명령을 받을 수 있는지 확인하는 것`이다.

`인터럽트`: 예외상황이 발생하여 처리가 필요한 경우 `CPU`에게 알려 처리할 수 있도록 하는 것

출처: <a href="https://velog.io/@yonii/OS-%EC%9E%85%EC%B6%9C%EB%A0%A5-%EA%B4%80%EB%A6%AC">yonii님의 velog</a>

### 🧵POSIX 기초

`stdin`, `stdout`, `stderr`은 `stream`이라고 불린다.

`stdin`은 입력 담당, `stdout`은 출력 담당, `stderr`은 디버깅 및 에러 출력용으로 사용된다.

<img src="https://user-images.githubusercontent.com/46777310/188262551-d22ec048-da77-487d-967f-84ce6c5a8a1c.png"/>

`Pipe`는 어떤 프로그램의 `출력 결과`를 다른 프로그램의 `입력 값`으로 사용할 때 연결해주는 매개체 역할을 수행한다.

예를 들어

```
$ echo "foo bar baz" | wc -w
```

위 명령어는 `|`파이프를 사용하여 `echo`명령어로 출력된 결과를 `wc`명령에 전달하는 것이다.

출처: <a href="https://velog.io/@jakeseo_me/%EC%9C%A0%EB%8B%89%EC%8A%A4%EC%9D%98-stdin-stdout-stderr-%EA%B7%B8%EB%A6%AC%EA%B3%A0-pipes%EC%97%90-%EB%8C%80%ED%95%B4-%EC%95%8C%EC%95%84%EB%B3%B4%EC%9E%90">Jake Seo님의 velog</a>

### ☮네트워크 기본 개념

`네트워크`는 정보공유를 목적으로 PC와 PC가 모여 구성된 망이며, 데이터를 보내기 위한 도구들을 `프로토콜`이라고 한다.

`프로토콜`: `TCP`, `IP`, `Ethernet`

`프로토콜`추가를 `인캡슐레이션`, 확인을 `디캡슐레이션`이라고 한다.

`LEN`: `로컬 네트워크`, `Ethernet`

`WAN`: `외부 네트워크`, `ISP`

`유니캐스트`: `1대 1`

`브로드캐스트`: `1대 다`

`멀티캐스트`: `1대 특정`

<img src="https://user-images.githubusercontent.com/46777310/188317123-18f94790-b102-478f-96f3-d9f084409f08.png" />

`허브`: `가까운 장비`
`스위치`: `맥 어드레스 테이블`을 통해 컴퓨터와 통신
`라우터`: `라우팅 테이블`을 참조하여 통신

<img src="https://user-images.githubusercontent.com/46777310/188317519-0c4aa5e4-db52-4c2d-b154-2e2ad7633fa8.png" />

`TCP`: `전송 제어 프로토콜`, `연결 지향성 프로토콜`, `3-Way Hand Shaking` 동작 실시
`UDP`: `사용자 데이터그램 프로토콜`, `비연결 지향성 프로토콜`
`IP`: `인터넷 프로토콜`, `비연결 지향성 프로토콜`

`운영체제`의 `TTL` 기본값

`Cisco`: `155`
`Window`: `128`
`Linux`: `64`

출처: <a href="https://you4-bimi.tistory.com/5">you4-bimi님의 tistory</a>

### 🥝언어 배우기

`JavaScript`

<img src="https://user-images.githubusercontent.com/46777310/188318997-9f0509a5-a105-4c24-b0de-3a7c8be59165.png" />

이미 너무 잘 알아서 패스

### 🥟Git 기본 사용법

`git status`: 현재 작업 중인 파일의 상태를 확인합니다.

`git add`: 파일의 변경사항을 추가합니다.

`git commit`: 추가된 변경 사항을 저장합니다.

`git log`: 전체 로그 확인.

`git reset {log시 확인한 커밋 아이디} --hard`: 이전 상태로 (기록 제거)

`git revert {log시 확인한 커밋 아이디}`: 이전 상태로 (기록 유지)

출처: <a href="https://subicura.com/git/guide/basic.html#%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%89%E1%85%A5">Git/GitHub 안내서</a>

### 📿관계형 데이터베이스

<img src="https://user-images.githubusercontent.com/46777310/188456379-819e1dd3-476c-4b8f-a923-0440f4fe3bc0.png" />

> PostgreSQL

`PostgreSQL`은 `Ingres`에 뿌리를 두고 있음

대용량의 복잡한 트랜잭션 처리를 위한 `RDBMS`이다.

`Portable`: `Windows`, `Linux`, `MAC OS` 등 다양한 플랫폼을 지원한다.

`Reliable`: `MVCC`패턴에 유용하다.

`Scalable`: 대용량 데이터 처리를 위한 기능 구현이 가능하다.

`Secure`: `암호화`, `접근 제어`, `감사`의 3가지로 구성 되어있으며, 전송 데이터를 암호화하는 방안 등을 지원한다.

`Recovery & Availability`: `동기`, `비동기식` 서버 구축 가능

`Advanced`: 웹 기반 또는 GUI 관리도구를 제공하여 모니터링 및 튜닝이 가능

출처: <a href="http://www.gurubee.net/lecture/2888">http://www.gurubee.net/lecture/2888</a>

### 🎟 NoSQL 데이터베이스

<img src="https://user-images.githubusercontent.com/46777310/188461697-48d1d6d7-fd6a-43cd-8863-7e5fd7ca8d05.png"/>

`NoSQL`데이터베이스 중 인지도 1위

`NoSQL`이란 `Not Only SQL`입니다. `RDBMS`의 한계를 극복하기 위해 만들어진 새로운 형태의 데이터저장소 이므로, `RDBMS`처럼 고정된 스키마 및 `JOIN`이 존재하지 않는다.

```json
{
    "_id": ObjectId("5099803df3f4948bd2f98391"),
    "username": "velopert",
    "name": { first: "M.J.", last: "Kim" }
}
```

위와같은 예시의 `key`, `value`로 저장된다.

출처: <a href="https://velopert.com/436">Velopert님의 게시물</a>

### 🎗 더 깊은 데이터베이스 지식

> ORM

`ORM`이란 `Object Relational Mapping`의 약자이다.

`영속성(Persistence)`란 프로그램이 종료되어도 데이터가 사라지지않는 특성을 말하며

`ORM`은 `객체-관계` 매핑을 말하는데, 

`장점`으로는 

1. 객체 지향적인 코드로 `직관적`이고 `비즈니스 로직에 더 집중`할 수 있게 도와준다.
2. `재사용 및 유지보수`의 편리성이 증가한다.
3. `DBMS`에 대한 종속성이 줄어든다

`단점`은

1. 완벽한 `ORM`으로만 서비스를 구현하기가 어렵다.
2. 프로시저가 많은 시스템에선 `ORM`의 객체 지향적인 장점을 활용하기 어렵다.

