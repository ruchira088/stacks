FROM openjdk:8-jdk

EXPOSE 7990

ENV BITBUCKET_HOME /root/.bitbucket

RUN mkdir /root/.bitbucket

WORKDIR /root/Software

RUN wget https://www.atlassian.com/software/stash/downloads/binary/atlassian-bitbucket-5.10.0.tar.gz && \
	tar -xvf atlassian-bitbucket-5.10.0.tar.gz

ENTRYPOINT ["/root/Software/atlassian-bitbucket-5.10.0/bin/start-bitbucket.sh"]

CMD ["-fg"] 