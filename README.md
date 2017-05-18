## 集成及JS API
> FogVDN是基于浏览器工作的，使用开放的Web标准（不需要额外的任何插件，只需要HTML5和WebRTC）
> 非常容易集成到现有项目中，只需了了几行JS代码便可以集成

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

