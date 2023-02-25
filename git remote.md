# git remote

## ✏️ 새로운 .git 생성하기

- 원하는 디렉토리로 이동해 서 .git 을 생성한다.

```html
git init
```

⚠️ git push 를 하게되면 .git 에 있는 파일들이 서버로 업로드 된다.

즉, .git 폴더에 있는 파일만 업로드를 시킬 수 있고,

.git 폴더가 없다면 서버에 업로드를 할 수 없다.

<br>

- .git 폴더가 잘 생성됬는지 확인

```html
ll -arlth
```

- 직접 폴더를 열어서 확인할 수도 있다.
    - 파일이 숨겨져 있어서 C + S + . 으로 숨긴파일보기를 해주어야 한다.



<br>

## ✏️ 기존 remote 변경하기

- 기존에 연결되어있는 remote 를 종료하고 새로운 remote 로 연결시켜 주어야 한다.
- remote 를 종료하는 명령어를 실행한다.

```html
git remote remove origin
```

<br>

- 원하는 remote 에 연결시켜준다.

```html
git remote add origin 주소
```

- 연결을 확인할 수 있다.
    - 연결 확인 명령어

```html
git remote -v
```

- project 저장하기

```
git push --set-upstream origin main
```


- 연결이 완료되면 파일을 원하는 repostiory 로 업로드 할 수 있게된다.

<br>

## ✏️ .git 삭제하기

- .git 이 존재하는 디렉토리로 이동한 뒤 삭제 명령어를 입력한다.

```html
rm -rf .git
```
