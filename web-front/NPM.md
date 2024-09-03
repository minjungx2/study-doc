# NPM

### 모듈 저장소 Node Package Manager
- 자주 사용하는 기능을 모듈화 => 모듈 저장소에 공유
- 공유된 모듈을 설치하여 사용할 수 있다.

### npm 설치
- Node.js 설치  
- `Node.js` : javascript 런타임 환경.

### 버전 확인
```
node: node -v
npm: npm -v
```


### package.json
- npm 으로 프로젝트를 관리할때 필수 파일
- `npm init` 명령어로 자동 생성

`name` : 프로젝트 명  
`version` : 프로젝트 버전. ex) 1.0.0  
`description` : 프로젝스 설명  
`private` : true 설정시 npm 게시 거부  
`scripts` : 자주 실행되는 명령어를 작성. npm 명령어로 실행 가능. ex) npm run ~  
`dependencies` : 프로젝트에서 사용하는 모듈을 기술하는 부분  
`devDependencies`: 개발할때만 의존하는 모듈

#### 라이브러리 설치
```
npm install <모듈명>
npm install --save-dev <모듈명>
```


### package-lock.json
- 프로젝트에 설치된 모듈들의 의존성 트리를 기록하고 있다.
- 라이브러리들 간에는 의존 관계를 갖고있다. 의존된 모든 라이브러리를 갖고있어야한다.

### node_modules
- 포로젝트에서 사용하는 라이브러리가 실제로 설치된 경로
