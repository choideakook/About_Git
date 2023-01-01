# repository 폴더명,  경로 변경하기

1. git clone 을 해서 local 에 repository 를 저장해 준다.
2. 폴더명을 변경하거나, 경로를 원하는 대로 변경 해준다.
    - 폴더명 변경
        - 참고로 대소문자 변경은 한번에 안된다.
    
    ```html
    git mv 현재폴더명 바꿀폴더명
    ```
    
3. 아래 명령어로 git 에 업로드를 해준다.

```html
git add .
git commit -am "rename folder"
git push origin main
```