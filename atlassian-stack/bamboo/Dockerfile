FROM openjdk:8-jdk

RUN apt update && \
	apt install curl apt-transport-https ca-certificates software-properties-common -y && \
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add - && \
	add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu artful stable" && \
	apt update && \
	apt install docker-ce -y && \
	service docker start

EXPOSE 8085

ENV BAMBOO_HOME "/root/.bamboo"

RUN mkdir /root/.bamboo

VOLUME /root/.bamboo

WORKDIR /root/Software 

RUN wget https://www.atlassian.com/software/bamboo/downloads/binary/atlassian-bamboo-6.5.0.tar.gz && \
	tar -xvf atlassian-bamboo-6.5.0.tar.gz

ENTRYPOINT ["/root/Software/atlassian-bamboo-6.5.0/bin/start-bamboo.sh"]

CMD ["-fg"]

