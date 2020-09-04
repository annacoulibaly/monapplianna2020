FROM httpd:2.4
LABEL version="AC_HTTPD_v1"
WORKDIR /home/nana1/monapplianna
COPY fichier_Cont_C22.txt /tmp
ADD mespaquets.txt .
EXPOSE 80
RUN apt-get update && apt-get install -y iputils-ping
RUN xargs -a mespaquets.txt apt-get install --assume-yes
RUN echo "FIN Installation Paquets for HTTPD Cont_C22 V1" >> /home/nana1/monapplianna/Status_Paquets_C22.txt
RUN /usr/local/apache2/bin/apachectl start
VOLUME /data/vol_anonyme_Apache2_Cont_C22
ENV my_hostname WEB_Apache2_C22_V1
CMD ["/bin/bash", "-c", "while true; do echo WELCOME on A.C. from $my_hostname and $HOSTNAME V1; sleep 10; done"]
