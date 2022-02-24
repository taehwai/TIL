# 2일차 정리

### 1.  github 가입 

 	1. https://github.com/ 에 접속
 	2. `sign up` 클릭
 	3.  e-mail과 username에 `git config` 설정에서 입력한 이메일과 닉네임 입력
 	4.  이메일 인증 후 회원 가입 완료

---

### 2. github 설정

​	1.오른쪽 상단 프로필 클릭

​	2.`Settings` 를 클릭합니다.

​	3.`왼쪽 안내 바에서 `Repositories`를 선택합니다.

​	4.`Repository default branch`의 입력 창에서  `main`을 지우고 `master`로 작성합니다.

​	5.`Update`를 클릭합니다.

---

### 3. github 원격 저장소 생성

1. `New repository` 클릭
2. 저장소의 이름, 설명, 공개 여부를 선택후 `Create repository` 클릭

---

### 4 . 로컬저장소와 원격저장소 연결, 조회

```bash
git remote add <이름> <주소>
git remote -v
git remote rm <이름> # 연결 삭제
```

---

### 5. 원격저장소에 업로드 하기

```bash
업로드할 파일이 있는 폴더에서 code로 열기후 vscode로 진행
git init
git status #파일 상태 확인
git add <파일 이름>
# ex) git add day1.md
git add . #폴더 내의 모든 파일
git commit -m "add <파일 이름>"
# ex) git commit -m "add day1.md"
git log --oneline #로그 확인
git push <저장소 이름> <브랜치이름>
#ex) git push origin master
```

---

### 6. .gitgnore

- 특정 파일 혹은 폴더에 대해 Git이 버전 관리를 하지 못하도록 지정하는 것

1. .gitignore에 작성하는 목록

- 민감한 개인 정보가 담긴 파일 (전화번호, 계좌번호, 각종 비밀번호, API KEY 등)
- OS(운영체제)에서 활용되는 파일
- IDE(통합 개발 환경 - pycharm) 혹은 Text editor(vscode) 등에서 활용되는 파일
  - 예) pycharm -> .idea/
- 개발 언어(python) 혹은 프레임워크(django)에서 사용되는 파일
  - 가상 환경 : `venv/`
  - `__pycache__/`

2. .gitignore 작성 시 주의 사항

- 반드시 이름을 `.gitignore`로 작성합니다. 앞의 점(.)은 숨김 파일이라는 뜻입니다.
- `.gitignore` 파일은 `.git` 폴더와 동일한 위치에 생성합니다.

3. .gitignore 사이트

- https://gitignore.io/ # 개발 환경에 맞는 걸로 복사, 붙여넣기 한다.