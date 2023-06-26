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
#### 4.js读取二进制数据
* [链接](https://juejin.cn/post/6844903672678203405)
* Blob API 用于处理二进制数据，可以方便地将数据转换为Blob对象或从Blob对象读取数据。
```javascript
// 创建一个Blob对象
const myBlob = new Blob(["Hello, world!"], { type: "text/plain" });
// 读取Blob对象的数据
const reader = new FileReader();
reader.addEventListener("loadend", () => {
 console.log(reader.result);
});
reader.readAsText(myBlob);
使用场景：在Web应用中，可能需要上传或下载二进制文件，使用Blob API可以方便地处理这些数据。
```
* TextEncoder 和 TextDecoder 用于处理字符串和字节序列之间的转换。它们可以方便地将字符串编码为字节序列或将字节序列解码为字符串。
```javascript
const encoder = new TextEncoder();
const decoder = new TextDecoder();
const myString = "Hello, world!";
const myBuffer = encoder.encode(myString);
console.log(myBuffer); // Uint8Array(13) [72, 101, 108, 108, 111, 44, 32, 119, 111, 114, 108, 100, 33]
const decodedString = decoder.decode(myBuffer);
console.log(decodedString); // "Hello, world!"
使用场景：在Web应用中，可能需要将字符串转换为二进制数据，或将二进制数据转换为字符串。使用TextEncoder和TextDecoder可以方便地进行这些转换。
```
