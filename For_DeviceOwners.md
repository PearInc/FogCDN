# For Device Oners

 边缘设备的机主或管理员，可以通过在设备上安装Pear Fog Suite来加入“梨享雾计算”计划。

## Owner Web管理平台(NMS)

### 用户注册 [signup](https://nms.webrtc.win/site/signup)
![用户注册](fig/owner/nms_signup.png)

### 用户登陆 [login](https://nms.webrtc.win/site/login)
![用户登陆](fig/owner/nms_login.png)

### 设备绑定
#### 手动绑定设备
- 通过NMS手动输入设备MAC地址及序列号SN
![手动绑定](fig/owner/hand_bind.png)

#### 微信绑定设备
- 通过微信扫描设备上的二维码进行绑定
![微信绑定](fig/wechat_bind.png)

### 绑定设备列表
![设备列表](fig/owner/node_state.png)

### 设备详细信息
![设备详细信息](fig/owner/single_node_state.png)

### 查看流量
### 暂时提供一个统一的账号，所有节点的流量全部统计到这个统一的账号，查询流量API如下(账号: newifi2 密码: 123456)
#### 查看所有设备下的流量列表
![查看所有设备下的流量列表](fig/owner/traffic_list.png)

#### 登录，获取token
```  shell
curl  -X POST https://api.webrtc.win:7201/v1/vdn/owner/login \
      -H "Content-Type:application/json" \
      -d '{
              "user_name": "newifi2",
              "password":  "123456"
          }'

```
#### 获取一定时间段内的流量（包括多个Mac）
``` shell
curl -v -X GET "https://api.webrtc.win:7201/v1/vdn/owner/51/traffic?start_date=1494780990&end_date=1495890990" \
    -H "X-Pear-Token: ${token}" \
    -H "Content-Type:application/json" 
```

**响应**
``` json
[
    {
        "mac_addr": "MAC地址 string",
        "values": [
          {
                "traffic": "流量 int",
                "time":    "时间戳 int"
          }
      ]
    }
]
```

#### 完整的Shell脚本如下（可以直接运行）
``` shell
#/bin/sh
# Pear Limited
r=`curl -X POST https://api.webrtc.win:7201/v1/vdn/owner/login \
         -H "Content-Type:application/json" \
         -d '{
                 "user_name": "newifi2",
                 "password":  "123456"
            }'`
user_id=`echo $r | cut -d ":" -f2 | cut -d "," -f1`
user_id="${user_id// /}"
echo $user_id;
token=`echo $r | cut -d "\"" -f14 `
#echo ${token}
curl -v -X GET "https://api.webrtc.win:7201/v1/vdn/owner/${user_id}/traffic?start_date=1494780990&end_date=1496443900" \ 
      -H "X-Pear-Token: ${token}" \
      -H "Content-Type:application/json" 
```
### 流量分布显示图
#### 查看某个设备下的流量
![查看某个设备下的流量](fig/owner/traffic.png)

### 流量兑换，查看每台设备的流量，统计3个月的流量，及时提现成Pear Coin。
#### 查看某个设备下的总流量
![查看某个设备下的总流量](fig/owner/total_traffic.png)

> 继续补充通过weixin等平台兑换Pear Coin

## 附：Pear推荐的合作厂商设备列表
- Newifi2/3
- QNAP TS-x51 Series