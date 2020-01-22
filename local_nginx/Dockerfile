FROM nginx:latest
MAINTAINER KAWAHARAsouta <kawahara6514@gmail.com>

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update 2>>/dev/null 

# use env, atode nosuyo.
COPY default.conf /etc/nginx/conf.d/default.conf


