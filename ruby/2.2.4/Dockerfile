FROM dockbit/base:latest
MAINTAINER The Dockbit Team "team@dockbit.com"

RUN . $HOME/.bash_profile \
 && rbenv shell 2.2.4

# Execution environment
COPY docker-entrypoint.sh /docker-entrypoint.sh
ENTRYPOINT ["/docker-entrypoint.sh"]
