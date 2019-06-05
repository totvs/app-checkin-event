# *app-checkin-event*

# *_Este arquivo está em atualização_*  


## **_getListEvents_**  
>Webservice que fornece a listagem dos eventos referentes a agenda do evento Universo Totvs desenvolvido em TLPP utilizando o serviço REST atual nativo do AppServer.  

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
De acordo com as configurações, o serviço será exposto na URL  
http://localhost:8180/api/v1/events  
sendo necessário enviar o _GET_, conforme exemplo a seguir:

http://localhost:8180/api/v1/events/?CODIGO_EVENTO=000001&DESCRICAO=Description&NOME_EVENTO=nome

Sempre enviando os campos e o conteúdo a ser pesquisado.  
Caso seja enviado um _GET_ desta forma : http://localhost:8180/api/v1/events , serão pesquisados e listados todo o conteúdo da tabela.

## **_Licença_**
Copyright © 2019 by  **TOTVS**
