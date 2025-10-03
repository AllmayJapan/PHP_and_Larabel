# docker/web/Dockerfile
FROM php:8.2-apache

# 必要なPHP拡張機能をインストール
RUN docker-php-ext-install mysqli pdo pdo_mysql

# Apacheの設定ファイルをコピー
COPY 000-default.conf /etc/apache2/sites-available/000-default.conf

# Apacheのモジュールを有効化
RUN a2enmod rewrite

# Apacheのログを標準出力にリダイレクト (オプション)
# ENV APACHE_LOG_DIR /dev/stdout
# ENV APACHE_RUN_DIR /var/run/apache2
# ENV APACHE_PID_FILE /var/run/apache2/apache2.pid
