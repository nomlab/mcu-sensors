# door_sensor
106 号室のドアに関するデータを取得し，MQTT を利用してopenHAB にデータを送信するプログラム．
106 号室のドアに設置してある．
<img src="https://github.com/nomlab/mcu-sensors/blob/main/door_sensor/mcu_door_sensor.JPG" alt="door_sensor" width="640px">
## 取得するデータと変数名
| 取得するドアの情報 | 変数名 | データの内容 |
| ---- | ---- | ---- |
| ドアの開閉状態 | door_open | "open" or "close" |
| ドアの施錠状態 | door_lock | "locked" or "unlocked" |
## 使用センサとピン割り当て
| センサ | ピン番号 | 説明 |
| ---- | :----: | ---- |
| マグネットスイッチ | 23 | ドアの開閉状態を取得する |
| マグネットスイッチ | 33 | ドアの施錠状態を取得する |
## 送信データの形式
データは以下の json 形式で送信される．
```json
{"door_open" : "<door_open>", "door_lock": "<door_lock>"}
```
