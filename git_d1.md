## GUI와 CUI

1. `GUI (Graphic User Interface)` : 그래픽을 통해 사용자가 컴퓨터 상호 작용
2. `CLI (Command Line Interface)` : 터미널을 통해 사용자와 컴퓨터 상호 작용
<br/><br/>


### CUI를 사용하는 이유


`ex) tandoori라는 새 폴더 생성하는 경우`

1. GUI : `마우스 우클릭 -> 새로 만들기 -> 폴더 -> 폴더명 작성`
2. CLI : `mkdir tandoori`

> 총 4단계를 소요하는 GUI에 비해 CLI는 1단계로 폴더 생성이 가능   
> GUI로는 불가능한 많고 세부적인 기능을 사용

<br/>

### 터미널 명령어 정리
<br/>

| 명령어 |              설명               |
| :----: | :-----------------------------: |
| mkdir  |            폴더 생성            |
| touch  |            파일 생성            |
|   ls   |   현재 폴더의 파일 목록 출력    |
|   cd   |        다른 폴더로 이동         |
|   mv   |  폴더/파일 이동 또는 이름 변경  |
|   rm   | 파일 삭제 / 폴더 삭제 (-r 옵션) |

<br/>

---

## Why Git & Github?
---
<br/>

![Git로고](https://user-images.githubusercontent.com/49775540/168756716-68f9aebb-380f-4897-8141-78d8403f6113.png)

<br/>

### Git

- **분산 버전 관리 프로그램**
- 백업, 복구, 협업을 위해 사용
- [Git 공식문서](https://git-scm.com/book/ko/v2)

### Github

- Git을 사용하는 프로젝트의 협업을 위한 **웹호스팅 서비스**

<br/>

---
## [1] Git 초기 설정
---

최초 한 번만 설정, 매번 설정할 필요가 없음
1. 누가 커밋 기록을 남겼는지 확인을 위해 이름과 이메일을 설정   
작성자를 수정하고 싶은 경우 이름, 메을 주소만 다르게 하여 동일하게 입력   
```bash
$ git config --global user.name "이름"
$ git config --global user.email "메일 주소"
```
2. 작성자가 올바르게 설정되었는지 확인
```bash
$ git config --global -l
$ git config --global --list # 둘 중 하나 사용 가능
```
<br/>

---
## [2] Git 기본 명령어
---

<br/>

### 1. 로컬 저장소 (Git local operation)

<br/>

![워크플로](https://noritersand.github.io/images/git-local-operations.png)
[이미지 출처](https://git-scm.com/book/en/v2)   
<br/>

- `Working Directory (= Working Tree)` :사용자가 일반적으로 작업하는 곳
- `Staging Area (= Index)` : 커밋을 위한 파일 및 폴더가 추가되는 곳
- `Repository` : Staging Area에 있던 파일 및 폴더의 변경사항(커밋)을 저장하는 곳
- Git은 **Working Directory** → **Staging Area** → **Repository** 의 과정으로 버전 관리를 수행

> **Working Directory** = **대기실**   
> **Staging Area** = **무대**   
> **Repository** = **사진** 으로 생각하니 이해하기 쉬웠음

> 버전 관리를 위해 마지막 수정 파일과 변경 내용만을 저장