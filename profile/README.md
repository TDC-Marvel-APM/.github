# Marvel-API-SpringBoot

![](https://c.tenor.com/YHDk9U9pUQQAAAAC/avengers-assemble-ready.gif)

## Sobre
Projeto feito para demonstração de Execução de APM com ELK(Elastic, Logstash e Kibana) na palestra sobre ELK, APM e Observabilidade - Observabilidade e implementação na pratica e seus conceitos de uso.

Palestra realizada no TDC Business 2022 onde vocês pode acompanhar sobre pelo link: https://thedevconf.com/tdc/2022/business/trilha-devops

## Versões utilizadas 💘

Versão do Java - java version "1.8.0_311"

Versão do NodeJs - v16.13.2

Versão do NPM - 8.10.0

Versão do Docker Desktop Server: Docker Desktop 4.5.0 (74594)


## Passo a passo de como utilizar no SpringBoot 💡💎

1. Acesse o site https://cloud.mongodb.com/ e crie sua conta por lá
2. Acessando sua conta crie um novo projeto e deixe o nome TDC - Testes e em add membros deixe como está no caso ele vai deixar você seu usuario de cadastro como owner
3. depois de criar clique na aba Network Access e clicando nele clica em Add IP Address e seleciona ALLOW ACCESS FROM ANYWHERE e clica em confirm
4. depois de criar clique na aba clica em Add New Database User e em Password Authentication coloque um user e passwoard que desejar
5. Clica na aba de DataBase clica em Create e seleciona o banco share, e clica em confirm, ele demora um pouco para carregar mas logo ja estará criado seu banco
6. Clica em Connect e logo em seguida seleciona connect your application e nele você  receberá na parte Add your connection string into your application code a url do nosso banco, copia e cola isso dentro da pasta ./src/main/resources dessa maneira:
    ```
    spring.data.mongodb.uri=mongodb+srv://giovana:queijo@cluster0.e2ye4.mongodb.net/?retryWrites=true&w=majority
    spring.data.mongodb.database=Marvel
    ```
7.Dentro do projeto vocês verão um arquivo chamado Marvel Universe.postman_collection.json com ele vocês conseguem importar no seu postman e utilizar as rotas desse projeto
8. Para funcionar seu projeto, é necessario rodar o comando: 
 ```
    mvn clean package
 ```
Ele irá gerar um diretorio target e nele irá conter o seu arquivo de SNAPSHOT.jar
9. para rodar basta utilizar o comando: 
  ```
    java -javaagent:./agent/elastic-apm-agent-1.33.0.jar \
   -Delastic.apm.service_name=Marvel-API-SpringBoot \
   -Delastic.apm.server_urls=http://localhost:8200 \
   -Delastic.apm.application_packages=com.example \
   -jar target/spring-mongodb-0.0.1-SNAPSHOT.jar
 ```
 
## Passo a passo de como utilizar no NodeJs 💡🐻

1. Para podermos utilizar precisaremos criar o arquivo .env dentro do nosso projeto, nele ficará a parte de variaveis de ambiente da nossa aplicação
2. Acesse o site https://cloud.mongodb.com/ e crie sua conta por lá
3. Acessando sua conta crie um novo projeto e deixe o nome TDC - Testes e em add membros deixe como está no caso ele vai deixar você seu usuario de cadastro como owner
4. depois de criar clique na aba Network Access e clicando nele clica em Add IP Address e seleciona ALLOW ACCESS FROM ANYWHERE e clica em confirm
5. depois de criar clique na aba clica em Add New Database User e em Password Authentication coloque um user e passwoard que desejar
6. Clica na aba de DataBase clica em Create e seleciona o banco share, e clica em confirm, ele demora um pouco para carregar mas logo ja estará criado seu banco
7. Clica em Connect e logo em seguida seleciona connect your application e nele você  receberá na parte Add your connection string into your application code a url do nosso banco, copia e cola isso dentro do seu env dessa maneira: MONGO=<suaURL>
8. no .env coloque tambem PORT=8080
9. antes de iniciar rode o npm i ou npm install
10.Dentro do projeto vocês verão um arquivo chamado Marvel Universe.postman_collection.json com ele vocês conseguem importar no seu postman e utilizar as rotas desse projeto

## Passo a passo de como utilizar no Docker 💡🐳

1. Verifique que está com seu docker ligado no seu computador com o docker desktop
2. Para elevar o container basta colcocar o comando:  docker compose up
3. Para desativar os container: docker compose down

## Tecnologias usadas nesse projeto projeto 💻

- 🍃 [MongoDB](https://www.mongodb.com/pt-br)
- 💎 [SpringBoot](https://spring.io/projects/spring-boot)
- 🐳 [Docker](https://www.docker.com/)
- ☕️ [Java](https://www.java.com/pt-BR/)
- 🦌 [ELK](https://www.elastic.co/pt/what-is/elk-stack)
- 💌 [Postman](https://www.postman.com/)
- 🌼 [NodeJS](https://nodejs.org/en/)


## Sobre como eu montei essa API e conceitos de Back-end na parte de NodeJs 🦋

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQDDAJ5fxuiCWJIvtYbHIq-1K0PL3j2-1bhKGdNL-9bf_jgZ2txPqDPBHL5F_2iP5N4GHY&usqp=CAU)

https://www.youtube.com/watch?v=mZh4Wd_Ijxk&t=1s
