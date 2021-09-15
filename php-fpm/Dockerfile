FROM php:8.0-fpm

RUN apt -y update && \
    apt install -y mariadb-client \
                   ca-certificates \
                   apt-transport-https \
                   software-properties-common \
                   gnupg2 \
	           wget && \
    echo "deb https://packages.sury.org/php/ bullseye main" | tee /etc/apt/sources.list.d/sury-php.list && \
    wget -qO - https://packages.sury.org/php/apt.gpg | apt-key add - && \
    apt -y update && \
    apt install -y "php8.0-mysql/bullseye" && \
    ln -s /usr/lib/php/20200930/* /usr/local/lib/php/extensions/no-debug-non-zts-20200930/ && \
    ln -s /usr/share/php8.0-mysql/mysql/* /usr/local/etc/php/conf.d/
    
