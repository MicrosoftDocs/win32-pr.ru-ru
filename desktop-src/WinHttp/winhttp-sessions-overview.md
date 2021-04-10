---
description: Службы Microsoft Windows HTTP (WinHTTP) предоставляют набор функций C/C++, позволяющих приложению получать доступ к ресурсам HTTP в Интернете. В этом разделе приводятся общие сведения о том, как эти функции используются для взаимодействия с HTTP-сервером.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Общие сведения о сеансах WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145163"
---
# <a name="winhttp-sessions-overview"></a>Общие сведения о сеансах WinHTTP

Службы Microsoft Windows HTTP (WinHTTP) предоставляют набор функций C/C++, позволяющих приложению получать доступ к ресурсам HTTP в Интернете. В этом разделе приводятся общие сведения о том, как эти функции используются для взаимодействия с HTTP-сервером.

-   [Использование API WinHTTP для доступа к веб-службам](#using-the-winhttp-api-to-access-the-web)
-   [Инициализация WinHTTP](#initializing-winhttp)
-   [Открытие запроса](#opening-a-request)
-   [Добавление заголовков запроса](#adding-request-headers)
-   [Отправка запроса](#sending-a-request)
-   [Отправка данных на сервер](#posting-data-to-the-server)
-   [Получение сведений о запросе](#getting-information-about-a-request)
-   [Загрузка ресурсов из Интернета](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a>Использование API WinHTTP для доступа к веб-службам

На следующей схеме показан порядок, в котором функции WinHTTP обычно вызываются при взаимодействии с HTTP-сервером. Затененные поля представляют функции, которые создают дескриптор [хинтернет](hinternet-handles-in-winhttp.md) , а обычные поля представляют функции, использующие эти дескрипторы.

![функции, создающие дескрипторы](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a>Инициализация WinHTTP

Перед взаимодействием с сервером необходимо инициализировать WinHTTP с помощью вызова [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) создает контекст сеанса для сохранения сведений об HTTP-сеансе и возвращает маркер сеанса. С помощью этого маркера функция [**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) может указать целевой сервер HTTP или протокол HTTPS.

> [!Note]  
> Вызов [**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) не приводит к фактическому подключению к HTTP-серверу до тех пор, пока не будет выполнен запрос к определенному ресурсу.

 

## <a name="opening-a-request"></a>Открытие запроса

Функция [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) открывает HTTP-запрос для определенного ресурса и возвращает маркер [хинтернет](hinternet-handles-in-winhttp.md) , который может использоваться другими функциями HTTP. [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) не отправляет запрос на сервер при вызове. Функция [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) на самом деле устанавливает подключение по сети и отправляет запрос.

В следующем примере показан пример вызова [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , в котором используются параметры по умолчанию.

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a>Добавление заголовков запроса

Функция [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) позволяет приложению добавлять в обработчик HTTP-запросов дополнительные заголовки запросов свободного формата. Он предназначен для использования сложными приложениями, требующими точного контроля над запросами, отправленными на HTTP-сервер.

Функции [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) требуется обработчик HTTP-запроса, созданный [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), строка, содержащая заголовки, длину заголовков и любые модификаторы.

С [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)можно использовать следующие модификаторы.



| Модификатор                                                                                         | Описание                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Добавление флага аддрек WinHTTP \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | Добавляет заголовок, если он не существует. Используется с [**\_ \_ флагом WinHTTP аддрек \_ Replace**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).                                                                                                                                                                                                               |
| [**\_флаг АДДРЕК \_ WinHTTP \_ Добавить, \_ Если \_ новый**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | Добавляет заголовок, только если он еще не существует; в противном случае возвращается ошибка.                                                                                                                                                                                                                                                           |
| [**\_ \_ объединение флагов WinHTTP аддрек \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | Объединяет заголовки с одним и тем же именем.                                                                                                                                                                                                                                                                                                              |
| [**\_ \_ объединение флага аддрек WinHTTP \_ \_ с \_ запятой**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | Объединяет заголовки с одним и тем же именем с помощью запятой. Например, добавление "Accept: Text/ \* " с последующим "Accept: Audio/ \* " с этим флагом образует один заголовок "Accept: Text/ \* , Audio/ \* ", что приводит к объединению первого заголовка. Для обеспечения согласованной схемы с объединенными и разделенными заголовками используется вызывающее приложение. |
| [**\_ \_ объединение флагов WinHTTP аддрек \_ \_ с \_ точкой с запятой**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | Объединяет заголовки с одним и тем же именем с помощью точки с запятой.                                                                                                                                                                                                                                                                                            |
| [**\_ \_ Замена флага аддрек WinHTTP \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | Заменяет или удаляет заголовок. Если значение заголовка пусто и заголовок найден, он удаляется. Если значение заголовка не пустое, значение заголовка заменяется.                                                                                                                                                                            |



 

## <a name="sending-a-request"></a>Отправка запроса

Функция [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) устанавливает соединение с сервером и отправляет запрос на указанный сайт. Для этой функции требуется обработчик [хинтернет](hinternet-handles-in-winhttp.md) , созданный [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) также может передавать дополнительные заголовки или дополнительные сведения. Необязательные сведения обычно используются для операций, которые записывают сведения на сервер, такие как операции размещения и POST.

После того как функция [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) отправит запрос, приложение может использовать функции [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) и [**винхттпкуеридатааваилабле**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) в обработчике [хинтернет](hinternet-handles-in-winhttp.md) для загрузки ресурсов сервера.

## <a name="posting-data-to-the-server"></a>Отправка данных на сервер

Для отправки данных на сервер [*HTTP-команда*](glossary.md) в вызове [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) должна быть либо POST, либо помещается. При вызове [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) параметр *двтоталленгс* должен быть установлен равным размеру данных в байтах. Затем используйте [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) для передачи данных на сервер.

Кроме того, можно присвоить параметру *Лпоптионал* [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) адрес буфера, содержащего данные, которые должны быть отправлены на сервер. При использовании этого метода необходимо установить оба параметра *двоптионалленгс* и *двтоталленгс* в [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) в качестве размера публикуемых данных. Вызов [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) таким образом устраняет необходимость вызова [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).

## <a name="getting-information-about-a-request"></a>Получение сведений о запросе

Функция [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) позволяет приложению получать сведения о HTTP-запросе. Функции требуется обработчик [хинтернет](hinternet-handles-in-winhttp.md) , созданный [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), значение информационного уровня и длина буфера. [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) также принимает буфер, в котором хранятся данные, и индекс заголовков, начинающийся с нуля, который перечисляет несколько заголовков с одним и тем же именем.

Используйте любое из значений уровня информации на странице « [**Флаги сведений о запросе**](query-info-flags.md) » с модификатором для управления форматом, в котором данные хранятся в параметре *лпвбуффер* [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).

## <a name="downloading-resources-from-the-web"></a>Загрузка ресурсов из Интернета

После открытия запроса с помощью функции [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , отправки ее на сервер с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)и подготовки обработчика запросов к получению ответа с помощью [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), приложение может использовать функции [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) и [**винхттпкуеридатааваилабле**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) для загрузки ресурса с HTTP-сервера.

В следующем примере кода показано, как скачать ресурс с семантикой защищенных транзакций. В примере кода инициализируется программный интерфейс (API) WinHTTP, выбирается целевой HTTPS-сервер, а затем открывается и отправляется запрос для этого защищенного ресурса. [**Винхттпкуеридатааваилабле**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) используется с обработчиком запросов для определения объема данных, доступных для загрузки, а затем для считывания этих данных используется [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) . Этот процесс повторяется до тех пор, пока не будет получен и отображен весь документ.


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



