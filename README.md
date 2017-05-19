## 集成及JS API

> FogVDN是基于浏览器工作的，使用开放的Web标准（不需要额外的任何插件，只需要HTML5和WebRTC）
> 非常容易集成到现有项目中，只需几行JS代码便可以集成

``` js
<video  id="pearvideo" controls="controls" autoplay="autoplay" ></video>
<script src="PearPlayer.js"></script>
<script>
    var PearPlayer = require('PearPlayer');
    PearPlayer('#pearvideo',{
        type: 'mp4',
        src: 'https://xxx.webrtc.win/tv/f.mp4',
        token: token
    });
</script>
```

## 安全问题

* HTTP通道全部切换到HTTPS通道
* WebRTC通道传输数据使用SCTP协议和TLS加密来保护的
* 信令通信是通过安全的WebSocket完成的，该WebSocket也使用TLS加密。


