fork from https://github.com/sphinx-doc/docker/base

```
$ docker build -t khwarizmi/sphinx .
$ docker run --rm -v /path/to/document:/work khwarizmi/sphinx make [target]
```
