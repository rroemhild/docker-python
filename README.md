# Python Docker Image

This image is based on Debian Jessie, contains packages required to build most of the popular Python libraries and can be used as a base image.

## Supported Tags

* `2.7` ([2.7/Dockerfile](https://github.com/rroemhild/python/blob/master/2.7/Dockerfile))
* `3.4` ([3.4/Dockerfile](https://github.com/rroemhild/python/blob/master/3.4/Dockerfile))

## Quick Start

Create a `Dockerfile` based on this image that copies your application code, installs dependencies, and declares an command or entrypoint:

```
FROM rroemhild/python:2.7

RUN virtualenv /env

ENV VIRTUAL_ENV=/env \
    PATH=/env/bin:$PATH

ADD requirements.txt /app/requirements.txt
RUN pip install -r /app/requirements.txt

ADD . /app

CMD ["python", "/app/production.py"]
```

## Licensing

* See [LICENSE](LICENSE)
