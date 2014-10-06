FROM dockerfile/java:oracle-java8

RUN apt-get update

RUN apt-get install -y maven

RUN cd /tmp \ 
&& git clone https://github.com/docker-for-the-enterprise-demo/simple-spring-rest-app.git \
&& cd simple-spring-rest-app \
&& mvn -Dmaven.test.skip=true package \
&& cp target/simple-app-*-SNAPSHOT.jar /data/app.jar \
&& rm -rf ~/.m2/repository/

VOLUME /data

CMD ["/bin/true"]

