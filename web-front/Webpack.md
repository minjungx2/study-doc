# Webpack

1. 개발 편의로 인해 여러개의 모듈로 개발된 웹 애플리케이션을 웹 서버로 배포.  
2. 브라우저는 웹 서버에 html, css, js 와 같은 자원을 요청.
3. 모듈을 분리하다보면 브라우저에서 서버에 요청하는 개수가 많아지게 됨.
4. 페이징 로딩시간이 길어지는 등의 이슈가 발생.  
	- 이러한 이슈로 배포전 여러개의 파일을 하나의 파일로 묶어서 베포.  

### 번들링(Bundling)
- 여러개의 파일 ( main.js + a.js + b.js + c.js ) 을 하나의 파일 ( bundle.js )로 압축.  

### 번들러 (Bundler)
- 여러개의 파일을 번들링해주는 도구.
- ex) Webpack  

### Webpack 설치
```
npm install --save-dev webpack webpack-cli

npx webpack --entry ./src/index.js : entry는 웹팩의 진입점. 어떠한 파일을 기준으로 번들링을 할것인지.
npx webpack --output ./dist : 번들링 한 파일의 위치.
npx webpack --output ./dist --mode develope : 압축없이 번들링하는 옵션.
npx webpack : webpack.config.js 의 설정을 참조하여 번들링.
```

### webpack.config.js
```javascript
const path = require('path');

module.exports = {
  entry: './src/index.js', // 징=진입점
  output: { // 번들링 파일이 위치할 경로
    path: path.resolve(__dirname, 'dist'),
    filename: 'bundle.js',
  },
};
```