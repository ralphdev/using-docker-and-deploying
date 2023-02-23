FROM neurodebian

LABEL Rafael Martinez <rafa.developers@gmail.com>

RUN apt-get update && apt-get install -y cowsay fortune

COPY entrypoint.sh /

ENTRYPOINT ["/entrypoint.sh"]