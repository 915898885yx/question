# question
#### 1.location.replace和vueRouter.replace safari浏览器下
* A、B、C页面。
* A -> B -replace> C   通过浏览器回退到A
* location.replace导致A页面请求走ajax缓存，同时导致报错
* vueRouter.replace 不会导致A页面走ajax缓存
#### 2.router-link和router.push跳转，safari浏览器 13.1.3版本
* A、B页面
* A通过router-link跳转到B，通过浏览器的退回返回到A
* A页面的初始化方法不执行（onMounted）或者setup下发起的接口请求
* 解决办法：将router-link跳转替换为router.push跳转
#### 3.ie浏览器不显示chrome、edge、firefox的logo的png图片。
* 解决办法：ui通过微调图片的颜色，看起来没什么变法，但是可以正常显示。
