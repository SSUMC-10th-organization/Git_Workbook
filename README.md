# Github Session
3월 19일 목요일에 진행되는 숭실대학교 UMC 10th Github Session 자료 입니다!

## Hand-On 실습 순서

### 1. 자신만의 Main Branch 만들기
<img width="1106" alt="image" src="https://github.com/user-attachments/assets/d1e9ee3d-cc84-4d52-90a3-a510449c67d2" />
<br/><br/>

먼저 branch 에 들어가서 자신만의 Main Branch를 만듭니다.
이게 운영진 측에서 과제를 제대로 진행했는지 확인하게 될 branch 입니다.

<img width="1144" alt="image" src="https://github.com/user-attachments/assets/dae7be38-4d11-49b5-bbce-1a43761feffe" />
<br/><br/>

여기서 새로 계속 분기하여 branch를 파고 pull request를 진행해서 합병하여 계속해서 workbook을 쌓아나갈 예정입니다.
<br/><br/><br/>

---

### 2. New Issue 만들기
<img width="1105" alt="image" src="https://github.com/user-attachments/assets/e66353e0-12f6-4d55-bf93-911610256aa8" />
<br/><br/>

원래는 기능, 버그 등 협업에서 맡는 부분을 작성하지만, workbook을 진행할 때는 어떤 내용을 스터디 하는지 나누는 용도로 사용합니다.
사진과 같이 미리 이슈 템플릿을 정의해놨으니 확인하시면 됩니다.

<img width="731" alt="image" src="https://github.com/user-attachments/assets/93e93069-149e-4421-a399-00f74dec0dfc" />
<br/><br/>

위의 그림과 같이 이슈가 생성될텐데, 닉네임 / 이름에 맞춰서 적어주세요
<br/><br/><br/>

---

### 3. Git Clone 하기
<img width="835" alt="image" src="https://github.com/user-attachments/assets/5d11607e-5ea4-4159-96e8-d85eb494208c" />
<br/><br/>

메인으로 돌아와서 code 버튼을 누르면, 이 레포지토리의 url이 뜨게 되는데 이를 복사해주세요.
우리 local 에서 이 레포지토리를 연결하기 위한 과정입니다.

```shell
git clone {원격 레포지토리 주소}
```
<br/>

