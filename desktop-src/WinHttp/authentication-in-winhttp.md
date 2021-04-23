---
description: Перед предоставлением доступа к ресурсам в Интернете некоторым серверам и прокси-службам HTTP требуется проверка подлинности. Функции служб Microsoft Windows HTTP (WinHTTP) поддерживают проверку подлинности сервера и прокси для сеансов HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Проверка подлинности в WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75c6703e9d28902c5705f0b8ab8433193c4d085
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380830"
---
# <a name="authentication-in-winhttp"></a><span data-ttu-id="ae727-104">Проверка подлинности в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="ae727-104">Authentication in WinHTTP</span></span>

<span data-ttu-id="ae727-105">Перед предоставлением доступа к ресурсам в Интернете некоторым серверам и прокси-службам HTTP требуется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae727-105">Some HTTP servers and proxies require authentication before allowing access to resources on the Internet.</span></span> <span data-ttu-id="ae727-106">Функции служб Microsoft Windows HTTP (WinHTTP) поддерживают проверку подлинности сервера и прокси для сеансов HTTP.</span><span class="sxs-lookup"><span data-stu-id="ae727-106">The Microsoft Windows HTTP Services (WinHTTP) functions support server and proxy authentication for HTTP sessions.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="ae727-107">Об аутентификации HTTP</span><span class="sxs-lookup"><span data-stu-id="ae727-107">About HTTP Authentication</span></span>

<span data-ttu-id="ae727-108">Если требуется проверка подлинности, HTTP-приложение получает код состояния 401 (для сервера требуется проверка подлинности) или 407 (прокси требует проверки подлинности).</span><span class="sxs-lookup"><span data-stu-id="ae727-108">If authentication is required, the HTTP application receives a status code of 401 (server requires authentication) or 407 (proxy requires authentication).</span></span> <span data-ttu-id="ae727-109">Вместе с кодом состояния прокси или сервер отправляет один или несколько заголовков проверки подлинности: WWW-Authenticate (для проверки подлинности сервера) или Proxy-Authenticate (для проверки подлинности прокси).</span><span class="sxs-lookup"><span data-stu-id="ae727-109">Along with the status code, the proxy or server sends one or more authenticate headers: WWW-Authenticate (for server authentication) or Proxy-Authenticate (for proxy authentication).</span></span>

<span data-ttu-id="ae727-110">Каждый заголовок проверки подлинности содержит поддерживаемую схему проверки подлинности, а для базовых и дайджест-схем — область.</span><span class="sxs-lookup"><span data-stu-id="ae727-110">Each authenticate header contains a supported authentication scheme and, for the Basic and Digest schemes, a realm.</span></span> <span data-ttu-id="ae727-111">Если поддерживаются несколько схем проверки подлинности, сервер возвращает несколько заголовков с проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae727-111">If multiple authentication schemes are supported, the server returns multiple authenticate headers.</span></span> <span data-ttu-id="ae727-112">Значение области учитывает регистр и определяет набор серверов или учетных записей-посредников, для которых принимаются одни и те же учетные данные.</span><span class="sxs-lookup"><span data-stu-id="ae727-112">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials are accepted.</span></span> <span data-ttu-id="ae727-113">Например, если требуется проверка подлинности сервера, может возвращаться заголовок "WWW-Authenticate: Basic realm =", например "".</span><span class="sxs-lookup"><span data-stu-id="ae727-113">For example, the header "WWW-Authenticate: Basic Realm="example"" might be returned when server authentication is required.</span></span> <span data-ttu-id="ae727-114">Этот заголовок указывает, что для домена "example" должны быть указаны учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="ae727-114">This header specifies that user credentials must be supplied for the "example" domain.</span></span>

<span data-ttu-id="ae727-115">Приложение HTTP может включать поле заголовка авторизации с запросом, который отправляется на сервер.</span><span class="sxs-lookup"><span data-stu-id="ae727-115">An HTTP application can include an authorization header field with a request it sends to the server.</span></span> <span data-ttu-id="ae727-116">Заголовок Authorization содержит схему проверки подлинности и соответствующий ответ, необходимый для этой схемы.</span><span class="sxs-lookup"><span data-stu-id="ae727-116">The authorization header contains the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="ae727-117">Например, заголовок «Authorization: Basic \<username:password> » будет добавлен в запрос и отправлен на сервер, если клиент получил заголовок ответа «WWW-Authenticate: Basic realm =» example».</span><span class="sxs-lookup"><span data-stu-id="ae727-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and sent to the server if the client received the response header "WWW-Authenticate: Basic Realm="example"".</span></span>

