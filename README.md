# 「Raspberry Piで学ぶ ROSロボット入門」の情報リポジトリ

* インストールが面倒臭い人のためのOSイメージ: https://b.ueda.tech/?post=20180617_raspi_ubuntu

## 重要な情報



### 2018/6/15

https://wiki.ubuntu.com/ARM/RaspberryPi#Wifi にある手順でWiFiの動くファームウェアがインストールできることを確認しました。-> [wifiproblem.md](https://github.com/ryuichiueda/raspimouse_book_info/blob/master/trouble_reports/wifiproblem.md)


### 2018/6/11

最新のROSをインストールして `catkin_create_pkg` を使うと、`package.xml` のフォーマットがバージョン2になります。このバージョンでは `run_depend` が `exec_depend` に変更になっていますので、バージョン2を使うときは書籍中の `run_depend` を `exec_depend` に読み替えてください。元のバージョンを使いたい時には、XML上部にある `format="2"`を消します。ただ、新しいほうを覚えた方が良いでしょう。


### 2018/5/26

ちょっと気づいてなかったのですが、WiFiが2017/5/6の方法では動作しないことに気づきました。調査中です。とりあえず解決までは、次のようにおねがいします。

* 今、インストールが済んでWiFiが使えている場合はapt upgradeしない。
* これからインストールするときは、[この](https://b.ueda.tech/?post=20171223_raspi_ubuntu_image)イメージを利用

### 2018/4/22

執筆当時のシミュレータ（E章）の状況が残っていなかったので、その当時のもののブランチを作っていただきました。

* 本体: https://github.com/rt-net/raspimouse_sim/tree/rpim_book_version
* インストーラ: https://github.com/ryuichiueda/raspimouse_sim_installer/tree/rpim_book_version

### 2017/12/18

10章において、xmlファイルが指定したパスにないことが原因で、OpenCVにエラーが出ることがあります。

* 対処法

以下のコマンドを実行お願いします。

```
$ sudo apt install opencv-data
```

### 2017/12/8

12章で使うJavaScriptへのコードがリンク切れ状態になっています。

* 詳細: https://github.com/ryuichiueda/raspimouse_book_info/issues/11

デバイスドライバにバグがありましたので修正しました。（2017/7/7）

* [最新のブランチ](https://github.com/rt-net/RaspberryPiMouse)

### 2017/5/6

カーネルをアップデートするとWiFiが使えないという不具合を確認しています。

* [対処の方法](./trouble_reports/wifiproblem.md)
* [issue](https://github.com/ryuichiueda/raspimouse_book_info/issues/1)

## その他の情報

* システムの設定シェルスクリプト集: [ryuichiueda/raspimouse_book_ubuntu_init](https://github.com/ryuichiueda/raspimouse_book_ubuntu_init)
* 本書で使用するOSイメージに関する情報: [os_images.md](./os_images.md)
* 正誤表: [errata.md](./errata.md)
* FAQ: [faq.md](./faq.md)
* Facebookグループ: https://www.facebook.com/RaspberryPiMouse

## 各章のリポジトリ
* 2章: ROSセットアップスクリプト
    * https://github.com/ryuichiueda/ros_setup_scripts_Ubuntu16.04_server
* 3章: デバイスドライバ
    * https://github.com/rt-net/RaspberryPiMouse
* 4章:
    * [cronを使うもの](https://github.com/ryuichiueda/pimouse_setup/tree/cad60aa542ac45c4e685dc81804a9f2aa90b897d)
    * [makeを使うもの](https://github.com/ryuichiueda/pimouse_setup)

* 5章: Raspberry Pi Mouse用基本制御パッケージ（既製品）
    * https://github.com/ryuichiueda/raspimouse_ros/
* 6〜8章: 本の中で作るRaspberry Pi Mouse用基本制御パッケージ
    * https://github.com/ryuichiueda/pimouse_ros/
    
* 9章: Raspberry Pi Mouseを廊下で走らせるコード
   * https://github.com/ryuichiueda/pimouse_run_corridor

* 10章: カメラで顔を認識して追従
    * https://github.com/ryuichiueda/pimouse_vision_control
* 11章: 音声で指示を受けて移動
    * https://github.com/ryuichiueda/pimouse_voice_control
* 12章: ウェブブラウザで使うコントローラ
    * https://github.com/ryuichiueda/pimouse_monitor
* 13章: SLAM
    * https://github.com/ryuichiueda/pimouse_slam
    
    
## 便利ツール

* ゲームコントローラでロボットを操作するためのパッケージ
    * https://github.com/zaki0929/raspimouse_game_controller
