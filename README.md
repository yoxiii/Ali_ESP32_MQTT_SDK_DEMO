# Ali_ESP32_MQTT_SDK_DEMO
阿里云物联网平台esp32官方移植sdk例程
<br><br>
## 移植

1. **先根据阿里云移植文档完成开发环境移植**
  [乐鑫ESP32开发板移植说明](https://help.aliyun.com/zh/iot/developer-reference/port-the-sdk-to-an-esp32-development-board?spm=a2c4g.11174283.0.i2)<br>
2. 进入menuconfig,修改`WiFi SSID`， `WiFi Password`和`Maximum retry`<br>
3. 修改设备三元组`product_key`,`device_name`和`device_secret`<br>
<br>

## 串口输出
```
I (1011) wifi:AP's beacon interval = 102400 us, DTIM period = 1
W (1031) wifi:<ba-add>idx:1 (ifx:0, d4:35:38:91:ae:12), tid:6, ssn:1, winSize:64
I (2581) esp_netif_handlers: sta ip: 192.168.31.216, mask: 255.255.255.0, gw: 192.168.31.1
I (2581) wifi station: got ip:192.168.31.216
I (2581) wifi station: connected to ap SSID:xxx password:12345678
I (2591) wifi station: Start linkkit mqtt
[2.040][LK-0313] MQTT user calls aiot_mqtt_connect api, connect
[2.050][LK-032A] mqtt host: ProductKey.iot-as-mqtt.cn-shanghai.aliyuncs.com
[2.060][LK-0317] user name: a002&k0r7zrmL7su
unknown option
establish mbedtls connection with server(host='ProductKey.iot-as-mqtt.cn-shanghai.aliyuncs.com', port=[443])
[2.920][LK-0313] MQTT connect success in 880 ms
AIOT_MQTTEVT_CONNECT
[2.920][LK-0309] sub: /ProductKey/a002/user/get
[2.930][LK-0309] pub: /ProductKey/a002/user/get

[LK-030A] > 7B 22 69 64 22 3A 22 31  22 2C 22 76 65 72 73 69 | {"id":"1","versi
[LK-030A] > 6F 6E 22 3A 22 31 2E 30  22 2C 22 70 61 72 61 6D | on":"1.0","param
[LK-030A] > 73 22 3A 7B 22 4C 69 67  68 74 53 77 69 74 63 68 | s":{"LightSwitch
[LK-030A] > 22 3A 30 7D 7D                                   | ":0}}

suback, res: -0x0000, packet id: 1, max qos: 1
heartbeat response
```
