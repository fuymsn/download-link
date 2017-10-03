# download-link
download-link可以通过判断浏览器类型跳转到指定的下载链接. 

The download-link can be reached the specified download link by judging the WEB Browser.

### Features
- 简单易用, 可用于绝大多数webview客户端或者浏览器.
- 可自由修改, 且仅有1个html页面.
- 响应式设计, 可用于不同终端.
<br><br>
- Easy to use, available for most webview clients and browsers.
- Only one html page, and can be freely modified.
- Responsive design used for different clients.

### The Principle
通过JavaScript判断navigator.userAgent特征字符实现.

Implementation by JavaScript navigator.userAgent character , as this follow:

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
- Language
``` javascript 
(navigator.browserLanguage || navigator.language).toLowerCase()
```

### 子组件 enterprise-app.html
提供iPhone企业App下载的流程说明

Provide instructions for the iPhone Enterprise App

### Release History
- 2017-10-03 v1.0.0 the first version