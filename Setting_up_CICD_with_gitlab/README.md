## 개요
- 사내 보안 문제를 해결하기 위해 GitLab을 구축하여 사용하는 경우가 많음
- Docker를 사용하는 시스템에서 GitLab CI/CD 환경구성하는 내용을 정리하려 함
- CI/CD Pipeline 구성은 React 프로젝트 배포를 예시로 진행할 예정

## 해야 할 일
- GitLab 회원가입 및 Repository 생성
- React 프로젝트 생성
- GitLab Repository에 올리기
- Gitlab Runner 토큰 발급
- gitlab-ci.yml 작성

---

### GitLab 회원가입 및 Repository 생성
1. GitLab에 접속하여 회원가입을 한다.  
  https://gitlab.com/-/trial_registrations/new
  ![register](image/gitlab_signin_230620/reigster.png)
2. 주어진 절차에 따라 진행하면 완료된다. (Group, Repository 생성, 회사 어디 다니는지 등..)
   ![login](image/gitlab_signin_230620/login.png)
3. 둘러보면 gitlab-ci.yml 에디터가 보이는데 이걸 통해서 추후에 파이프라인을 구축하게 된다.
   ![login](image/gitlab_signin_230620/gitlab_ci.png)

### React 프로젝트 생성하기
1. 터미널 열어 create-react-app 으로 생성
   ```
   npx create-react-app {원하는 프로젝트 이름}
   ```
2. 터미널 열어 npm start로 잘 실행되는지 확인
   ```
   npm start
   ```
   ![npm_start](image/make_react_project_230621/npm_start.png)
   
- 참고
  - npm이 아닌 npx create-react-app 을 쓰는 이유
  https://ljh86029926.gitbook.io/coding-apple-react/undefined/npm-npx

### GitLab Repository에 생성한 React 프로젝트 올리기
1. 프로젝트 생성한걸 GitLab에 커밋 및 푸쉬
   ![commit](image/push_project_in_gitlab_230622/commit.png)