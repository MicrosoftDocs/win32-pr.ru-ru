---
description: Перед предоставлением доступа к ресурсам в Интернете некоторым серверам и прокси-службам HTTP требуется проверка подлинности. функции служб Microsoft Windows HTTP (WinHTTP) поддерживают проверку подлинности сервера и прокси для сеансов HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Проверка подлинности в WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810fadf470861b23ed2291bfa5665e1e429e86b7be77675f332267ee1d1c4de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052122"
---
# <a name="authentication-in-winhttp"></a>Проверка подлинности в WinHTTP

Перед предоставлением доступа к ресурсам в Интернете некоторым серверам и прокси-службам HTTP требуется проверка подлинности. функции служб Microsoft Windows HTTP (WinHTTP) поддерживают проверку подлинности сервера и прокси для сеансов HTTP.

## <a name="about-http-authentication"></a>Об аутентификации HTTP

Если требуется проверка подлинности, HTTP-приложение получает код состояния 401 (для сервера требуется проверка подлинности) или 407 (прокси требует проверки подлинности). Вместе с кодом состояния прокси или сервер отправляет один или несколько заголовков проверки подлинности: WWW-Authenticate (для проверки подлинности сервера) или Proxy-Authenticate (для проверки подлинности прокси).

Каждый заголовок проверки подлинности содержит поддерживаемую схему проверки подлинности, а для базовых и дайджест-схем — область. Если поддерживаются несколько схем проверки подлинности, сервер возвращает несколько заголовков с проверкой подлинности. Значение области учитывает регистр и определяет набор серверов или учетных записей-посредников, для которых принимаются одни и те же учетные данные. Например, если требуется проверка подлинности сервера, может возвращаться заголовок "WWW-Authenticate: Basic realm =", например "". Этот заголовок указывает, что для домена "example" должны быть указаны учетные данные пользователя.

Приложение HTTP может включать поле заголовка авторизации с запросом, который отправляется на сервер. Заголовок Authorization содержит схему проверки подлинности и соответствующий ответ, необходимый для этой схемы. Например, заголовок «Authorization: Basic \<username:password> » будет добавлен в запрос и отправлен на сервер, если клиент получил заголовок ответа «WWW-Authenticate: Basic realm =» example».

> [!Note]  
> Хотя они показаны в виде обычного текста, имя пользователя и пароль фактически кодируются в [*кодировке Base64*](glossary.md).

 

Существует два общих типа схем проверки подлинности:

-   Базовая схема проверки подлинности, в которой имя пользователя и пароль отправляются на сервер открытым текстом.

    Основная схема проверки подлинности основана на модели, которую клиент должен идентифицировать самостоятельно, указав имя пользователя и пароль для каждой области. Сервер служб запрашивается, только если запрос отправляется с заголовком авторизации, который содержит допустимые имя пользователя и пароль.

-   Схемы запросов и ответов, такие как Kerberos, в которых сервер запрашивает у клиента [*данные проверки подлинности*](glossary.md). Клиент преобразует данные с учетными данными пользователя и отправляет преобразованные данные обратно на сервер для проверки подлинности.

    Схемы "запрос — ответ" обеспечивают более безопасную проверку подлинности. В схеме "запрос — ответ" имя пользователя и пароль никогда не передаются по сети. После того как клиент выберет схему "запрос — ответ", сервер возвращает соответствующий код состояния с запросом, содержащим [*данные проверки подлинности*](glossary.md) для этой схемы. Затем клиент повторно отправляет запрос с правильным ответом для получения запрошенной службы. Схемы "запрос — ответ" могут выполнять несколько обменов.

Следующая таблица содержит схемы проверки подлинности, поддерживаемые WinHTTP, типом проверки подлинности и описанием схемы.



