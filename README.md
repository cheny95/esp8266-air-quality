# esp8266-air-quality
ESP8266空气质量检测DIY-esphome代码参考

#### ESPHOME烧录文件是： 8266-tvoc.yaml

#### 引脚图是
![20200615211225201](https://user-images.githubusercontent.com/6293952/179972145-a94c0d0e-2584-407a-8a90-a4821bc2c445.png)

#### 其他的是对应元器件的文档


### 接线：

### MH-Z19B：
![image](https://user-images.githubusercontent.com/6293952/179967532-aa8dfbcb-cce2-477e-9aea-d71077fe65bf.png)


1. 把MH-Z19B的VIN和PMS7003 pin1的线接在一起。然后接8266的VU口，两个设备的GND口的线接在一起，然后接在esp8266的任意GND
2. 将MH-Z19B的tx接板子rx（D7），rx接板子tx（D8）

### PMS7003

![image](https://user-images.githubusercontent.com/6293952/179967621-f4b25598-914c-4a85-8784-49a7a8253c03.png)

3. PMS7003的TX（pin9）接到板子另外一个rx（D9）的口子上，最后再将pin10的reset口接到D3口，用于PMS7003的休眠


### SHTC3

![image](https://user-images.githubusercontent.com/6293952/179967382-09f52d03-6d7e-4918-8bcc-ae127fb4d501.png)

4. 引脚说明

- 1 --- VDD    供电 3.3～5.5V DC

- 2 --- GND    接地，电源负极

- 3 --- SDA    串行数据，双向口

- 4 --- SCL    串行时钟，输入口

5. 其中3、4接口分别接D2、D1。1、2分别接3.3V的电源口和GND
