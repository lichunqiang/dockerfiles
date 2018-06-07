FROM php:7.1-cli

RUN curl -fsSL 'https://github.com/swoole/swoole-src/archive/v1.10.5.tar.gz' -o swoole.tar.gz \
    && mkdir -p swoole \
    && tar -xf swoole.tar.gz -C swoole --strip-components=1 \
    && rm swoole.tar.gz \
    && ( \
        cd swoole \
        && phpize \
        && ./configure \
        && make -j$(nproc) \
        && make install \
    ) \
    && rm -r swoole \
    && docker-php-ext-enable swoole

CMD ["php"]
