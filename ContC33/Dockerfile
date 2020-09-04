FROM mysql:8.0
LABEL version="AC_MYSQL_v1"
WORKDIR /home/nana1/monapplianna
COPY fichier_Cont_C33.txt /tmp
ADD mespaquets.txt .
EXPOSE 3306
RUN apt-get update && apt-get install -y iputils-ping
RUN xargs -a mespaquets.txt apt-get install --assume-yes
RUN echo "FIN Installation Paquets for MYSQL Cont_C33 V1" >> /home/nana1/monapplianna/Status_Paquets_C33.txt
VOLUME /data/vol_anonyme_Mysql_Cont_C33
ENV my_hostname BDD_Mysql_C33_V1
CMD ["/bin/bash", "-c", "while true; do echo WELCOME on A.C. from $my_hostname and $HOSTNAME V1; sleep 10; done"]
