FROM nginx:1.23.0-alpine

COPY ./nginx/* /etc/nginx/
COPY ./run.sh /run.sh

COPY ./cert/* /etc/cert/

ENV APP_HOST=app
ENV APP_PORT=8000

USER root

RUN apk add --no-cache openssl bash
RUN chmod +x /run.sh

VOLUME /vol/static
VOLUME /vol/www

CMD ["/run.sh"]