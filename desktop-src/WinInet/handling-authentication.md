---
title: Обработка проверки подлинности
description: Перед предоставлением доступа к ресурсам в Интернете некоторым учетным записям-посредникам и серверам требуется проверка подлинности.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8eaa38f61f0d97f1f543e0623313aa196aab7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104070786"
---
# <a name="handling-authentication"></a><span data-ttu-id="2db92-103">Обработка проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="2db92-103">Handling Authentication</span></span>

<span data-ttu-id="2db92-104">Перед предоставлением доступа к ресурсам в Интернете некоторым учетным записям-посредникам и серверам требуется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-104">Some proxies and servers require authentication before granting access to resources on the Internet.</span></span> <span data-ttu-id="2db92-105">Функции WinINet поддерживают проверку подлинности сервера и прокси для сеансов HTTP.</span><span class="sxs-lookup"><span data-stu-id="2db92-105">The WinINet functions support server and proxy authentication for http sessions.</span></span> <span data-ttu-id="2db92-106">Проверка подлинности FTP-серверов должна обрабатываться функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .</span><span class="sxs-lookup"><span data-stu-id="2db92-106">Authentication of ftp servers must be handled by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function.</span></span> <span data-ttu-id="2db92-107">В настоящее время проверка подлинности через FTP-шлюз не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2db92-107">Currently, FTP gateway authentication is not supported.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="2db92-108">Об аутентификации HTTP</span><span class="sxs-lookup"><span data-stu-id="2db92-108">About HTTP Authentication</span></span>

<span data-ttu-id="2db92-109">Если требуется проверка подлинности, клиентское приложение получает код состояния 401, если для сервера требуется проверка подлинности или 407, если прокси-сервер требует проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-109">If authentication is required, the client application receives a status code 401, if the server requires authentication, or 407, if the proxy requires authentication.</span></span> <span data-ttu-id="2db92-110">С кодом состояния прокси или сервер отправляет один или несколько заголовков ответа с проверкой подлинности — прокси-проверка подлинности (для проверки подлинности прокси) или WWW-Authenticate (для проверки подлинности сервера).</span><span class="sxs-lookup"><span data-stu-id="2db92-110">With the status code, the proxy or server sends one, or more, authenticate response headers—Proxy-Authenticate (for proxy authentication) or WWW-Authenticate (for server authentication).</span></span>

<span data-ttu-id="2db92-111">Каждый заголовок ответа проверки подлинности содержит доступную схему проверки подлинности и область.</span><span class="sxs-lookup"><span data-stu-id="2db92-111">Each authenticate response header contains an available authentication scheme and a realm.</span></span> <span data-ttu-id="2db92-112">Если поддерживаются несколько схем проверки подлинности, сервер возвращает несколько заголовков ответа проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-112">If multiple authentication schemes are supported, the server returns multiple authenticate response headers.</span></span> <span data-ttu-id="2db92-113">Значение области чувствительно к регистру и определяет пространство защиты на прокси или сервере.</span><span class="sxs-lookup"><span data-stu-id="2db92-113">The realm value is case-sensitive and defines a protection space on the proxy or server.</span></span> <span data-ttu-id="2db92-114">Например, заголовок "WWW-Authenticate: Basic realm =", например "" является примером заголовка, возвращаемого при необходимости проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="2db92-114">For example, the header "WWW-Authenticate: Basic Realm="example"" would be an example of a header returned when server authentication is required.</span></span>

<span data-ttu-id="2db92-115">Клиентское приложение, отправившего запрос, может пройти проверку подлинности, включив поле заголовка авторизации с запросом.</span><span class="sxs-lookup"><span data-stu-id="2db92-115">The client application that sent the request can authenticate itself by including an Authorization header field with the request.</span></span> <span data-ttu-id="2db92-116">Заголовок авторизации будет содержать схему проверки подлинности и соответствующий ответ, необходимый для этой схемы.</span><span class="sxs-lookup"><span data-stu-id="2db92-116">The Authorization header would contain the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="2db92-117">Например, заголовок "Authorization: Basic <имя_пользователя: пароль>" будет добавлен в запрос и повторно отправлен на сервер, если клиент получил заголовок ответа проверки подлинности "WWW-Authenticate: Basic realm =" example "".</span><span class="sxs-lookup"><span data-stu-id="2db92-117">For example, the header "Authorization: Basic <username:password>" would be added to the request and re-sent to the server if the client received the authenticate response header "WWW-Authenticate: Basic Realm="example"".</span></span>

