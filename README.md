# mypkg

ロボットシステム学「課題２」

# 概要

講義ビデオを視聴しながらパッケージを作成する。

# 動作環境

・Ubuntu20.04

・ROS (Meldic Morenia)

また、今回の課題で必要なものは以下の通りだ。

・Raspberry Pi 4 Computer Model B (4GB RAM)

・ロジクール ウェブカメラ C270n 

　公式サイトURL：https://urlzs.com/AL7kw
 
※ウェブカメラは下図のようにラズパイと接続する。

![S__23232538](https://user-images.githubusercontent.com/94817675/148517303-4502f90a-ac4e-48e4-8046-bf1a5789f41c.jpg)

# 準備

・ROSのインストール

　以下の順番で実行する。
 
 ```
 git clone git@github.com:ryuichiueda/ros_setup_scripts_Ubuntu20.04_server.git
 
 cd ros_setup_scripts_Ubuntu20.04_server/
 
 ./step0.bash
 
 ./step1.bash
 ```

・パッケージをラズパイに入れる

 ```
 git clone git@github.com:SakaTaku2/mypkg.git
 ```
 
# 実行方法

・ウェブカメラの動作確認

　➀一つ目の端末で以下のプログラムを入力する。

　```　
　roscore 
　```
 
　➁2つ目の端末で以下のプログラムを入力する。この時、1行目を実行し、「/dev/video0」があるか確認する。
 
  ```
  ls /dev/video*
  
  rosrun cv_camera cv_camera_node
  ```
 
 　➂3つ目の端末で以下プログラムを入力する。
  
  ```
  rosrun web_video_server web_video_server
  ```
  
　ブラウザで「ラズパイのIPアドレス:8080」と検索すると、ウェブカメラの映像が見れる。
  
・count.pyの実行

　➀1つ目の端末で以下のプログラムを入力する。
　
  ```
  roscore
  ```
  
  ➁2つ目の端末で以下のプログラムを入力する。
  
  ```
  catkin_make
  
  chmod +x count.py
  
  rosrun mypkg count.py
  ```
  
  ➂3つ目の端末で以下のプログラムを入力する。
  
  ```
  rostopic echo /count_up
  ```
  
・twice.pyの実行

　➀count.pyの➀～➁を実行する。

　➁3つ目の端末で以下のプログラムを入力する。
 
　```
　rosrun mypkg twice.py
　```
 
　➂4つ目の端末で以下のプログラムを入力する。
 
　```
　rostopic echo /twice
　```

# サンプル動画

URL:

# ライセンス

GNU General Public License v3.0　
