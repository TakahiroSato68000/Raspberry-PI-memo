# Raspberry Piの選定情報

## おすすめ

PoC（実装検証）では、用途に応じて次のいずれかが候補になります。価格は販売店や時期で変動するため、購入時に確認してください。

- Linux OSを使う場合（microSDカードが別途必要）
  - Raspberry Pi 3 Model B+：比較的安価で、基本的な検証に向く：約5,000円〜6,500円
  - Raspberry Pi Zero 2 W：小型・省電力。性能や拡張性には制約がある：約3,000円〜3,500円
- OSを使わない場合
  - Raspberry Pi Pico / Raspberry Pi Pico 2：マイコンボード。センサー制御などに向く：約940円〜1,100円

Raspberry Pi 4および5は高性能ですが、価格や周辺機器を含めた費用が高くなりやすいです。
Raspberry Pi 4以降だと、値段が跳ね上がります。
- Raspberry Pi 4 Model B：約20,700円〜
- Raspberry Pi 5： 約22,000円〜  


Raspberry Pi 2以前は、ほぼ在庫がないです。  
(ただ、私は持っているので、どうしても必要な場合は声をかけてください。)

## 購入先

主に利用したことのある販売店です。Amazonなどでは、販売者によって価格が大きく異なる場合があるため、正規販売店も確認することをおすすめします。

- 以下は使った実績があります
    - マルツ
    https://www.marutsu.co.jp/GoodsListNavi.jsp?path=1100020007
    - スイッチサイエンス
    https://www.switch-science.com/pages/raspberry-pi

- 公式なら定価で購入できます。
    - Raspberry Pi公式  
        https://www.raspberrypi.com/products/

    - 公式リセール
        - スイッチサイエンス  
        https://www.switch-science.com/pages/raspberry-pi
        - DigiKey（デジキー）  
        https://www.digikey.jp/
        - KSY
        https://raspberry-pi.ksyic.com/




# Raspberry Piの選定情報

Raspberry Piには、Linuxを動かすシングルボードコンピューターと、OSを使わないマイコンボード（Picoシリーズ）があります。  
モデルによって性能、消費電力、必要な電源、価格が異なるため、要件に合わせて選定します。  
なお、Raspberry Pi 5は公式に5V/5A（27W）のUSB-C電源が推奨されていたりと、一般的なCPUボードと比較して、ミニPCに近いものになっています。  
電源容量が不足すると、安定して動作しない場合があります。

## Raspberry Piシリーズ

Raspberry Pi は現在は5まで発売されています。

主要モデルの数値比較です。メモリ容量はモデルによって異なります。

| モデル | CPU | メモリ | 無線通信 | 電源の目安 | 位置づけ |
|---|---|---:|---|---|---|
| Raspberry Pi 3 Model B+ | 4コア Cortex-A53 / 1.4GHz | 1GB | 2.4/5GHz Wi-Fi、Bluetooth 4.2 | 5V/2.5A | 基本的なPoC向け |
| Raspberry Pi 4 Model B | 4コア Cortex-A72 / 1.5GHz | 1/2/4/8GB | 2.4/5GHz Wi-Fi、Bluetooth 5.0 | 5V/3A | 性能と価格のバランス型 |
| Raspberry Pi 5 | 4コア Cortex-A76 / 2.4GHz | 1/2/4/8/16GB | 2.4/5GHz Wi-Fi、Bluetooth 5.0 | 5V/5A（27W）推奨 | 高性能。冷却も必要 |


現時点のPoC（実装検証）で使用するのであればRaspberry Pi 3 がおすすめだと思います。


### 産業用Raspberry Pi

Raspberry Piは基板が露出しているため、工場などの厳しい環境で使用する場合は、防塵・防水、温度、固定方法などの検討が必要です。PoCで実証した後、必要に応じて産業用ケースや産業用製品を検討します。
### PiLink
https://pilink.jp/product-category/pleco/

### 防水型産業用ラズパイ MICA-Rシリーズ
https://www.takagi-c.com/products/industrial-RaspberryPi.html


## Raspberry Pi Zero

Raspberry Pi Zeroは、通常のRaspberry Piより小型・軽量になるよう構成されたモデルです。Raspberry Pi Zero Wは、無線LANとBluetoothを搭載しています。Zero 2 Wなど、世代によって性能や機能が異なります。

## Raspberry Pi Pico

Raspberry Pi Picoは、Raspberry Pi ZeroのようにOSを起動するコンピューターではなく、プログラムを直接実行するマイコンボードです。Arduinoに近い用途で、センサーやモーターなどの制御に向いています。

そのため、Linuxやファイルシステムが必要な処理にはRaspberry Pi Zeroなどを、単純な制御や低消費電力を重視する処理にはPicoを選びます。用途によってはArduinoも十分な選択肢です。
