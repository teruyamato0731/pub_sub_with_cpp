# pub_sub_with_cpp
[![Open in Dev Containers](https://img.shields.io/static/v1?label=Dev%20Containers&message=Open&color=blue&logo=visualstudiocode)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/teruyamato0731/pub_sub_with_cpp)

ROS2 humble の pub/sub を C++ で実行してみる。
[ROS公式の記事](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Writing-A-Simple-Cpp-Publisher-And-Subscriber.html)を参考に実行した。

# Quick Start
あなたがすでにVS CodeとDockerをインストールしている場合は、上記のバッジまたは[こちら](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/teruyamato0731/pub_sub_with_cpp)をクリックすることで使用することができる。<br>
これらのリンクをクリックすると、vscodeが必要に応じてdev container拡張機能を自動的にインストールし、ソースコードをコンテナボリュームにクローンし、使用するためのdev containerを起動する。

# How to use
1. Docker, vscode, devcontainer拡張機能をインストールする。
1. GitHub上部の緑の「Use this template」を押し、自身のGitHubアカウントで新規リポジトリを作成。
1. X11のアクセスをローカルに対して許可する。
    ```bash
    xhost +local:
    # non-network local connections being added to access control list
    ```
1. 自身の作成したリポジトリをcloneしvscodeで開く。<br>
    リポジトリのリンクやディレクトリ名は各自で読み替えること。
    ```bash
    git clone https://github.com/teruyamato0731/pub_sub_with_cpp.git
    code pub_sub_with_cpp
    ```
1. 「Reopen in Container」でdevcontainerを開く
1. 下記コマンドを実行すると pub/subが行える。
    ```bash
    colcon build
    . install/local_setup.bash
    ros2 run cpp_pubsub talker
    ```
    ```bash
    . install/local_setup.bash
    ros2 run cpp_pubsub listener
    ```