<span data-ttu-id="2db92-118">Существует два общих типа схем проверки подлинности:</span><span class="sxs-lookup"><span data-stu-id="2db92-118">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="2db92-119">Базовая схема проверки подлинности, в которой имя пользователя и пароль отправляются на сервер открытым текстом.</span><span class="sxs-lookup"><span data-stu-id="2db92-119">Basic authentication scheme, where the user name and password are sent in cleartext to the server.</span></span>
-   <span data-ttu-id="2db92-120">Схемы "запрос — ответ", которые позволяют использовать формат "запрос — ответ".</span><span class="sxs-lookup"><span data-stu-id="2db92-120">Challenge-response schemes, which allow for a challenge-response format.</span></span>

<span data-ttu-id="2db92-121">Основная схема проверки подлинности основана на модели, которую клиент должен пройти для проверки подлинности с помощью имени пользователя и пароля для каждой области.</span><span class="sxs-lookup"><span data-stu-id="2db92-121">The Basic authentication scheme is based on the model that a client must authenticate itself with a user name and password for each realm.</span></span> <span data-ttu-id="2db92-122">Сервер служб отправляет запрос при повторной отправку с помощью заголовка авторизации, включающего допустимые имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="2db92-122">The server services the request if it is resent with an Authorization header that includes a valid user name and password.</span></span>

<span data-ttu-id="2db92-123">Схемы "запрос — ответ" обеспечивают более безопасную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-123">Challenge-response schemes enable more secure authentication.</span></span> <span data-ttu-id="2db92-124">Если запрос требует проверки подлинности с помощью схемы запроса и ответа, клиенту возвращается соответствующий код состояния и заголовки проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-124">If a request requires authentication using a challenge-response scheme, the appropriate status code and Authenticate headers are returned to the client.</span></span> <span data-ttu-id="2db92-125">Клиент должен повторно отправить запрос с помощью Negotiate.</span><span class="sxs-lookup"><span data-stu-id="2db92-125">The client must then to resend the request with a negotiate.</span></span> <span data-ttu-id="2db92-126">Сервер возвратит соответствующий код состояния с запросом, и клиент потребует повторно отправить запрос с правильным ответом, чтобы получить запрошенную службу.</span><span class="sxs-lookup"><span data-stu-id="2db92-126">The server would return an appropriate status code with a challenge, and the client would then require to resend the request with the proper response to get the requested service.</span></span>

<span data-ttu-id="2db92-127">В следующей таблице перечислены схемы проверки подлинности, тип проверки подлинности, Библиотека DLL, которая их поддерживает, и описание схемы.</span><span class="sxs-lookup"><span data-stu-id="2db92-127">The following table lists authentication schemes, the authentication type, the DLL that supports them, and a description of the scheme.</span></span>



