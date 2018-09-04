FROM anapsix/alpine-java

RUN apk add unzip git linux-pam && \
	wget https://dl.gogs.io/0.11.53/gogs_0.11.53_linux_amd64.zip -O gogs.zip && \
	unzip gogs.zip
RUN adduser -S git 
RUN mkdir /home/git/gogs-repositories
RUN chown -R git /gogs/ && chown -R git /home/git/


ENTRYPOINT ["/gogs/gogs", "web"]
