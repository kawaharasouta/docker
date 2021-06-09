fork from https://github.com/sphinx-doc/docker/base


wikiをビルドする例

```
$ docker build -t khwarizmi/sphinx .
$ docker run --rm -v ~/git/wiki:/work khwarizmi/sphinx make docs
```
