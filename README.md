## FogVDN

FogVDN，是Pear（梨享计算）出品的一个面向未来、专注于服务在线视频流媒体的CDN。它是Pear Fog（梨享雾计算）平台的重要组成部分，具有以下特色：
* 众包
  绝大部分带宽和存储收集自普通用户稳定在线的边缘网关设备，如智能路由器、NAS
* 全部基于开放的、国际标准的协议，如：
  + HTTP2
  + WebRTC
  + HLS
  + DASH
* Web友好，“连接一切”
* 高效率，在VoD、Live、VoIP等场景中均有专门优化的定制算法
* 安全可靠

## 集成及JS API

> FogVDN是Web友好的，使用开放的Web标准（不需要额外的任何插件，只需要HTML5和WebRTC）
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


## 海量可长时间稳定提供服务的节点

![节点架构](fig/pear-fog-node-engine.png)


