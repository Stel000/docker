FROM openjdk:8

MAINTAINER Stel000(kkcyc1996@gmail.com)

RUN apt-get update
RUN apt-get install -y curl git maven sudo

RUN curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
RUN sudo apt-get install -y nodejs build-essential

RUN curl --insecure -o ./sonarscanner.zip -L https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-4.0.0.1744-linux.zip && \
	unzip sonarscanner.zip && \
	rm sonarscanner.zip && \
	mv sonar-scanner-4.0.0.1744-linux /usr/lib/sonar-scanner && \
	ln -s /usr/lib/sonar-scanner/bin/sonar-scanner /usr/local/bin/sonar-scanner && \
  rm -rf /usr/lib/sonar-scanner/conf/sonar-scanner.properties

ENV SONAR_RUNNER_HOME=/usr/lib/sonar-scanner
