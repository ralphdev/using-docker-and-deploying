FROM python:3.9

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi

RUN pip install --upgrade pip
RUN pip install Flask
RUN pip install uWSGI

WORKDIR /app

COPY app /app

COPY cmd.sh /

EXPOSE 9090
USER uwsgi

CMD ["/cmd.sh"]

#CMD [ "uwsgi", "--http", "0.0.0.0:9090", \
#               "--wsgi-file", "/app/identidock.py", \
#               "--callable", "app", \
#               "--stats", "0.0.0.0:9191"]
