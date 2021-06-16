# 42netpractice

### level10
- level9 と同じ

### level9
- Internet の Routes は，Internet と繋がっている Interface に繋がるネットワークの Network Address を記入する
- switch で繋がってる Interface は同じ network にする
- プライベート IP アドレスは Internet に繋ぐのあれば使えない

### level8
- Internet の Routes は，Internet と繋がっている Interface に繋がるネットワークの Network Address を記入する
- プライベート IP アドレスは Internet に繋ぐのあれば使えない
  - 10.0.0.0 ~ 10.255.255.255 (10.0.0.0/8) (Class A)
  - 172.16.0.0 ~ 172.31.255.255 (172.16.0.0/12) (Class B)
  - 192.168.0.0 ~ 192.168.255.255 (192.168.0.0/16) (Class C)

### level7
- (A) Interface A1 と Interface R11 は同じサブネットマスクにする
  - client A の設定は，Interface A1 -> Interface R11 への設定をする
- (B) Interface R12 と Interface R21 は同じサブネットマスクにする
  - roter R1 の設定では，Interface R12 -> Interface R21 への設定をする
  - roter R2 の設定では，Interface R21 -> Interface R12 への設定をする
- (C) Interface R22 と Interface C1 は同じサブネットマスクにする
  - client C の設定では，Interface C1 -> Interface R22 への設定をする
- (A), (B), (C) はそれぞれ別のサブネットマスクにする
  - なぜならば，ルータは別のネットワークを繋ぐものだから，同じネットワークにある IP Address は突っぱねる

### level6
- I の宛先の下1桁は 1 なのに気をつける
  - つまり `internet: Internet Routs: 163.172.250.1/32 -> xxx.xxx.xxx.xxx` にするということ
- ルーティングテーブルの宛先ルート (Routes) には，相手先の `Interface の IP Address` を入力する
- [ルーティングテーブルの見方](https://qiita.com/cafedrip/items/8f0cc9544910cba23be8#ルーティングテーブルの見方)
- switch でつながっている部分のサブネットマスクは同じで構わない

### level5
- Routes には，`default` -> `通信先の Interface の IP Address` を入れる

### level4
- Interface R2 で 110.102.43.1 ~ 110.102.43.126 がホストとして使われる
- Interface R3 で 110.102.43.193 ~ 110.102.43.254 がホストとして使われる
- ので残りの 110.102.43.129 ~ 110.102.43.190 までが Interfase R1 のホストとして使える

### References
#### Gateway
- ゲートウェイとは，「ネクストホップ」と同じ情報，つまり，ネットワークに到達するためのゲートウェイを示す．
  - ゲートウェイとは，OSI 参照モデルのトランスポート層からアプリケーション層までの階層で，データを変換して中継する装置のこと．
- インターフェイスは，ローカルで利用可能なインターフェイスのうち，ゲートウェイへの到達を担当するもの．
