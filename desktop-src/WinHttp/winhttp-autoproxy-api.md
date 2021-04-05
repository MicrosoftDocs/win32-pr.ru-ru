---
description: 'WinHTTP реализует протокол WPAD с помощью функции WinHttpGetProxyForUrl и двух вспомогательных служебных функций: Винхттпдетектаутопроксиконфигурл и Винхттпжетиепроксиконфигфоркуррентусер.'
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: Функции автопрокси WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd4cf8289add4c72c2266df4bb9025e0b4c1aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991126"
---
# <a name="winhttp-autoproxy-functions"></a><span data-ttu-id="ee07f-103">Функции автопрокси WinHTTP</span><span class="sxs-lookup"><span data-stu-id="ee07f-103">WinHTTP AutoProxy Functions</span></span>

<span data-ttu-id="ee07f-104">WinHTTP реализует протокол WPAD с помощью функции [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) и двух вспомогательных служебных функций: [**винхттпдетектаутопроксиконфигурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) и [**винхттпжетиепроксиконфигфоркуррентусер**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span><span class="sxs-lookup"><span data-stu-id="ee07f-104">WinHTTP implements the WPAD protocol using the [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function along with two supporting utility functions, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) and [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span></span>

<span data-ttu-id="ee07f-105">Поддержка автопрокси не полностью интегрирована в стек HTTP в WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="ee07f-105">AutoProxy support is not fully integrated into the HTTP stack in WinHTTP.</span></span> <span data-ttu-id="ee07f-106">Перед отправкой запроса приложение должно вызвать [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) для получения имени прокси-сервера, а затем вызвать [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с помощью **\_ \_ прокси-сервера параметров WinHTTP** , чтобы задать конфигурацию прокси-сервера для маркера запроса WinHTTP, созданного с помощью [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span><span class="sxs-lookup"><span data-stu-id="ee07f-106">Before sending a request, the application must call [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to obtain the name of a proxy server and then call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) using **WINHTTP\_OPTION\_PROXY** to set the proxy configuration on the WinHTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span>

<span data-ttu-id="ee07f-107">Функция [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) может выполнять все три шага протокола WPAD, как описано в предыдущем обзоре: (1) обнаружение URL-адреса PAC, (2) скачивание файла скрипта PAC, (3) выполнение кода скрипта и возврат конфигурации прокси-сервера в **структуре \_ \_ сведений о прокси-сервере WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="ee07f-107">The [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function can execute all three steps of the WPAD protocol described in the previous overview: (1) discover the PAC URL, (2) download the PAC script file, (3) execute the script code and return the proxy configuration in a **WINHTTP\_PROXY\_INFO** structure.</span></span> <span data-ttu-id="ee07f-108">При необходимости, если приложение заранее знает URL-адрес PAC, его можно указать как **WinHttpGetProxyForUrl**.</span><span class="sxs-lookup"><span data-stu-id="ee07f-108">Optionally, if the application knows in advance the PAC URL it can specify this to **WinHttpGetProxyForUrl**.</span></span>

<span data-ttu-id="ee07f-109">В следующем примере кода используется автопрокси.</span><span class="sxs-lookup"><span data-stu-id="ee07f-109">The following example code uses autoproxy.</span></span> <span data-ttu-id="ee07f-110">Он настраивает HTTP-запрос GET, сначала создавая обработчики соединения и подключения сеанса WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="ee07f-110">It sets up an HTTP GET request by first creating the WinHTTP session connect and request handles.</span></span> <span data-ttu-id="ee07f-111">В [](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) вызове WinHttpOpen **указан \_ тип доступа WinHTTP \_ \_ No \_ proxy** для конфигурации начального прокси-сервера, чтобы указать, что по умолчанию запросы отправляются непосредственно на целевой сервер.</span><span class="sxs-lookup"><span data-stu-id="ee07f-111">The [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) call specifies **WINHTTP\_ACCESS\_TYPE\_NO\_PROXY** for the initial proxy configuration, to indicate that requests are sent directly to the target server by default.</span></span> <span data-ttu-id="ee07f-112">Используя автопрокси, он задает конфигурацию прокси-сервера непосредственно в обработчике запроса.</span><span class="sxs-lookup"><span data-stu-id="ee07f-112">Using autoproxy, it then sets the proxy configuration directly on the request handle.</span></span>


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



<span data-ttu-id="ee07f-113">В приведенном примере кода вызов [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) предписывает функции автоматически обнаружить файл автоматической настройки прокси-сервера, указав флаг **\_ \_ автоматического \_ определения автопрокси WinHTTP** в структуре [**\_ \_ параметров автопрокси WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) .</span><span class="sxs-lookup"><span data-stu-id="ee07f-113">In the provided example code, the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) instructs the function to discover the proxy auto-config file automatically by specifying the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag in the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure.</span></span> <span data-ttu-id="ee07f-114">Использование флага **\_ \_ автоматического \_ определения автопрокси WinHTTP** требует, чтобы в коде был указан один или оба флага автоматического обнаружения (**\_ \_ тип автоматического обнаружения WinHTTP \_ \_ DHCP**, **\_ \_ тип автоматического обнаружения \_ \_ \_ WinHTTP**).</span><span class="sxs-lookup"><span data-stu-id="ee07f-114">Use of the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag requires the code to specify one or both of the auto-detection flags (**WINHTTP\_AUTO\_DETECT\_TYPE\_DHCP**, **WINHTTP\_AUTO\_DETECT\_TYPE\_DNS\_A**).</span></span> <span data-ttu-id="ee07f-115">В примере кода используется функция автоматического обнаружения **WinHttpGetProxyForUrl** , так как URL-адрес PAC заранее не известен.</span><span class="sxs-lookup"><span data-stu-id="ee07f-115">The example code uses the auto-detection feature of **WinHttpGetProxyForUrl** because the PAC URL is not known in advance.</span></span> <span data-ttu-id="ee07f-116">Если URL-адрес PAC не удается найти в сети в этом сценарии, **WinHttpGetProxyForUrl** завершается неудачей ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку \_ \_ автообнаружение \_ WinHTTP**).</span><span class="sxs-lookup"><span data-stu-id="ee07f-116">If a PAC URL cannot be located on the network in this scenario, **WinHttpGetProxyForUrl** fails ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_WINHTTP\_AUTODETECTION\_FAILED**).</span></span>

## <a name="if-the-pac-url-is-known-in-advance"></a><span data-ttu-id="ee07f-117">Если URL-адрес PAC известен заранее</span><span class="sxs-lookup"><span data-stu-id="ee07f-117">If the PAC URL is Known in Advance</span></span>

<span data-ttu-id="ee07f-118">Если в приложении известен URL-адрес PAC, он может указать его в \_ структуре параметров АВТОПРОКСИ WinHTTP \_ и настроить [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) для пропуска этапа автоматического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="ee07f-118">If the application does know the PAC URL, it can specify it in the WINHTTP\_AUTOPROXY\_OPTIONS structure and configure [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to skip the auto-detection phase.</span></span>

<span data-ttu-id="ee07f-119">Например, если файл PAC доступен в локальной сети по URL-адресу, https://InternalSite/proxy-config.pac то вызов [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ee07f-119">For example, if a PAC file is available on the local network at the URL, "https://InternalSite/proxy-config.pac", the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) would look the following.</span></span>


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



<span data-ttu-id="ee07f-120">Если в [**структуре \_ \_ параметров автопрокси WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) заданы флаги **\_ \_ \_ АВТОопределения** и **\_ \_ \_ URL-адреса** автоматической проверки прокси WinHTTP (и заданы флаги Auto-детктион и URL-адрес автоматической настройки), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) First пытается автоматически определить, а затем, если автоматическое обнаружение не может найти URL-адрес PAC, "перейдет на URL-адрес автоматической настройки, предоставленный приложением.</span><span class="sxs-lookup"><span data-stu-id="ee07f-120">If the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure specifies both **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** and **WINHTTP\_AUTOPROXY\_CONFIG\_URL** flags (and specifies auto-detction flags and an auto-config URL), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) first attempts auto-detection, and then, if auto-detection fails to locate a PAC URL, "falls back" to the auto-config URL supplied by the application.</span></span>

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a><span data-ttu-id="ee07f-121">Функция Винхттпдетектаутопроксиконфигурл</span><span class="sxs-lookup"><span data-stu-id="ee07f-121">The WinHttpDetectAutoProxyConfigUrl Function</span></span>

<span data-ttu-id="ee07f-122">Функция [**винхттпдетектаутопроксиконфигурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) реализует подмножество протокола WPAD: пытается автоматически определить URL-адрес для файла автоматической конфигурации прокси-сервера, не загружая или не выполняя файл PAC.</span><span class="sxs-lookup"><span data-stu-id="ee07f-122">The [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) function implements a subset of the WPAD protocol: it attempts to auto-detect the URL for the proxy auto-config file, without downloading or executing the PAC file.</span></span> <span data-ttu-id="ee07f-123">Эта функция полезна в особых ситуациях, когда веб-клиентское приложение должно выполнять загрузку и выполнение файла PAC.</span><span class="sxs-lookup"><span data-stu-id="ee07f-123">This function is useful in special situations where a Web client application must handle the download and execution of the PAC file itself.</span></span>

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a><span data-ttu-id="ee07f-124">Функция Винхттпжетиепроксиконфигфоркуррентусер</span><span class="sxs-lookup"><span data-stu-id="ee07f-124">The WinHttpGetIEProxyConfigForCurrentUser Function</span></span>

<span data-ttu-id="ee07f-125">Функция [**винхттпжетиепроксиконфигфоркуррентусер**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) возвращает текущие параметры прокси-сервера Internet Explorer для текущего активного сетевого подключения без вызова "WinInet.dll".</span><span class="sxs-lookup"><span data-stu-id="ee07f-125">The [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) function returns the current user Internet Explorer proxy settings for the current active network connection, without calling into "WinInet.dll".</span></span> <span data-ttu-id="ee07f-126">Эта функция полезна только при вызове в процессе, который выполняется от имени интерактивной учетной записи пользователя, так как в противном случае конфигурация прокси-сервера Internet Explorer, скорее всего, будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="ee07f-126">This function is only useful when called within a process that is running under an interactive user account identity, because no Internet Explorer proxy configuration is likely to be available otherwise.</span></span> <span data-ttu-id="ee07f-127">Например, не рекомендуется вызывать эту функцию из DLL ISAPI, выполняющегося в процессе службы IIS.</span><span class="sxs-lookup"><span data-stu-id="ee07f-127">For example, it would not be useful to call this function from an ISAPI DLL running in the IIS service process.</span></span> <span data-ttu-id="ee07f-128">Дополнительные сведения и сценарий, в котором приложение на основе WinHTTP будет использовать **винхттпжетиепроксиконфигфоркуррентусер**, см. в разделе [Обнаружение без файла автоматической настройки](discovery-without-an-auto-config-file.md).</span><span class="sxs-lookup"><span data-stu-id="ee07f-128">For more information and a scenario in which a WinHTTP-based application would use **WinHttpGetIEProxyConfigForCurrentUser**, see [Discovery Without an Auto-Config File](discovery-without-an-auto-config-file.md).</span></span>

 

 
