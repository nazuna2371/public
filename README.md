AI / 機械学習 画像認識 人物判定 ver 1.0（今回作成した分についてはソースコードと実行結果のみです。）<br>
このreadmeはソースコード内上部と内容は一緒です。<br><br>

【見方】<br>
※スマホから開いた場合は↑のView codeを押す必要があります。<br>
person_judgment_ver1.0.ipynbを開くとソースコードや実行結果が表示されます。<br>
requirements_20210724.txtは入れていたパッケージの一覧、バージョンです。（最低限ではないかもしれません。）<br>
判定結果はin4, 5の出力の箇所です。<br>
今回は全画像使用パターンのみ出力しています。<br><br>

【概要】<br>
趣旨: 機械学習を用い、画像内の人物判定を行う。<br>
元の画像枚数が7枚しかないので、NumPy Data Augmentationで画像データを水増ししています。<br><br>

教師あり学習: k近傍法(k-NN)、サポートベクタマシン、ランダムフォレスト、グリッドサーチでそれぞれ試してみました。<br>
教師なし学習: ついでにKMeansによるクラスタリングもやってみました。<br><br>

今回行ったものの中ではランダムフォレスト, グリッドサーチバージョンが一番正解率が高めでした。<br>
（元画像素材7枚 → 水増しからの機械学習予測正解率99%越え。増やしまくった甲斐があったんでしょうね。。。）<br><br>

【詳細】<br>
in1, 2で画像や.csv（教師データ）の処理、<br>
in3で学習させるためのデータ（画像から作ったヒストグラムを特徴量に使用）の処理、<br>
in4で学習 → 予測させ判定、in5は正解率の一覧です。
それ以降は他のアルゴリズムで作ったソースです。<br><br>

交差検証の回数を増やすとPCが悲鳴をあげていました笑<br>
回帰や次元削減、グラフ描画、他アルゴリズム等、ちょうどいいテーマが見つかり次第、また新しく作ります。<br><br>

作成日: 2021/7/25, 作成者: Y.T（nazuna2371）<br>
画像引用元（所属会社）ホームページ: https://toyo-integration.co.jp/