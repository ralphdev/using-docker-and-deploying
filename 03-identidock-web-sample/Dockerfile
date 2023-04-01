FROM python:3.9

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi

RUN pip install --upgrade pip
RUN pip3 install Flask uWSGI requests redis

WORKDIR /app

COPY app /app

COPY cmd.sh /

EXPOSE 9090
USER uwsgi

CMD ["/cmd.sh"]