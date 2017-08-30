# FogVDN - The Video CDN in the Fog with Crowdsourcing

 FogVDN proposed by Pear, future oriented, focuse on online video streaming service. It is an important component of the Pear Fog. It has the following features

## <img src="fig/icon/一键接入.png" width="28"> Integrate Easily, CP or CDN can  "Click to Start"

``` js
<video id="v1" src="https://example.com/v1.mp4"></video>
<script src="PearPlayer.js"></script>
<script>
    var player = new PearPlayer('#v1', token, opts);
</script>
```

> Web friendly, uses the Web open standard (No plug in, just need HTML5 and WebRTC)

> Integrate with your project easily , only need few JS code.

## <img src="fig/icon/海量规模.png" width="28"> Crowdsourcing, Massive Node, Wide Coverage

   - Massive, stable service node.
   - Most bandwidth, storage and computing resources were collected by crowdsourcing from the stabilize online edge devices owned by users.
   - Service cover all regions, all operators, all edge of the network.
   - Dynamic, real-time monitoring and scheduling, data transmission distances would be "zero hop".

![节点架构](fig/pear-fog-node-engine.png)

<img src="fig/devices/PearSharingBox1.jpg" height="90"> <img src="fig/devices/PearSharingBox2.png" height="90"> <img src="fig/devices/QNAP.png" height="90"> <img src="fig/devices/newifi2.png" height="90"> <img src="fig/devices/newifi3.png" height="90">

## <img src="fig/icon/延迟.png" width="28"> Low Latency
Through massive node and dynamic, real-time monitoring and scheduling, data transmission distances would be "zero hop".


## <img src="fig/icon/多通道.png" width="28"> Multi Source, Robustness

   1. In data transmission, the traditional CDN is one-to-many relationship, that means, the average of the user quality of service is inversely proportional to the number of users. Pear FogVDN schemes to get file data from multi channels, reducing the dependency on a single point or single link, solve the HD video play back problem that the single link may not meet the bandwidth, also solve the problem of weak network packet loss problem through the UDP channel, users will have a better watching experience.

  ![multisources](fig/fogvdn_multisources.png)

   2. In service, it will dynamically explore the status and service capabilities of other nodes, automatically switch to the optimal node group and adjust the data ratio to guarantee the user experience.

## <img src="fig/icon/iso.png" width="28"> Support International Open Standard Protocol

   + [HTTP2](https://en.wikipedia.org/wiki/HTTP/2)
   + [WebRTC](https://webrtc.org/)
   + [HLS](https://developer.apple.com/streaming/)
   + [DASH](http://mpeg.chiariglione.org/standards/mpeg-dash)

## <img src="fig/icon/连接一切.png" width="28"> Web Friendly, "Connect the World"

![播放器](fig/PearPlayer.png)

## <img src="fig/icon/智能算法.png" width="28"> High Effciency, Customized Algorithm in VoD, Live, VoIP.

## <img src="fig/icon/安全.png" width="28"> Safe and Reliable

   It supports the secure storage and transmission, prevents the data from being tampered, avoids the leakage of the copyright document and the content hijacking.

   * All edge nodes support TLS, HTTP use HTTPS(HTTP2.0) by default.
   * WebRTC channel tranfer data encoded by SCTP and DTLS.
   * Signaling communication by WebSocket, also encrypted by TLS/SSL.
   * Optional data encryption, segmentation, fragmentation and blocking.
## <img src="fig/icon/降低成本.png" width="28"> Low Cost

Compared to the traditional CDN which relying on expensive servers and bandwidth.  Pear FogVDN with massive nodes and sharing economy, the price is lower than traditional CDN.
## <img src="fig/icon/地域统计.png" width="28"> Network Awareness, Content Prefetching, Personalization

   1. accurate service

      * Get user's real IP address (although use OpenDNS or VPN), and mapping the area, ISP with a probability of 99.9%, choose the "zero hop" node for service.

   2.  Efficient content distribution and distribution network

      * Accurate, real- time get the high frequency data, push the content to the edge node quickly.

   3. Big data based recommendation, prediction and  prefetching

      * Provide API and other service, for the CP which have user personas and content feature,content prefetching  can be accurate to one user and the "Small-world"(A social networks concept).
## <img src="fig/icon/合作.png" width="28"> Business

CP access, CDN access or player, JS, SDK customized, ISP data usage optimize,  Hardware Vendor software integrate. Please send E-mail to <service@pear.hk>
