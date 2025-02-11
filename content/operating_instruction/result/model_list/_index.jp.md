---
title: "モデルの一覧画面"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
# 重要ではないので一番下に
weight: 10
draft: false
# metaタグのパラメータ
meta:
  description: ""
# クラウド・デスクトップ限定ページの場合は片方のみtrueにする
visible:
  is_cloud_only: false
  is_desktop_only: false
# 検索でヒットする文字列の指定
keywords:
  [
    "モデル一覧",
    "モデルの一覧",
    "コピーして予測モデルを新規作成",
    "評価用データに対する予測結果を出力",
    "エクスポート",
    "インポート",
    "予測モデルをエクスポート",
    "予測モデルをインポート",
  ]
---

Prediction One を起動した状態で複数のモデルがすでに作成されているとき、左側にモデル・フォルダーの一覧が表示されます。

![](../../img/t_slide48.png)
![](../../img/t_slide49.png)

{{% div_method_area "新しくモデルを作成する" %}}
{{% step_n2 1 "「新規モデル作成」ボタンをクリックしてください。" %}}
{{% /div_method_area %}}

{{% cloud_only %}}
{{% div_method_area "モデルを共有する" %}}
元となるモデルのモデルプルダウンをクリックし、「共有」をクリックしてください。共有用のスペースにコピーされ、同じテナントのアカウント利用者がモデル詳細の閲覧や予測ができるようになります。
{{% /div_method_area %}}

{{% div_method_area "共有したモデルを確認・利用する" %}}
モデル一覧の「共有」タブをクリックしてください。共有用のモデル一覧がに切り替わります。
{{% /div_method_area %}}
{{% /cloud_only %}}

{{% div_method_area "モデルをお気に入りに追加する" %}}
{{% step_n_area2 1 "「お気に入りボタン」をクリックしてください。" %}}
お気に入りに追加されたモデルは、モデル一覧にて並び順の上位に表示されるようになります。
再び「お気に入りボタン」をクリックすることでお気に入りから外すことができます。
{{% /step_n_area2 %}}
{{% /div_method_area %}}

{{% desktop_only %}}
{{% div_method_area "予測モデルをインポートする" %}}
{{% step_n2 1 "予測モデル作成プルダウンをクリックしてください。" %}}
{{% step_n2 2 "「予測モデルをインポート」をクリックしてください。" %}}
{{% step_n2 3 "Prediction Oneでエクスポートされたモデル(zipファイル)を指定してください。" %}}
{{% /div_method_area %}}
{{% /desktop_only %}}

{{% div_method_area "新しくフォルダーを作成する" %}}
{{% step_n2 1 "「新規フォルダー作成」ボタンをクリックしてください。" %}}
{{% /div_method_area %}}

{{% div_method_area "フォルダーを削除する" %}}
{{% step_n2 1 "フォルダープルダウンをクリックしてください。" %}}
{{% step_n_area2 2 "「削除」をクリックしてください。" %}}
<u>フォルダーを削除した場合、フォルダー内部のモデルはすべて削除されます。</u>
この操作は取り消すことができません。
{{% /step_n_area2 %}}
{{% /div_method_area %}}

{{% div_method_area "フォルダー名を変更する" %}}
{{% step_n2 1 "フォルダー名をクリックし、新しいフォルダー名を入力してください。" %}}
{{% /div_method_area %}}

{{% div_method_area "お気に入りに追加したモデルを表示する" %}}
{{% step_n2 1 "「お気に入りのみ表示ボタン」をクリックしてください。" %}}
{{% /div_method_area %}}

{{% div_method_area "モデルリストをソートする" %}}
{{% step_n2 1 "モデルソートプルダウンからソート基準の指標を選択してください。" %}}
{{% /div_method_area %}}

{{% div_method_area "モデルに対する操作(コピーや削除など)をする" %}}
![](../../img/t_slide50.png)

モデル名の右側に表示されているモデルプルダウンをクリックすると、上のようなメニューが表示されます。
ここから、モデルのコピーや削除を行うことができます。
{{% /div_method_area %}}

{{% div_method_area "作成済みのモデルを編集し、再度学習を実行するには" %}}
元となるモデルのモデルプルダウンをクリックし、「コピーして予測モデルを新規作成」をクリックしてください。
元となるモデルの設定が入力された状態で、学習設定画面を開くことができます。
ただし、<u>元となるモデルの作成時に利用した学習データが同じ場所に同じファイル名で存在しない場合、この操作は実行できません。
また、元となるモデル作成後に学習データのファイル内容を変更していた場合、その後の処理が正しく動作しない場合があります</u>。
{{% /div_method_area %}}

{{% desktop_only %}}
{{% a_id "output-result" %}}
{{% div_method_area "評価用データに対する予測結果を出力するには" %}}
元となるモデルのモデルプルダウンをクリックし、「評価用データに対する予測結果を出力」をクリックしてください。
「精度」画面で各種精度を算出するのに使用した評価用データと、それに対する予測結果を csv ファイルで出力できます。

通常は、{予測結果列}→{評価用データ列}の順番で出力されますが、時系列予測モードで予測モデルを作成した場合は、{forecast_before 列}→{予測結果列}→{評価用データ列}の順番で出力されます。
({forecast_before 列}はどれだけ先を予測するモデルに関する評価なのかを表します。たとえば、1 ヶ月先、4 ヶ月先、7 ヶ月先、9 ヶ月先、12 ヶ月先を予測するモデルを評価した場合、{forecast_before 列}には、1, 4, 7, 9, 12 のいずれかの値が入ります。)
{{% /div_method_area %}}
{{% /desktop_only %}}


{{% desktop_only %}}
{{% div_method_area "予測ヒストリーを見るには" %}}
予測ヒストリーから、過去にこのモデルを使って予測した予測用データのファイル名一覧を確認できます。
![](../../img/t_slide51.png)

予測ヒストリーは削除することもできます。
![](../../img/t_slide52.png)
削除したい予測用データを選択し、削除をクリックしてください。
<u>この操作では Prediction One に残された予測用データの履歴のみが削除され、予測用データそのものが削除されることはありません</u>。
{{% /div_method_area %}}
{{% /desktop_only %}}

{{% desktop_only %}}
{{% div_method_area "予測モデルをエクスポートするには" %}}
元となるモデルのモデルプルダウンをクリックし、「予測モデルをエクスポート」をクリックしてください。
予測モデルと、予測モデルが参照しているファイル(予測モデル作成(学習)用データなど)を、1つのzipファイルに圧縮して保存できます。
エクスポートされたモデル(zipファイル)は、別のPCにコピーし「予測モデルをインポート」すると、モデルを移行できます。
{{% /div_method_area %}}
{{% /desktop_only %}}


{{% div_method_area "モデルを削除するには" %}}
{{% step_n2 1 "モデルプルダウンをクリックし、表示されたメニューから「削除」をクリックしてください。" %}}
{{% /div_method_area %}}

{{% div_method_area "モデルのモデル名や説明を編集するには" %}}
{{% step_n2 1 "モデルプルダウンをクリックし、表示されたメニューから「編集」をクリックしてください。" %}}
{{% /div_method_area %}}

{{% div_method_area "モデル一覧の表示・非表示を切替える" %}}
{{% step_n2 1 "「モデル一覧表示切替」ボタンをクリックしてください。" %}}
{{% /div_method_area %}}
