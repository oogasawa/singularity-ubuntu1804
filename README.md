# Ubuntu18 Singularity

Ubuntu Linux 18.04 (Bionic) のSingularityコンテナ


## 前提

Ubuntu Linuxにdebootstrap他の必要なソフトをインストールする場合は以下の通り。

    sudo apt update
    sudo apt upgrade
    sudo apt install build-essential libtool automake libarchive-dev debootstrap git

Singularityはversion 2.x系をインストールすること。

- [Singularityのインストール方法（Official Document)](https://www.sylabs.io/guides/2.6/user-guide/installation.html) 



## 使い方

    # コンテナのビルド
    git clone http://gitlab.ddbj.nig.ac.jp/oogasawa/singularity-ubuntu18
    cd singularity-ubuntu18
    mkdir $HOME/singularity-images
    sudo singularity build --sandbox $HOME/singularity-images/ubuntu18 Singularity
    
    # コンテナ内での作業
    sudo singularity shell --write $HOME/singularity-images/ubuntu18
    
