---
description: 'WinHTTP реализует протокол WPAD с помощью функции WinHttpGetProxyForUrl и двух вспомогательных служебных функций: Винхттпдетектаутопроксиконфигурл и Винхттпжетиепроксиконфигфоркуррентусер.'
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: Функции автопрокси WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8443567e12d7a0f3b75d09fc284dc634315ec635ff8b630821bb84031e39781b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955714"
---
# <a name="winhttp-autoproxy-functions"></a>Функции автопрокси WinHTTP

WinHTTP реализует протокол WPAD с помощью функции [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) и двух вспомогательных служебных функций: [**винхттпдетектаутопроксиконфигурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) и [**винхттпжетиепроксиконфигфоркуррентусер**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

Поддержка автопрокси не полностью интегрирована в стек HTTP в WinHTTP. Перед отправкой запроса приложение должно вызвать [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) для получения имени прокси-сервера, а затем вызвать [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с помощью **\_ \_ прокси-сервера параметров WinHTTP** , чтобы задать конфигурацию прокси-сервера для маркера запроса WinHTTP, созданного с помощью [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).

Функция [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) может выполнять все три шага протокола WPAD, как описано в предыдущем обзоре: (1) обнаружение URL-адреса PAC, (2) скачивание файла скрипта PAC, (3) выполнение кода скрипта и возврат конфигурации прокси-сервера в **структуре \_ \_ сведений о прокси-сервере WinHTTP** . При необходимости, если приложение заранее знает URL-адрес PAC, его можно указать как **WinHttpGetProxyForUrl**.

В следующем примере кода используется автопрокси. Он настраивает HTTP-запрос GET, сначала создавая обработчики соединения и подключения сеанса WinHTTP. В [](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) вызове WinHttpOpen **указан \_ тип доступа WinHTTP \_ \_ No \_ proxy** для конфигурации начального прокси-сервера, чтобы указать, что по умолчанию запросы отправляются непосредственно на целевой сервер. Используя автопрокси, он задает конфигурацию прокси-сервера непосредственно в обработчике запроса.


```C++
  HINTERNET hHttpSession = NULL;
  HINTERNET hConnect     = NULL;
  HINTERNET hRequest     = NULL;
  
  WINHTTP_AUTOPROXY_OPTIONS  AutoProxyOptions;
  WINHTTP_PROXY_INFO         ProxyInfo;
  DWORD                      cbProxyInfoSize = sizeof(ProxyInfo);
  
  ZeroMemory( &AutoProxyOptions, sizeof(AutoProxyOptions) );
  ZeroMemory( &ProxyInfo, sizeof(ProxyInfo) );
  
//
// Create the WinHTTP session.
//
  hHttpSession = WinHttpOpen( L"WinHTTP AutoProxy Sample/1.0",
                              WINHTTP_ACCESS_TYPE_NO_PROXY,
                              WINHTTP_NO_PROXY_NAME,
                              WINHTTP_NO_PROXY_BYPASS,
                              0 );
  
// Exit if WinHttpOpen failed.
  if( !hHttpSession )
    goto Exit;
  
//
// Create the WinHTTP connect handle.
//
  hConnect = WinHttpConnect( hHttpSession,
                             L"www.microsoft.com",
                             INTERNET_DEFAULT_HTTP_PORT,
                             0 );
  
// Exit if WinHttpConnect failed.
  if( !hConnect )
    goto Exit;
  
//
// Create the HTTP request handle.
//
  hRequest = WinHttpOpenRequest( hConnect,
                                 L"GET",
                                 L"ms.htm",
                                 L"HTTP/1.1",
                                 WINHTTP_NO_REFERER,
                                 WINHTTP_DEFAULT_ACCEPT_TYPES,
                                 0 );
  
// Exit if WinHttpOpenRequest failed.
  if( !hRequest )
    goto Exit;
  
//
// Set up the autoproxy call.
//

// Use auto-detection because the Proxy 
// Auto-Config URL is not known.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_AUTO_DETECT;

// Use DHCP and DNS-based auto-detection.
  AutoProxyOptions.dwAutoDetectFlags = 
                             WINHTTP_AUTO_DETECT_TYPE_DHCP |
                             WINHTTP_AUTO_DETECT_TYPE_DNS_A;

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If 
// auto-proxy succeeds, then set the proxy info on the 
// request handle. If auto-proxy fails, ignore the error 
// and attempt to send the HTTP request directly to the 
// target server (using the default WINHTTP_ACCESS_TYPE_NO_PROXY 
// configuration, which the requesthandle will inherit 
// from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo))
  {
  // A proxy configuration was found, set it on the
  // request handle.
    
    if( !WinHttpSetOption( hRequest, 
                           WINHTTP_OPTION_PROXY,
                           &ProxyInfo,
                           cbProxyInfoSize ) )
    {
      // Exit if setting the proxy info failed.
      goto Exit;
    }
  }

//
// Send the request.
//
  if( !WinHttpSendRequest( hRequest,
                           WINHTTP_NO_ADDITIONAL_HEADERS,
                           0,
                           WINHTTP_NO_REQUEST_DATA,
                           0,
                           0,
                           NULL ) )
  {
    // Exit if WinHttpSendRequest failed.
    goto Exit;
  }

//
// Wait for the response.
//

  if( !WinHttpReceiveResponse( hRequest, NULL ) )
    goto Exit;

//
// A response has been received, then process it.
// (omitted)
//


  Exit:
  //
  // Clean up the WINHTTP_PROXY_INFO structure.
  //
    if( ProxyInfo.lpszProxy != NULL )
      GlobalFree(ProxyInfo.lpszProxy);

    if( ProxyInfo.lpszProxyBypass != NULL )
      GlobalFree( ProxyInfo.lpszProxyBypass );

  //
  // Close the WinHTTP handles.
  //
    if( hRequest != NULL )
      WinHttpCloseHandle( hRequest );
  
    if( hConnect != NULL )
      WinHttpCloseHandle( hConnect );
  
    if( hHttpSession != NULL )
      WinHttpCloseHandle( hHttpSession );

```



В приведенном примере кода вызов [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) предписывает функции автоматически обнаружить файл автоматической настройки прокси-сервера, указав флаг **\_ \_ автоматического \_ определения автопрокси WinHTTP** в структуре [**\_ \_ параметров автопрокси WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) . Использование флага **\_ \_ автоматического \_ определения автопрокси WinHTTP** требует, чтобы в коде был указан один или оба флага автоматического обнаружения (**\_ \_ тип автоматического обнаружения WinHTTP \_ \_ DHCP**, **\_ \_ тип автоматического обнаружения \_ \_ \_ WinHTTP**). В примере кода используется функция автоматического обнаружения **WinHttpGetProxyForUrl** , так как URL-адрес PAC заранее не известен. Если URL-адрес PAC не удается найти в сети в этом сценарии, **WinHttpGetProxyForUrl** завершается неудачей ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку \_ \_ автообнаружение \_ WinHTTP**).

## <a name="if-the-pac-url-is-known-in-advance"></a>Если URL-адрес PAC известен заранее

Если в приложении известен URL-адрес PAC, он может указать его в \_ структуре параметров АВТОПРОКСИ WinHTTP \_ и настроить [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) для пропуска этапа автоматического обнаружения.

Например, если файл PAC доступен в локальной сети по URL-адресу, https://InternalSite/proxy-config.pac то вызов [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) будет выглядеть следующим образом.


```C++
//
// Set up the autoproxy call.
//

// The proxy auto-config URL is known. Auto-detection
// is not required.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_CONFIG_URL;

// Set the proxy auto-config URL.
  AutoProxyOptions. lpszAutoConfigUrl =  L"https://InternalSite/proxy-config.pac";

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If auto-proxy
// succeeds, then set the proxy info on the request handle.
// If auto-proxy fails, ignore the error and attempt to send the
// HTTP request directly to the target server (using the default
// WINHTTP_ACCESS_TYPE_NO_PROXY configuration, which the request
// handle will inherit from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo ) )
{
  //...

```



Если в [**структуре \_ \_ параметров автопрокси WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) заданы флаги **\_ \_ \_ АВТОопределения** и **\_ \_ \_ URL-адреса** автоматической проверки прокси WinHTTP (и заданы флаги Auto-детктион и URL-адрес автоматической настройки), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) First пытается автоматически определить, а затем, если автоматическое обнаружение не может найти URL-адрес PAC, "перейдет на URL-адрес автоматической настройки, предоставленный приложением.

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a>Функция Винхттпдетектаутопроксиконфигурл

Функция [**винхттпдетектаутопроксиконфигурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) реализует подмножество протокола WPAD: пытается автоматически определить URL-адрес для файла автоматической конфигурации прокси-сервера, не загружая или не выполняя файл PAC. Эта функция полезна в особых ситуациях, когда веб-клиентское приложение должно выполнять загрузку и выполнение файла PAC.

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a>Функция Винхттпжетиепроксиконфигфоркуррентусер

Функция [**винхттпжетиепроксиконфигфоркуррентусер**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) возвращает текущие параметры прокси-сервера Internet Explorer для текущего активного сетевого подключения без вызова "WinInet.dll". Эта функция полезна только при вызове в процессе, который выполняется от имени интерактивной учетной записи пользователя, так как в противном случае конфигурация прокси-сервера Internet Explorer, скорее всего, будет недоступна. Например, не рекомендуется вызывать эту функцию из DLL ISAPI, выполняющегося в процессе службы IIS. Дополнительные сведения и сценарий, в котором приложение на основе WinHTTP будет использовать **винхттпжетиепроксиконфигфоркуррентусер**, см. в разделе [Обнаружение без файла автоматической настройки](discovery-without-an-auto-config-file.md).

 

 
