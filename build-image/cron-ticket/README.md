## Buildx otras plataformas

* **Listar plataformas**
```bash
$ docker buildx ls
```
* **Agregar variable de entorno en el Dockerfile**
> FROM --platform=$BUILDPLATFORM node:current-alpine3.18

* Ejecutar las plataformas
```bash
$ docker buildx build --platform linux/arm64,linux/arm/v7 -t <username>/<image>:latest --push .
```
Más detalles en **[Docker Docs](https://docs.docker.com/build/building/multi-platform/)**