# 42netpractice

### level6
- I の宛先の下1桁は 1 なのに気をつける
- ルーティングテーブルの宛先ルート (Routes) には，相手先のアドレスとサブネットマスクを直接入力する
- [ルーティングテーブルの見方](https://qiita.com/cafedrip/items/8f0cc9544910cba23be8#ルーティングテーブルの見方)

### level5
- Routes には，自分の Interface の IP Address を入れてあげる

### level4
- Interface R2 で 110.102.43.1 ~ 110.102.43.126 がホストとして使われる
- Interface R3 で 110.102.43.193 ~ 110.102.43.254 がホストとして使われる
- ので残りの 110.102.43.129 ~ 110.102.43.190 までが Interfase R1 のホストとして使える
