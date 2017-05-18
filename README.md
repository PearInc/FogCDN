# 集成及JS API
··· javascript
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
···
