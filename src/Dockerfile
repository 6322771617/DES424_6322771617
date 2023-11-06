FROM nginx
LABEL MAINTAINER "Srisakul Prateepchinda"
ENV MY_HOST localhost
RUN apt-get update && apt-get install -y git sed
RUN mkdir /mycode && cd /mycode && git clone https://github.com/6322771617/DES424_6322771617.git
RUN cp -r /mycode/DES424_6322771617/src /usr/share/nginx/html/mygitweb
CMD sed -i 's/< MY_HOST >/'"$MY_HOST"'/gi' /usr/share/nginx/html/mygitweb/check4.html
