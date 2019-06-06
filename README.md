# *app-checkin-event*

# *_Este arquivo está em atualização_*  

## **_getListEvents_**  
>Webservice que fornece a listagem dos eventos referentes a agenda do evento Universo Totvs desenvolvido na linguagemmm TLPP utilizando o serviço REST atual nativo do AppServer.  

## **_Modo de uso_**  
>????
  

## **_Configurações (verificar)_**  
>???

```
Bloco de código:  
    {
      }
```  


**OBS: Deve ser alterado de acordo com o banco criado.**

## **_Subindo o Serviço_**  
Para subirmos o serviço, basta executar ???

## **_Enviando para o Endpoint_** 
De acordo com as configurações, o serviço responde no seguinte endpoint:  
**_/api/v1/event_**  
Como se trata de um serviço do tipo _GET_ onde foi adotada a convenção **pathParam** e a _URI_ deve ser enviada conforme exemplo:  

http://localhost:8180/api/v1/event/?event_code=000001&description=Description&event_name=name

Quando necessário efetuar alguma seleção de dados, deve ser enviado os campos e o conteúdo a ser pesquisado conforme descrito para evitar erros no retorno na aplicação.  
Caso seja enviado uma  _URI_ desta forma : http://localhost:8180/api/v1/event , será listado todo o conteúdo da tabela **_events_**.

## **_Licença_**
Copyright © 2019 by  **TOTVS**
