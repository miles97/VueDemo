#### sharp 

* doing about future

* 小程序渲染的默认wx:for-item="item"，需要嵌套循环的时候使用wx:for-item="name"重命名,相当于vue中的 name,index in Array

* 使用web-view

小程序使用webview

直接新建一个components,js中配置，wxml写
```js
 <web-view  src="{{url}}?openId={{openId}}&uid={{uid}}&hash=1"></web-view>
 ```
 
 vue中使用webview(实际上并不叫webview)
 ```
 window.location.href =
  "https://baidu.com/html/dd.html?id=" +
  item.1d +
  "&sourceType=1&deviceType=1";
  ```
 
 ### 使用WS的场景 原生
在原生h5的端到端通信请求出现之前，客户端请求所用的技术都是 Ajax 轮询。轮询是在特定的的时间间隔（如每1秒），由浏览器对服务器发出HTTP请求，然后由服务器返回最新的数据给客户端的浏览器。这种传统的模式带来很明显的缺点，即浏览器需要不断的向服务器发出请求，然而HTTP请求可能包含较长的头部，其中真正有效的数据可能只是很小的一部分，显然这样会浪费很多的带宽等资源。

HTML5 定义的 WebSocket 协议，能更好的节省服务器资源和带宽，并且能够更实时地进行通讯。
WebSocket 事件
以下是 WebSocket 对象的相关事件。假定我们使用了以上代码创建了 Socket 对象：

open	Socket.onopen	连接建立时触发
message	Socket.onmessage	客户端接收服务端数据时触发
error	Socket.onerror	通信发生错误时触发
close	Socket.onclose	连接关闭时触发
```js
        var socket;
        if (!window.WebSocket) {
            window.WebSocket = window.MozWebSocket;
        }
        if (window.WebSocket) {
            socket = new WebSocket("ws://101.222.210.73:12/ws");//使用字符串拼接${this.requestUrl}
            socket.onmessage = function(event) {
                console.log(event.data);
                pollingFun();
            };
            socket.onopen = function(event) {
                var msg = {
                    type : '001',
                    ad : ad
                };
                socket.send(JSON.stringify(msg));
                console.log("连接开启!");
                pollingFun();
            };
            socket.onclose = function(event) {
                console.log("连接被关闭");
                setInterval(pollingFun,1500);
            };
        } else {
            alert("你的浏览器不支持 WebSocket！");
            setInterval(pollingFun,1500);
        }
```

属性	描述
Socket.readyState	
只读属性 readyState 表示连接状态，可以是以下值：

0 - 表示连接尚未建立。

1 - 表示连接已建立，可以进行通信。

2 - 表示连接正在进行关闭。

3 - 表示连接已经关闭或者连接不能打开。

Socket.bufferedAmount	
只读属性 bufferedAmount 已被 send() 放入正在队列中等待传输，但是还没有发出的 UTF-8 文本字节数。

### 除了使用原生h5API的websocket，还可以使用socket.io

后者是通过封装不同浏览器环境下的客户端服务端双向请求进行的服务，所以一定程度上兼容了很多不同环境的情况，如果没有什么特别的
兼容性要求，直接使用原生请求即可，同时react和vue各自有封装好的socketio可进行调用，减少部分代码依赖，减少体积。

3 - 表示连接已经关闭或者连接不能打开。

### 使用vue适配应用的基本原则

很多npm插件现在基本都有vue适配的应用来减少对应的冗余代码，并且合理的进行按需引入。
客观上允许的话，优先使用vue-xxx进行条件引入，尽量注意不要全局引入。

## 解决sourcetree上传代码没有引起视图更新的问题

在项目看板的账户配置中关联github账户，进行尝试

##  解决preventDefault (react onclick事件相关)
所有元素
*{
touch-action: none; 
} 
 
