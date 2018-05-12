FROM openjdk:8-jdk

EXPOSE 8085

ENV BAMBOO_HOME "/root/.bamboo"

RUN mkdir /root/.bamboo

WORKDIR /root/Software 

RUN wget https://www.atlassian.com/software/bamboo/downloads/binary/atlassian-bamboo-6.5.0.tar.gz && \
	tar -xvf atlassian-bamboo-6.5.0.tar.gz

ENTRYPOINT ["/root/Software/atlassian-bamboo-6.5.0/bin/start-bamboo.sh"]

CMD ["-fg"]

