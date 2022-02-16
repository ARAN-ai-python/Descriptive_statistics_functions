# describe_functions

## 概要
統計学の勉強も兼ねて、データを入力として記述統計情報を**一から計算して**出力するdescribe関数を作っています。  
なので、なるべく便利なライブラリを用いず、計算過程が分かりやすい様にプログラムを書いています。  
まだ正確に計算できていない箇所や追加できていない要素もありますので、これから随時改良していく予定です。


## 背景
データ分析を行う際、記述統計を求める作業が必ずと行って良い程あります。そのような時にはpandasライブラリのdescribeメソッドを用いるのですが、たった一行のプログラムで平均や標準偏差といった代表的な統計量を求められるという事に感動しました。  
ある時、ふとpandasのdescribeメソッドを見て「そういえば第一四分位数と第三四分位数はあるのに四分位範囲は出力されないのか」と気付きました。そこで私は四分位範囲も出力してくれる機能を追加したいと思い、実際にSeries型データを引数とした一行データdescribe関数を作ってみました。自分がプログラミングしたコードでpandasのdescribe要素+四分位範囲が出力されるという事象が想像以上に面白く、もっと統計量を出力する関数を作りたいと思いました。その好奇心が高じて、二行・三行バージョンのdescribe関数も作成に至りました。


## 機能
### 一行describe関数
- サンプルサイズ(count)
- 合計値(sum)
- 算術平均(mean)
- 幾何平均(g_mean)
- 調和平均(h_mean)
- 平均偏差(meang)
- 母分散(var.p)
- 不偏分散(var.s)
- 母標準偏差(std.p)
- 不偏標準偏差(std.s)
- 標準誤差(std_e)
- 区間推定（母分散既知）(mean_95cl_known)
- 最小値(min)
- 第一四分位数(25%)
- 中央値(50%)
- 第三四分位数(75%)
- 最大値(max)
- 四分位偏差(25-75%)
- ミッドレンジ(mid-range)
- レンジ(range)
- 最頻値(mode)
- ジニ係数(gini)
- 歪度(skewness)
- 尖度(kurtosis)
- ジャック-ベラ検定(検定統計量x2)(Jarque-Bara_test.x2)

#### グラフ(一標本)
- 線グラフ
- 散布図
- ヒストグラム
- ヒストグラム(累積)
- 箱ひげ図
- バイオリンプロット
- イベントプロット


### 二行describe関数
#### それぞれ求めるもの
- サンプルサイズ(count)
- 合計値(sum)
- 算術平均(mean)
- 幾何平均(g_mean)
- 調和平均(h_mean)
- 平均偏差(meang)
- 母分散(var.p)
- 不偏分散(var.s)
- 母標準偏差(std.p)
- 不偏標準偏差(std.s)
- 標準誤差(std_e)
- 区間推定（母分散既知）(mean_95cl_known)
- 最小値(min)
- 第一四分位数(25%)
- 中央値(50%)
- 第三四分位数(75%)
- 最大値(max)
- 四分位偏差(25-75%)
- ミッドレンジ(mid-range)
- レンジ(range)
- 最頻値(mode)
- ジニ係数(gini)
- 歪度(skewness)
- 尖度(kurtosis)
- ジャック-ベラ検定(検定統計量x2)(Jarque-Bara_test.x2)

#### 2つのデータから求めるもの
- 母共分散(cov.p)
- 不偏共分散(cov.s)
- ピアソン相関係数&ピアソン無相関検定(検定統計量t)(Pearson_cor.t)
- スピアマン相関係数&スピアマン無相関検定(検定統計量t)(Spearman_cor.t)
- ケンドール相関係数&ケンドール無相関検定(検定統計量z)(Kendall_cor.z)
- 単回帰分析(回帰係数&切片&決定係数)(simple_regression)
- 単回帰係数の無相関検定(検定統計量t)(simple_regression_test.t)
- F検定(検定統計量F)(F_test.F)
- 対応なし2標本z検定(検定統計量z)(ind_ztest.z)
- 対応なし2標本t検定(検定統計量t)(ind_ttest.t)
- 効果量(対応なしt検定ver)(ind_cohen_d)
- 対応あり2標本z検定(検定統計量z)(dep_ztest.z)
- 対応あり2標本t検定(検定統計量t)(dep_ttest.t)
- 効果量(対応ありt検定ver)(dep_cohen_d)
- ウェルチのt検定(検定統計量t)(Welch.ttest.t)
- マン=ホイットニーのU検定(検定統計量U)(Mann-whitney_utest.U)
- ウィルコクソンの順位和検定(検定統計量Tw)(Wilcoxon_rstest.Tw)
- 符号検定(検定統計量r)(sign_test.r)
- ウィルコクソンの符号順位検定(検定統計量Tw)(Wilcoxon_srtest.Tw)

