# *app-checkin-event*

# *_Este arquivo est� em atualiza��o_*  

## **_getListEvents_**  
>Webservice que fornece a listagem dos eventos referentes a agenda do evento Universo Totvs desenvolvido na linguagemmm TLPP utilizando o servi�o REST atual nativo do AppServer.  

## **_Modo de uso_**  
>????
  

## **_Configura��es (verificar)_**  
>???

```
Bloco de c�digo:  
    {
      }
```  


**OBS: Deve ser alterado de acordo com o banco criado.**

## **_Subindo o Servi�o_**  
Para subirmos o servi�o, basta executar ???

## **_Enviando para o Endpoint_** 
De acordo com as configura��es, o servi�o responde no seguinte endpoint:  
**_/api/v1/event_**  
Como se trata de um servi�o do tipo _GET_ onde foi adotada a conven��o **pathParam** e a _URI_ deve ser enviada conforme exemplo:  

http://localhost:8180/api/v1/event/?event_code=000001&description=Description&event_name=name

Quando necess�rio efetuar alguma sele��o de dados, deve ser enviado os campos e o conte�do a ser pesquisado conforme descrito para evitar erros no retorno na aplica��o.  
Caso seja enviado uma  _URI_ desta forma : http://localhost:8180/api/v1/event , ser� listado todo o conte�do da tabela **_events_**.

## **_Licen�a_**
Copyright � 2019 by  **TOTVS**
