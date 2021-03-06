# esp12f_plant_tem_and_hum

N1植物温湿度传感器二次开发固件，基于ESPHOME，接入HA作为温湿度采集节点

# APP源代码
[配套APP源码](https://github.com/zouguo-eng/IOTHumTemp)

# 引脚说明
![引脚图](https://github.com/zouguo-eng/esp12f_plant_tem_and_hum/blob/master/Snipaste_2020-08-19_15-12-10.png)

USB的ID线对应GPIO0
USB的d+线对应tx
USB的d-线对应rx
GPIO12为板载LED
GPIO4位DHT传感器

# 源码说明
```
ssid: "xxxx"	替换为自己的无线名称
```
```
password: "xxxx"	替换为自己的无线密码
```
```
api:
	password: "xxxx"	任意设置一个密钥
```
```
ota:
	password: "xxxx"	任意设置一个密钥，OTA升级时用
```
```
mqtt设置服务器IP、用户名、密码
```
```
on_message部分用于在设备深度睡眠时唤醒，OTA升级时用
```
# 烧写固件
下载工具[esphome-flasher](https://github.com/esphome/esphome-flasher)

# 烧写说明
### 1.接线
![USB-TTL实际接线图](https://github.com/zouguo-eng/esp12f_plant_tem_and_hum/blob/master/Snipaste_2020-08-19_23-49-00.png)

![USB母座针脚图](https://github.com/zouguo-eng/esp12f_plant_tem_and_hum/blob/master/Snipaste_2020-08-19_23-50-34.png)

### 2.烧写

![烧写图](https://github.com/zouguo-eng/esp12f_plant_tem_and_hum/blob/master/Snipaste_2020-08-19_15-26-08.png)

Serial port选择COM口
Browse选择固件
Flash ESP开始刷写固件