#### グラフ(一標本)
- ヒストグラム
- 箱ひげ図
- バイオリンプロット
- イベントプロット

#### グラフ(二標本)
- 線グラフ
- 散布図
- ステムプロット
- ステッププロット
- hist2d


### 三行describe関数
#### それぞれ求めるもの
- サンプルサイズ(count)
- 合計値(sum)
- 算術平均(mean)
- 幾何平均(g_mean)
- 調和平均(h_mean)
- 平均偏差(meang)
- 母分散(var.p)
- 不偏分散(var.s)
- 母標準偏差(std.p)
- 不偏標準偏差(std.s)
- 標準誤差(std_e)
- 区間推定（母分散既知）(mean_95cl_known)
- 最小値(min)
- 第一四分位数(25%)
- 中央値(50%)
- 第三四分位数(75%)
- 最大値(max)
- 四分位偏差(25-75%)
- ミッドレンジ(mid-range)
- レンジ(range)
- 最頻値(mode)
- ジニ係数(gini)
- 歪度(skewness)
- 尖度(kurtosis)
- ジャック-ベラ検定(検定統計量x2)(Jarque-Bara_test.x2)

#### 2つのデータから求めるもの
- 母共分散(cov.p)
- 不偏共分散(cov.s)
- ピアソン相関係数(Pearson_cor)
- ピアソン無相関検定(検定統計量t)(Pearson_cor_test.t)
- スピアマン相関係数(Spearman_cor)
- スピアマン無相関検定(検定統計量t)(Spearman_cor_test.t)
- ケンドール相関係数(Kendall_cor)
- ケンドール無相関検定(検定統計量z)(Kendall_cor_test.z)

#### 3つのデータから求めるもの
- 偏相関係数(partial_cor)
- 偏相関係数の無相関検定(検定統計量t)(partial_cor_test.t)
- バートレット検定(検定統計量x2)(Bartlett_test.x2)
- ルビーン検定(検定統計量F)(Levene_test.F)
- ブラウンフォーサイス検定(検定統計量F)(Brown-Forsythe_test.F)
- 一元配置分散分析(検定統計量F)(ANOVA.F)
- 一元配置反復測定分散分析(検定統計量F)(RM_ANOVA.F)
- クラスカル=ウォリス検定(検定統計量H)(Kruskal-Wallis_test.H)
- フリードマン検定(検定統計量Q)(Friedman_test.Q)
- テューキー・クレーマー検定(検定統計量q)(Tukey-kramer_test.q)
- スティール・ドゥワス検定(検定統計量t)(Steel-dwass_test.t)

#### グラフ(一標本)
- ヒストグラム
- 箱ひげ図
- バイオリンプロット
- イベントプロット

Coming soon...


## 今後の展望
- 検定統計量の出力とセットで自由度も出力するように改善したい。
- 現在出力している統計量の他に何か計算できる統計量を調査し、それを新たに出力するプログラムを追加したい。
- 上記の出力内容の説明にて、その統計量の意味を正確にまとめていきたい。
- 三行describe関数を四行以上の引数にて正常に動作するプログラムに改善したい。(もしくは別の関数として定義するのもアリ)


## 参考文献
- 統計学入門　東京大学教養学部統計学教室　東京大学出版会(1991)
- 統計学図鑑　栗原伸一ほか　オーム社(2017)
- 44の例題で学ぶ 統計的検定と推定の解き方　上田拓治　オーム社(2009)
- ノンパラメトリック統計　前園宜彦　共立出版(2019)

![Unknown](https://user-images.githubusercontent.com/67265109/145838872-156f49a7-75ee-486e-8bf3-565803fe22ec.jpeg)
![Unknown](https://user-images.githubusercontent.com/67265109/145839013-6cbf6a0b-33de-40d7-ac06-719985cd3be9.jpeg)
![Unknown](https://user-images.githubusercontent.com/67265109/145839027-9d735397-942c-44dd-8b5d-f7fdb5dd33e9.jpeg)
![Unknown](https://user-images.githubusercontent.com/67265109/153242943-0805af3a-335a-4fd9-85c8-a79270a0aa26.png)