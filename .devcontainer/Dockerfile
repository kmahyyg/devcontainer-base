FROM archlinux:base-devel

RUN echo "" >> /etc/pacman.conf && \
    echo "[archlinuxcn]" >> /etc/pacman.conf && \
    echo "Server = https://repo.archlinuxcn.org/\$arch" >> /etc/pacman.conf

RUN rm -rf /etc/pacman.d/gnupg; pacman-key --init; pacman-key --populate archlinux && \
    pacman -Syy && \
    pacman -Su --noconfirm archlinux-keyring archlinuxcn-keyring && \
    pacman -S --noconfirm zsh sudo python python-pip python2 python2-pip supervisor git && \
    pacman -S --noconfirm python-setuptools python2-setuptools curl wget && \
    pacman -S --noconfirm ca-certificates openssh zip jq p7zip nano vim && \
    pacman -S --noconfirm go oh-my-zsh-git delve go-tools gopls && \
    pacman -S --noconfirm diff-so-fancy
