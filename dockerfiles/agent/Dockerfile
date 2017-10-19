FROM gocd/gocd-agent-alpine-3.5:v17.10.0

RUN apk -U add git openssh

USER gocd:gocd
COPY files/ssh/config /opt/gocd/.ssh/config

ENTRYPOINT ["cat $SSH_KEY > /opt/gocd/.ssh/id_rsa && cat $SSH_KEY_PUB > /opt/gocd/.ssh/id_rsa.pub && /docker-entrypoint.sh"]
