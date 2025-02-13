FROM python:3.12.8-slim-bookworm

# 必要モジュールのインストール
RUN apt-get update && apt-get install -y default-libmysqlclient-dev build-essential pkg-config

# 作業ディレクトリを設定
WORKDIR /usr/src/app

# requirements.txtをコピー
COPY requirements.txt /usr/src/app/

# 仮想環境作成 & pipでrequirements.txtをインストール
RUN python -m venv ~/.virtualenvs/djangodev && . ~/.virtualenvs/djangodev/bin/activate && pip install --upgrade pip && pip install --no-cache-dir -r requirements.txt
