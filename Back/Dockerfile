#comando pra buildar "docker build -t maisagua:latest ."

#pega a imagem do tomcat comob ase
FROM tomcat:9.0-jre11
#definir o diretório de trabalho atual para as instruções subsequentes no Dockerfile
WORKDIR /usr/local/tomcat/webapps/seu-aplicativo
#copia o executavel da aplicaçao para o workdir
COPY maisagua-0.0.1-SNAPSHOT.jar /usr/local/tomcat/webapps/seu-aplicativo/
#expõe a porta 8080
EXPOSE 8080
#comando pra executar o tomcat e a aplicaçao
CMD ["catalina.sh", "run"]



#caso o uso do tomcat seja um problema
#abaixo tem o codigo que cria uma imagem com base ubuntu e baixa as dependencias necessarias pra rodar a aplicaçao



#FROM ubuntu:latest
#RUN apt-get update && apt-get install -y \
#    openjdk-17-jdk \
#    unzip \
#    wget

#RUN wget https://services.gradle.org/distributions/gradle-7.2-bin.zip -P /tmp \
#    && unzip -d /opt /tmp/gradle-*.zip \
#    && rm -f /tmp/gradle-*.zip

#ENV GRADLE_HOME /opt/gradle-7.2
#ENV PATH $GRADLE_HOME/bin:$PATH

#WORKDIR /app

#COPY . /app/

#EXPOSE 8080

#caso queira rodar o aplicativo ao iniciar o container
#CMD ["java", "-jar", "maisagua-0.0.1-SNAPSHOT.jar"] 

# caso queira entar no terminal do container e depois iniciar a aplicaçao manualmente
#CMD ["/bin/bash"]                                   