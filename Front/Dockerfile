FROM httpd:latest

#WORKDIR /var/www/html
WORKDIR /usr/local/apache2/htdocs

#limpa o diretorio para garantir que apenas o projeto estara dentro do diretorio
RUN rm -rf ./*

#cria a pasta assets
RUN mkdir assets

#caso nao funcione o projeto em htdocs vai funcionar em html

# copia todo o projeto pra pasta htdocs 
COPY index.html /usr/local/apache2/htdocs/
COPY buscarBoletim.html /usr/local/apache2/htdocs/
COPY buscarProblema.html /usr/local/apache2/htdocs/
COPY cadastrarBoletim.html /usr/local/apache2/htdocs/
COPY cadastrarProblema.html /usr/local/apache2/htdocs/
COPY assets/ /usr/local/apache2/htdocs/assets/

#copia todo o projeto pra pasta html
#COPY index.html /var/www/html/
#COPY buscarBoletim.html /var/www/html/
#COPY buscarProblema.html /var/www/html/
#COPY cadastrarBoletim.html /var/www/html/
#COPY cadastrarProblema.html /var/www/html/
#COPY assets/ /var/www/html/assets/

#RUN chmod -R 644 /usr/local/apache2/htdocs/assets/

EXPOSE 80
