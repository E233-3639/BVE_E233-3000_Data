# BVE5.8,6向け E233系3000番台 車両データ ver1.05 説明書

**このデータをダウンロードした場合、「著作権について」に同意したことになります。**

## 再現車両について
E233系3000番台(15両)を再現したBVE Train Simulator 車両データです。<br>
E233系3000番台はJR東日本が所有する一般型車両で、東海道線、宇都宮線(東北本線)、高崎線などで使用されている車両です。

## 再現部分
運転台、計器モニター、TIMSモニター、モニター類の表示のラグ、予備ワイパー(未動作)、モーター音、走行音、ブレーキ音など。<br>
※本物をもとに再現しておりますが、全てを再現しきれていなかったり本物と違う箇所がある場合があります。ご了承ください。

## 著作権について
この車両データはOriginalDataとExternalDataの構成に分かれています。

### OriginalData
OriginalDataは[当方](https://github.com/E233-3639)が制作したものです。<br>
**著作権は[当方](https://github.com/E233-3639)にあり、クリエイティブコモンズ ライセンスを適用します。**<br>
<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />OriginalData は <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">クリエイティブ・コモンズ 表示 - 非営利 - 改変禁止 4.0 国際 ライセンス</a>の下に提供されています。意味は以下の通りです。<br>
* 作品のクレジットを必ず表示を義務付けます。
* 営利目的での利用を禁止します。
* 元の作品を改変することを禁止します。

### ExternalData
ExternalDataは他作者からお借りしているデータがございます。お借りしているデータは以下の通りです。<br>
ATS.wav、ATS_Cnt.wav、EB.wav、HornA.wav、HornB.wav、HornC.wav、HornD.wavは[BVE Trainsim 内房線 for BVE5.8 & BVE6.0 正式版](http://bvets.net/uchibo/)に含まれるデータをお借りし、一部編集して使用しております。<br>
ats_p_bell.wavはUnicorn様が制作した[ats_p_bell.wav](https://github.com/uifnm/GeneralAtsPlugin/tree/master/Unicorn/sound)を使用させていただいております。<br>
**ExternalDataの著作権は[当方](https://github.com/E233-3639)にはありません。**

### 二次利用などについて
**個人の範囲内(自分が所有するPCなどのデバイスでのみ)であれば**改造は自由です。改造したデータを自分が所有しないPCなどのデバイスにデータをコピーする(SDカードなどの記憶媒体メモリを介すことも含む)、インターネット上に公開することは禁止です。<br>
**改造は自己責任**です。改造による損失は当方は一切責任を負いません。

## 動画投稿について
広告収入を得ないなど**営利目的でない場合に限り**E233系3000番台車両データを使用した動画、スクリーンショットの投稿を認めます。<br>
動画、スクリーンショット以外は認めません。<br>
車両データを改変している場合は、動画、スクリーンショットの投稿は**認められません**。

## ダウンロード
[こちら](https://github.com/E233-3639/BVE_E233-3000_Data/archive/refs/tags/ver1.05.zip)よりダウンロードください。<br>
ダウンロード後、「BVE_E233-3000_Data-ver1.05.zip」を右クリック→すべて展開を選択してください。<br>
※車両データをダウンロードしたことによる損失は当方は一切責任を負いません。

## 運転方法
### 対応保安装置
対応している保安装置はATS-Pのみとなります。

### Vehicleファイルについて
**車両データを読み込ませるためにはVehicleファイルをScenarioファイルに定義する必要があります。**<br>
この車両データにはVehicle1.txtとVehicle2.txtがありドアチャイムが異なります。
* Vehicle1.txt  一般的なドアチャイム
* Vehicle2.txt  2017年増備車(E73編成 E74編成)のドアチャイム

では実際にどうやって車両データを読み込ませるのかをご説明します。その際にはVehicleファイル、Scenarioファイル、ファイルパスについて理解する必要があります。<br>
* Vehicleファイルとは？<br>
Vehicleファイルとは車両データを読み込ませる読み込ませるために必要です。Vehicleファイルの場所(ファイルパス)をScenarioファイルに定義することでできます。

* Scenarioファイルとは？<br>
Scenarioファイルとは路線データを読み込ませるために必要です。ダイヤや種別ごとにそれぞれ用意されています。<br>
ScenarioファイルをBVEに読み込むことでプレイできるようになります。<br>
Scenarioファイルは開くと頭に「BveTs Scenario」と書かれています。シナリオ一つ一つがScenarioファイルです。<br>
![image](https://user-images.githubusercontent.com/66541951/131004091-2b30a83f-2ea3-40a7-b725-03a95cad675b.png)

画像内に「Vehicle = 車両データのファイルパス」という式があります。<br>
**この式の右辺にVehicleファイルまでのファイルパスを記述することで、このシナリオをプレイする際に定義した車両データが読み込まれるようになります。**<br>
![image](https://user-images.githubusercontent.com/66541951/130986557-982bb36a-c8d5-4823-b528-1dcf3be5e516.png)<br>

* ファイルパスとは？
**ファイルパスとはファイルの場所を表す地図のようなものです。** これをもとにBVEは車両データを探します。<br>
(そもそもファイルとは画像や音などのデータのこと、それらをまとめるものをフォルダーと言います。)<br><br>
Vehicleファイルのファイルパスを書いてみましょう。<br><br>

例<br>
Scenario.txtはScenarioファイル、Vehicle.txtはVehicleファイルのことを指します。<br>
Vehicle.txtへのファイルパスを記述するのはScenario.txtです。なのでScenario.txtにVehicle.txtまでの道を教えてあげましょう。<br>
Scenario.txtはtestlineの中にあります。<br>
Vehicle.txtまでは、「①testlineから一つ戻ってScenarioに移動、②trainに進む、③Vehicle.txtを見つける」というように表すことができます。<br>
![名称未設定](https://user-images.githubusercontent.com/66541951/131015446-e21c93c8-4f9a-4788-97c2-7a22af765fae.png)<br>
ですがこれは日本語ですので伝わりません。これをPCがわかるように書き換えましょう。<br>
書き換えると「①..¥、②train¥、③Vehicle.txt」となります。<br>
「..」は一つ前のフォルダー(この場合Scenarioを指します)という意味、そしてフォルダー名(ファイル名)の間に「¥」を書きます。<br>
よってこの場合のファイルパスは ..¥train¥Vehicle.txt となります。


### BVEにおけるキー
BVEにはキーボードで様々な操作ができます。またBVEではA1キー、B1キーといった名前のものが存在します。これはBVE内でのキーの名称で、実際にどのキー(Enterキーやスペースキーなど)に割り当てることで使用できます。またキーの割り当ては個人で自由に変更できます。<br>
変更や割り当てられているキーを確認する場合は、BVEの画面を右クリック→設定→入力デバイス→キーの割り当てです。<br>
![image](https://user-images.githubusercontent.com/66541951/129451992-ca2eb0f6-2469-4d7a-b36d-99b9a27b48db.png)

### ATS復帰扱い
ATS-Pのパターンを超えたり、進んでいる向きとは逆に逆転ハンドルを切り替えるとATSブレーキが動作します。<br>
「ブレーキ動作」が点灯中はATSブレーキが作動しています。<br>
![image](https://user-images.githubusercontent.com/66541951/129451622-0256f428-8c88-4f96-99b5-fa304fca4b73.png)<br>
ATS復帰扱いは常用ブレーキ以上または非常ブレーキ(状況によりかける必要があるブレーキが異なります)をかけた状態で、B1キー(BVE内でのキー名称　デフォルトではHOMEキー)を押すと解除されます。

### EB装置について
一分間マスコンなどを操作しないとブザーが鳴動します。<br>
ブザー鳴動から10秒以内にA2キー(BVE内でのキー名称　デフォルトではdeleteキー)を押さなかった場合、非常ブレーキが動作します。
その場合は停止したのち、非常ブレーキをかけることで復帰します。

### 定速・抑速制御
この車両では定速・抑速制御があります。<br>
定速　速度が55km/h以上かつマスコンをP5にした状態でLキー(BVE内でのキー名称　デフォルトでは0キー)を押すことで動作します。<br>
抑速　速度が55km/h以上かつマスコンをNにした状態でLキー(BVE内でのキー名称　デフォルトでは0キー)を押すことで動作します。<br><br>

## Run音について
Run音とは走行中、常に再生される走行音のことです(モーター音とは異なります)。路線データによっては「鉄橋を走っていないのに鉄橋の走行音になる」といったことが起きる場合があります。<br>
Run音は車両データのSound.txtで以下の画像のように定義されてます。<br>
![image](https://user-images.githubusercontent.com/66541951/129504233-e93cf162-e93c-4825-95dd-a546376bad1b.png)<br>
* Run_Long1.wav        ロングレール
* Run_Long2.wav        ロングレール(東海道線 川崎ー品川間)
* Run_Short.wav        25mレール
* Run_SlabShort.wav    スラブ軌道
* Run_Tekkyo.wav       鉄橋
* Run_Tunnel.wav       トンネル 地下区間

Run音は「0 = 〇〇¥〇〇.wav」のように定義します。左辺はインデックス名、右辺は音源ファイルまでの相対パスです。<br><br>

実際にどのRun音を再生するかは路線データのMapファイルで定義します。構文はRollingNoise.Change(index)です。indexには「0 = 〇〇¥〇〇.wav」の左辺を入力します。この構文を記述すると、インデックスに定義されている走行音に変わります。<br>
「鉄橋を走っていないのに鉄橋の走行音になる」といった異常な状態の場合は、車両データのRun音定義、または路線データのMapファイルにRollingNoise.Change(index)を記述する方法があります。<br>
※路線データを改変する場合、他作者のデータを改変することになるため、説明書やReadmeなど確認するなど**路線制作者の許可を取った上で**行ってください。

### 最後に
ご質問、ご意見などは[Twitter](https://twitter.com/E233_3639)までお寄せください。<br>
全てにご対応できない場合がございます。ご了承ください。
