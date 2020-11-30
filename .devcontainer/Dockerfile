FROM archlinux:base-devel

RUN pacman -Syy && \
    pacman -Su --noconfirm && \
    pacman -S --noconfirm zsh sudo python python-pip python2 python2-pip supervisor && \
    pacman -S --noconfirm python-setuptools python2-setuptools curl wget && \
    pacman -S --noconfirm ca-certificates openssh zip jq p7zip nano vim
