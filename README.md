# package 배포 방법
```
//package.json 버전 확인
pnpm build
pnpm login --registry=https://npm.pkg.github.com/ // 로그인 필요시, 토큰으로
pnpm publish //--no-git-checks
```
### 배포 상태 확인
```
npm view @kkkamango/lib-react-test --registry=https://npm.pkg.github.com/
```

# 배포한 package 사용 방법
- '.npmrc' 파일
```
# 기본은 npmjs
registry=https://registry.npmjs.org/

# GitHub 스코프만 별도로 지정
@kkkamango:registry=https://npm.pkg.github.com/
npm.pkg.github.com/:_authToken=YOUR_GITHUB_TOKEN
```

```
pnpm add @kkkamango/lib-react-test
```
