# terminal 에서 git clone & push

## ✏️ git clone

repository 에 있는 source 들을 내 로컬로 복사하는 기능

### 1. repository 주소 복사

local 로 복사를 원하는 repositry 에서 <> Code 버튼을 눌러서 나오는 url 을 복사한다.
![1](https://github.com/choideakook/Terminal/blob/main/images/221225_1.png)

### 2. directory 이동

터미널에서 clone 할 directroy 로 이동한다.

### 3. git clone

git clone 명령어 뒤에 복사했던 url 을 붙여넣기한다.

```
git clone url
```

## ✏️ git push

로컬에 있는 source 들을 repository 로 업로드 하는 기능

### 1. directory 이동

### 2. add

업로드 하고자 하는 source 를 스테이지에 push 하기전 트렉으로 이동시키는 작업이다.

```
git add 파일명
```

만약 해당 directory 에 있는 모든 파일을 업로드 하는 경우엔 파일명대신 . 을 붙이면 된다.

```
git add .
```

🔍 트렉으로 잘 이동되었는지 확인

제대로 되었다면 초록색으로 나타난다.

```
git status
```

❗️ add 취소하는 방법

만약 add 한 모든 파일을 삭제해야할 땐 파일명을 생략한다.

```
git reset HAED 파일명
```

### 3. commit message

파일을 업로드하거나 수정할 경우에 목적을 쉽게 확인할 수 있게 주석을 넣는 작업

```
git commit -m "commit message"
```

🔍 message 가 잘 처리되었는지 확인

작업이 정상적으로 되었다면 commit message 가 보인다.

```
git log
```

log 창에서 나가는 방법 : q

#### ❗️ commit 취소하는 방법

add 취소하는 방법과 비슷하다.

```
git reset HAED^ 파일명
```
  
만약 직전 commit message 를 취소하고싶다면  

```
amend
```
  

### 4. push

준비된 파일들을 스테이징 하는 기능

```
git push
```

🔍 push 확인

작업이 정상적으로 되었다면 Origin 이라는 문구가 뜬다.

```
git log
```

❗️강제로 push 하는 방법

브랜치의 끝이 리모트 브랜치 보다 뒤에있을 경우 앞선 commit 을 무시하고 새로 덮어쓴느 방법 (앞선 commit 을 무시하고 덮어쓰기때문에 꼭 확인 후 사용해야한다.)

```
git push origin main --force
```

🔍 브랜치 확인

```
git log --branches --graph --decorate --oneline
```

### ✏️ git 파일 삭제하는 방법

```
# 원격 저장소와 로컬 저장소에 있는 파일을 삭제한다.
$ git rm [File Name]
 
# 원격 저장소에 있는 파일을 삭제한다. 로컬 저장소에 있는 파일은 삭제하지 않는다.
$ git rm --cached [File Name]
```
