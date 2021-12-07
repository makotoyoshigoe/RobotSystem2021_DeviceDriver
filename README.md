# RobotSystem2021_DeviceDriver
- RaspberryPi4を使用して, 入力した計算式の計算結果を, LEDを制御し, 2進数で表示するデバイスドライバを作成した. 4096未満の有理数を表示でき, 整数部分は3Byte, 少数部分は1Byteで表示する. 
---
## 動作環境
- Ubuntu 20.04.3 LTS
- Raspberry Pi 4
---
## 使用するもの
- RaspberryPi4
- USBケーブル TypeC
- ブレッドボード
- LED, 抵抗(200Ω), ジャンパ線(オス-メス): 各17個
---
## 配線図
- 配線は以下の実際の写真と各LEDとGPIOピンの対応表を参照してください. 
### 実際に配線した写真
![figure](https://user-images.githubusercontent.com/91446273/145028123-3f1e35ad-0464-444b-ad85-98b0b1590e61.png)
- 黄, オレンジ, 赤が整数部分を表す. 順番に1, 2, 3Byte目を表す. 
- 緑は整数と少数の区切りのピリオドを表す. 
- 青は少数部分を表す. 
### 各LEDとGPIOピンの対応表
- RaspberryPi4のピン配置は[こちら](https://www.raspberrypi.com/documentation/computers/os.html#gpio-and-the-40-pin-header)を参考にしてください. 

| LED | GPIO番号 |
| :-------|:------|
| LED0 | 21 |
| LED1 | 20 |
| LED2 | 26 |
| LED3 | 16 |
| LED4 | 19 |
| LED5 | 13 |
| LED6 | 12 |
| LED7 | 6 |
| LED8 | 5 |
| LED9 | 25 |
| LED10 | 24 |
| LED11 | 23 |
| LED12 | 22 |
| LED13 | 27 |
| LED14 | 18 |
| LED15 | 17 |
| LED16 | 4 |
---
## 実行方法
### セットアップ
```sh
git clone https://github.com/makotoyoshigoe/RobotSystem2021_DeviceDriver.git
cd RobotSystem2021_DeviceDriver
./setup.bash
```
### pythonスクリプトを実行
```sh
python3 calc.py
#input formula:
```
### 計算式を入力
```

