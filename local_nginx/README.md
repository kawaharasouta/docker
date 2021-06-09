```
$ docker build -t khwarizmi/local_nginx .
$ docker run --name nginx -d -v ~/git/wiki/docs:/usr/share/nginx/html/wiki/docs -v ~/git/hobbies/docs:/usr/share/nginx/html/hobbies/docs -p 8080:80 khwarizmi/local_nginx
```
