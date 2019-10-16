FROM node:latest

MAINTAINER Stel000(kkcyc1996@gmail.com)

WORKDIR /install/
USER root

RUN apt-get update && \
  apt-get install -y git && \
  rm -rf /var/lib/apt/lists/* && \
  npm install -g grunt-cli && \ 
  git clone https://github.com/gchq/CyberChef && \
  cd CyberChef && \
  npm install

ENV NODE_OPTIONS --max_old_space_size=2048

EXPOSE 8080
WORKDIR /install/CyberChef
ENTRYPOINT ["grunt"]
CMD ["prod"]
