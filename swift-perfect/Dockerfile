FROM swiftdocker/swift:latest
MAINTAINER mizhdi <mizhdi@gmail.com>

# Install Dependencies

RUN apt-get update && \
    apt-get install -y openssl libssl-dev uuid-dev mysql-client \
    libmysqlclient-dev libcurl4-openssl-dev libcurl4-openssl-dev && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN mkdir web && \
    cd web  && \
    git clone https://github.com/mizhdi/swift-server-demo.git && \
    cd swift-server-demo && \
    swift build
#   .build/debug/PerfectTemplate

# EXPOSE 8181
