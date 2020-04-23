# (2020.04.23) Git 특강

- 코드관리도구
- 협업 도구
- 배포 도구

## 1. 코드관리 도구

---

### (1) SCM (Source Code Management)

- **버전**을 통해 관리 (Version Control System)
- **디렉토리** 중심 관리 (Repository)

### (2) 기본 명령어

### `git init` (git 삭제 : `rm -rf .git`)

- .git 폴더 생성 : git 관련 데이터가 저장된 폴더
- (master) 프롬프트로 변경

### `git status`

- 현재 git 저장소(Repository)의 상태를 확인

### `git add`

- 버전 관리할 파일/폴더를 지정

### `git commit`

- 스냅샷 (버전 생성)

### `git log` (`git log —oneline` : 한줄로 표시)

- 현재까지 저장된 버전을 조회

### `git diff`

- 변경된 내용 확인

### `git checkcout [COMMIT HASH]`

- 특정 commit 상태로 돌아감 (과거 상태를 조회하기만 하고 수정은 하면 안됨)
- master 상태로 돌아가기 : `git checkout master`

### (3) 원격 저장소 관련 명령어

### `git remote`

- 현재 설정된 원격 저장소 관련 정보를 조회

### `git remote add [저장소의 별명] [저장소의 주소]`

- git remote add origin [https://github.com/](https://github.com/.../.../)깃헙아이디/레포 이름

### `git push [저장소의 별명] [Branch의 이름]`

- 원격 저장소에 저장

### `git clone [저장소의 주소]([디렉토리명])`

### (4) Branch

**Branch는 일회용
⇒ 더 이상 쓰이지 않는 Branch는 정리가 필요하다**

### `git branch`

- 모든 branch 목록을 조회

### `git branch [브렌치명]`

- 새로운 브렌치를 생성

### `git checkout [브렌치명]`

- 해당 브렌치로 이동

### `git merge [(합칠)브렌치명]`

- (주의) master에서 test를 병합할 때, merge 전에 master로 이동 후 merge를 진행해야 함
- `git checkout master` ⇒ `git merge test`

### `git branch -d [(삭제할)브렌치명] / git branch -D [브렌치명]`

- -d : 이미 병합된 브렌치를 삭제 (soft deletion)
- -D : 병합되지 않은 브렌치를 삭제 (hard deletion)

### (5) Merge 시나리오

### 1. Fast-Forward Merge

### 2. Auto Merge

### 3. Merge Coflict

## 2. 협업 도구

### (1) Push & Pull 모델

- Synchronuous  작업
- 해당 프로젝트에 대한 push 권한이 필요함 (공동작업자로 초대)

### (2) Fork & Pull Request 모델