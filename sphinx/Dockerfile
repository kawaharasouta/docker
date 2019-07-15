FROM ubuntu:18.04
MAINTAINER KAWAHARAsouta <kawahara6514@gmail.com>

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt install -y apache2 git vim tmux python3 python3-pip python3-sphinx \
 && pip3 install sphinx sphinx_rtd_theme \
 && mkdir ~/git && git clone https://github.com/kawaharasouta/dotfiles.git ~/git/dotfiles \
 && bash ~/git/dotfiles/setup.sh

# lang jp
RUN apt install -y locales \
 && locale-gen ja_JP.UTF-8 \
 && echo "export LANG=ja_JP.UTF-8" >> ~/.bashrc

