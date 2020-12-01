FROM centos:8

RUN yum -y update && \
    yum install -y openssh-server \
    vim \
    lrzsz \
    wget \
    gcc \
    gcc-c++ \
    pcre \
    pcre-devel \
    zlib \
    zlib-devel \
    ruby \
    openssl \
    openssl-devel \
    patch \
    bash-completion \
    zlib.i686 \
    libstdc++.i686 \
    lsof \
    unzip \
    zip \
    net-tools \
    initscripts \
    net-tools.x86_64 \
    openssh-server \
    passwd \
    postgresql-devel \
    xz-devel \
    epel-release \
    bzip2-devel \
    ncurses-devel \
    sqlite-devel \
    readline-devel \
    tk-devel \
    make \
    automake \
    autoconf \
    libtool \
    yum-utils \
    libffi-devel \
    libnsl2 \
    bluez-libs \
    tix \
    python38 \
    cmake \
    rsync \
    gdb \
    gdb-gdbserver

RUN echo  root:asd123 | chpasswd

CMD [ "/usr/sbin/init", "service sshd restart" ]


