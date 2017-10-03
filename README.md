# download-link
download-link可以通过判断浏览器类型跳转到指定的下载链接. 

### 具有如下特点
1. 简单易用, 可用于绝大多数webview客户端或者浏览器.
2. 可自由修改, 且仅有1个html页面.

### 实现原理
通过JavaScript判断navigator.userAgent特征字符实现.
``` javascript
var u = navigator.userAgent;
```
- iOS (iPhone & iPad)
``` javascript
/iPhone/i.test(u)
/iPad/i.test(u)
```
- Android
``` javascript
/Mozilla\/5.0/i.test(u) && /Android/i.test(u) && /AppleWebKit/i.test(u)
```
- Safari
``` javascript
/^((?!chrome|android).)*safari/i.test(u)
```
- Wechat
``` javascript
/micromessenger/i.test(u)
```

### 子组件enterprise-app.html
提供iPhone企业App下载的流程说明
