# ATMで「お金を引き出す」ユースケース記述
## ユースケース図
ATMで「お金を引き出す」
## 概略
銀行のATMを利用して、自分の口座からキャッシュカードで必要なお金を引き出します
## アクター
利用者
## 事前条件
アクターが口座とキャッシュカードを持っていること
## 事後条件
アクターの口座から指定された金額が引き出されること
## イベントフロー
### 基本フロー
・利用者がATMでお金を引き出すと、このユースケースは開始する
・利用者はキャッシュカードをATMに挿入する
・利用者は次の情報を入力する > 利用者の口座の暗証番号 (E-1)
・利用者は次の情報を入力する > 引き出すお金
・利用者は再度、次の情報を入力するを入力する > 利用者の口座の暗証番号 (E-2)
・設定したお金が引き出される
・ATMは明細表を発行する
・利用者がお金の引き出しを終了すると、このユースケースは終了する
### 代替フロー
E-1:口座の暗証番号が一致しない
    1.再度、暗証番号を入力する
    2.暗証番号が一致した場合、E-1以降の処理に進む
    3.一致しなかった場合、ATMは処理を中止する
E-2:口座の暗証番号が一致しない
    1.再度、暗証番号を入力する
    2.暗証番号が一致した場合、E-1以降の処理に進む
    3.一致しなかった場合、ATMは処理を中止する
### 例外フロー

### 基本シナリオ
 1.シナリオ1:引き出しに成功する場合
 2.利用者は現金引き出しを選択する
 3.利用者はキャッシュカードをATMに挿入する
 4.利用者は暗証番号〇〇〇〇を入力する
 5.利用者は引き出す現金を入力する
 　現金2万5千
 6.再度、利用者は暗証番号〇〇〇〇を入植する
 7.ATMは現金引き出しを実行する
 8.ATMは明細表を発行する
 9.利用者は、引き出された現金と明細表を受け取る
 10.ATMは終了を実行する
### 例外シナリオ
