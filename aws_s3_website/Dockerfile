FROM dockbit/base:latest
MAINTAINER The Dockbit Team "team@dockbit.com"

# Install S3 Website via RubyGems
WORKDIR /tmp
COPY components/aws_s3_website.sh .
RUN ./aws_s3_website.sh

# Cleanup & execution environment
USER root
RUN rm -f aws_s3_website.sh
COPY docker-entrypoint.sh /docker-entrypoint.sh
USER dockbit
WORKDIR /home/dockbit
ENTRYPOINT ["/docker-entrypoint.sh"]