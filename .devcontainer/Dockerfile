# githubのNodeのDockerイメージ（参照：https://hub.docker.com/_/node）
FROM node

# インストール可能なパッケージ一覧の最新化
RUN apt-get update

# 作業用ディレクトリの作成
WORKDIR /devcontainer/workspace

# textlintのインストール
COPY package.json /devcontainer
RUN npm install \
    && npm install --save-dev textlint-rule-preset-ja-technical-writing \
    && npm install --save-dev textlint-rule-preset-jtf-style
COPY .textlintrc.json /devcontainer