> [!Note]  
> <span data-ttu-id="ae727-118">Хотя они показаны в виде обычного текста, имя пользователя и пароль фактически кодируются в [*кодировке Base64*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="ae727-118">Although they are shown here as plain text, the username and password are actually [*base64 encoded*](glossary.md).</span></span>

 

<span data-ttu-id="ae727-119">Существует два общих типа схем проверки подлинности:</span><span class="sxs-lookup"><span data-stu-id="ae727-119">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="ae727-120">Базовая схема проверки подлинности, в которой имя пользователя и пароль отправляются на сервер открытым текстом.</span><span class="sxs-lookup"><span data-stu-id="ae727-120">Basic authentication scheme, in which the user name and password are sent in clear text to the server.</span></span>

    <span data-ttu-id="ae727-121">Основная схема проверки подлинности основана на модели, которую клиент должен идентифицировать самостоятельно, указав имя пользователя и пароль для каждой области.</span><span class="sxs-lookup"><span data-stu-id="ae727-121">The Basic authentication scheme is based on the model that a client must identify itself with a user name and password for each realm.</span></span> <span data-ttu-id="ae727-122">Сервер служб запрашивается, только если запрос отправляется с заголовком авторизации, который содержит допустимые имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="ae727-122">The server services the request only if the request is sent with an authorization header that includes a valid user name and password.</span></span>

-   <span data-ttu-id="ae727-123">Схемы запросов и ответов, такие как Kerberos, в которых сервер запрашивает у клиента [*данные проверки подлинности*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="ae727-123">Challenge-response schemes, such as Kerberos, in which the server challenges the client with [*authentication data*](glossary.md).</span></span> <span data-ttu-id="ae727-124">Клиент преобразует данные с учетными данными пользователя и отправляет преобразованные данные обратно на сервер для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae727-124">The client transforms the data with the user credentials and sends the transformed data back to the server for authentication.</span></span>

    <span data-ttu-id="ae727-125">Схемы "запрос — ответ" обеспечивают более безопасную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae727-125">Challenge-response schemes enable a more secure authentication.</span></span> <span data-ttu-id="ae727-126">В схеме "запрос — ответ" имя пользователя и пароль никогда не передаются по сети.</span><span class="sxs-lookup"><span data-stu-id="ae727-126">In a challenge-response scheme, the username and password are never transmitted over the network.</span></span> <span data-ttu-id="ae727-127">После того как клиент выберет схему "запрос — ответ", сервер возвращает соответствующий код состояния с запросом, содержащим [*данные проверки подлинности*](glossary.md) для этой схемы.</span><span class="sxs-lookup"><span data-stu-id="ae727-127">After the client selects a challenge-response scheme, the server returns an appropriate status code with a challenge that contains the [*authentication data*](glossary.md) for that scheme.</span></span> <span data-ttu-id="ae727-128">Затем клиент повторно отправляет запрос с правильным ответом для получения запрошенной службы.</span><span class="sxs-lookup"><span data-stu-id="ae727-128">The client then resends the request with the proper response to obtain the requested service.</span></span> <span data-ttu-id="ae727-129">Схемы "запрос — ответ" могут выполнять несколько обменов.</span><span class="sxs-lookup"><span data-stu-id="ae727-129">Challenge-response schemes can take multiple exchanges to complete.</span></span>

<span data-ttu-id="ae727-130">Следующая таблица содержит схемы проверки подлинности, поддерживаемые WinHTTP, типом проверки подлинности и описанием схемы.</span><span class="sxs-lookup"><span data-stu-id="ae727-130">The following table contains the authentication schemes that are supported by WinHTTP, the authentication type, and a description of the scheme.</span></span>



| <span data-ttu-id="ae727-131">Схема</span><span class="sxs-lookup"><span data-stu-id="ae727-131">Scheme</span></span>            | <span data-ttu-id="ae727-132">Тип</span><span class="sxs-lookup"><span data-stu-id="ae727-132">Type</span></span>               | <span data-ttu-id="ae727-133">Описание</span><span class="sxs-lookup"><span data-stu-id="ae727-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae727-134">Базовый (обычный текст)</span><span class="sxs-lookup"><span data-stu-id="ae727-134">Basic (plaintext)</span></span> | <span data-ttu-id="ae727-135">Basic</span><span class="sxs-lookup"><span data-stu-id="ae727-135">Basic</span></span>              | <span data-ttu-id="ae727-136">Использует строку в [*кодировке Base64*](glossary.md) , содержащую имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="ae727-136">Uses a [*base64 encoded*](glossary.md) string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ae727-137">Digest (дайджест)</span><span class="sxs-lookup"><span data-stu-id="ae727-137">Digest</span></span>            | <span data-ttu-id="ae727-138">Запрос-ответ</span><span class="sxs-lookup"><span data-stu-id="ae727-138">Challenge-response</span></span> | <span data-ttu-id="ae727-139">Проблемы с использованием nonce (определяемой сервером строки данных).</span><span class="sxs-lookup"><span data-stu-id="ae727-139">Challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="ae727-140">Допустимый ответ содержит контрольную сумму имени пользователя, пароля, заданного значения nonce, [*HTTP-команды*](glossary.md)и запрошенного универсального кода ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="ae727-140">A valid response contains a checksum of the user name, the password, the given nonce value, the [*HTTP verb*](glossary.md), and the requested Uniform Resource Identifier (URI).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ae727-141">NTLM</span><span class="sxs-lookup"><span data-stu-id="ae727-141">NTLM</span></span>              | <span data-ttu-id="ae727-142">Запрос-ответ</span><span class="sxs-lookup"><span data-stu-id="ae727-142">Challenge-response</span></span> | <span data-ttu-id="ae727-143">Требует, чтобы [*данные проверки подлинности*](glossary.md) были преобразованы с учетными данными пользователя для подтверждения личности.</span><span class="sxs-lookup"><span data-stu-id="ae727-143">Requires the [*authentication data*](glossary.md) to be transformed with the user credentials to prove identity.</span></span> <span data-ttu-id="ae727-144">Для правильной работы проверки подлинности NTLM в одном и том же соединении необходимо выполнить несколько обменов.</span><span class="sxs-lookup"><span data-stu-id="ae727-144">For NTLM authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="ae727-145">Поэтому проверка подлинности NTLM не может быть использована, если промежуточный прокси-сервер не поддерживает подключения, поддерживающие проверку активности.</span><span class="sxs-lookup"><span data-stu-id="ae727-145">Therefore, NTLM authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="ae727-146">Проверка подлинности NTLM также завершается ошибкой, если [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) используется с флагом проверки [**\_ \_ \_ активности WinHTTP**](option-flags.md) , который отключает семантику проверки активности.</span><span class="sxs-lookup"><span data-stu-id="ae727-146">NTLM authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="ae727-147">Паспорт</span><span class="sxs-lookup"><span data-stu-id="ae727-147">Passport</span></span>          | <span data-ttu-id="ae727-148">Запрос-ответ</span><span class="sxs-lookup"><span data-stu-id="ae727-148">Challenge-response</span></span> | <span data-ttu-id="ae727-149">Использует [Microsoft Passport 1,4](passport-authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="ae727-149">Uses [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ae727-150">Согласование</span><span class="sxs-lookup"><span data-stu-id="ae727-150">Negotiate</span></span>         | <span data-ttu-id="ae727-151">Запрос-ответ</span><span class="sxs-lookup"><span data-stu-id="ae727-151">Challenge-response</span></span> | <span data-ttu-id="ae727-152">Если сервер и клиент работают под управлением Windows 2000 или более поздней версии, используется проверка подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ae727-152">If both the server and client are using Windows 2000 or later, Kerberos authentication is used.</span></span> <span data-ttu-id="ae727-153">В противном случае используется проверка подлинности NTLM.</span><span class="sxs-lookup"><span data-stu-id="ae727-153">Otherwise NTLM authentication is used.</span></span> <span data-ttu-id="ae727-154">Протокол Kerberos доступен в операционных системах Windows 2000 и более поздних версий и считается более безопасным, чем проверка подлинности NTLM.</span><span class="sxs-lookup"><span data-stu-id="ae727-154">Kerberos is available in Windows 2000 and later operating systems and is considered to be more secure than NTLM authentication.</span></span> <span data-ttu-id="ae727-155">Для правильной работы проверки подлинности в одном и том же соединении необходимо выполнить несколько обменов.</span><span class="sxs-lookup"><span data-stu-id="ae727-155">For Negotiate authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="ae727-156">Таким образом, проверка подлинности Negotiate не может быть использована, если промежуточный прокси-сервер не поддерживает подключения, поддерживающие проверку активности.</span><span class="sxs-lookup"><span data-stu-id="ae727-156">Therefore, Negotiate authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="ae727-157">Согласование проверки подлинности также завершается сбоем, если [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) используется с флагом проверки [**\_ \_ \_ активности WinHTTP**](option-flags.md) , который отключает семантику сохранения активности.</span><span class="sxs-lookup"><span data-stu-id="ae727-157">Negotiate authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span> <span data-ttu-id="ae727-158">Схема проверки подлинности Negotiate иногда называется встроенной проверкой подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="ae727-158">The Negotiate authentication scheme is sometimes called Integrated Windows authentication.</span></span> |



 

## <a name="authentication-in-winhttp-applications"></a><span data-ttu-id="ae727-159">Проверка подлинности в приложениях WinHTTP</span><span class="sxs-lookup"><span data-stu-id="ae727-159">Authentication in WinHTTP Applications</span></span>

<span data-ttu-id="ae727-160">Интерфейс прикладного программирования (API) WinHTTP предоставляет две функции, используемые для доступа к Интернет-ресурсам в ситуациях, когда требуется проверка подлинности: [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) и [**винхттпкуеряуссчемес**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span><span class="sxs-lookup"><span data-stu-id="ae727-160">The WinHTTP application programming interface (API) provides two functions used to access Internet resources in situations where authentication is required: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) and [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span></span>

<span data-ttu-id="ae727-161">При получении ответа с кодом состояния 401 или 407 можно использовать [**винхттпкуеряуссчемес**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) для анализа заголовков проверки подлинности, чтобы определить поддерживаемые схемы проверки подлинности и целевой объект проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae727-161">When a response is received with a 401 or 407 status code, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) can be used to parse the authentication headers to determine the supported authentication schemes and the authentication target.</span></span> <span data-ttu-id="ae727-162">Целевой объект проверки подлинности — это сервер или прокси, который запрашивает проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae727-162">The authentication target is the server or proxy that requests authentication.</span></span> <span data-ttu-id="ae727-163">**Винхттпкуеряуссчемес** также определяет первую схему проверки подлинности из доступных схем на основе настроек схемы проверки подлинности, предлагаемых сервером.</span><span class="sxs-lookup"><span data-stu-id="ae727-163">**WinHttpQueryAuthSchemes** also determines the first authentication scheme, from the available schemes, based on the authentication scheme preferences suggested by the server.</span></span> <span data-ttu-id="ae727-164">Этот метод выбора схемы проверки подлинности — это поведение, предлагаемое [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="ae727-164">This method for choosing an authentication scheme is the behavior suggested by [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

<span data-ttu-id="ae727-165">[**Винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) позволяет приложению указать схему проверки подлинности, которая используется вместе с допустимыми именем пользователя и паролем для использования на целевом сервере или прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="ae727-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) enables an application to specify the authentication scheme that is used along with a valid username and password for use on the target server or proxy.</span></span> <span data-ttu-id="ae727-166">После настройки учетных данных и повторной отправки запроса необходимые заголовки создаются и добавляются в запрос автоматически.</span><span class="sxs-lookup"><span data-stu-id="ae727-166">After setting the credentials and resending the request, the necessary headers are generated and added to the request automatically.</span></span> <span data-ttu-id="ae727-167">Поскольку некоторым схемам проверки подлинности требуется несколько транзакций, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) может возвращать ошибку, ошибка \_ \_ запроса повторной отправки WinHTTP \_ .</span><span class="sxs-lookup"><span data-stu-id="ae727-167">Because some authentication schemes require multiple transactions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) could return the error, ERROR\_WINHTTP\_RESEND\_REQUEST.</span></span> <span data-ttu-id="ae727-168">При возникновении этой ошибки приложение должно продолжать повторно отправить запрос, пока не будет получен ответ, не содержащий код состояния 401 или 407.</span><span class="sxs-lookup"><span data-stu-id="ae727-168">When this error is encountered, the application should continue to resend the request until a response is received that does not contain a 401 or 407 status code.</span></span> <span data-ttu-id="ae727-169">Код состояния 200 указывает, что ресурс доступен и запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ae727-169">A 200 status code indicates that the resource is available and the request is successful.</span></span> <span data-ttu-id="ae727-170">Дополнительные коды состояния, которые могут быть возвращены, см. в разделе [**коды состояния HTTP**](http-status-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ae727-170">See [**HTTP Status Codes**](http-status-codes.md) for additional status codes that can be returned.</span></span>

<span data-ttu-id="ae727-171">Если допустимая схема проверки подлинности и учетные данные известны до отправки запроса на сервер, приложение может вызвать [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) перед вызовом [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="ae727-171">If an acceptable authentication scheme and credentials are known before a request is sent to the server, an application can call [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) before calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="ae727-172">В этом случае WinHTTP пытается выполнить предварительную проверку подлинности на сервере, предоставляя учетные данные или [*данные проверки подлинности*](glossary.md) в исходном запросе к серверу.</span><span class="sxs-lookup"><span data-stu-id="ae727-172">In this case, WinHTTP attempts pre-authentication with the server by providing credentials or [*authentication data*](glossary.md) in the initial request to the server.</span></span> <span data-ttu-id="ae727-173">Предварительная проверка подлинности может уменьшить количество обменов в процессе проверки подлинности и, таким образом, повысить производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="ae727-173">Pre-authentication can decrease the number of exchanges in the authentication process and therefore improve application performance.</span></span>

<span data-ttu-id="ae727-174">Предварительная проверка подлинности может использоваться со следующими схемами проверки подлинности:</span><span class="sxs-lookup"><span data-stu-id="ae727-174">Preauthentication can be used with the following authentication schemes:</span></span>

-   <span data-ttu-id="ae727-175">Basic — всегда возможно.</span><span class="sxs-lookup"><span data-stu-id="ae727-175">Basic - always possible.</span></span>
-   <span data-ttu-id="ae727-176">Согласованное разрешение в Kerberos — очень вероятно, возможно; Единственным исключением является то, что неравномерное распределение времени между клиентом и контроллером домена.</span><span class="sxs-lookup"><span data-stu-id="ae727-176">Negotiate resolving into Kerberos - very likely possible; the only exception is when the time-skews are off between the client and the domain controller.</span></span>
-   <span data-ttu-id="ae727-177">(Согласование разрешения в NTLM) — никогда не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ae727-177">(Negotiate resolving into NTLM) - never possible.</span></span>
-   <span data-ttu-id="ae727-178">NTLM — возможно только в Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ae727-178">NTLM - possible in Windows Server 2008 R2 only.</span></span>
-   <span data-ttu-id="ae727-179">Дайджест — никогда не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ae727-179">Digest - never possible.</span></span>
-   <span data-ttu-id="ae727-180">Passport — никогда не поддерживается; После первоначального ответа на запрос служба WinHTTP использует файлы cookie для предварительной проверки подлинности в Passport.</span><span class="sxs-lookup"><span data-stu-id="ae727-180">Passport - never possible; after the initial challenge-response, WinHTTP uses cookies to pre-authenticate to Passport.</span></span>

<span data-ttu-id="ae727-181">Стандартное приложение WinHTTP выполняет следующие действия, чтобы обеспечить проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae727-181">A typical WinHTTP application completes the following steps in order to handle authentication.</span></span>

-   <span data-ttu-id="ae727-182">Запросите ресурс с помощью [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) и [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="ae727-182">Request a resource with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) and [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>
-   <span data-ttu-id="ae727-183">Проверьте заголовки ответа с помощью [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="ae727-183">Check the response headers with [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
-   <span data-ttu-id="ae727-184">Если возвращается код состояния 401 или 407, указывающий на необходимость проверки подлинности, вызовите [**винхттпкуеряуссчемес**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) , чтобы найти допустимую схему.</span><span class="sxs-lookup"><span data-stu-id="ae727-184">If a 401 or 407 status code is returned indicating that authentication is required, call [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) to find an acceptable scheme.</span></span>
-   <span data-ttu-id="ae727-185">Задайте схему проверки подлинности, имя пользователя и пароль с помощью [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span><span class="sxs-lookup"><span data-stu-id="ae727-185">Set the authentication scheme, username, and password with [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span></span>
-   <span data-ttu-id="ae727-186">Повторно отправьте запрос с тем же маркером запроса, вызвав [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="ae727-186">Resend the request with the same request handle by calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

<span data-ttu-id="ae727-187">Учетные данные, установленные [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) , используются только для одного запроса.</span><span class="sxs-lookup"><span data-stu-id="ae727-187">The credentials set by [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) are only used for one request.</span></span> <span data-ttu-id="ae727-188">Служба WinHTTP не кэширует учетные данные для использования в других запросах. Это означает, что приложения должны быть написаны, которые могут отвечать на несколько запросов.</span><span class="sxs-lookup"><span data-stu-id="ae727-188">WinHTTP does not cache the credentials to use in other requests, which means that applications must be written that can respond to multiple requests.</span></span> <span data-ttu-id="ae727-189">Если подключение с проверкой подлинности используется повторно, другие запросы могут быть не вызваны, но ваш код должен иметь возможность отвечать на запросы в любое время.</span><span class="sxs-lookup"><span data-stu-id="ae727-189">If an authenticated connection is re-used, other requests may not be challenged, but your code should be able to respond to a request at any time.</span></span>

### <a name="example-retrieving-a-document"></a><span data-ttu-id="ae727-190">Пример. получение документа</span><span class="sxs-lookup"><span data-stu-id="ae727-190">Example: Retrieving a Document</span></span>

<span data-ttu-id="ae727-191">Следующий пример кода пытается получить указанный документ с HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="ae727-191">The following sample code attempts to retrieve a specified document from an HTTP server.</span></span> <span data-ttu-id="ae727-192">Код состояния извлекается из ответа, чтобы определить, требуется ли проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae727-192">The status code is retrieved from the response to determine if authentication is required.</span></span> <span data-ttu-id="ae727-193">Если код состояния 200 найден, документ становится доступным.</span><span class="sxs-lookup"><span data-stu-id="ae727-193">If a 200 status code is found, the document is available.</span></span> <span data-ttu-id="ae727-194">Если обнаружен код состояния 401 или 407, для извлечения документа требуется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae727-194">If a status code of 401 or 407 is found, authentication is required before the document can be retrieved.</span></span> <span data-ttu-id="ae727-195">Для любого другого кода состояния выводится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ae727-195">For any other status code, an error message is displayed.</span></span> <span data-ttu-id="ae727-196">Список возможных кодов состояния см. в разделе [**коды состояния HTTP**](http-status-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ae727-196">See [**HTTP Status Codes**](http-status-codes.md) for a list of possible status codes.</span></span>


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



## <a name="automatic-logon-policy"></a><span data-ttu-id="ae727-197">Политика автоматического входа в систему</span><span class="sxs-lookup"><span data-stu-id="ae727-197">Automatic Logon Policy</span></span>

<span data-ttu-id="ae727-198">Политика автоматического входа в систему (автоматический вход в систему) определяет, когда служба WinHTTP может включать в запрос учетные данные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae727-198">The automatic logon (auto-logon) policy determines when it is acceptable for WinHTTP to include the default credentials in a request.</span></span> <span data-ttu-id="ae727-199">Учетные данные по умолчанию — это либо текущий маркер потока, либо маркер сеанса, в зависимости от того, используется ли WinHTTP в синхронном или асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="ae727-199">The default credentials are either the current thread token or the session token depending on whether WinHTTP is used in synchronous or asynchronous mode.</span></span> <span data-ttu-id="ae727-200">Токен потока используется в синхронном режиме, а маркер сеанса используется в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="ae727-200">The thread token is used in synchronous mode, and the session token is used in asynchronous mode.</span></span> <span data-ttu-id="ae727-201">Эти учетные данные часто являются именем пользователя и паролем, используемыми для входа в систему Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ae727-201">These default credentials are often the username and password used to log on to Microsoft Windows.</span></span>

<span data-ttu-id="ae727-202">Политика автоматического входа была реализована, чтобы предотвратить случайное использование этих учетных данных для проверки подлинности на недоверенном сервере.</span><span class="sxs-lookup"><span data-stu-id="ae727-202">The auto-logon policy was implemented to prevent these credentials from being casually used to authenticate against an untrusted server.</span></span> <span data-ttu-id="ae727-203">По умолчанию для уровня безопасности задано значение уровень \_ безопасности автоматического входа WinHTTP \_ \_ \_ Medium, что позволяет использовать учетные данные по умолчанию только для запросов в интрасети.</span><span class="sxs-lookup"><span data-stu-id="ae727-203">By default, the security level is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM, which allows the default credentials to be used only for Intranet requests.</span></span> <span data-ttu-id="ae727-204">Политика автоматического входа применяется только к схемам проверки подлинности NTLM и Negotiate.</span><span class="sxs-lookup"><span data-stu-id="ae727-204">The auto-logon policy only applies to the NTLM and Negotiate authentication schemes.</span></span> <span data-ttu-id="ae727-205">Учетные данные никогда не передаются автоматически с другими схемами.</span><span class="sxs-lookup"><span data-stu-id="ae727-205">Credentials are never automatically transmitted with other schemes.</span></span>

<span data-ttu-id="ae727-206">Политику автоматического входа можно задать с помощью функции [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с флагом WinHTTP для [**\_ параметра \_ Autologon \_**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="ae727-206">The auto-logon policy can be set using the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function with the [**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**](option-flags.md) flag.</span></span> <span data-ttu-id="ae727-207">Этот флаг применяется только к обработчику запроса.</span><span class="sxs-lookup"><span data-stu-id="ae727-207">This flag applies only to the request handle.</span></span> <span data-ttu-id="ae727-208">Если для политики задано значение \_ \_ низкий уровень безопасности автоматического входа WinHTTP \_ \_ , учетные данные по умолчанию могут отправляться на все серверы.</span><span class="sxs-lookup"><span data-stu-id="ae727-208">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW, default credentials can be sent to all servers.</span></span> <span data-ttu-id="ae727-209">Если для политики задано значение \_ \_ высокий уровень безопасности автоматического входа WinHTTP \_ \_ , учетные данные по умолчанию нельзя использовать для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae727-209">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH, default credentials cannot be used for authentication.</span></span> <span data-ttu-id="ae727-210">Настоятельно рекомендуется использовать автоматический вход на среднем уровне.</span><span class="sxs-lookup"><span data-stu-id="ae727-210">It is strongly recommended that you use the auto-logon at the MEDIUM level.</span></span>

## <a name="stored-user-names-and-passwords"></a><span data-ttu-id="ae727-211">Сохранение имен пользователей и паролей</span><span class="sxs-lookup"><span data-stu-id="ae727-211">Stored User Names and Passwords</span></span>

<span data-ttu-id="ae727-212">В Windows XP была представлена концепция сохраненных имен пользователей и паролей.</span><span class="sxs-lookup"><span data-stu-id="ae727-212">Windows XP introduced the concept of Stored User Names and Passwords.</span></span> <span data-ttu-id="ae727-213">Если учетные данные пользователя Passport сохраняются с помощью **мастера регистрации паспорта** или стандартного **диалогового окна учетных данных**, они сохраняются в сохраненных именах пользователей и паролях.</span><span class="sxs-lookup"><span data-stu-id="ae727-213">If a user's Passport credentials are saved through the **Passport Registration Wizard** or the standard **Credential Dialog**, it is saved in the Stored User Names and Passwords.</span></span> <span data-ttu-id="ae727-214">При использовании WinHTTP в Windows XP или более поздней версии WinHTTP автоматически использует учетные данные в сохраненных именах пользователей и паролях, если учетные данные не заданы явно.</span><span class="sxs-lookup"><span data-stu-id="ae727-214">When using WinHTTP on Windows XP or later, WinHTTP automatically uses the credentials in the Stored User Names and Passwords if credentials are not explicitly set.</span></span> <span data-ttu-id="ae727-215">Это похоже на поддержку учетных данных входа по умолчанию для NTLM/Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ae727-215">This is similar to the support of default logon credentials for NTLM/Kerberos.</span></span> <span data-ttu-id="ae727-216">Однако использование учетных данных паспорта по умолчанию не подчиняется параметрам политики автоматического входа.</span><span class="sxs-lookup"><span data-stu-id="ae727-216">However, use of default Passport credentials is not subject to the automatic logon policy settings.</span></span>

 

 



