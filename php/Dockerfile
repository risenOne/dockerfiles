FROM debian:jessie

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install --quiet --yes --force-yes --no-install-recommends \
        apt-utils \
        ca-certificates \
        curl \
        git \
        grep \
        lynx \
        bz2 \
        openssh-client \
        rsync \
        software-properties-common \
        unzip \
        wget \
        zip \
        && apt-get clean -qq \
        && apt-get autoremove -qq \
        && ( -rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* >/dev/null 2>&1 || true ) \

RUN wget --no-clobber --quiet https://www.dotdeb.org/dotdeb.gpg \
        && apt-key add dotdeb.gpg \
        && apt-get update \
        && rm dotdeb.gpg
        && echo 'deb http://packages.dotdeb.org jessie all' > /etc/apt/sources.list.d/dotdeb.list \
        && echo 'deb-src http://packages.dotdeb.org jessie all' >> /etc/apt/sources.list.d/dotdeb.list \

RUN apt-get update && apt-get install --quiet --yes --force-yes --no-install-recommends \
        php7.0-apcu \
        php7.0-apcu-bc \
        php7.0-bcmath \
        php7.0-bz2 \
        php7.0-cli \
        php7.0-common \
        php7.0-curl \
        php7.0-enchant \
        php7.0-gd \
        php7.0-geoip \
        php7.0-gmp \
        php7.0-imagick \
        php7.0-imap \
        php7.0-intl \
        php7.0-json \
        php7.0-ldap \
        php7.0-mbstring \
        php7.0-mcrypt \
        php7.0-memcached \
        php7.0-mongodb \
        php7.0-mysql \
        php7.0-opcache \
        php7.0-pgsql \
        php7.0-readline \
        php7.0-redis \
        php7.0-sqlite3 \
        php7.0-ssh2 \
        php7.0-xdebug \
        php7.0-xml \
        php7.0-xmlrpc \
        php7.0-xsl \
        php7.0-zip \
    && apt-get clean -qq \
    && apt-get autoremove -qq \
    && ( -rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* >/dev/null 2>&1 || true ) \
    && ( echo 'date.timezone="Europe/Berlin"' >> /etc/php/7.0/cli/conf.d/timezone.ini || true ) \
    && rm -rf /etc/php/7.0/cli/conf.d/20-xdebug.ini