| <span data-ttu-id="2db92-128">Схема</span><span class="sxs-lookup"><span data-stu-id="2db92-128">Scheme</span></span>                                    | <span data-ttu-id="2db92-129">Тип</span><span class="sxs-lookup"><span data-stu-id="2db92-129">Type</span></span>               | <span data-ttu-id="2db92-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2db92-130">DLL</span></span>                  | <span data-ttu-id="2db92-131">Описание</span><span class="sxs-lookup"><span data-stu-id="2db92-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db92-132">Базовый (открытый текст)</span><span class="sxs-lookup"><span data-stu-id="2db92-132">Basic (cleartext)</span></span>                         | <span data-ttu-id="2db92-133">basic</span><span class="sxs-lookup"><span data-stu-id="2db92-133">basic</span></span>              | <span data-ttu-id="2db92-134">Wininet.dll</span><span class="sxs-lookup"><span data-stu-id="2db92-134">Wininet.dll</span></span>          | <span data-ttu-id="2db92-135">Использует строку в кодировке Base64, содержащую имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="2db92-135">Uses a base64 encoded string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="2db92-136">Digest (дайджест)</span><span class="sxs-lookup"><span data-stu-id="2db92-136">Digest</span></span>                                    | <span data-ttu-id="2db92-137">запрос-ответ</span><span class="sxs-lookup"><span data-stu-id="2db92-137">challenge-response</span></span> | <span data-ttu-id="2db92-138">Digest.dll</span><span class="sxs-lookup"><span data-stu-id="2db92-138">Digest.dll</span></span>           | <span data-ttu-id="2db92-139">Схема "запрос — ответ", которая дает трудности при использовании nonce (определяемая сервером строка данных).</span><span class="sxs-lookup"><span data-stu-id="2db92-139">A challenge-response scheme that challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="2db92-140">Допустимый ответ содержит контрольную сумму имени пользователя, пароля, заданного значения nonce, метода HTTP и запрошенного универсального кода ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="2db92-140">A valid response contains a checksum of the user name, the password, the given nonce value, the HTTP method, and the requested Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="2db92-141">Поддержка дайджест-проверки подлинности появилась в Microsoft Internet Explorer 5.</span><span class="sxs-lookup"><span data-stu-id="2db92-141">Digest authentication support was introduced in Microsoft Internet Explorer 5.</span></span> |
| <span data-ttu-id="2db92-142">Диспетчер LAN NT (NTLM)</span><span class="sxs-lookup"><span data-stu-id="2db92-142">NT LAN Manager (NTLM)</span></span>                     | <span data-ttu-id="2db92-143">запрос-ответ</span><span class="sxs-lookup"><span data-stu-id="2db92-143">challenge-response</span></span> | <span data-ttu-id="2db92-144">Winsspi.dll</span><span class="sxs-lookup"><span data-stu-id="2db92-144">Winsspi.dll</span></span>          | <span data-ttu-id="2db92-145">Схема запроса и ответа, которая основывается на имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="2db92-145">A challenge-response scheme that bases the challenge on the user name.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="2db92-146">Сеть Microsoft (MSN)</span><span class="sxs-lookup"><span data-stu-id="2db92-146">Microsoft Network (MSN)</span></span>                   | <span data-ttu-id="2db92-147">запрос-ответ</span><span class="sxs-lookup"><span data-stu-id="2db92-147">challenge-response</span></span> | <span data-ttu-id="2db92-148">Msnsspc.dll</span><span class="sxs-lookup"><span data-stu-id="2db92-148">Msnsspc.dll</span></span>          | <span data-ttu-id="2db92-149">Схема проверки подлинности сети Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2db92-149">The Microsoft Network's authentication scheme.</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="2db92-150">Распределенная проверка пароля (DPA)</span><span class="sxs-lookup"><span data-stu-id="2db92-150">Distributed Password Authentication (DPA)</span></span> | <span data-ttu-id="2db92-151">запрос-ответ</span><span class="sxs-lookup"><span data-stu-id="2db92-151">challenge-response</span></span> | <span data-ttu-id="2db92-152">Msapsspc.dll</span><span class="sxs-lookup"><span data-stu-id="2db92-152">Msapsspc.dll</span></span>         | <span data-ttu-id="2db92-153">Аналогичен проверке подлинности MSN и также используется сетью Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2db92-153">Similar to MSN authentication and is also used by the Microsoft Network.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2db92-154">Проверка подлинности удаленной парольной фразы (РПА)</span><span class="sxs-lookup"><span data-stu-id="2db92-154">Remote Passphrase Authentication (RPA)</span></span>    | <span data-ttu-id="2db92-155">CompuServe</span><span class="sxs-lookup"><span data-stu-id="2db92-155">CompuServe</span></span>         | <span data-ttu-id="2db92-156">Rpawinet.dll, da.dll</span><span class="sxs-lookup"><span data-stu-id="2db92-156">Rpawinet.dll, da.dll</span></span> | <span data-ttu-id="2db92-157">Схема проверки подлинности CompuServe.</span><span class="sxs-lookup"><span data-stu-id="2db92-157">CompuServe authentication scheme.</span></span> <span data-ttu-id="2db92-158">Дополнительные сведения см. в [спецификации механизма РПА](https://www.compuserve.com/).</span><span class="sxs-lookup"><span data-stu-id="2db92-158">For more information, see the [RPA Mechanism Specifications](https://www.compuserve.com/).</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="2db92-159">Для всех, кроме обычной проверки подлинности, необходимо настроить разделы реестра в дополнение к установке соответствующей библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="2db92-159">For anything other than Basic authentication, the registry keys must be set up in addition to installing the appropriate DLL.</span></span>

