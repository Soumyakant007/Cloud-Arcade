FROM ubuntu:22.04

RUN apt-get update && apt-get install -y software-properties-common && add-apt-repository universe && apt-get update

RUN apt-get install -y --fix-missing nginx zip curl
RUN apt-get -y install p7zip-full

RUN echo "daemon off;" >>/etc/nginx/nginx.conf
RUN curl -o /var/www/html/main.zip -L https://github.com/harshalparmar/tower-blocks-game/archive/refs/heads/main.zip
RUN cd /var/www/html/ && 7z x main.zip && mv tower-blocks-game-main/* . && rm -rf game6-main main.zip

EXPOSE 80

CMD ["/usr/sbin/nginx", "-c","/etc/nginx/nginx.conf"]
