# BOM

### 브라우저 객체 모델 Browser Object Model

`window`  
브라우저 창. 모든 객체가 소속된 객체

```markdown
window.open('https://google.com')
window.close()
```
  
`document`  
현재 웹문서에 대한 정보

```markdown
document.querySelector('.btn-del')
```

`history`  
현재 브라우저가 접근했던 url 히스토리 제어

```markdown
history.back()
history.forward()
```

`location`  
window, document의 프로퍼티. 문서의 url을 변경 혹은 문서의 위치 정보

```markdown
location.host
location.href = 'https:// google.com'
```

`screen`  
사용자의 디스플레이 화면에 대한 정보

```markdown
console.dir(screen)
```

`navigator`  
실행중인 애플리케이션(브라우저)

```markdown
navigator.geolocation.getCurrentPosition()
navigator.appName
navigator.appVersion
```