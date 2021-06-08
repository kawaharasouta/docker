FROM python:slim
MAINTAINER KAWAHARAsouta <kawahara6514@gmail.com>

WORKDIR /work
RUN apt-get update \
 && apt-get install --no-install-recommends -y \
      graphviz \
      imagemagick \
      make \
 && apt-get autoremove \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

RUN python3 -m pip install --no-cache-dir -U pip
RUN python3 -m pip install --no-cache-dir Sphinx==4.0.2 Pillow
RUN python3 -m pip install --no-cache-dir sphinx_rtd_theme

CMD ["make", "docs"]
