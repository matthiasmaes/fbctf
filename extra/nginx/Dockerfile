FROM ubuntu:xenial

ENV HOME /root

ARG DOMAIN
ARG EMAIL
ARG MODE=dev
ARG TYPE=self
ARG KEY
ARG CRT
ARG HHVM=hhvm.ctf

WORKDIR $HOME
COPY . $HOME

RUN echo $HHVM
RUN apt-get update && apt-get -y install sudo apt-utils
RUN ./extra/provision.sh -m $MODE -c $TYPE -k $KEY -C $CRT -D $DOMAIN -e $EMAIL -s `pwd` --docker --multiple-servers --server-type nginx --hhvm-server $HHVM
CMD ["./extra/nginx/nginx_startup.sh"]

EXPOSE 80
EXPOSE 443