| Схема            | Тип               | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Базовый (обычный текст) | Basic              | Использует строку в [*кодировке Base64*](glossary.md) , содержащую имя пользователя и пароль.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Digest (дайджест)            | Запрос-ответ | Проблемы с использованием nonce (определяемой сервером строки данных). Допустимый ответ содержит контрольную сумму имени пользователя, пароля, заданного значения nonce, [*HTTP-команды*](glossary.md)и запрошенного универсального кода ресурса (URI).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NTLM              | Запрос-ответ | Требует, чтобы [*данные проверки подлинности*](glossary.md) были преобразованы с учетными данными пользователя для подтверждения личности. Для правильной работы проверки подлинности NTLM в одном и том же соединении необходимо выполнить несколько обменов. Поэтому проверка подлинности NTLM не может быть использована, если промежуточный прокси-сервер не поддерживает подключения, поддерживающие проверку активности. Проверка подлинности NTLM также завершается ошибкой, если [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) используется с флагом проверки [**\_ \_ \_ активности WinHTTP**](option-flags.md) , который отключает семантику проверки активности.                                                                                                                                                                                                                                       |
| Паспорт          | Запрос-ответ | Использует [Microsoft Passport 1,4](passport-authentication-in-winhttp.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Согласование         | Запрос-ответ | если сервер и клиент используют Windows 2000 или более поздней версии, используется проверка подлинности Kerberos. В противном случае используется проверка подлинности NTLM. протокол Kerberos доступен в Windows 2000 и более поздних операционных системах и считается более безопасным, чем проверка подлинности NTLM. Для правильной работы проверки подлинности в одном и том же соединении необходимо выполнить несколько обменов. Таким образом, проверка подлинности Negotiate не может быть использована, если промежуточный прокси-сервер не поддерживает подключения, поддерживающие проверку активности. Согласование проверки подлинности также завершается сбоем, если [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) используется с флагом проверки [**\_ \_ \_ активности WinHTTP**](option-flags.md) , который отключает семантику сохранения активности. схема проверки подлинности Negotiate иногда называется встроенной проверкой подлинности Windows. |



 

## <a name="authentication-in-winhttp-applications"></a>Проверка подлинности в приложениях WinHTTP

Интерфейс прикладного программирования (API) WinHTTP предоставляет две функции, используемые для доступа к Интернет-ресурсам в ситуациях, когда требуется проверка подлинности: [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) и [**винхттпкуеряуссчемес**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).

При получении ответа с кодом состояния 401 или 407 можно использовать [**винхттпкуеряуссчемес**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) для анализа заголовков проверки подлинности, чтобы определить поддерживаемые схемы проверки подлинности и целевой объект проверки подлинности. Целевой объект проверки подлинности — это сервер или прокси, который запрашивает проверку подлинности. **Винхттпкуеряуссчемес** также определяет первую схему проверки подлинности из доступных схем на основе настроек схемы проверки подлинности, предлагаемых сервером. Этот метод выбора схемы проверки подлинности — это поведение, предлагаемое [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

[**Винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) позволяет приложению указать схему проверки подлинности, которая используется вместе с допустимыми именем пользователя и паролем для использования на целевом сервере или прокси-сервер. После настройки учетных данных и повторной отправки запроса необходимые заголовки создаются и добавляются в запрос автоматически. Поскольку некоторым схемам проверки подлинности требуется несколько транзакций, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) может возвращать ошибку, ошибка \_ \_ запроса повторной отправки WinHTTP \_ . При возникновении этой ошибки приложение должно продолжать повторно отправить запрос, пока не будет получен ответ, не содержащий код состояния 401 или 407. Код состояния 200 указывает, что ресурс доступен и запрос выполнен успешно. Дополнительные коды состояния, которые могут быть возвращены, см. в разделе [**коды состояния HTTP**](http-status-codes.md) .

Если допустимая схема проверки подлинности и учетные данные известны до отправки запроса на сервер, приложение может вызвать [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) перед вызовом [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). В этом случае WinHTTP пытается выполнить предварительную проверку подлинности на сервере, предоставляя учетные данные или [*данные проверки подлинности*](glossary.md) в исходном запросе к серверу. Предварительная проверка подлинности может уменьшить количество обменов в процессе проверки подлинности и, таким образом, повысить производительность приложения.

Предварительная проверка подлинности может использоваться со следующими схемами проверки подлинности:

-   Basic — всегда возможно.
-   Согласованное разрешение в Kerberos — очень вероятно, возможно; Единственным исключением является то, что неравномерное распределение времени между клиентом и контроллером домена.
-   (Согласование разрешения в NTLM) — никогда не поддерживается.
-   NTLM — возможно только в Windows Server 2008 R2.
-   Дайджест — никогда не поддерживается.
-   Passport — никогда не поддерживается; После первоначального ответа на запрос служба WinHTTP использует файлы cookie для предварительной проверки подлинности в Passport.

Стандартное приложение WinHTTP выполняет следующие действия, чтобы обеспечить проверку подлинности.

-   Запросите ресурс с помощью [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) и [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).
-   Проверьте заголовки ответа с помощью [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).
-   Если возвращается код состояния 401 или 407, указывающий на необходимость проверки подлинности, вызовите [**винхттпкуеряуссчемес**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) , чтобы найти допустимую схему.
-   Задайте схему проверки подлинности, имя пользователя и пароль с помощью [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).
-   Повторно отправьте запрос с тем же маркером запроса, вызвав [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

Учетные данные, установленные [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) , используются только для одного запроса. Служба WinHTTP не кэширует учетные данные для использования в других запросах. Это означает, что приложения должны быть написаны, которые могут отвечать на несколько запросов. Если подключение с проверкой подлинности используется повторно, другие запросы могут быть не вызваны, но ваш код должен иметь возможность отвечать на запросы в любое время.

### <a name="example-retrieving-a-document"></a>Пример. получение документа

Следующий пример кода пытается получить указанный документ с HTTP-сервера. Код состояния извлекается из ответа, чтобы определить, требуется ли проверка подлинности. Если код состояния 200 найден, документ становится доступным. Если обнаружен код состояния 401 или 407, для извлечения документа требуется проверка подлинности. Для любого другого кода состояния выводится сообщение об ошибке. Список возможных кодов состояния см. в разделе [**коды состояния HTTP**](http-status-codes.md) .


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a>Политика автоматического входа в систему

Политика автоматического входа в систему (автоматический вход в систему) определяет, когда служба WinHTTP может включать в запрос учетные данные по умолчанию. Учетные данные по умолчанию — это либо текущий маркер потока, либо маркер сеанса, в зависимости от того, используется ли WinHTTP в синхронном или асинхронном режиме. Токен потока используется в синхронном режиме, а маркер сеанса используется в асинхронном режиме. Эти учетные данные по умолчанию часто являются именем пользователя и паролем, используемыми для входа в Microsoft Windows.

Политика автоматического входа была реализована, чтобы предотвратить случайное использование этих учетных данных для проверки подлинности на недоверенном сервере. По умолчанию для уровня безопасности задано значение уровень \_ безопасности автоматического входа WinHTTP \_ \_ \_ Medium, что позволяет использовать учетные данные по умолчанию только для запросов в интрасети. Политика автоматического входа применяется только к схемам проверки подлинности NTLM и Negotiate. Учетные данные никогда не передаются автоматически с другими схемами.

Политику автоматического входа можно задать с помощью функции [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с флагом WinHTTP для [**\_ параметра \_ Autologon \_**](option-flags.md) . Этот флаг применяется только к обработчику запроса. Если для политики задано значение \_ \_ низкий уровень безопасности автоматического входа WinHTTP \_ \_ , учетные данные по умолчанию могут отправляться на все серверы. Если для политики задано значение \_ \_ высокий уровень безопасности автоматического входа WinHTTP \_ \_ , учетные данные по умолчанию нельзя использовать для проверки подлинности. Настоятельно рекомендуется использовать автоматический вход на среднем уровне.

## <a name="stored-user-names-and-passwords"></a>Сохранение имен пользователей и паролей

Windows В XP появилась концепция сохраненных имен пользователей и паролей. Если учетные данные пользователя Passport сохраняются с помощью **мастера регистрации паспорта** или стандартного **диалогового окна учетных данных**, они сохраняются в сохраненных именах пользователей и паролях. при использовании winhttp в Windows XP или более поздней версии winhttp автоматически использует учетные данные в сохраненных именах пользователей и паролях, если учетные данные не заданы явно. Это похоже на поддержку учетных данных входа по умолчанию для NTLM/Kerberos. Однако использование учетных данных паспорта по умолчанию не подчиняется параметрам политики автоматического входа.

 

 



