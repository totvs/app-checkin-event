# app-checkin-event
Tlpp List Events :: Eventos
Webservice que fornece a listagem dos eventos referentes a agenda do evento Universo Totvs.

Modo de uso
Incluir a biblioteca como dependência no pom.xml da aplicação:

<dependency>
    <groupId>com.totvs.tjf</groupId>
    <artifactId>tjf-checkin-signup</artifactId>
    <version>0.0.1-SNAPSHOT</version>
</dependency>
Configurações (application.yml)
No arquivo de configurações src/main/resources/application.yml teremos configurado as informações do banco de dados (PostgreSQL):

spring:
  datasource:
    driver-class-name: org.postgresql.Driver
    url: jdbc:postgresql://localhost:5432/checkin
    username: checkin
    password: checkin!123
OBS: Deve ser alterado de acordo com o banco criado.

Subindo o Serviço
Para subirmos o serviço, basta executar como Spring Boot App.

Enviando para o Endpoint
De acordo com as configurações, o serviço será exposto na URL http://localhost:8180/api/v1/checkin, sendo necessário enviar um POST, conforme exemplo a seguir:

{
	"email": "participante@email.com",
	"code_event": "CódigoDoEvento",
	"date":"2019-06-04T00:00:00Z"
}
Os campos email e code_event são do tipo texto (String) e são obrigatórios.
Validações
O serviço valida caso o mesmo Email já tenha sido informado no evento.

Licença
Copyright © 2019 by TOTVS
