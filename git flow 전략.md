# git flow 전략

## ✏️ ***프로젝트 개발자***

- ***이슈 확인***
    - 양수인과 이슈 내용을 확인해 처리해야 할 업무를 숙지한다.
- ***코드 가져오기***

```sql
git clone ..
```

(main)

```sql
git pull origin main
```

- ***Branch 생성 (main)***
    - 처리해야 할 업무 / issue 번호 로 브랜치 명을 하는 것이 관례이다.

```
git checkout -b enhancement/#
```

- ***작업 시작 (enhancement/#)***
    - branch 가 enhancement/# 상태로 작업을 한다.
    - commit 으로 data 를 틈틈히 저장해준다.
- ***코드 최신화 (enhancement/#)***
    - 작업 중간 중간 틈틈히 최신화를 해준다.

```
git pull origin main --rebase
```

- ***작업 완료 repository 에 push***

```
git push origin enhancement/#
```

- ***PR 작성***
    - repository pr 에서 코드 검토 요청과 main 에 merger 를 요청한다.
    - close # 으로 승인될 경우 issue 가 닫힐 수 있게 참조해준다.
- ***branch 삭제***
    - pr 이 허가되면 branch 를 삭제해야 한다.
    - 일단 main 브랜치로 돌아간다. (enhancement/#)
    
    ```
    git checkout main
    ```
    
    - 코드 최신화 (main)
        - 내가 pr 한 코드도 이때 pull 로 최신화 된다.
    
    ```
    git pull origin main
    ```
    
    - 브랜치 삭제 (main)
    
    ```
    git branch -D enhancement/#
    ```
    
    - 브랜치 완전 삭제 (main)
    
    ```
    git fetch --prune
    ```
    

<br>

## ✏️ ***프로젝트 매니저***

- 이상이 있을경우 코맨트와 함께 리젝한다.
    - file changed → request changes
- 이상이 없다면 squash merge 로 허가해준다.
    - pr 을 허가후 enhancement/# 브랜치를 삭제해준다.