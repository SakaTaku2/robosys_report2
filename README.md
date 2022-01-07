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

・ワークスペースの準備(変更あり)

　.bashrcの118行目以降に以下のコードを入力

 ```
 source /opt/ros/noetic/setup.bash
 source ~/ros_setup_scripts_Ubuntu20.04_server/catkin_ws/devel/setup.bash
 export ROS_MASTER_URI=http://localhost:11311
 export ROS_HOSTNAME=localhost
 ```

・パッケージをラズパイに入れる

 ```
 
 ```
 
# 実行方法

# サンプル動画

URL:

# ライセンス

GNU General Public License v3.0　
