---
description: В этом разделе показано, как написать скрипт, использующий объект WinHttpRequest для доступа к данным с сервера, для которого требуется проверка подлинности HTTP.
ms.assetid: 9e46777c-4d79-4f9b-9b31-1280ed1e3289
title: Проверка подлинности с помощью скрипта
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81e2dec50ccf765239bbbd1d6a71c8f8fb2be0e4f70f2db5717b0072f0b62d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052102"
---
# <a name="authentication-using-script"></a>Проверка подлинности с помощью скрипта

В этом разделе показано, как написать скрипт, использующий объект [**WinHttpRequest**](winhttprequest.md) для доступа к данным с сервера, для которого требуется проверка подлинности HTTP.

-   [Необходимые условия и требования](#prerequisites-and-requirements)
-   [Доступ к веб-сайту с проверкой подлинности](#accessing-a-web-site-with-authentication)
-   [Проверка кодов состояния](#checking-the-status-codes)
-   [Связанные темы](#related-topics)

## <a name="prerequisites-and-requirements"></a>Необходимые условия и требования

в дополнение к опыту работы с Microsoft JScript, для этого примера требуется следующее:

-   текущая версия пакета средств разработки Microsoft Windows Software Development Kit (SDK).
-   средство настройки прокси-сервера для установки параметров прокси-сервера для служб Microsoft Windows HTTP (WinHTTP), если подключение к интернету осуществляется через прокси-сервер. Дополнительные сведения см. [ в разделеProxycfg.exe, средство настройки прокси-сервера](proxycfg-exe--a-proxy-configuration-tool.md) .
-   Знакомство с [терминологией](network-terminology.md) и концепциями сети.

## <a name="accessing-a-web-site-with-authentication"></a>Доступ к веб-сайту с проверкой подлинности

**Чтобы создать скрипт, демонстрирующий проверку подлинности, выполните следующие действия.**

1.  откройте текстовый редактор, например Microsoft Блокнот.
2.  Скопируйте следующий код в текстовый редактор после замены " \[ аусентикатионсите" на \] соответствующий текст, чтобы указать URL-адрес сайта, для которого требуется проверка подлинности HTTP.

    ```VB
    // Load the WinHttpRequest object.
    var WinHttpReq = 
              new ActiveXObject("WinHttp.WinHttpRequest.5.1");

    function getText1( )
    {
      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false;

      // Send a request to the server and wait for a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "No Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText);
      WScript.Echo( WinHttpReq.GetAllResponseHeaders);
      WScript.Echo( );
    };

    function getText2( )
    {
      // HttpRequest SetCredentials flags
      HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;

      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false );

      // Set credentials for server.
      WinHttpReq.SetCredentials( "User Name", 
                                 "Password",
                                 HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

      // It might also be necessary to supply credentials 
      // to the proxy if you connect to the Internet 
      // through a proxy that requires authentication.

      // Send a request to the server and wait for 
      // a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
      WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
      WScript.Echo( );
    };

    getText1( );
    getText2( );
    ```

    

3.  Сохраните файл как "Auth.js".
4.  В командной строке введите "cscript Auth.js" и нажмите клавишу ВВОД.

Теперь у вас есть программа, которая запрашивает ресурс двумя разными способами. Первый метод запрашивает ресурс, не указывая учетные данные. Возвращается код состояния 401, указывающий, что сервер требует проверки подлинности. Заголовки ответов также отображаются и должны выглядеть следующим образом:

``` syntax
Connection: Keep-Alive
Content-Length: 0
Date: Fri, 27 Apr 2001 01:47:18 GMT
Content-Type: text/html
Server: Microsoft-IIS/5.0
WWW-Authenticate: NTLM
WWW-Authenticate: Negotiate
Cache-control: private
```

Хотя ответ означает, что доступ к ресурсу был отклонен, он по-прежнему возвращает несколько заголовков, предоставляющих некоторую информацию о ресурсе. Заголовок с именем WWW-Authenticate указывает, что сервер требует проверки подлинности для этого ресурса. Если существовал заголовок с именем "Proxy-Authenticate", он указывает, что прокси-сервер требует проверки подлинности. Каждый заголовок проверки подлинности содержит доступную схему проверки подлинности и иногда область. Значение области учитывает регистр и определяет набор серверов или учетных записей-посредников, для которых должны приниматься одни и те же учетные данные.

Существует два заголовка с именем WWW-Authenticate, которые указывают, что поддерживаются несколько схем проверки подлинности. При вызове метода [**жетреспонсехеадер**](iwinhttprequest-getresponseheader.md) для поиска заголовков WWW-Authenticate метод возвращает только содержимое первого заголовка этого имени. В этом случае возвращается значение NTLM. Чтобы обеспечить обработку всех вхождений заголовка, используйте вместо этого метод [**жеталлреспонсехеадерс**](iwinhttprequest-getallresponseheaders.md) .

Второй вызов метода запрашивает тот же ресурс, но сначала предоставляет учетные данные для проверки подлинности путем вызова метода [**сеткредентиалс**](iwinhttprequest-setcredentials.md) . В следующем разделе кода показано, как используется этот метод.


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



Этот метод задает имя пользователя "UserName", пароль в "Password" и указывает, что учетные данные авторизации применяются к серверу ресурсов. Учетные данные проверки подлинности также могут отправляться на прокси-сервер.

Если указаны учетные данные, сервер возвращает код состояния 200, указывающий, что документ можно извлечь.

## <a name="checking-the-status-codes"></a>Проверка кодов состояния

Предыдущий пример — инструкции, но он требует, чтобы пользователь явно предоставил учетные данные. Приложение, которое предоставляет учетные данные при необходимости и не предоставляет учетные данные, если это не требуется. Чтобы реализовать функцию, которая делает это, необходимо изменить пример, чтобы проверить код состояния, возвращенный с ответом.

Полный список возможных кодов состояния, а также описания см. в разделе [**коды состояния HTTP**](http-status-codes.md). Однако в этом примере следует возникать только один из трех кодов. Код состояния 200 указывает, что ресурс доступен и отправляется с ответом. Код состояния 401 указывает на то, что сервер требует проверки подлинности. Код состояния 407 указывает на то, что прокси-сервер требует проверки подлинности.

Измените пример, созданный в последнем разделе, заменив функцию "getText2" следующим кодом (замените " \[ аусентикатионсите \] " собственным текстом, чтобы указать URL-адрес сайта, для которого требуется проверка подлинности HTTP):


```VB
function getText2() {
  WScript.Echo( "Credentials: " );

  // HttpRequest SetCredentials flags.
  HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
  HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

  // Specify the target resource.
  var targURL = "https://[authenticationSite]";
  WinHttpReq.open( "GET", targURL, false );

  var Done = false;
  var Attempts = 0;
  do
  {
    // Keep track of the number of request attempts.
    Attempts++;

    // Send a request to the server and wait for a response.
    WinHttpReq.send( );

    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status)
    {
      // A 200 status indicates that the resource was retrieved.
      case 200:
        Done = true;
        break;

      // A 401 status indicates that the server 
      // requires authentication.
      case 401:
        WScript.Echo( "Requires Server UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the server.
        WinHttpReq.SetCredentials( "User Name", 
                             "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        break;

      // A 407 status indicates that the proxy 
      // requires authentication.
      case 407:
        WScript.Echo( "Requires Proxy UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the proxy.
        WinHttpReq.SetCredentials( "User Name", 
                              "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_PROXY );
        break;
    }
  } while( ( !Done ) && ( Attempts < 3 ) );

  // Display the results of the request.
  WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
  WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
  WScript.Echo( );
};
```



Снова сохраните и запустите файл. Второй метод по-прежнему извлекает документ, но при необходимости предоставляет учетные данные. Функция "getText2" выполняет методы [**Open**](iwinhttprequest-open.md) и [**Send**](iwinhttprequest-send.md) , как если бы проверка подлинности не требовалась. Состояние извлекается со свойством [**Status**](iwinhttprequest-status.md) , а оператор switch реагирует на полученный код состояния. Если состояние равно 401 (сервер требует проверки подлинности) или 407 (прокси требует проверки подлинности), метод [**Open**](iwinhttprequest-open.md) выполняется снова. За ним следует метод [**сеткредентиалс**](iwinhttprequest-setcredentials.md) , который задает имя пользователя и пароль. Затем код перебирается обратно в метод [**Send**](iwinhttprequest-send.md) . Если после трех попыток не удается успешно получить ресурс, функция прекратит выполнение.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Проверка подлинности в WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[WinHttpRequest](winhttprequest.md)
</dt> <dt>

[**сеткредентиалс**](iwinhttprequest-setcredentials.md)
</dt> <dt>

[Запрос HTTP/1.1 для комментариев (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



