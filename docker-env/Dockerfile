cat << 'EOF' > Dockerfile
FROM ubuntu:16.04

# Gerekli tüm derleme araçlarını ve bağımlılıkları kur
RUN apt-get update && apt-get install -y \
    curl \
    git-core \
    gnupg \
    flex \
    bison \
    gperf \
    build-essential \
    zip \
    zlib1g-dev \
    gcc-multilib \
    g++-multilib \
    libc6-dev-i386 \
    lib32ncurses5-dev \
    x11proto-core-dev \
    libx11-dev \
    libgl1-mesa-dev \
    libxml2-utils \
    xsltproc \
    unzip \
    openjdk-8-jdk \
    python \
    bzip2 \
    bsdmainutils \
    libssl-dev \
    && rm -rf /var/lib/apt/lists/*

# Repo aracını indir ve kur
RUN mkdir -p /root/bin && \
    curl https://storage.googleapis.com/git-repo-downloads/repo > /root/bin/repo && \
    chmod a+x /root/bin/repo

ENV PATH="/root/bin:${PATH}"

# Çalışma dizinini ayarla
WORKDIR /neoOS_src

CMD ["/bin/bash"]
EOF
