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
ms.openlocfilehash: 1d33b8042cd1fd15d46e15dfb3624e0d3b4a885b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712035"
---
# <a name="authentication-using-script"></a><span data-ttu-id="49242-103">Проверка подлинности с помощью скрипта</span><span class="sxs-lookup"><span data-stu-id="49242-103">Authentication Using Script</span></span>

<span data-ttu-id="49242-104">В этом разделе показано, как написать скрипт, использующий объект [**WinHttpRequest**](winhttprequest.md) для доступа к данным с сервера, для которого требуется проверка подлинности HTTP.</span><span class="sxs-lookup"><span data-stu-id="49242-104">This section demonstrates how to write script that uses the [**WinHttpRequest**](winhttprequest.md) object to access data from a server that requires HTTP authentication.</span></span>

-   [<span data-ttu-id="49242-105">Необходимые условия и требования</span><span class="sxs-lookup"><span data-stu-id="49242-105">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="49242-106">Доступ к веб-сайту с проверкой подлинности</span><span class="sxs-lookup"><span data-stu-id="49242-106">Accessing a Web Site With Authentication</span></span>](#accessing-a-web-site-with-authentication)
-   [<span data-ttu-id="49242-107">Проверка кодов состояния</span><span class="sxs-lookup"><span data-stu-id="49242-107">Checking the Status Codes</span></span>](#checking-the-status-codes)
-   [<span data-ttu-id="49242-108">См. также</span><span class="sxs-lookup"><span data-stu-id="49242-108">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="49242-109">Необходимые условия и требования</span><span class="sxs-lookup"><span data-stu-id="49242-109">Prerequisites and Requirements</span></span>

<span data-ttu-id="49242-110">В дополнение к опыту работы с Microsoft JScript для этого примера требуется следующее:</span><span class="sxs-lookup"><span data-stu-id="49242-110">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="49242-111">Текущая версия пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="49242-111">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="49242-112">Средство настройки прокси-сервера для установки параметров прокси-сервера для служб Microsoft Windows HTTP (WinHTTP), если подключение к Интернету осуществляется через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="49242-112">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="49242-113">Дополнительные сведения см. [ в разделеProxycfg.exe, средство настройки прокси-сервера](proxycfg-exe--a-proxy-configuration-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="49242-113">See [Proxycfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md) for more information.</span></span>
-   <span data-ttu-id="49242-114">Знакомство с [терминологией](network-terminology.md) и концепциями сети.</span><span class="sxs-lookup"><span data-stu-id="49242-114">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="accessing-a-web-site-with-authentication"></a><span data-ttu-id="49242-115">Доступ к веб-сайту с проверкой подлинности</span><span class="sxs-lookup"><span data-stu-id="49242-115">Accessing a Web Site With Authentication</span></span>

<span data-ttu-id="49242-116">**Чтобы создать скрипт, демонстрирующий проверку подлинности, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="49242-116">**To create a script that demonstrates authentication, do the following:**</span></span>

1.  <span data-ttu-id="49242-117">Откройте текстовый редактор, например Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="49242-117">Open a text editor such as Microsoft Notepad.</span></span>
2.  <span data-ttu-id="49242-118">Скопируйте следующий код в текстовый редактор после замены " \[ аусентикатионсите" на \] соответствующий текст, чтобы указать URL-адрес сайта, для которого требуется проверка подлинности HTTP.</span><span class="sxs-lookup"><span data-stu-id="49242-118">Copy the following code into the text editor after replacing "\[authenticationSite\]" with the appropriate text to specify the URL of a site that requires HTTP authentication.</span></span>

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

    

3.  <span data-ttu-id="49242-119">Сохраните файл как "Auth.js".</span><span class="sxs-lookup"><span data-stu-id="49242-119">Save the file as "Auth.js".</span></span>
4.  <span data-ttu-id="49242-120">В командной строке введите "cscript Auth.js" и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="49242-120">From a command prompt, type "cscript Auth.js" and press ENTER.</span></span>

<span data-ttu-id="49242-121">Теперь у вас есть программа, которая запрашивает ресурс двумя разными способами.</span><span class="sxs-lookup"><span data-stu-id="49242-121">You now have a program that requests a resource two different ways.</span></span> <span data-ttu-id="49242-122">Первый метод запрашивает ресурс, не указывая учетные данные.</span><span class="sxs-lookup"><span data-stu-id="49242-122">The first method requests the resource without supplying credentials.</span></span> <span data-ttu-id="49242-123">Возвращается код состояния 401, указывающий, что сервер требует проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="49242-123">A 401 status code is returned to indicate that the server requires authentication.</span></span> <span data-ttu-id="49242-124">Заголовки ответов также отображаются и должны выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49242-124">The response headers are also displayed and should look similar to the following:</span></span>

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

<span data-ttu-id="49242-125">Хотя ответ означает, что доступ к ресурсу был отклонен, он по-прежнему возвращает несколько заголовков, предоставляющих некоторую информацию о ресурсе.</span><span class="sxs-lookup"><span data-stu-id="49242-125">Although the response indicates that access to the resource was denied, it still returns several headers that provide some information about the resource.</span></span> <span data-ttu-id="49242-126">Заголовок с именем WWW-Authenticate указывает, что сервер требует проверки подлинности для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="49242-126">The header named "WWW-Authenticate" indicates that the server requires authentication for this resource.</span></span> <span data-ttu-id="49242-127">Если существовал заголовок с именем "Proxy-Authenticate", он указывает, что прокси-сервер требует проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="49242-127">If there was a header named "Proxy-Authenticate", it would indicate that the proxy server requires authentication.</span></span> <span data-ttu-id="49242-128">Каждый заголовок проверки подлинности содержит доступную схему проверки подлинности и иногда область.</span><span class="sxs-lookup"><span data-stu-id="49242-128">Each authenticate header contains an available authentication scheme and sometimes a realm.</span></span> <span data-ttu-id="49242-129">Значение области учитывает регистр и определяет набор серверов или учетных записей-посредников, для которых должны приниматься одни и те же учетные данные.</span><span class="sxs-lookup"><span data-stu-id="49242-129">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials should be accepted.</span></span>

<span data-ttu-id="49242-130">Существует два заголовка с именем WWW-Authenticate, которые указывают, что поддерживаются несколько схем проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="49242-130">There are two headers named "WWW-Authenticate", which indicate that multiple authentication schemes are supported.</span></span> <span data-ttu-id="49242-131">При вызове метода [**жетреспонсехеадер**](iwinhttprequest-getresponseheader.md) для поиска заголовков WWW-Authenticate метод возвращает только содержимое первого заголовка этого имени.</span><span class="sxs-lookup"><span data-stu-id="49242-131">If you call the [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) method to find "WWW-Authenticate" headers, the method only returns the contents of the first header of that name.</span></span> <span data-ttu-id="49242-132">В этом случае возвращается значение NTLM.</span><span class="sxs-lookup"><span data-stu-id="49242-132">In this case, it returns a value of "NTLM".</span></span> <span data-ttu-id="49242-133">Чтобы обеспечить обработку всех вхождений заголовка, используйте вместо этого метод [**жеталлреспонсехеадерс**](iwinhttprequest-getallresponseheaders.md) .</span><span class="sxs-lookup"><span data-stu-id="49242-133">To ensure that all occurrences of a header are processed, use the [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) method instead.</span></span>

<span data-ttu-id="49242-134">Второй вызов метода запрашивает тот же ресурс, но сначала предоставляет учетные данные для проверки подлинности путем вызова метода [**сеткредентиалс**](iwinhttprequest-setcredentials.md) .</span><span class="sxs-lookup"><span data-stu-id="49242-134">The second method call requests the same resource, but first supplies authentication credentials by calling the [**SetCredentials**](iwinhttprequest-setcredentials.md) method.</span></span> <span data-ttu-id="49242-135">В следующем разделе кода показано, как используется этот метод.</span><span class="sxs-lookup"><span data-stu-id="49242-135">The following section of code shows how this method is used.</span></span>


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



<span data-ttu-id="49242-136">Этот метод задает имя пользователя "UserName", пароль в "Password" и указывает, что учетные данные авторизации применяются к серверу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49242-136">This method sets the user name to "UserName", the password to "Password", and indicates that the authorization credentials apply to the resource server.</span></span> <span data-ttu-id="49242-137">Учетные данные проверки подлинности также могут отправляться на прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="49242-137">Authentication credentials can also be sent to a proxy.</span></span>

<span data-ttu-id="49242-138">Если указаны учетные данные, сервер возвращает код состояния 200, указывающий, что документ можно извлечь.</span><span class="sxs-lookup"><span data-stu-id="49242-138">When credentials are supplied, the server returns a 200 status code that indicates that the document can be retrieved.</span></span>

## <a name="checking-the-status-codes"></a><span data-ttu-id="49242-139">Проверка кодов состояния</span><span class="sxs-lookup"><span data-stu-id="49242-139">Checking the Status Codes</span></span>

<span data-ttu-id="49242-140">Предыдущий пример — инструкции, но он требует, чтобы пользователь явно предоставил учетные данные.</span><span class="sxs-lookup"><span data-stu-id="49242-140">The previous example is instructional, but it requires that the user explicitly supply credentials.</span></span> <span data-ttu-id="49242-141">Приложение, которое предоставляет учетные данные при необходимости и не предоставляет учетные данные, если это не требуется.</span><span class="sxs-lookup"><span data-stu-id="49242-141">An application that supplies credentials when it is necessary and does not supply credentials when it is not necessary is more useful.</span></span> <span data-ttu-id="49242-142">Чтобы реализовать функцию, которая делает это, необходимо изменить пример, чтобы проверить код состояния, возвращенный с ответом.</span><span class="sxs-lookup"><span data-stu-id="49242-142">To implement a feature that does this, you must modify your example to examine the status code returned with the response.</span></span>

<span data-ttu-id="49242-143">Полный список возможных кодов состояния, а также описания см. в разделе [**коды состояния HTTP**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="49242-143">For a complete list of possible status codes, along with descriptions, see [**HTTP Status Codes**](http-status-codes.md).</span></span> <span data-ttu-id="49242-144">Однако в этом примере следует возникать только один из трех кодов.</span><span class="sxs-lookup"><span data-stu-id="49242-144">For this example, however, you should encounter only one of three codes.</span></span> <span data-ttu-id="49242-145">Код состояния 200 указывает, что ресурс доступен и отправляется с ответом.</span><span class="sxs-lookup"><span data-stu-id="49242-145">A status code of 200 indicates that a resource is available and is being sent with the response.</span></span> <span data-ttu-id="49242-146">Код состояния 401 указывает на то, что сервер требует проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="49242-146">A status code of 401 indicates that the server requires authentication.</span></span> <span data-ttu-id="49242-147">Код состояния 407 указывает на то, что прокси-сервер требует проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="49242-147">A status code of 407 indicates that the proxy requires authentication.</span></span>

<span data-ttu-id="49242-148">Измените пример, созданный в последнем разделе, заменив функцию "getText2" следующим кодом (замените " \[ аусентикатионсите \] " собственным текстом, чтобы указать URL-адрес сайта, для которого требуется проверка подлинности HTTP):</span><span class="sxs-lookup"><span data-stu-id="49242-148">Modify the example you created in the last section by replacing the "getText2" function with the following code (replace "\[authenticationSite\]" with your own text to specifies the URL of a site that requires HTTP authentication):</span></span>


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



<span data-ttu-id="49242-149">Снова сохраните и запустите файл.</span><span class="sxs-lookup"><span data-stu-id="49242-149">Again, save and run the file.</span></span> <span data-ttu-id="49242-150">Второй метод по-прежнему извлекает документ, но при необходимости предоставляет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="49242-150">The second method still retrieves the document, but it only provides credentials when required.</span></span> <span data-ttu-id="49242-151">Функция "getText2" выполняет методы [**Open**](iwinhttprequest-open.md) и [**Send**](iwinhttprequest-send.md) , как если бы проверка подлинности не требовалась.</span><span class="sxs-lookup"><span data-stu-id="49242-151">The "getText2" function executes the [**Open**](iwinhttprequest-open.md) and [**Send**](iwinhttprequest-send.md) methods as if authentication was not required.</span></span> <span data-ttu-id="49242-152">Состояние извлекается со свойством [**Status**](iwinhttprequest-status.md) , а оператор switch реагирует на полученный код состояния.</span><span class="sxs-lookup"><span data-stu-id="49242-152">The status is retrieved with the [**Status**](iwinhttprequest-status.md) property and a switch statement responds to the resulting status code.</span></span> <span data-ttu-id="49242-153">Если состояние равно 401 (сервер требует проверки подлинности) или 407 (прокси требует проверки подлинности), метод [**Open**](iwinhttprequest-open.md) выполняется снова.</span><span class="sxs-lookup"><span data-stu-id="49242-153">If the status is 401 (server requires authentication) or 407 (proxy requires authentication), the [**Open**](iwinhttprequest-open.md) method is executed again.</span></span> <span data-ttu-id="49242-154">За ним следует метод [**сеткредентиалс**](iwinhttprequest-setcredentials.md) , который задает имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="49242-154">This is followed by the [**SetCredentials**](iwinhttprequest-setcredentials.md) method, which sets the user name and password.</span></span> <span data-ttu-id="49242-155">Затем код перебирается обратно в метод [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="49242-155">The code then loops back to the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="49242-156">Если после трех попыток не удается успешно получить ресурс, функция прекратит выполнение.</span><span class="sxs-lookup"><span data-stu-id="49242-156">If, after three attempts, the resource cannot be successfully retrieved, then the function stops execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49242-157">См. также</span><span class="sxs-lookup"><span data-stu-id="49242-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49242-158">Проверка подлинности в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49242-158">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="49242-159">WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="49242-159">WinHttpRequest</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="49242-160">**сеткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="49242-160">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)
</dt> <dt>

[<span data-ttu-id="49242-161">Запрос HTTP/1.1 для комментариев (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="49242-161">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



