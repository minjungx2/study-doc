# Module Sysyem

### 모듈시스템 장점
- `네임스페이스화`  
코드의양이 많아질수록 전역 스코프에 존재하는 변수명이 겹치는 경우가 발생.  
모듈로 분리하면 모듈만의 네임스페이스를 갖기때문에 이러한 문제를 해결할 수 있다.
- `재사용성`  
같은 코드를 반복하지 않고 모듈로 분리시켜 재활용할 수 있다.

### 모듈시스템 종류
- `AMD`
- `CommonJs` : NodeJS 환경을 위해 만들어진 모듈 시스템
- `UMD`
- `ES Module` : ES6 에 도입된 자바스크립트 모듈 시스템

### ES Module
script 태그에 `type="module"` 적용하면 모듈로 사용 가능.
- `export`
```javascript
// user.js
export const userName = 'Rita'

// main.js
import { userName } from './user.js'
import * as user from './user.js'
```

- `export default`
```javascript
// user.js
const userName = 'Rita'
export default {
	userName
}

// main.js
import user from './user.js'
```

### CommonJS
- `exports`
```javascript
// user.js
exports.userName = 'Rita'

// main.js
const { userName } = require('./user')
const user = require('./user')
```

- `module.exports`
```javascript
// user.js
const userName = 'Rita'
module.exports = {
	userName
}

// main.js
const { userName } = require('./user')
const user = require('./user')
```

### NodeJS에서 ES 모듈 실행
- package.json 에 `"type" : "module"` 설정