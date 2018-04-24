FROM sonarqube:latest
MAINTAINER Kumbasar

WORKDIR $SONARQUBE_HOME/extensions/plugins

RUN set -x \
&& curl -fSL -o sonar-cxx-plugin-0.9.9.jar https://github.com/SonarOpenCommunity/sonar-cxx/releases/download/cxx-0.9.9/sonar-cxx-plugin-0.9.9.jar

VOLUME ["$SONARQUBE_HOME/data", "$SONARQUBE_HOME/extensions"]


WORKDIR $SONARQUBE_HOME

ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
