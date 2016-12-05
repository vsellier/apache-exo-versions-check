FROM exoplatform/base-jdk:1.8

RUN apt-get update && apt-get install -y wget unzip
RUN cd / && wget https://downloads.exoplatform.org/public/exo-platform-community-edition-4.4.0-latest.zip
RUN unzip exo-platform-community-edition-4.4.0-latest.zip
RUN rm exo-platform-community-edition-4.4.0-latest.zip && ln -s platform-community-4.4.0* plf

WORKDIR /plf
CMD ./start_eXo.sh
