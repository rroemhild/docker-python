FROM debian:jessie

MAINTAINER Rafael Römhild <rafael@roemhild.de>

# http://bugs.python.org/issue19846
ENV LANG C.UTF-8

RUN apt-get -q update && \
     apt-get install --no-install-recommends -y -q \
       ca-certificates build-essential git mercurial \
       python3.4 python3.4-dev python-pip \
       libffi-dev libssl-dev libxml2-dev \
       libxslt1-dev libpq-dev libmysqlclient-dev libcurl4-openssl-dev \
       libjpeg-dev zlib1g-dev libpng12-dev \
       gfortran libblas-dev liblapack-dev libatlas-dev libquadmath0 \
       libfreetype6-dev pkg-config swig \
       && \
     apt-get clean && rm /var/lib/apt/lists/*_*

# Upgrade pip and install virtualenv
RUN pip install --upgrade pip virtualenv

WORKDIR /app

CMD ["python3.4"]
