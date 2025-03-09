FROM python:latest

RUN apt update && apt install -y --no-install-recommends \
    git \
    curl \
    wget \
    unzip \
    vim \
    nano \
    zsh \
    tmux \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*

# Install rust & cargo
RUN curl https://sh.rustup.rs -sSf | bash -s -- -y

# Install uv
RUN curl -LsSf https://astral.sh/uv/install.sh | sh

ENV UV_CACHE_DIR=/workspace/.uv/cache