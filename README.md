# 探索アルゴリズム実証モデル
## このプログラムの実証するもの
### 1.線形探索アルゴリズムと2分探索アルゴリズムの動作速度の違い
### 2.配列とArrayListクラスの動作速度の違い
### 3.absractとinterfaceを用いて強化学習により多態性を実現した場合の動作速度の違い
## 学習方法
### 1.TestSearchを実行して各ケースごとの実行時間を確認します
### 2.TestSearchのサーチオブジェクトのインスタンスを他の5つの実装クラスと変えてみて動作速度を確認します
※ソースコードを解析して各クラスの関係性を理解したうえでプログラムを変えることができるのはプログラマとしても重要なスキルになります。
### 3.6つ目の実装クラスとしてListインターフェースを持つLearningSearchListを実装します
### 4.サンプル以外にもさらに動作速度が削減できるアルゴリズムを見つけ出して実装します
## 構成
### 1.線形探索と2分探索
線形探索と2分探索は結果を求めるのにかかる所要時間が探索元のデータ集合の並びと探索対象のデータに依存します。このため、どちらのアルゴリズムを選択すればよいかはプログラム時に決められません。また、2分探索にはソートされていることが前提という制約があります。仮に探索するたびにソートする処理を組み込むのであればその分のオーバーヘッド(本来の処理にかかる負荷とは別に関連的に発生する負荷)も考慮する必要があります。
### 2.配列とArrayListクラス
ArrayListとは配列に様々な機能を付加したクラスです。例えば配列には通常、新たにデータを加えることも削除することもできず、これを行いたければ新たに配列を再定義してデータを移すプログラムをコーディングする必要があります。しかしArrayListクラスには既にそれらの機能が実装されているため、わざわざコーディングする必要がありません。その一方で反復処理などではArrayListクラスは配列よりも動作が遅くなってしまいます。これはプログラムを高度にオブジェクト化した結果として余分な動作が増える傾向にあるためです。このため、高速な処理を求められるプログラムでは便利なArrayListよりも配列が用いられます。