![image](https://github.com/user-attachments/assets/8dcfd06e-abb9-427e-87ea-11d1269e24e3)
<br/><br/>
실제 제 디렉토리에 Git_Workbook 레포지토리가 생긴 것을 확인할 수 있습니다.
<br/><br/><br/>

---

### 4. info.sh 실행시키고 따라가기

![image](https://github.com/user-attachments/assets/5dcd9638-096e-4a4e-8aa0-2db1a1af2dd1)
<br/><br/>
week1에 들어가서 info.sh를 실행시키면 위와 같이 가이드라인을 확인할 수 있습니다.
아래에 많이 쓰이는 명령어들을 정리해드릴테니 직접 따라가 보세요!

---

### 5. validate.sh로 확인하기

![image](https://github.com/user-attachments/assets/b112eb46-8446-4f89-bf10-aba2e45b74d9)
<br/><br/>
수많은 가이드라인을 헤치고 오시면, validate.sh를 실행시켜 보세요!
위와 같이 확인되었다고 뜨면 성공입니다 -! 이제 pull request 하러 가볼게요

<br/>

---

### 6. Pull Request 올리고 merge 하기

<img width="1088" alt="image" src="https://github.com/user-attachments/assets/4ac553df-89ed-4e09-ad4d-af5fd6486e4a" />


<img width="506" alt="image" src="https://github.com/user-attachments/assets/120cd1ba-cafe-49b1-8f97-2c5ebc0ec9b7" />


<img width="548" alt="image" src="https://github.com/user-attachments/assets/bd3dc51c-ab81-4b87-b2d2-085f2baba5d3" />


<br/><br/>
**이 부분 정말 정말 중요합니다!!!**

pull request 올릴때 저렇게 초기에 설정되어 있는 곳으로 올리면 안됩니다!!!
꼭 저렇게 다시 merge 할 곳을 다시 정해주셔야 합니다 .... 🤗

그 뒤에 자신의 main 브랜치에 week1-{닉네임} branch를 합병하게끔 처리해주시면 됩니다 -!

<img width="1092" alt="image" src="https://github.com/user-attachments/assets/fddf7f6f-b449-4e9f-b915-ab30ecac0fd3" />

가이드라인대로 풀리퀘까지 만드신다면 바로 합병하지 마시고, 주변 운영진의 심사 후에! 함께 합병해주시면 됩니다-! 고생 많으셨습니다 🥰

---

# Git 명령어

### Add

```zsh
git add "file name"
```

- "file name"의 파일을 추적 및 Staged로 전환하는 명령어

```zsh
git add .
```

- 작업 중인 모든 파일을 추가 및 Staged로 전환하는 명령어

---

### Commit

```zsh
git commit -m "Commit Message"

git commit --amend

git commit --amend -m "Commit message"
```

`-m` 옵션은 커밋에 이름을 적어주는 옵션<br>
`--amend` 옵션은 현재 커밋 내용을 제일 최근 커밋과 합치는 것.

---

### Log

```zsh
git log

git log --oneline #주로 사용, 로그를 한 줄로 볼 수 있음.
```

과거 버전을 확인할 수 있습니다.

---

### Branch

```zsh
git branch
```

로컬에서 사용 중인 브랜치를 확인하는 명령어

```zsh
git branch -D "브랜치명"
```

로컬에서 사용 중인 브랜치를 제거하는 명령어

---

### Checkout

```zsh
git checkout "Branch Name"
```

- "Branch Name"의 브랜치로 이동하는 명령어

```zsh
git checkout -b "New Branch Name" # 이 방법으로 브랜치 개설을 추천
```

- 새로운 브랜치 "New Branch Name"으로 개설하면서 이동하는 명령어

---

### Push

```zsh
git push origin
```

커밋한 내용을 `origin` 원격 레포지토리로 업로드

---

### Pull

```zsh
git pull
```

현재 작업 중인 브랜치에서 원격 브랜치의 버전이 더 높을 때, 변경사항을 원격에서 로컬로 가져오는 명령어

---

### Merge

> 개발자가 "Branch A"에서 작업 중이고, "Branch B"의 변경사항을 병합한다고 가정.

```zsh
git merge "Branch B"
```

"Branch B"의 변경사항을 병합하는 명령어

---

### Pull Request

> Pull Request는 git의 기능이 아니고, GitHub의 기능입니다. \
> D 브랜치의 작업사항을 C 브랜치에 병합을 하고 싶은 상황에서, 팀원들과 변경사항을 공유해야 하는 시나리오가 빈번합니다. \
> `develop` 브랜치에 개발자 개별 작업 브랜치의 변경사항을 병합해야 하는 상황을 앞으로 개발하면서 많이 마주하게 될 것 입니다.

```zsh
git checkout D

git push origin D
```
<br>

- GitHub Pull Request에서 PR을 개설합니다.
- C 브랜치에 병합합니다. 이 때 병합은 원격 레포지토리의 C 브랜치(origin/c)에 병합이 진행됩니다.
- 변경된 origin/c 브랜치의 변경 사항을 로컬로 `pull` 받아옵니다.

```zsh
git checkout C

git pull origin C
```

## Advanced Skills

### Delete Push

```zsh
git push -d "Remote Name" "Branch Name"

git push -d origin feat/#55
```

원격에 브랜치를 푸시가 되어있는 상황에서, 푸시를 제거하고 싶을 때 수행하는 명령어입니다.

---

### Fetch

`pull`과 `fetch`의 가장 큰 차이점은 원격의 사항들을 가져와서 로컬에 자동으로 적용한다는 점 입니다.
1. `git fetch` 명령어를 실행하면 레포지토리에 있는 변경사항들을 `origin/branch`으로 가져옵니다.
2. `origin/branch`에 가져온 변경사항들을 `branch`에 적용합니다.

즉 정리하자면, `git pull`로 수행되는 동작을 `git fetch`와 `git merge`로 두 단계를 거쳐서 진행합니다.

그렇다면 해당 작업을 왜 사용하는가?

- 더욱 세부적으로 원격에 있는 변경사항을 적용할 수 있습니다.
- 다른 로컬 브랜치에 번경사항을 적용할 수 있습니다.
    - 예를 들어 `A`라는 브랜치로 원격에 있는 `origin/A`의 변경사항을 적용할 수 있는 상황입니다.
    - 여기서 `B`라는 브랜치에도 `origin/A`를 적용할 수 있습니다.

즉, 더욱 세부적으로 작업할 수 있습니다.

```zsh
git fetch origin
```

```zsh
git merge origin/"fetched branch name"
```

---

### Stash (임시저장)

> `git stash` 명령어는 현재 작업하던 브랜치에서 다른 브랜치로 전환하는데, 변경사항들을 임시저장하고 넘어가려고 할 때 사용합니다.

```zsh
git stash
```

작업 중인 항목들을 임시저장합니다.

```zsh
git stash list
```

임시저장된 변경사항들의 리스트를 보여줍니다.

```zsh
git stash pop
```

stash는 스택으로 관리가 됩니다. <br>
가장 최근에 stash한 작업 내용이 불러와집니다.


임시저장된 항목 중 하나를 선택하여 저장합니다.

---

### HEAD

HEAD의 개념
1. HEAD는 일종의 포인터입니다.
2. 터미널에서 현재 상태로 보여지는 값을 HEAD라고 합니다.

---

### Checkout into Hash

```zsh
git log --onelist # 기존 커밋들의 리스트가 나열됨. 이때 커밋의 해시값을 확인.


git commit checkout "commit hash"
```

과거 버전으로 돌아갑니다.

---

### Merge Conflict Resolve Editor & GUI Tools

- [GitKraken](https://www.gitkraken.com/)
- VSCode Extensions
    - [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
    - [GitHub Pull Requests](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)

---

### PR 병합 간 충돌을 줄일 수 있는 팁

> develop 브랜치로 내가 작업 중인 feat/#7 브랜치를 병합하려고 가정을 해봅시다.

`feat/#7` 브랜치를 원격으로 업로드 하기 전에 가장 최신의 `develop` 브랜치를 `feat/#7` 브랜치로 병합합니다.

```zsh
git checkout feat/#7

git merge develop
```

이렇게 했을 때의 이점이 무엇이냐?

- 로컬에서 미리 충돌을 잡고 원격으로 업로드 하기 때문에, 충돌이 발생한다는 불필요한 상황을 미리 해결할 수 있음.
- GitHub에서 웹브라우저에서 충돌을 잡을 수 있는 도구도 있지만, 로컬에서 사용할 수 있는 도구가 훨씬 더 강력해서 개발자의 피로도를 줄일 수 있음.

---

### 브랜치 전환 / 파일 복원

- **기존 방식 (`checkout`)**

    ```bash
    # 브랜치 전환
    git checkout develop

    # 파일 복원 (마지막 커밋 상태로 되돌림)
    git checkout -- app.py
    ```

- **새로운 방식 (`switch` / `restore`)**

    ```bash
    # 브랜치 전환
    git switch develop

    # 파일 복원
    git restore app.py
    ```

→ `checkout`의 역할을 분리해서 더 직관적

---

### reset vs revert

- **reset**
    - HEAD를 특정 커밋으로 이동, 이후 커밋은 사라짐
    - 옵션:
        - `--soft`: 변경을 staging area에 남김
        - `--mixed`(기본): 변경을 working directory에 남김
        - `--hard`: 변경까지 모두 삭제

      ```bash
      git reset --hard a1b2c3d
      ```

      → `a1b2c3d` 이후 커밋이 전부 삭제됨  
      → 로컬 정리용, 협업에서는 위험

- **revert**
    - 특정 커밋을 취소하는 “반대 커밋”을 새로 기록
    - 히스토리는 보존됨 → 협업 시 안전

      ```bash
      git revert a1b2c3d
      ```

      → `a1b2c3d`를 무효화하는 커밋이 추가됨

---

### rebase

- **용도**
    - 브랜치 기반을 다른 브랜치로 옮겨 커밋을 다시 쌓음
    - `merge`는 병합 커밋이 생기지만, `rebase`는 히스토리를 직선(linear)으로 유지

      ```bash
      git checkout feature
      git rebase main
      ```

      → feature 브랜치의 커밋들이 main 최신 위로 다시 적용됨

- **예시 상황**

    ```
    main:    A---B---C
    feature: A---B---D---E
    ```

  `git rebase main` 결과

    ```
    A---B---C---D'---E'
    ```

- **충돌 시 장점**
    - `merge`: 한 번에 병합 → 큰 충돌
    - `rebase`: 커밋 단위로 적용 → 충돌을 나눠서 해결

---

# Git-Study
### 💻 실행 환경 안내
과제 확인과 수행, 인증은 모두 CLI 환경에서 진행됩니다.
> 맥의 경우 `Git_Study` 폴더 위에서 오른쪽 버튼을 클릭하신 후 `서비스` > `폴더에서 새로운 터미널 열기`를 클릭하셔서 터미널을 실행해주세요!

> 윈도우의 경우 Git Bash를 이용해 진행해주세요.

###  🌳 주차별 과제 브랜치 생성
아래와 같은 양식으로 생성해주세요. (e.g. `week10-zimging`)
```swift
week(주차 번호)-(본인 닉네임)
```

### 📚 주차별 과제 확인 안내
10주차 과제는 꼭 명령어 실행 전에 과제 브랜치를 생성하시고 이동하신 뒤 아래 명령어를 실행해주세요.
터미널에서 아래 명령어를 실행하셔서 주차별 과제를 확인하신 후 수행해주세요! (e.g. `./week10/info.sh`)
```
./week(주차 번호)/info.sh
```

### 💯 주차별 과제 인증 안내
터미널에서 아래 명령어를 실행하셔서 주차별 과제가 제대로 수행되었는지 확인해주세요!
`✅ 모든 과제가 확인되었습니다!` 라는 문장이 출력되면 캡쳐하신 후 Pull Request 양식에 맞춰 첨부하시고 PR을 올려주세요.
```
./week(주차 번호)/validate.sh
```
과제 확인과 리뷰가 완료되면 PR은 `merge`되지 않고 `closed` 상태로 변경됩니다.
정상적으로 closed 되지 않았다면 리뷰를 확인해주세요!

---
Copyright © 2024 Lee Youjin All rights reserved.
