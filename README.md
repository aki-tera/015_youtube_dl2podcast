# 015_youtube_dl2podcast

![python3](https://img.shields.io/badge/type-python3-brightgreen)  ![passing](https://img.shields.io/badge/windows%20build-passing-brightgreen) ![MIT](https://img.shields.io/badge/license-MIT-brightgreen)  
![Apache](https://img.shields.io/badge/Server-Apache-red) ![iPhone](https://img.shields.io/badge/SmartPhone-iPhone-red)  
![youtube_dl](https://img.shields.io/badge/libraly-youtube_dl-blue)  

## DEMO

### This is a program that can create RSS feeds of videos retrieved by youtube_dl

<img src="https://user-images.githubusercontent.com/44888139/143860818-53d49fbb-8e36-40d8-ac5d-34cb66684152.png" width="250px"> <img src="https://user-images.githubusercontent.com/44888139/143860972-8d79e6b4-e564-4272-8bdb-8311ccd3349b.png" width="250px">  <img src="https://user-images.githubusercontent.com/44888139/143861091-0ce1f586-178f-47c6-926f-4ae28f50fe4b.png" width="250px">  

### You can watch the videos registered in RSS with the podcast application on your smartphone  

<img src="https://user-images.githubusercontent.com/44888139/143861364-f32db240-497e-4ad8-b9f6-fdda529f482e.png" width="250px">

## Features

If you register the url in the podcast app, you can watch the videos you get from youtube_dl on your smartphone.

### specification

- The supported videos are what youtube_dl can go.
- If you need to log in, you can do in the following two ways
  - You can be handled by setting usernames and login passwords for each services.
  - If the above is not possible, you can use `cookie.txt`.
- Assuming a home LAN
- Warning
  - Publishing the data generated by this software on the Internet may cause legal problems.
  - This software is MIT licensed.

## Requirement

Python & HTTP Server & Smartphone

- I ran this program with the following execution environment.
  - Windows 10
    - Python 3.9
    - Apache HTTP Server 2.4
  - iPhone11
    - ios 14.8/ios 15.2
    - Apple Podcast App

Python Library

- the external package
  - youtube_dl
  - pyperclip
- the standard library
  - cgi, cgitb
  - codecs
  - re
  - sys, io, os
  - xml.etree.ElementTree
  - glob
  - email import utils
  - json

Podcast software

- Apple Podcast App

## Usage

### How to use (Initial Settings)

1. Install Apache.
1. Clone this repository into the apache folder.
1. Run `create_setting_file.py`.
   1. You can get URL for `podcast.rss` in two patterns: View and Clipboard.
   1. Generate `podcast/podcast.rss` and `setting_file.json` automatically.
1. Please register the URL above in the Podcast App from your iPhone.

### How to use (Execution)

1. Run apache.
1. Open "localhost" in your browser
1. See the operation in the picture above
1. Finally update your Podcast App.

## Others

### How to change the your podcast cover

If you want to change the podcast cover, please overwrite `cgi-bin\art-work\001.png`.  
Apple recommends the following, but I think 400px x 400px is also possible.  
(<https://podcasters.apple.com/support/896-artwork-requirements>)  

- jpeg or png
- Square
- Size
  - Maximum pixel: 3000px x 3000px
  - Minimum pixel: 1400px x 1400px

## License

This program is under MIT license.  

***

## 【日本語】

## 機能

Youtube_dlで取得したビデオを、Podcastに登録できるようにします。

- 仕様
  - ビデオはYoutube_dlで対応しているものです。
  - ログインが必要な場合、以下の2通りで対応できます。
    - サービスごとにユーザネームとパスワードの登録が可能
    - 上記で対応できない場合は、`cookie.txt`を対応
  - 家庭内LANで使用
  - 警告
    - 本ソフトで作成したデータをインターネットに公開すると、法的な問題が発生する可能性があります。
    - 本ソフトは、MITライセンスです。

## 必要なもの

Python & HTTP Server

- このプログラムは、Windows10上で、Python 3.9とApache HTTP Server 2.4で動作確認しています。
- スマホ側は、iPhone11(ios14.8/ios15.2)のPodcast Appで動作確認しています。

## 使い方

### 初期設定

1. Apacheをインストールします。
1. このリポジトリをApacheフォルダにCloneします。
1. `create_setting_file.py`を実行します。
   1. Podcast Appに登録するリンクが取得できます（クリップボード ＆ 画面表示）。
   1. 各種設定がされます。
1. 取得したリンクをPodcast Appに登録します。

### 取得と登録

1. Apacheを実行します
1. ブラウザでlocalhostを開きます。
1. 上記の絵を見て操作します。
1. Podcast Appを更新すると、登録されていることが分かります。

## その他

### ポッドキャストの画像変更に関して

このファイル`cgi-bin\art-work\001.png`を上書きして下さい。  
Appleは以下の内容を推奨していますが、画素サイズは400px x 400pxでも大丈夫です。

- jpeg or png
- 正方形
- サイズ
  - 最大画素: 3000px x 3000px
  - 最小画素: 1400px x 1400px

## ライセンス

本プログラムは、MITライセンスです。
