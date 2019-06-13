# *app-checkin-event*

# *_Este arquivo está em atualização_*  

## **_getListEvents_**  
>Webservice que fornece a listagem dos eventos referentes a agenda do evento Universo Totvs desenvolvido na linguagemmm TLPP utilizando o serviço REST atual nativo do AppServer.  

## **_Configurações (event.yaml)_** 
Realizaremos a criação do container com o appserver, e a partir das variáveis de ambiente do sistema operacional descritas a seguir, que deverão ser informadas na seção ``environment`` de cada serviço, será possível configurá-los conforme a estrutura desejada.

###### AppServer (appserver.ini)
Será criado automaticamente no diretório ``/totvs/tec/appserver``

>``
"APPSERVER_019=[TCP]PORT=PORTA_SERVER"
``
>``
"APPSERVER_009=[TLF]DBDATABASE=BANCO"
``
>``
"APPSERVER_010=[TLF]DBSERVER=IP_DBACESS"
``
>``
"APPSERVER_011=[TLF]DBALIAS=NOME_ODBC"
``
>``
"APPSERVER_012=[TLF]DBPORT=PORTA_DBACCESS"
``
>``
"APPSERVER_036=[HTTP_9080]port=PORTA_REST"
``
>``
"APPSERVER_044=[THREAD_POOL_01]Threads=NUMERO_THREADS"
``

###### DbAccess (dbaccess.ini)
Será criado automaticamente no diretório ``/totvs/tec/dbaccess/multi``
>``
"DBACCESS_023=[BANCO_DE_DADOS]environments=NOME_ODBC"
``
>``
"DBACCESS_026=[BANCO_DE_DADOS/NOME_ODBC]user=USUARIO_DO_BANCO_DE_DADOS"
``
>``
"DBACCESS_027=[BANCO_DE_DADOS/NOME_ODBC]password=SENHA_DO_BANCO_DE_DADOS"
``

###### ODBC (odbc.ini)
Será criado automaticamente no diretório ``/etc``
>``
"ODBC_POSTGRES_001=[NOME_ODBC]Servername=IP_SERVIDOR_BANCO_DE_DADOS"
``
>``
"ODBC_POSTGRES_002=[NOME_ODBC]Username=USUARIO_BANCO_DE_DADOS"
``
>``
"ODBC_POSTGRES_004=[NOME_ODBC]Database=NOME_BANCO_DE_DADOS"
``
>``
"ODBC_POSTGRES_003=[NOME_ODBC]Password=SENHA_BANCO_DE_DADOS"
``
>``
"ODBC_POSTGRES_006=[NOME_ODBC]Port=PORTA_BANCO_DE_DADOS"
``

#####NOTA
> Para subir a aplicação respondendo para um banco de dados diferente do ``POSTGRES``, é necesário criar novas variáveis de ambiente, por exemplo:
``ODBC_MSSQL_001=[NOME_ODBC]Servername=IP_SERVIDOR_BANCO_DE_DADOS``

## **_Subindo o Serviço_** 
Executar o comando via ``docker-compose``
>``
docker-compose -f event.yaml up -d
``

## **_Enviando para o Endpoint_** 
De acordo com as configurações, o serviço responde no seguinte endpoint: 
``/api/v1/event``
Como se trata de um serviço do tipo _GET_ onde foi adotada a convenção ``pathParam`` e a _URI_ deve ser enviada conforme exemplo:  

``http://localhost:8180/api/v1/event/?event_code=000001&description=Description&event_name=name``

Quando necessário efetuar alguma seleção de dados, deve ser enviado os campos e o conteúdo a ser pesquisado conforme descrito para evitar erros no retorno na aplicação.  
Caso seja enviado uma  _URI_ desta forma : ``http://localhost:8180/api/v1/event`` , será listado todo o conteúdo da tabela ``events``.

## **_Licença_**
Copyright © 2019 by  **TOTVS**
