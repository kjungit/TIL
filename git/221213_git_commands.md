# TIL git, github 시작하기

## [ git, github 차이점 ]

---

### ● git은 도구, 버전 관리 프로그램

      - 나의 코드 수정 내역등을 기록하고 관리하는 관리 프로그램이다.
      - 로컬 저장소를 사용하기 때문에 다른 개발자와 실시간으로 작업을 공유할 수 없다.

### ● github 버전 관리, 소스 코드 공유, 원격 저장소

      - git 저장소를 관리하는 클라우드 기반 호스팅 서비스!
      - 클라우드 기반으로 다른사람들과 소스코드 공유 및 git기능을 확장하여 제공
      - 여러 사람들과 참여하여 버전 제어 및 공동 작업이 가능

---

---

<br/>

## [ Shell ]

- 운영체제의 커널과 사용자를 이어주는 소프트웨어 : 커널과 사용자간의 다리역할

> Shell에는 여러 종류가 있다. sh, csh, bash, zsh...
> 이 중에서 bash shall은 리눅스 뿐만 아니라 GNU운영체제, 맥 OS 등 다양한 운영체제에 사용되고 있다.

---

### **● CLI( Command Line Interface ) vs GUI( Graphpic User Interface )**

#### _CLI( Command Line Interface )?_

      - 입출력을 하는 명령줄, 사용자와 컴퓨터 간의 소통
      - windows = cmd, mac = terminal, linux = terminal
      - 키보드 + 명령어

#### _GUI( Graphpic User Interface )?_

      - 그래픽을 통해서 사용자와 컨퓨터 간의 소통
      - 그림 또는 아이콘 등
      - 키보드 + 마우스

---

---

<br/>

### **[ shell Command ]**

<br/>

- ~ : 지금 로그인한 사용자가 제한없이 사용할 수 있는 최상의 공간

- . : 현재위치

- .. : 상위경로 위치

- pwd ( print working directory )

      - 지금 사용하고 있는 위치, 현재 디렉토리를 알려주는 명령어

- ls ( list seg ) - 현재 파일에서 하위로 이동할 수 있는 파일들

- ls -a

      - 숨겨진 파일들을 모두 확인

- cd (Change Directory) "이동할 이름"

      - 현재 위치를 이동

- cd ..

      - 현재 파일경로에서 상위파일경로로 이동

- cd ../..

      - 상위에서 상위로 이동 ( 단계별로 더 이동하려면 /.. 추가)

      * 이동할 때는 디렉토리 단위로 이동

- mkdir (make directory)

      - 새로운 폴더 경로(디렉토리) 생성

- touch

      - 새로운 파일 생성

- mv( move) ./파일이름 ./이동할 경로 이름

      - 파일을 이동시킬 때

      * mv 파일이름 파일이름 : 파일이름 변경

- cp(copy) 복사할파일 ./복사할파일이름

- 파일 복사 명령어

      rm (remove)

- 파일 삭제

- rm \*.\*

  - 모든 파일 삭제

    ex ) rm 파일이름.\* : 파일이름을 가진 확장자를 모두 지운다.

    rm -r 파일이름/ : 모든 파일들을 지우고 디렉토리(폴더)를 지운다.
    rm -rf : 바로 다 지우기

- cat

      - 파일 내용, 텍스트 출력 확인

---

---

<br/>

## [ VIM ]

- vim은 max os 환경에서 shell script, code등을 작성할때 사용한다. ( 그 외 환경에도 사용할 수 있다.)

- 마크다운 등 텍스트 편집기로 사용했다.

### **[ Vim Command ]**

<br/>

- i

      - insert mode

- v

      - visual mode

- d

      - delete

- dd

      - delete a line

- esc

      - back to normal mode

- :w

      - 저장

- :wq

      - 저장하고 나가기

- o

      - insert 전 적어진 문장을 개행 후 insert 적용

- shift + y

      - 잘라내기

- p

      - 붙혀넣기

- u

      - 지운 내용 되돌리기

---

---

<br/>

## [ git object ]

▶ Blob

      - git add 명령 시 생성
      - 파일 하나의 내용에 대한 정보
      - 파일 내용

▶ Tree

      - git commit 명령 시 생성
      - Blob이나 subtree의 메타 데이터(디렉터리 위치, 속성, 이름 등)
      - type, 이름, 파일명 등이 기록

▶ Commit

      - git commit 명령 시 생성

---

### [ git 에서 github 업로드 ]

> clone -> cd clone위치 -> add -> commit -> push

- clone이 익숙하지 않아서 clone을 하지않고 add, commit, push를 했다. push가 제대로 되지 않았다..clone 꼭 하기!!!

```javascript
// git 환경설정
git config --g user.name // 유저 네임
git config --g user.email // 유저 이메일
git config --g core.editor // "vim"
git config --g core.pager // "cat"
```

- git add (파일이름): 수정파일 올리기

  > git add . 은 사용하지 않는게 좋다. 안좋은 습관을 멀리하자.

- git commit : 커밋 메세지 작성

  > -m "..." 을 사용했는데 vim으로 작성하기!

- git status : 현재 파일 상태 확인

- git status -uall : 정확한 파일 이름 확인 가능

- git reset Head 파일명 : commit 취소 (스테이지 취소)

- git remote : 현재 github 원격 저장소와 연결된 이름 확인

- git remote -v : 현재 github 원격 저장소와 연결된 이름 및 주소 확인

- git remote remove 이름 : 원격 저장소 연결된 이름 삭제

- git remote add 이름 주소 : 원격 저장소와 새로 연결 하는 명령어

- git remote remove 이름 : 원격 저장소 연결된 이름 삭제

- git remote add 이름 주소 : 원격 저장소와 새로 연결 하는 명령어

- git restore 파일명

      add 전 수정된 파일 되돌릴때 / 전부지울 때는 파일명 자리에 . 사용

- git reset HEAD 파일명

      commit 전 스토리지에서 제거하기

- git commit --amend

      바로 직전 commit 메세지 수정하기

---

---

### [ prefix ]

- feat: 기능 개발 관련

- fix: 오류 개선 혹은 버그 패치

- docs: 문서화 작업

- test: test 관련

- conf: 환경설정 관련

- build: 빌드 관련
- ci: Continuous Integration 관련(지속적 통합)
