FROM ubuntu:22.04

RUN apt-get update && apt-get install -y software-properties-common && add-apt-repository universe && apt-get update

RUN apt-get install -y --fix-missing nginx zip curl

RUN echo "daemon off;" >>/etc/nginx/nginx.conf
RUN curl -o /var/www/html/master.zip -L https://codeload.github.com/ImKennyYip/flappy-bird/zip/master
RUN cd /var/www/html/ && unzip master.zip && mv flappy-bird-master/* . && rm -rf flappy-bird-master master.zip

EXPOSE 80

CMD ["/usr/sbin/nginx", "-c","/etc/nginx/nginx.conf"]
