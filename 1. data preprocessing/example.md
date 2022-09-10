### **値データの処理と把握 / data preprocessing and comprehension**
---

　一般に、欠損値・異常値・誤データ等のエラー値を修正、または削除することをデータ処理と呼んでいますが、今回はデータカテゴリー（株、FX、仮想通貨、金利）によってエラー値の定義が異なることに注意が必要です。例えば、株価は0より小さくなりませんが、金利はマイナスの値を取ることができます。FXの小数桁数は3〜5桁が一般的ですが、仮想通貨は更に細かい小数桁数を取ることがあります。

　基本となるデータ処理プロセスの内容、及びカテゴリー毎のデータ処理条件は、以下のように設定します。

基本となるデータ処理プロセス
 - 日時チェック　・・・ datetimeデータを抽出
 - null（1回目）・・・ 値カラムが全てnanのrowを削除
 - マイナス値   ・・・  値カラムにマイナスが含まれるrowを削除
 - ゼロ        ・・・  値カラムに０が含まれるrowを削除
 - 小数桁数     ・・・  値カラムの小数桁数を条件毎にround
 - 値
  - 高値       ・・・  高値カラムに高値以外の値があるrowを削除
  - 安値       ・・・  安値カラムに安値以外の値があるrowを削除
  - 終値-始値   ・・・  終値 - 始値が閾値を超えるrow数をカウント
 - null（2回目）・・・  残るnullを検証し、修正or削除


データ処理条件のマトリックス

 |             |               product categories                 |
 |  check list |:-------------------------------------------------|
 |:------------|   Stocks   |   Forex   |   Cryptos   |   Rates   |
 |    date     |
 | null(first) |
 |  negative   |
 |     zero    |
 |   decimal   |
 |    value    |

 　<!-- なお、code詳細についてはリポジトリの[preprocess1](www.example.com)を参照してください。 -->

&emsp;

　Generally speaking, we call data preprocessing

&emsp;

<!-- ### **文字データの処理と把握 / data preprocessing and comprehension**
---
twitter文字列やセンチメントを扱うようになると、文字データの処理も必要になる -->

### **データ尺度の変更 / change the data scale**
---

　データの尺度変更も広義のデータ処理に含まれるかと思うので、

- Min-Max scaling
 - []
- 標準化
 - []
- 正規化
 - []
- ビニング
 - []
- xx
 - []

 　<!-- こちらも、code詳細についてはリポジトリの[preprocess2](www.example.com)を参照してください。 -->

&emsp;

- Min-Max scaling
  - []
- Standardization
  - []
- Normalization
  - []
- Binning
  - []
- xx
  - []

&emsp;