<span data-ttu-id="2db92-160">Если требуется проверка подлинности, в вызове [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)следует использовать флаг [ \_ \_ \_ подключения к Интернету](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="2db92-160">If authentication is required, the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag should be used in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="2db92-161">\_ \_ Флаг подключения к Интернету \_ необходим для проверки подлинности NTLM и других типов аутентификации, чтобы обеспечить подключение при завершении процесса проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-161">The INTERNET\_FLAG\_KEEP\_CONNECTION flag is required for NTLM and other types of authentication in order to maintain the connection while completing the authentication process.</span></span> <span data-ttu-id="2db92-162">Если соединение не сохраняется, процесс проверки подлинности должен быть перезапущен с прокси-сервером или с сервера.</span><span class="sxs-lookup"><span data-stu-id="2db92-162">If the connection is not maintained, the authentication process must be restarted with the proxy or server.</span></span>

<span data-ttu-id="2db92-163">Функции [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) и [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) успешно выполнены, даже если требуется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-163">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions complete successfully even when authentication is required.</span></span> <span data-ttu-id="2db92-164">Разница заключается в том, что данные, возвращаемые в файлах заголовков и [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) , ПОлучит HTML-страницу с уведомлением пользователя о коде состояния.</span><span class="sxs-lookup"><span data-stu-id="2db92-164">The difference is, the data returned in the header files and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) would receive an HTML page informing the user of the status code.</span></span>

### <a name="registering-authentication-keys"></a><span data-ttu-id="2db92-165">Регистрация ключей проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="2db92-165">Registering Authentication Keys</span></span>

<span data-ttu-id="2db92-166">В \_ \_ \_ разделе "Конфигурация открытых типов в Интернете" рассматриваются значения реестра **Проксенабле**, **proxyserver** и **проксйоверриде**.</span><span class="sxs-lookup"><span data-stu-id="2db92-166">INTERNET\_OPEN\_TYPE\_PRECONFIG looks at the registry values **ProxyEnable**, **ProxyServer**, and **ProxyOverride**.</span></span> <span data-ttu-id="2db92-167">Эти значения находятся в разделе **hKey \_ Current \_ User** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.</span><span class="sxs-lookup"><span data-stu-id="2db92-167">These values are located under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Internet Settings**.</span></span>

<span data-ttu-id="2db92-168">Для схем проверки подлинности, отличных от Basic, необходимо добавить ключ в реестр в разделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="2db92-168">For authentication schemes other than Basic, a key must be added to the registry under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="2db92-169">Значение **DWORD** , **flags**, должно быть задано соответствующим значением.</span><span class="sxs-lookup"><span data-stu-id="2db92-169">A **DWORD** value, **Flags**, should be set with the appropriate value.</span></span> <span data-ttu-id="2db92-170">В следующем списке приведены возможные значения **флагов** .</span><span class="sxs-lookup"><span data-stu-id="2db92-170">The following list shows the possible values for the **Flags** value.</span></span>

-   <span data-ttu-id="2db92-171">\_Флаг проверки подлинности подключаемого модуля \_ \_ уникальный \_ контекст \_ на \_ TCP/IP (значение = 0x01)</span><span class="sxs-lookup"><span data-stu-id="2db92-171">PLUGIN\_AUTH\_FLAGS\_UNIQUE\_CONTEXT\_PER\_TCPIP (value=0x01)</span></span>

    <span data-ttu-id="2db92-172">Каждый сокет TCP/IP протокола управления передачей содержит другой контекст.</span><span class="sxs-lookup"><span data-stu-id="2db92-172">Each Transmission Control Protocol/Internet Protocol (TCP/IP) socket contains a different context.</span></span> <span data-ttu-id="2db92-173">В противном случае для каждого шаблона области или URL-адреса блока передается новый контекст.</span><span class="sxs-lookup"><span data-stu-id="2db92-173">Otherwise, a new context is passed for each realm or block URL template.</span></span>

-   <span data-ttu-id="2db92-174">\_Флаги проверки подлинности подключаемого модуля \_ \_ могут \_ управлять \_ пользовательским интерфейсом (значение = 0x02)</span><span class="sxs-lookup"><span data-stu-id="2db92-174">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_UI (value=0x02)</span></span>

    <span data-ttu-id="2db92-175">Эта библиотека DLL может работать с собственными данными, введенными пользователем.</span><span class="sxs-lookup"><span data-stu-id="2db92-175">This DLL can handle its own user input.</span></span>

-   <span data-ttu-id="2db92-176">\_Флаги проверки подлинности подключаемого модуля \_ \_ могут \_ \_ не работать без \_ PASSWD (значение = 0x04)</span><span class="sxs-lookup"><span data-stu-id="2db92-176">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_NO\_PASSWD (value=0x04)</span></span>

    <span data-ttu-id="2db92-177">Эта библиотека DLL может выполнять проверку подлинности без запроса пароля пользователем.</span><span class="sxs-lookup"><span data-stu-id="2db92-177">This DLL might be capable of doing an authentication without prompting the user for a password.</span></span>

-   <span data-ttu-id="2db92-178">\_Флаги проверки подлинности подключаемого модуля \_ \_ без \_ области (значение = 0x08)</span><span class="sxs-lookup"><span data-stu-id="2db92-178">PLUGIN\_AUTH\_FLAGS\_NO\_REALM (value=0x08)</span></span>

    <span data-ttu-id="2db92-179">Эта библиотека DLL не использует стандартную строку области HTTP.</span><span class="sxs-lookup"><span data-stu-id="2db92-179">This DLL does not use a standard http realm string.</span></span> <span data-ttu-id="2db92-180">Все данные, которые отображаются как область, представляют собой данные, относящиеся к схеме.</span><span class="sxs-lookup"><span data-stu-id="2db92-180">Any data that appears to be a realm is scheme-specific data.</span></span>

-   <span data-ttu-id="2db92-181">\_Флаги проверки активности подключаемого модуля \_ \_ \_ \_ не \_ требуются (значение = 0x10)</span><span class="sxs-lookup"><span data-stu-id="2db92-181">PLUGIN\_AUTH\_FLAGS\_KEEP\_ALIVE\_NOT\_REQUIRED (value=0x10)</span></span>

    <span data-ttu-id="2db92-182">Эта библиотека DLL не требует постоянного подключения для своей последовательности "запрос — ответ".</span><span class="sxs-lookup"><span data-stu-id="2db92-182">This DLL does not require a persistent connection for its challenge-response sequence.</span></span>

<span data-ttu-id="2db92-183">Например, чтобы добавить проверку подлинности NTLM, необходимо добавить ключ NTLM в раздел **hKey \_ Локальное \_ компьютерное** \\ **программное обеспечение** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="2db92-183">For example, to add NTLM authentication, the key NTLM must be added to **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="2db92-184">В **разделе \_ hKey локальный \_ компьютер** \\ **программное обеспечение** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM** необходимо добавить строковое значение, **дллфиле** и значение **DWORD** , **flags**.</span><span class="sxs-lookup"><span data-stu-id="2db92-184">Under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**\\**NTLM**, the string value, **DLLFile**, and a **DWORD** value, **Flags**, must be added.</span></span> <span data-ttu-id="2db92-185">Для **дллфиле** необходимо задать значение Winsspi.dll, а для **флагов** должно быть задано значение 0x08.</span><span class="sxs-lookup"><span data-stu-id="2db92-185">**DLLFile** must be set to Winsspi.dll, and **Flags** must be set to 0x08.</span></span>

### <a name="server-authentication"></a><span data-ttu-id="2db92-186">Проверка подлинности сервера</span><span class="sxs-lookup"><span data-stu-id="2db92-186">Server Authentication</span></span>

<span data-ttu-id="2db92-187">Когда сервер получает запрос, требующий проверки подлинности, сервер возвращает сообщение с кодом состояния 401.</span><span class="sxs-lookup"><span data-stu-id="2db92-187">When a server receives a request that requires authentication, the server returns a 401 status code message.</span></span> <span data-ttu-id="2db92-188">В этом сообщении сервер должен содержать один или несколько WWW-Authenticate заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="2db92-188">In that message, the server should include one or more WWW-Authenticate response headers.</span></span> <span data-ttu-id="2db92-189">Эти заголовки содержат методы проверки подлинности, доступные для сервера.</span><span class="sxs-lookup"><span data-stu-id="2db92-189">These headers include the authentication methods the server has available.</span></span> <span data-ttu-id="2db92-190">WinINet выбирает первый распознаваемый метод.</span><span class="sxs-lookup"><span data-stu-id="2db92-190">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="2db92-191">Обычная проверка подлинности обеспечивает слабую безопасность, если канал не зашифрован с помощью SSL или PCT.</span><span class="sxs-lookup"><span data-stu-id="2db92-191">Basic authentication provides weak security unless the channel is first link-encrypted with SSL or PCT.</span></span>

<span data-ttu-id="2db92-192">Функцию [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) можно использовать для получения данных имени пользователя и пароля от пользователя, а также для получения данных с помощью настраиваемого пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2db92-192">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed to obtain the data.</span></span>

<span data-ttu-id="2db92-193">Пользовательский интерфейс может использовать функцию [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) , чтобы задать значения параметров [" \_ \_ пароль в Интернете](option-flags.md) " и [ \_ "параметр \_ Интернета](option-flags.md) ", а затем повторно отправить запрос на сервер.</span><span class="sxs-lookup"><span data-stu-id="2db92-193">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_USERNAME](option-flags.md) values and then resend the request to the server.</span></span>

### <a name="proxy-authentication"></a><span data-ttu-id="2db92-194">Проверка подлинности прокси</span><span class="sxs-lookup"><span data-stu-id="2db92-194">Proxy Authentication</span></span>

<span data-ttu-id="2db92-195">Когда клиент пытается использовать прокси-сервер, требующий проверки подлинности, прокси-сервер возвращает клиенту сообщение с кодом состояния 407.</span><span class="sxs-lookup"><span data-stu-id="2db92-195">When a client attempts to use a proxy that requires authentication, the proxy returns a 407 status code message to the client.</span></span> <span data-ttu-id="2db92-196">В этом сообщении прокси-сервер должен содержать один или несколько Proxy-Authenticate заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="2db92-196">In that message, the proxy should include one or more Proxy-Authenticate response headers.</span></span> <span data-ttu-id="2db92-197">Эти заголовки включают методы проверки подлинности, доступные из прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="2db92-197">These headers include the authentication methods available from the proxy.</span></span> <span data-ttu-id="2db92-198">WinINet выбирает первый распознаваемый метод.</span><span class="sxs-lookup"><span data-stu-id="2db92-198">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="2db92-199">Функцию [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) можно использовать для получения данных имени пользователя и пароля от пользователя, а также для разработки настраиваемого пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2db92-199">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed.</span></span>

<span data-ttu-id="2db92-200">Пользовательский интерфейс может использовать функцию [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) для задания [ \_ \_ \_ пароля прокси-сервера](option-flags.md) и параметров Интернета, а затем повторно отправить запрос на прокси-сервер [ \_ \_ \_](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="2db92-200">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PROXY\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_PROXY\_USERNAME](option-flags.md) values and then resend the request to the proxy.</span></span>

<span data-ttu-id="2db92-201">Если имя пользователя и пароль прокси-сервера не заданы, WinINet пытается использовать имя пользователя и пароль для сервера.</span><span class="sxs-lookup"><span data-stu-id="2db92-201">If no proxy user name and password are set, WinINet attempts to use the user name and password for the server.</span></span> <span data-ttu-id="2db92-202">Такое поведение позволяет клиентам реализовать тот же пользовательский интерфейс, который используется для проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="2db92-202">This behavior enables clients to implement the same customized user interface used to handle server authentication.</span></span>

## <a name="handling-http-authentication"></a><span data-ttu-id="2db92-203">Обработка проверки подлинности HTTP</span><span class="sxs-lookup"><span data-stu-id="2db92-203">Handling HTTP Authentication</span></span>

<span data-ttu-id="2db92-204">Проверка подлинности HTTP может быть обработана с помощью [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) или настраиваемой функции, которая использует [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) или добавляет собственные заголовки проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-204">HTTP authentication can be handled with either [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or a customized function that uses [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) or adds its own authentication headers.</span></span> <span data-ttu-id="2db92-205">[**Интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) может проверить заголовки, связанные с маркером [**хинтернет**](appendix-a-hinternet-handles.md) , чтобы найти скрытые ошибки, такие как коды состояния от прокси-сервера или на сервере.</span><span class="sxs-lookup"><span data-stu-id="2db92-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can examine the headers associated with an [**HINTERNET**](appendix-a-hinternet-handles.md) handle to find hidden errors, such as status codes from a proxy or server.</span></span> <span data-ttu-id="2db92-206">[**Интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) можно использовать для задания имени пользователя и пароля для прокси и сервера.</span><span class="sxs-lookup"><span data-stu-id="2db92-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) can be used to set the user name and password for the proxy and server.</span></span> <span data-ttu-id="2db92-207">Для проверки подлинности MSN и DPA необходимо использовать [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) для задания имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="2db92-207">For MSN and DPA authentication, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) must be used to set the user name and password.</span></span>

<span data-ttu-id="2db92-208">Для любой настраиваемой функции, добавляющей собственные заголовки WWW-Authenticate или Proxy-Authenticate, [флаг \_ Internet \_ флаг \_ проверки подлинности не](api-flags.md) должен быть установлен для отключения проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-208">For any customized function that adds its own WWW-Authenticate or Proxy-Authenticate headers, the [INTERNET\_FLAG\_NO\_AUTH](api-flags.md) flag should be set to disable authentication.</span></span>

<span data-ttu-id="2db92-209">В следующем примере показано, как [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) можно использовать для проверки подлинности HTTP.</span><span class="sxs-lookup"><span data-stu-id="2db92-209">The following example shows how [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can be used to handle HTTP authentication.</span></span>


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



<span data-ttu-id="2db92-210">В этом примере Дверроркоде используется для хранения любых ошибок, связанных с вызовом [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="2db92-210">In the example, dwErrorCode is used to store any errors associated with the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="2db92-211">[**Хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) завершается успешно, даже если прокси или сервер требует проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completes successfully, even if the proxy or server requires authentication.</span></span> <span data-ttu-id="2db92-212">Если в \_ \_ \_ \_ интернетеррордлг передается флаг "Фильтрация пользовательского интерфейса для ошибок" \_ , функция проверяет заголовки на наличие скрытых ошибок. [](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)</span><span class="sxs-lookup"><span data-stu-id="2db92-212">When the FLAGS\_ERROR\_UI\_FILTER\_FOR\_ERRORS flag is passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), the function checks the headers for any hidden errors.</span></span> <span data-ttu-id="2db92-213">Эти скрытые ошибки включают в себя любые запросы на проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="2db92-213">These hidden errors would include any requests for authentication.</span></span> <span data-ttu-id="2db92-214">[**Интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) отображает соответствующее диалоговое окно, в котором пользователю предлагается ввести необходимые данные.</span><span class="sxs-lookup"><span data-stu-id="2db92-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) displays the appropriate dialog box to prompt the user for the necessary data.</span></span> <span data-ttu-id="2db92-215">Флаги пользовательского интерфейса с флагами \_ ошибок " \_ \_ \_ создать данные" \_ и "флаги \_ \_ пользовательского интерфейса ошибок" \_ \_ \_ также должны передаваться в [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), чтобы функция создавала соответствующую структуру данных для ошибки и сохраняла результаты диалогового окна в обработчике [**хинтернет**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="2db92-215">The FLAGS\_ERROR\_UI\_FLAGS\_GENERATE\_DATA and FLAGS\_ERROR\_UI\_FLAGS\_CHANGE\_OPTIONS flags should also be passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), so that the function constructs the appropriate data structure for the error and stores the results of the dialog box in the [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="2db92-216">В следующем примере кода показано, как можно обработать проверку подлинности с помощью [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="2db92-216">The following example code shows how authentication could be handled using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> <span data-ttu-id="2db92-217">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="2db92-217">WinINet does not support server implementations.</span></span> <span data-ttu-id="2db92-218">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="2db92-218">In addition, it should not be used from a service.</span></span> <span data-ttu-id="2db92-219">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="2db92-219">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 