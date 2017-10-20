FROM webcenter/alpine-gocd-server:17.3.0-1

RUN apk -U add git openssh

COPY files/ssh/config /opt/gocd/.ssh/config
COPY files/install-ssh-certs-before /install-ssh-certs-before

ENTRYPOINT ["/install-ssh-certs-before", "/init"]
