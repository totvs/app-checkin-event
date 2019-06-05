# *app-checkin-event*

# *_Este arquivo est� em atualiza��o_*  


## **_getListEvents_**  
>Webservice que fornece a listagem dos eventos referentes a agenda do evento Universo Totvs desenvolvido em TLPP utilizando o servi�o REST atual nativo do AppServer.  

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
De acordo com as configura��es, o servi�o ser� exposto na URL  
http://localhost:8180/api/v1/events  
sendo necess�rio enviar o _GET_, conforme exemplo a seguir:

http://localhost:8180/api/v1/events/?CODIGO_EVENTO=000001&DESCRICAO=Description&NOME_EVENTO=nome

Sempre enviando os campos e o conte�do a ser pesquisado.  
Caso seja enviado um _GET_ desta forma : http://localhost:8180/api/v1/events , ser�o pesquisados e listados todo o conte�do da tabela.

## **_Licen�a_**
Copyright � 2019 by  **TOTVS**
