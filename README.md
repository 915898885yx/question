# question
#### 1.location.replace和vueRouter.replace safari浏览器下
* A、B、C页面。
* A -> B -replace> C   通过浏览器回退到A
* location.replace导致A页面请求走ajax缓存，同时导致报错
* vueRouter.replace 不会导致A页面走ajax缓存
