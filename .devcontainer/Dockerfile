# ベースイメージとして 24.04 を使用、base イメージ以降のタグ指定が ubuntu バージョンにより異なるため要注意
# NOTE: 22.04 の場合は podman v3 系になり、 24.04 の場合は podman v4 系になる
# NOTE: そのため新しいものを使いたい場合は 24.04 を明示的に指定する
ARG VARIANT="24.04"
FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu-${VARIANT}

# 必要なツールをインストール
RUN apt-get update && apt-get install -y \
    curl \
    git \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# 作業ディレクトリを設定
WORKDIR /workspaces/LTSlides
