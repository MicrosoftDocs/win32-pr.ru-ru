---
Description: В Винхттпкуерйоптион и Винхттпсетоптион поддерживаются следующие флаги параметров.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Флаги параметров (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 25049ee11c59c6b320b794c07bd65e5ec9b930c9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395419"
---
# <a name="option-flags"></a><span data-ttu-id="fc010-103">Флаги параметров</span><span class="sxs-lookup"><span data-stu-id="fc010-103">Option Flags</span></span>

<span data-ttu-id="fc010-104">В [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) и [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)поддерживаются следующие флаги параметров.</span><span class="sxs-lookup"><span data-stu-id="fc010-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="fc010-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_параметр WinHTTP \_ — \_ \_ неблокирующие \_ обратные вызовы**</span><span class="sxs-lookup"><span data-stu-id="fc010-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-106">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="fc010-106">The default is FALSE.</span></span> <span data-ttu-id="fc010-107">Если задано значение TRUE, служба WinHTTP не гарантирует ход выполнения, если клиентское приложение блокирует обратные вызовы состояния.</span><span class="sxs-lookup"><span data-stu-id="fc010-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="fc010-108">Клиентское приложение должно соблюдать особое внимание для выполнения минимальных операций в обратном вызове без блокировки, возврата как можно быстрее, а в частности не должен ждать последующего вызова WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="fc010-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="fc010-109">Если это не соответствует этим рекомендациям, вероятно, это отрицательное воздействие на производительность или зависание приложения.</span><span class="sxs-lookup"><span data-stu-id="fc010-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="fc010-110">Если используется заранее, этот параметр может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="fc010-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**\_ \_ политика автоматического входа в службу WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-112">Задает длинное целочисленное значение без знака, определяющее [политику автоматического входа в систему](authentication-in-winhttp.md) с одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fc010-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="fc010-113">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-113">Term</span></span> | <span data-ttu-id="fc010-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-114">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>\_ \_ \_ высокий уровень безопасности автоматического входа \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="fc010-116">Учетные данные по умолчанию не используются.</span><span class="sxs-lookup"><span data-stu-id="fc010-116">Default credentials are not used.</span></span> <span data-ttu-id="fc010-117">Обратите внимание, что этот флаг вступает в силу только в том случае, если сервер задается фактическим именем компьютера.</span><span class="sxs-lookup"><span data-stu-id="fc010-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="fc010-118">Он не вступит в силу, если сервер указывается как localhost или IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="fc010-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="fc010-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>\_ \_ \_ низкий уровень безопасности автоматического входа \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="fc010-120">Вход с проверкой подлинности с использованием учетных данных по умолчанию выполняется для всех запросов.</span><span class="sxs-lookup"><span data-stu-id="fc010-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="fc010-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>\_уровень безопасности автоматического входа WinHTTP — \_ \_ \_ средний</span><span class="sxs-lookup"><span data-stu-id="fc010-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="fc010-122">Вход с проверкой подлинности с использованием учетных данных по умолчанию выполняется только для запросов в локальной интрасети.</span><span class="sxs-lookup"><span data-stu-id="fc010-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="fc010-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**\_Параметры WinHTTP \_ фоновых \_ подключений**</span><span class="sxs-lookup"><span data-stu-id="fc010-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc010-124">Если этот параметр задан для обработчика сеанса, необходимо передать число открываемых подключений.</span><span class="sxs-lookup"><span data-stu-id="fc010-124">When you set this option on a session handle, you must pass the number of connections you wish to open.</span></span> <span data-ttu-id="fc010-125">Затем, при первой отправке запроса, вместо того, чтобы открывать только одно соединение, служба WinHttp открывает несколько подключений параллельно.</span><span class="sxs-lookup"><span data-stu-id="fc010-125">Then, upon first sending a request, rather than opening only a single connection, WinHttp opens a number of connections in parallel.</span></span> <span data-ttu-id="fc010-126">Это может повысить производительность последующих запросов к тому же назначению, что не приведет к излишней нагрузке на подключение.</span><span class="sxs-lookup"><span data-stu-id="fc010-126">This can improve the performance of subsequent requests to the same destination, which won't have the overhead of connection establishment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_ \_ обратный вызов параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-128">Получает указатель на функцию обратного вызова, заданную с помощью [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="fc010-128">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_ \_ \_ контекст сертификата клиента для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-130">Задает контекст сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="fc010-130">Sets the client certificate context.</span></span> <span data-ttu-id="fc010-131">Если приложение получает [**сообщение об ошибке " \_ \_ \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP**](error-messages.md)", он должен вызвать [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) для предоставления сертификата, прежде чем повторять запрос.</span><span class="sxs-lookup"><span data-stu-id="fc010-131">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="fc010-132">В ходе обработки этого параметра служба WinHttp вызывает [**цертдупликатецертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) в контексте сертификата, предоставленного вызывающим объектом, чтобы контекст сертификата можно было независимо освободить от вызывающего.</span><span class="sxs-lookup"><span data-stu-id="fc010-132">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="fc010-133">Приложению не следует попытаться закрыть хранилище сертификатов с помощью \_ флага "Close" ( \_ \_ Сбросить флаг принудительного восстановления сертификата) \_ в вызове [**цертклосесторе**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) в хранилище сертификатов, из которого был получен контекст сертификата.</span><span class="sxs-lookup"><span data-stu-id="fc010-133">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="fc010-134">Может произойти нарушение прав доступа.</span><span class="sxs-lookup"><span data-stu-id="fc010-134">An access violation may occur.</span></span>

<span data-ttu-id="fc010-135">Когда сервер запрашивает сертификат клиента, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)или [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) возвращает [**ошибку, \_ \_ \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP**](error-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="fc010-135">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="fc010-136">Если сервер запрашивает сертификат, но не требует его, приложение может указать этот параметр, чтобы указать, что у него нет сертификата.</span><span class="sxs-lookup"><span data-stu-id="fc010-136">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="fc010-137">Сервер может выбрать другую схему проверки подлинности или разрешить анонимный доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="fc010-137">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="fc010-138">Приложение предоставляет **\_ \_ \_ \_ Контекстный макрос WinHTTP No Client** Certificate в параметре *лпбуффер* объекта [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="fc010-138">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="fc010-139">Если серверу требуется сертификат клиента, он может отправить код состояния HTTP 403 в ответе.</span><span class="sxs-lookup"><span data-stu-id="fc010-139">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="fc010-140">Дополнительные сведения см. в описании параметра **WinHTTP Certificate \_ \_ Client \_ CERT \_ Issuer \_** .</span><span class="sxs-lookup"><span data-stu-id="fc010-140">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_ \_ \_ \_ список поставщиков сертификатов клиента для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-142">Извлекает структуру [**\_ иссуерлистинфоекс секпкгконтекст**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , когда ошибка из [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) или [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) является **ошибкой \_ \_ \_ сертификата проверки подлинности \_ \_ клиента WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="fc010-142">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="fc010-143">Список издателей в структуре содержит список приемлемых центров сертификации (ЦС) с сервера.</span><span class="sxs-lookup"><span data-stu-id="fc010-143">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="fc010-144">Клиентское приложение может отфильтровать список центров сертификации, чтобы получить сертификат клиента для проверки подлинности SSL.</span><span class="sxs-lookup"><span data-stu-id="fc010-144">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="fc010-145">Кроме того, если сервер запрашивает сертификат клиента, но не требует его, приложение может вызвать [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с параметром **\_ контекста WinHTTP параметр \_ \_ сертификата \_ клиента** .</span><span class="sxs-lookup"><span data-stu-id="fc010-145">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="fc010-146">Дополнительные сведения см. в описании параметра службы **WinHTTP \_ параметр \_ \_ \_ контекста сертификата клиента** .</span><span class="sxs-lookup"><span data-stu-id="fc010-146">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**\_ \_ кодовая страница параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-148">Задает [*кодовую страницу*](glossary.md) , используемую для обработки URL-адреса (то есть строки запроса).</span><span class="sxs-lookup"><span data-stu-id="fc010-148">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="fc010-149">По умолчанию используется значение UTF8.</span><span class="sxs-lookup"><span data-stu-id="fc010-149">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_параметр WinHTTP \_ Настройка \_ \_ проверки подлинности паспорта**</span><span class="sxs-lookup"><span data-stu-id="fc010-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-151">Задает длинное целое число без знака, указывающее, включена ли [Проверка подлинности Passport при](passport-authentication-in-winhttp.md) проверке подлинности WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="fc010-151">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="fc010-152">Он может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fc010-152">The value can be one of the following:</span></span>

| <span data-ttu-id="fc010-153">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-153">Term</span></span> | <span data-ttu-id="fc010-154">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-154">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>\_Служба WinHTTP отключает проверку \_ \_ подлинности Passport</span><span class="sxs-lookup"><span data-stu-id="fc010-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="fc010-156">Microsoft Passport проверка подлинности отключена.</span><span class="sxs-lookup"><span data-stu-id="fc010-156">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="fc010-157">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc010-157">This is the default.</span></span> |
| <span data-ttu-id="fc010-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ отключение \_ набора \_ ключей паспорта</span><span class="sxs-lookup"><span data-stu-id="fc010-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="fc010-159">Набор ключей паспорта отключен.</span><span class="sxs-lookup"><span data-stu-id="fc010-159">The Passport keyring is disabled.</span></span> <span data-ttu-id="fc010-160">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc010-160">This is the default.</span></span> |
| <span data-ttu-id="fc010-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>\_Служба WinHTTP включает проверку \_ \_ подлинности паспорта</span><span class="sxs-lookup"><span data-stu-id="fc010-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="fc010-162">Проверка подлинности паспорта включена.</span><span class="sxs-lookup"><span data-stu-id="fc010-162">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="fc010-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>\_Служба WinHTTP включает набор \_ \_ ключей Passport</span><span class="sxs-lookup"><span data-stu-id="fc010-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="fc010-164">Набор ключей паспорта включен.</span><span class="sxs-lookup"><span data-stu-id="fc010-164">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="fc010-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_ \_ повторные попытки соединения с ПАРАМЕТРом WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-166">Задает или получает длинное целое число без знака, которое содержит число попыток подключения к узлу Тимесвинхттп.</span><span class="sxs-lookup"><span data-stu-id="fc010-166">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="fc010-167">Службы Microsoft Windows HTTP (WinHTTP) пытаются попытаться только один раз на IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="fc010-167">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="fc010-168">Например, при попытке подключиться к многосетевому узлу, имеющему 10 IP-адресов, а **\_ параметру WinHTTP \_ \_ попыток подключения** будет присвоено значение 7, служба WinHTTP попытается подключиться только к первым семи IP-адресам.</span><span class="sxs-lookup"><span data-stu-id="fc010-168">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="fc010-169">Если один набор из 10 IP-адресов установлен в значение 20, то служба WinHTTP попытается выполнить каждую из 10 только один раз. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-169">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="fc010-170">Если попытка соединения по-прежнему завершается неудачей после указанного числа попыток или если время ожидания соединения истекло раньше, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="fc010-170">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="fc010-171">Значение по умолчанию **для \_ параметра \_ \_ WinHTTP** — пять попыток.</span><span class="sxs-lookup"><span data-stu-id="fc010-171">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**\_ \_ время ожидания соединения для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-173">Задает или получает длинное целое число без знака, содержащее значение времени ожидания в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="fc010-173">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="fc010-174">Если установить для этого параметра значение Infinite (0xFFFFFFFF), этот таймер будет отключен.</span><span class="sxs-lookup"><span data-stu-id="fc010-174">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="fc010-175">Если запрос на TCP-соединение длится дольше этого значения времени ожидания, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="fc010-175">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="fc010-176">Время ожидания по умолчанию — 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="fc010-176">The default timeout is 60 seconds.</span></span> <span data-ttu-id="fc010-177">При попытке подключения к нескольким IP-адресам для одного узла (многосетевой узел) для каждого отдельного соединения устанавливается ограничение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="fc010-177">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**\_ \_ сведения о соединении параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-179">Извлекает исходный и конечный IP-адрес и порт запроса, который создал ответ при возвращении [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) .</span><span class="sxs-lookup"><span data-stu-id="fc010-179">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="fc010-180">Приложение вызывает [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) с параметром **WinHTTP \_ \_ \_ сведения о соединении** и предоставляет структуру [**\_ \_ сведений о соединении WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) в параметре *лпбуффер* .</span><span class="sxs-lookup"><span data-stu-id="fc010-180">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="fc010-181">Дополнительные сведения см. в **разделе \_ \_ сведения о подключении к WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="fc010-181">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="fc010-182">**Windows Server 2003 с пакетом обновления SP1 и Windows XP с пакетом обновления 2 (SP2):** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="fc010-182">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_Параметр WinHTTP \_ Connection \_ stats \_ v0**</span><span class="sxs-lookup"><span data-stu-id="fc010-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-184">Извлекает структуру [**TCP \_ info \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) для базового соединения, используемого запросом.</span><span class="sxs-lookup"><span data-stu-id="fc010-184">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="fc010-185">Возвращаемая структура может содержать статистику предыдущих запросов, отправленных по тому же соединению.</span><span class="sxs-lookup"><span data-stu-id="fc010-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="fc010-186">Этот параметр был заменен **\_ параметром WinHTTP \_ Connection \_ stats \_ v1**.</span><span class="sxs-lookup"><span data-stu-id="fc010-186">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Параметр WinHTTP \_ Connection \_ stats \_ v1**</span><span class="sxs-lookup"><span data-stu-id="fc010-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-188">Извлекает структуру [**TCP \_ \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) для базового соединения, используемого запросом.</span><span class="sxs-lookup"><span data-stu-id="fc010-188">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="fc010-189">Возвращаемая структура может содержать статистику предыдущих запросов, отправленных по тому же соединению.</span><span class="sxs-lookup"><span data-stu-id="fc010-189">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_ \_ значение контекста WinHTTP для параметра \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-191">Задает или получает **двойное слово \_ типа DWORD** , содержащее указатель на значение контекста, связанное с этим [хинтернет](hinternet-handles-in-winhttp.md) -обработчиком.</span><span class="sxs-lookup"><span data-stu-id="fc010-191">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="fc010-192">Используется значение, хранящееся в буфере, а для флага Option **\_ \_ \_ значения контекста WinHTTP** задано новое значение.</span><span class="sxs-lookup"><span data-stu-id="fc010-192">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**\_ \_ распаковка параметров WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-194">Задает параметр DWORD флагов, который определяет, будет ли WinHTTP автоматически распаковывать текст ответа с сжатыми кодировками содержимого.</span><span class="sxs-lookup"><span data-stu-id="fc010-194">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="fc010-195">WinHTTP также установит соответствующий заголовок Accept-Encoding, переопределив все, предоставленные вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="fc010-195">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="fc010-196">Поддерживаются значения:</span><span class="sxs-lookup"><span data-stu-id="fc010-196">Supported values are:</span></span>

| <span data-ttu-id="fc010-197">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-197">Term</span></span> | <span data-ttu-id="fc010-198">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-198">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_флаг распаковки \_ WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="fc010-200">Распаковка содержимого в кодировке: отклики gzip.</span><span class="sxs-lookup"><span data-stu-id="fc010-200">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="fc010-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_ДЕуплотнение \_ ФЛАГа РАСПАКОВКи WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="fc010-202">Распаковка содержимого в кодировке: разворачивает ответы.</span><span class="sxs-lookup"><span data-stu-id="fc010-202">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="fc010-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_ \_ все ФЛАГи РАСПАКОВКи WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="fc010-204">Распаковка ответов с любой поддерживаемой кодировкой содержимого.</span><span class="sxs-lookup"><span data-stu-id="fc010-204">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="fc010-205">По умолчанию WinHTTP будет доставлять сжатые ответы вызывающему объекту без изменений.</span><span class="sxs-lookup"><span data-stu-id="fc010-205">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**\_параметр WinHTTP \_ Отключить \_ \_ Построение цепочки сертификатов \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="fc010-207">Установка этого параметра для обработчика сеанса WinHttp позволяет включить или отключить сборку цепочки сертификатов сервера.</span><span class="sxs-lookup"><span data-stu-id="fc010-207">Setting this option on a WinHttp session handle allows you to enable/disable whether the server certificate chain is built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**\_ \_ функция отключения параметров \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-209">Задает длинное целочисленное значение без знака, указывающее, какие функции отключены с помощью одного или нескольких из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="fc010-209">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="fc010-210">Имейте в виду, что эта функция должна передаваться только в [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) в дескрипторах запросов после создания дескриптора запроса с помощью [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)и перед отправкой запроса с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="fc010-210">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="fc010-211">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-211">Term</span></span> | <span data-ttu-id="fc010-212">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-212">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ отключение \_ проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="fc010-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="fc010-214">Автоматическая проверка подлинности отключена.</span><span class="sxs-lookup"><span data-stu-id="fc010-214">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="fc010-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ отключение \_ файлов cookie</span><span class="sxs-lookup"><span data-stu-id="fc010-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="fc010-216">Автоматическое добавление заголовков файлов cookie в запросы отключено.</span><span class="sxs-lookup"><span data-stu-id="fc010-216">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="fc010-217">Кроме того, возвращенные файлы cookie не добавляются автоматически в базу данных cookie.</span><span class="sxs-lookup"><span data-stu-id="fc010-217">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="fc010-218">Отключение файлов cookie может привести к низкой производительности проверки подлинности Passport.</span><span class="sxs-lookup"><span data-stu-id="fc010-218">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="fc010-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>\_отключение \_ поддержания \_ активности WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="fc010-220">Отключает семантику поддержания активности для соединения.</span><span class="sxs-lookup"><span data-stu-id="fc010-220">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="fc010-221">Семантика проверки активности требуется для MSN, NTLM и других типов аутентификации.</span><span class="sxs-lookup"><span data-stu-id="fc010-221">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="fc010-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>\_отключение \_ ПЕРЕнаправлений WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="fc010-223">Автоматическое перенаправление отключено при отправке запросов с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="fc010-223">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="fc010-224">Если автоматическое перенаправление отключено, приложение должно зарегистрировать функцию обратного вызова, чтобы обеспечить успешную проверку подлинности Passport.</span><span class="sxs-lookup"><span data-stu-id="fc010-224">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="fc010-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_параметр WinHTTP \_ Отключить \_ откат безопасных \_ протоколов \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-226">Предотвращает повторное выполнение службой WinHTTP соединения с более ранней версией протокола безопасности при сбое согласования первоначального протокола.</span><span class="sxs-lookup"><span data-stu-id="fc010-226">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**\_параметр WinHTTP \_ Отключить \_ \_ очередь потока**</span><span class="sxs-lookup"><span data-stu-id="fc010-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-228">Позволяет новым запросам открывать дополнительное соединение HTTP/2 при достижении максимального количества одновременных потоков, а не ждать следующего доступного потока в существующем соединении.</span><span class="sxs-lookup"><span data-stu-id="fc010-228">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**\_ \_ Включение \_ функции WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-230">Задает длинное целое число без знака, определяющее включенные в данный момент функции.</span><span class="sxs-lookup"><span data-stu-id="fc010-230">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="fc010-231">Может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fc010-231">Can be one of the following values.</span></span>

| <span data-ttu-id="fc010-232">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-232">Term</span></span> | <span data-ttu-id="fc010-233">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-233">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ Включение \_ \_ олицетворения при отмене SSL \_</span><span class="sxs-lookup"><span data-stu-id="fc010-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="fc010-235">Если параметр включен, WinHTTP временно восстанавливает олицетворение клиента на время выполнения операций аутентификации SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="fc010-235">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="fc010-236">Это значение может быть задано только в обработчике сеанса.</span><span class="sxs-lookup"><span data-stu-id="fc010-236">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="fc010-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ Включение \_ \_ отзыва SSL</span><span class="sxs-lookup"><span data-stu-id="fc010-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="fc010-238">Если этот режим включен, WinHTTP разрешает отзыв SSL.</span><span class="sxs-lookup"><span data-stu-id="fc010-238">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="fc010-239">Это значение можно задать только в обработчике запроса.</span><span class="sxs-lookup"><span data-stu-id="fc010-239">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_параметр WinHTTP \_ Включение \_ \_ протокола HTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-241">Задает битовую маску DWORD допустимых расширенных версий HTTP.</span><span class="sxs-lookup"><span data-stu-id="fc010-241">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="fc010-242">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fc010-242">Possible values are:</span></span>

| <span data-ttu-id="fc010-243">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-243">Term</span></span> | <span data-ttu-id="fc010-244">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-244">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_Флаг протокола \_ WinHTTP \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="fc010-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="fc010-246">Включает HTTP/2 для запроса.</span><span class="sxs-lookup"><span data-stu-id="fc010-246">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="fc010-247">Нет (0x0)</span><span class="sxs-lookup"><span data-stu-id="fc010-247">None (0x0)</span></span> | <span data-ttu-id="fc010-248">Разрешает запрос в формате HTTP/1.1 и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="fc010-248">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="fc010-249">Устаревшие версии протокола HTTP (1,1 и более ранних версий) нельзя отключить с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="fc010-249">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="fc010-250">Значение по умолчанию — 0x0.</span><span class="sxs-lookup"><span data-stu-id="fc010-250">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**\_Параметр WinHTTP \_ включить \_ \_ \_ сертификат клиента HTTP2 \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="fc010-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="fc010-252">Этот параметр можно задать для обработчика сеанса WinHttp, чтобы разрешить WinHttp использовать контекст сертификата клиента, предоставленный вызывающим объектом, при использовании HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="fc010-252">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_параметр WinHTTP \_ енаблетраЦинг**</span><span class="sxs-lookup"><span data-stu-id="fc010-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-254">Задает **логическое** значение, указывающее, включена ли трассировка в данный момент.</span><span class="sxs-lookup"><span data-stu-id="fc010-254">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="fc010-255">Дополнительные сведения о средстве трассировки в WinHTTP см. в разделе [средство трассировки WinHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="fc010-255">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="fc010-256">Этот параметр можно задать только для **нулевого** маркера **хинтернет** .</span><span class="sxs-lookup"><span data-stu-id="fc010-256">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="fc010-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**\_ \_ добавочная кодировка параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-258">Включает кодировку URL в процентах для пути и строки запроса.</span><span class="sxs-lookup"><span data-stu-id="fc010-258">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="fc010-259">Кроме того, можно закодировать процент перед вызовом WinHttp.</span><span class="sxs-lookup"><span data-stu-id="fc010-259">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="fc010-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**\_ \_ срок действия соединения для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-261">Этот параметр может быть установлен только для того обработчика запроса, который все еще активен (отправка или получение).</span><span class="sxs-lookup"><span data-stu-id="fc010-261">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="fc010-262">Установка этого параметра сообщит службе WinHttp о необходимости прекращать обслуживание запросов в соединении, связанном с переданным маркером запроса.</span><span class="sxs-lookup"><span data-stu-id="fc010-262">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="fc010-263">Соединение будет закрыто после того, как обработчик запроса вызывает этот параметр с завершенным.</span><span class="sxs-lookup"><span data-stu-id="fc010-263">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="fc010-264">Этот параметр не принимает никаких параметров.</span><span class="sxs-lookup"><span data-stu-id="fc010-264">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ Расширенная ошибка при выборе WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-266">Извлекает длинное целое число без знака, содержащее код ошибки сокетов Microsoft Windows, сопоставленный с ошибкой сообщения WinHTTP, которые были \_ \_ \* возвращены в данном контексте потока.</span><span class="sxs-lookup"><span data-stu-id="fc010-266">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="fc010-267">В качестве значения Handle можно передать значение **null** .</span><span class="sxs-lookup"><span data-stu-id="fc010-267">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**\_параметр WinHTTP \_ первое \_ доступное \_ подключение**</span><span class="sxs-lookup"><span data-stu-id="fc010-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="fc010-269">По умолчанию, когда служба WinHttp отправляет запрос, если нет доступных соединений для обслуживания запроса, служба WinHttp попытается установить новое соединение, и запрос будет привязан к этому новому соединению.</span><span class="sxs-lookup"><span data-stu-id="fc010-269">By default, when WinHttp sends a request, if there are no available connections to serve the request, WinHttp will attempt to establish a new connection, and the request will be bound to this new connection.</span></span> <span data-ttu-id="fc010-270">При задании этого параметра такой запрос будет обрабатываться в первом соединении, которое становится доступным, и не обязательно должно быть установлено.</span><span class="sxs-lookup"><span data-stu-id="fc010-270">When you set this option, such a request will instead be served on the first connection that becomes available, and not necessarily the one being established.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**\_ \_ \_ учетные записи глобального прокси-сервера параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-272">Принимает указатель на структуру с указанием учетных данных [**\_ \_ WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) с параметром функции *хинтернет* , имеющим значение **null**.</span><span class="sxs-lookup"><span data-stu-id="fc010-272">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="fc010-273">Для этого параметра требуется раздел реестра **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet параметры Интернета! Шарекредсвисвинхттп**.</span><span class="sxs-lookup"><span data-stu-id="fc010-273">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="fc010-274">Если этот раздел реестра не задан, служба WinHTTP вернет ошибку **Ошибка \_ WinHTTP \_ Недопустимый \_ параметр**.</span><span class="sxs-lookup"><span data-stu-id="fc010-274">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="fc010-275">Этот раздел реестра отсутствует по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc010-275">This registry key is not present by default.</span></span> <span data-ttu-id="fc010-276">Когда она задана, WinINet отправит учетные данные на WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="fc010-276">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="fc010-277">Всякий раз, когда WinHttp получает запрос проверки подлинности и если для текущего обработчика не заданы учетные данные, он будет использовать учетные данные, предоставляемые WinINet.</span><span class="sxs-lookup"><span data-stu-id="fc010-277">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="fc010-278">Чтобы предоставить общий доступ к учетным данным сервера в дополнение к учетным данным прокси-сервера, пользователям необходимо задать **\_ параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера** .</span><span class="sxs-lookup"><span data-stu-id="fc010-278">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**Параметры WINHTTP глобальные учетные значения \_ \_ \_ сервера \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-280">Принимает указатель на структуру с указанием учетных данных [**\_ \_ WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) с параметром функции *хинтернет* , имеющим значение **null**.</span><span class="sxs-lookup"><span data-stu-id="fc010-280">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="fc010-281">Для этого параметра требуется раздел реестра **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet параметры Интернета! Шарекредсвисвинхттп**.</span><span class="sxs-lookup"><span data-stu-id="fc010-281">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="fc010-282">Если этот раздел реестра не задан, служба WinHTTP вернет ошибку **Ошибка \_ WinHTTP \_ Недопустимый \_ параметр**.</span><span class="sxs-lookup"><span data-stu-id="fc010-282">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="fc010-283">Этот раздел реестра отсутствует по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc010-283">This registry key is not present by default.</span></span> <span data-ttu-id="fc010-284">Когда она задана, WinINet отправит учетные данные на WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="fc010-284">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="fc010-285">Всякий раз, когда WinHttp получает запрос проверки подлинности и если для текущего обработчика не заданы учетные данные, он будет использовать учетные данные, предоставляемые WinINet.</span><span class="sxs-lookup"><span data-stu-id="fc010-285">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="fc010-286">Чтобы предоставить общий доступ к учетным данным сервера в дополнение к учетным данным прокси-сервера, пользователям необходимо задать **\_ параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера** .</span><span class="sxs-lookup"><span data-stu-id="fc010-286">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**\_ \_ тип обработчика параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-288">Извлекает длинное целочисленное значение без знака, содержащее тип переданного в [хинтернет](hinternet-handles-in-winhttp.md) маркера.</span><span class="sxs-lookup"><span data-stu-id="fc010-288">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="fc010-289">Может возвращаться одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fc010-289">The return value can be one of the following:</span></span>

| <span data-ttu-id="fc010-290">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-290">Term</span></span> | <span data-ttu-id="fc010-291">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-291">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_тип обработчика WinHTTP \_ \_ Connect</span><span class="sxs-lookup"><span data-stu-id="fc010-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="fc010-293">Этот маркер является маркером соединения.</span><span class="sxs-lookup"><span data-stu-id="fc010-293">The handle is a connection handle.</span></span> |
| <span data-ttu-id="fc010-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_запрос типа для обработчика WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc010-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="fc010-295">Этот маркер является обработчиком запросов.</span><span class="sxs-lookup"><span data-stu-id="fc010-295">The handle is a request handle.</span></span> |
| <span data-ttu-id="fc010-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_сеанс типа для обработчика WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc010-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="fc010-297">Этот обработчик является обработчиком сеанса.</span><span class="sxs-lookup"><span data-stu-id="fc010-297">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="fc010-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_ \_ \_ требуется протокол HTTP для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-299">Предотвращает использование в запросе версий протокола, отличных от, включенных **\_ параметром WinHTTP, \_ Включение \_ \_ протокола HTTP** .</span><span class="sxs-lookup"><span data-stu-id="fc010-299">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**\_ \_ \_ используемый протокол HTTP \_ для параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-301">Возвращает значение типа DWORD, указывающее, какая расширенная версия HTTP использовалась для данного запроса.</span><span class="sxs-lookup"><span data-stu-id="fc010-301">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="fc010-302">Список возможных значений см. в разделе **параметр WinHTTP \_ \_ включить \_ \_ протокол HTTP**.</span><span class="sxs-lookup"><span data-stu-id="fc010-302">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_ \_ Версия HTTP параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-304">Задает или получает структуру [**\_ \_ сведений о версии HTTP**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) , которая содержит поддерживаемую версию HTTP.</span><span class="sxs-lookup"><span data-stu-id="fc010-304">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="fc010-305">Это параметр на уровне процесса; для этого маркера используйте **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="fc010-305">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**\_Параметр WinHTTP \_ HTTP2 \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="fc010-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="fc010-307">Этот параметр можно задать в обработчике сеанса, чтобы WinHttp использовала пакеты проверки связи HTTP/2 в качестве механизма KeepAlive.</span><span class="sxs-lookup"><span data-stu-id="fc010-307">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="fc010-308">Вызывающие объекты указывают время ожидания в миллисекундах, а после того, как в течение этого времени не будет активности, служба WinHttp начнет отсылать пакеты проверки связи HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="fc010-308">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="fc010-309">Вызывающие объекты не могут установить значение времени ожидания менее 5000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="fc010-309">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**\_Параметр WinHTTP \_ HTTP2 \_ и \_ \_ Кодировка перемещения**</span><span class="sxs-lookup"><span data-stu-id="fc010-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="fc010-311">Этот параметр можно задать для обработчика запросов WinHttp, чтобы управлять тем, как служба WinHttp работает, когда ответ HTTP/2 содержит заголовок "передавать данные".</span><span class="sxs-lookup"><span data-stu-id="fc010-311">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="fc010-312">В этом случае служба WinHttp возвратит ошибку, если этому параметру присвоено значение **false**.</span><span class="sxs-lookup"><span data-stu-id="fc010-312">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="fc010-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_параметр WinHTTP \_ игнорировать \_ отзыв сертификата в \_ \_ автономном режиме**</span><span class="sxs-lookup"><span data-stu-id="fc010-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-314">Позволяет защищенным подключениям использовать сертификаты безопасности, для которых не удалось скачать список отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="fc010-314">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_ \_ \_ Быстрый откат параметров WinHTTP \_ IPv6**</span><span class="sxs-lookup"><span data-stu-id="fc010-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-316">Включает быстрое резервное восстановление IPv6 (более глаз) для подключения.</span><span class="sxs-lookup"><span data-stu-id="fc010-316">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="fc010-317">Такое поведение аналогично поведению счастливого глаз, описанного в [RFC 6555](https://tools.ietf.org/html/rfc6555) , для повышения времени подключения в сетях, в которых IPv6 является ненадежным.</span><span class="sxs-lookup"><span data-stu-id="fc010-317">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="fc010-318">Если адреса IPv6 и IPv4 разрешаются для данного узла, служба WinHttp начнет с подключения к первому разрешенному IPv6-адресу с коротким (300 мс) временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="fc010-318">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="fc010-319">Если соединение не будет выполнено, служба WinHttp попытается подключиться к первому разрешенному IPv4-адресу со стандартным временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="fc010-319">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="fc010-320">Если произойдет сбой второго подключения, служба WinHttp попытается повторить первый разрешенный IPv6-адрес со стандартным временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="fc010-320">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="fc010-321">В случае сбоя третьего подключения WinHttp вернется к поведению по умолчанию для оставшихся адресов, пытаясь подключиться к каждому из них со стандартным временем ожидания до тех пор, пока не будет установлено соединение или не останется ни одного адреса.</span><span class="sxs-lookup"><span data-stu-id="fc010-321">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**\_параметр WinHTTP \_ — \_ ответ прокси- \_ подключения \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-323">Возвращает значение, указывающее, может ли быть получен ответ на возвращаемое соединение прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="fc010-323">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_Параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ \_ \_ сервер 1 0**</span><span class="sxs-lookup"><span data-stu-id="fc010-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-325">Задает или получает длинное целое число без знака, содержащее максимально допустимое количество подключений на сервер HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="fc010-325">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="fc010-326">Значение по умолчанию — **Infinite**.</span><span class="sxs-lookup"><span data-stu-id="fc010-326">The default value is **INFINITE**.</span></span>

<span data-ttu-id="fc010-327">**Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008:** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="fc010-327">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ сервер**</span><span class="sxs-lookup"><span data-stu-id="fc010-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-329">Задает или получает длинное целое число без знака, содержащее максимально допустимое количество подключений на сервер.</span><span class="sxs-lookup"><span data-stu-id="fc010-329">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="fc010-330">Значение по умолчанию — **Infinite**.</span><span class="sxs-lookup"><span data-stu-id="fc010-330">The default value is **INFINITE**.</span></span>

<span data-ttu-id="fc010-331">Если этот параметр имеет значение 0, WinHTTP устанавливает ограничение на число подключений равным 2.</span><span class="sxs-lookup"><span data-stu-id="fc010-331">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**\_параметр WinHTTP \_ Максимальное \_ число \_ автоматических \_ перенаправлений HTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-333">Задает максимальное число перенаправлений, которые следует указать WinHTTP; значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="fc010-333">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="fc010-334">Это ограничение не позволяет неавторизованным сайтам сделать остановку клиента WinHTTP после большого числа перенаправлений.</span><span class="sxs-lookup"><span data-stu-id="fc010-334">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="fc010-335">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="fc010-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_продолжение параметра \_ максимального \_ \_ состояния HTTP \_ для WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-337">Максимальное число ответов с кодом состояния 100-199, которые игнорируются перед возвратом окончательного кода состояния клиенту WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="fc010-337">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="fc010-338">Коды состояния 100-199 могут отправляться сервером перед окончательным кодом состояния и описаны в спецификации HTTP/1.1 (Дополнительные сведения см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="fc010-338">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="fc010-339">Значение по умолчанию равно 10.</span><span class="sxs-lookup"><span data-stu-id="fc010-339">The default is 10.</span></span>

<span data-ttu-id="fc010-340">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="fc010-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**параметр WINHTTP — \_ \_ максимальный \_ \_ Размер очистки ответа \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-342">Объект, привязанный к объему данных, остановленных из ответов для повторного использования соединения, указанного в байтах.</span><span class="sxs-lookup"><span data-stu-id="fc010-342">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="fc010-343">Значение по умолчанию — 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="fc010-343">The default is 1MB.</span></span>

<span data-ttu-id="fc010-344">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="fc010-344">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_параметр WinHTTP \_ максимальный \_ \_ размер заголовка \_ ответа**</span><span class="sxs-lookup"><span data-stu-id="fc010-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-346">Ограничивающий набор для максимального размера части заголовка ответа сервера, указанного в байтах.</span><span class="sxs-lookup"><span data-stu-id="fc010-346">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="fc010-347">Эта привязка защищает клиента от неавторизованного сервера, пытающегося приостановки работы клиента, отправив ответ с бесконечным объемом данных заголовка.</span><span class="sxs-lookup"><span data-stu-id="fc010-347">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="fc010-348">Значение по умолчанию — 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="fc010-348">The default value is 64KB.</span></span>

<span data-ttu-id="fc010-349">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="fc010-349">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ родительский маркер параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-351">Получает родительский маркер для этого маркера.</span><span class="sxs-lookup"><span data-stu-id="fc010-351">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**\_параметр WinHTTP \_ , \_ софирменный текст в паспорте \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-353">Извлекает строку, содержащую [*фирменный*](glossary.md) текст, предоставленный сервером входа Passport.</span><span class="sxs-lookup"><span data-stu-id="fc010-353">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="fc010-354">Этот параметр следует получать сразу после ответа сервера входа с кодом состояния 401.</span><span class="sxs-lookup"><span data-stu-id="fc010-354">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="fc010-355">Приложение должно передавать размер буфера в байтах, достаточно большой для хранения возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="fc010-355">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_ \_ \_ URL-адрес КОфирменной символики для службы WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-357">Извлекает строку, содержащую URL-адрес [*фирменной символики*](glossary.md) , предоставляемой сервером входа Passport.</span><span class="sxs-lookup"><span data-stu-id="fc010-357">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="fc010-358">Этот параметр следует получать сразу после ответа сервера входа с кодом состояния 401.</span><span class="sxs-lookup"><span data-stu-id="fc010-358">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="fc010-359">Приложение должно передавать размер буфера в байтах, достаточно большой для хранения возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="fc010-359">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_ \_ \_ \_ URL-адрес возврата паспорта с параметром WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-361">Устанавливает параметр "только для чтения" для обработчика запроса, который получает URL-адрес возврата Passport.</span><span class="sxs-lookup"><span data-stu-id="fc010-361">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**\_команда WinHTTP \_ выход \_ \_ из паспорта**</span><span class="sxs-lookup"><span data-stu-id="fc010-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-363">Задает параметр в обработчике сеанса для выхода из любых имен входа Passport.</span><span class="sxs-lookup"><span data-stu-id="fc010-363">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="fc010-364">Приложение должно передать URL-адрес возврата Passport, полученный с помощью **\_ функции WinHTTP \_ \_ \_ URL-адрес возврата Passport**.</span><span class="sxs-lookup"><span data-stu-id="fc010-364">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="fc010-365">Все файлы cookie, связанные с URL-адресом возврата, очищаются.</span><span class="sxs-lookup"><span data-stu-id="fc010-365">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_пароль для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-367">Задает или получает строковое значение, содержащее пароль, связанный с обработчиком запроса.</span><span class="sxs-lookup"><span data-stu-id="fc010-367">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_ \_ прокси-сервер параметров WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-369">Задает или получает структуру [**\_ \_ сведений о прокси-сервере WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) , которая содержит данные прокси-сервера для существующего обработчика сеанса или обработчика запроса.</span><span class="sxs-lookup"><span data-stu-id="fc010-369">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="fc010-370">При получении данных прокси-сервера приложение должно освободить строки **лпсзпрокси** и **лпсзпроксибипасс** , содержащиеся в этой структуре (если они не **равны NULL**), с помощью функции [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="fc010-370">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="fc010-371">Приложение может запросить данные глобального прокси-сервера (прокси-сервер по умолчанию), передав маркер **null** .</span><span class="sxs-lookup"><span data-stu-id="fc010-371">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_ \_ пароль прокси-сервера для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-373">Задает или получает строковое значение, содержащее пароль, используемый для доступа к прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="fc010-373">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**\_используется параметр WinHTTP \_ прокси- \_ службы \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-375">Возвращает имя участника прокси-сервера, предоставляемое WinHTTP для SSPI во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="fc010-375">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="fc010-376">Это строковое значение является усефор передачей в [**сспипромптфоркредентиалс**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) после сбоя проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="fc010-376">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_параметр WinHTTP \_ \_ имя пользователя-посредника**</span><span class="sxs-lookup"><span data-stu-id="fc010-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-378">Задает или получает строковое значение, содержащее имя пользователя, используемое для доступа к прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="fc010-378">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_ \_ \_ Размер буфера чтения параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-380">Этот параметр является устаревшим; Он не действует.</span><span class="sxs-lookup"><span data-stu-id="fc010-380">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**\_параметр WinHTTP \_ Получение \_ ответа прокси-сервера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-382">Задает, может ли быть получена сущность ответа прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="fc010-382">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="fc010-383">Этот параметр отключен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc010-383">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**\_ \_ \_ время ожидания ответа для получения параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-385">Задает или получает длинное целое число без знака, которое содержит значение времени ожидания (в миллисекундах) ожидания получения всех заголовков ответа в запрос.</span><span class="sxs-lookup"><span data-stu-id="fc010-385">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="fc010-386">Если служба WinHTTP не получает все заголовки в течение этого периода ожидания, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="fc010-386">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="fc010-387">Значение времени ожидания по умолчанию — 90 секунд.</span><span class="sxs-lookup"><span data-stu-id="fc010-387">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="fc010-388">Это время ожидания проверяется только при получении данных от сокета.</span><span class="sxs-lookup"><span data-stu-id="fc010-388">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="fc010-389">В результате, по истечении времени ожидания клиентское приложение не получает уведомления, пока не поступают дополнительные данные с сервера.</span><span class="sxs-lookup"><span data-stu-id="fc010-389">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="fc010-390">Если данные не поступают с сервера, задержка между истечением времени ожидания и уведомлением клиентского приложения может быть выше, чем значение времени ожидания, заданное с помощью параметра *дврецеиветимеаут* функции [**винхттпсеттимеаутс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .</span><span class="sxs-lookup"><span data-stu-id="fc010-390">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_ \_ время ожидания получения параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-392">Задает или получает длинное целое число без знака, которое содержит значение времени ожидания (в миллисекундах) для получения частичного ответа на запрос или чтения некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="fc010-392">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="fc010-393">Если ответ длится дольше этого значения времени ожидания, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="fc010-393">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="fc010-394">По умолчанию время ожидания составляет 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="fc010-394">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_ \_ политика перенаправления для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-396">Задает поведение WinHTTP в отношении обработки кода состояния перенаправления HTTP повышалась.</span><span class="sxs-lookup"><span data-stu-id="fc010-396">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="fc010-397">Этот параметр может быть установлен для сеанса или в обработчике запроса на одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fc010-397">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="fc010-398">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-398">Term</span></span> | <span data-ttu-id="fc010-399">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-399">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_параметр WinHTTP \_ политика перенаправления \_ \_ всегда</span><span class="sxs-lookup"><span data-stu-id="fc010-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="fc010-401">Все перенаправления выполняются автоматически.</span><span class="sxs-lookup"><span data-stu-id="fc010-401">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="fc010-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_ \_ политика перенаправления параметра WinHTTP \_ \_ запретить \_ HTTPS \_ для \_ http</span><span class="sxs-lookup"><span data-stu-id="fc010-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="fc010-403">Все перенаправления выполняются, за исключением тех, которые исходят от защищенного URL-адреса (HTTPS) на небезопасный (http) URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="fc010-403">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="fc010-404">Это параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc010-404">This is the default setting.</span></span> |
| <span data-ttu-id="fc010-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_параметр WinHTTP \_ Перенаправление \_ политики \_ никогда не</span><span class="sxs-lookup"><span data-stu-id="fc010-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="fc010-406">Перенаправления не идут.</span><span class="sxs-lookup"><span data-stu-id="fc010-406">Redirects are never followed.</span></span> <span data-ttu-id="fc010-407">Состояние повышалась возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="fc010-407">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_параметр WinHTTP \_ отклонять \_ усерпвд \_ в \_ URL-адресе**</span><span class="sxs-lookup"><span data-stu-id="fc010-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-409">Отклоняет URL-адреса, содержащие имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="fc010-409">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="fc010-410">Этот параметр также отклоняет URL-адреса, содержащие семантику *username: Password* , даже если имя пользователя или пароль не указаны.</span><span class="sxs-lookup"><span data-stu-id="fc010-410">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="fc010-411">Например, " u:p@hostname ", " :@hostname ", " u:@hostname " и " :p@hostname " будут помечены как недопустимые.</span><span class="sxs-lookup"><span data-stu-id="fc010-411">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="fc010-412">Если функции передан недопустимый URL-адрес, он возвращает [ошибку \_ WinHTTP \_ Недопустимый \_ URL-адрес](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="fc010-412">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="fc010-413">По умолчанию этот параметр выключен.</span><span class="sxs-lookup"><span data-stu-id="fc010-413">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_ \_ приоритет запроса параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-415">Этот параметр является устаревшим; Он не действует.</span><span class="sxs-lookup"><span data-stu-id="fc010-415">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_ \_ Статистика запросов параметров \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-417">Статистика извлекает для запроса.</span><span class="sxs-lookup"><span data-stu-id="fc010-417">Retreives statistics for the request.</span></span>  <span data-ttu-id="fc010-418">Список доступных статистических данных см. в разделе [**\_ \_ Статистика запросов WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="fc010-418">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_ \_ время запроса параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-420">Сведения о времени извлекает для запроса.</span><span class="sxs-lookup"><span data-stu-id="fc010-420">Retreives timing information for the request.</span></span> <span data-ttu-id="fc010-421">Список доступных времени см. в разделе [**\_ \_ время запроса WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="fc010-421">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**\_параметр WinHTTP \_ требует \_ \_ завершения потока**</span><span class="sxs-lookup"><span data-stu-id="fc010-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="fc010-423">Этот параметр указывает, что служба WinHttp пропускает заголовки ответа Content-Length и продолжает получать поток, пока не будет получен флаг END_STREAM.</span><span class="sxs-lookup"><span data-stu-id="fc010-423">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**\_ \_ имя узла для разрешения параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="fc010-425">Этот параметр можно задать для обработчика запроса WinHttp перед его отправкой.</span><span class="sxs-lookup"><span data-stu-id="fc010-425">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="fc010-426">Если задано, служба WinHttp будет использовать предоставленную вызывающей стороной строку в качестве имени узла для разрешения DNS.</span><span class="sxs-lookup"><span data-stu-id="fc010-426">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**\_ \_ время ожидания разрешения параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-428">Задает или получает длинное целое число без знака, содержащее значение времени ожидания (в миллисекундах) для разрешения имени узла.</span><span class="sxs-lookup"><span data-stu-id="fc010-428">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="fc010-429">Значение времени ожидания по умолчанию — **Infinite**.</span><span class="sxs-lookup"><span data-stu-id="fc010-429">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="fc010-430">Если указано значение, отличное от значения по умолчанию, то для разрешения имен создается дополнительная нагрузка на один поток.</span><span class="sxs-lookup"><span data-stu-id="fc010-430">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**Параметры WINHTTP для \_ \_ защищенных \_ протоколов**</span><span class="sxs-lookup"><span data-stu-id="fc010-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-432">Задает длинное целое число без знака, которое указывает, какие безопасные протоколы приемлемы.</span><span class="sxs-lookup"><span data-stu-id="fc010-432">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="fc010-433">По умолчанию в Windows 7 и Windows 8 включены только SSL3 и TLS1.</span><span class="sxs-lookup"><span data-stu-id="fc010-433">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="fc010-434">По умолчанию в Windows 8.1 и Windows 10 включены только SSL3, TLS 1.0, TLS 1.1 и TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="fc010-434">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="fc010-435">Значение может быть сочетанием одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fc010-435">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="fc010-436">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-436">Term</span></span> | <span data-ttu-id="fc010-437">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-437">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_флаг WinHTTP \_ безопасный \_ протокол \_</span><span class="sxs-lookup"><span data-stu-id="fc010-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="fc010-439">Можно использовать протоколы SSL (SSL) 2,0, SSL 3,0 и TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc010-439">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="fc010-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>SSL2 протокола WINHTTP с \_ флагом \_ Secure \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc010-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="fc010-441">Можно использовать протокол SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="fc010-441">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="fc010-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>SSL3 протокола WINHTTP с \_ флагом \_ Secure \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc010-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="fc010-443">Можно использовать протокол SSL 3,0.</span><span class="sxs-lookup"><span data-stu-id="fc010-443">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="fc010-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>TLS1 протокола WINHTTP с \_ флагом \_ Secure \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc010-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="fc010-445">Можно использовать протокол TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc010-445">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="fc010-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_Флаг WinHTTP \_ \_ протокол Secure \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="fc010-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="fc010-447">Можно использовать протокол TLS 1,1.</span><span class="sxs-lookup"><span data-stu-id="fc010-447">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="fc010-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_Флаг WinHTTP \_ \_ протокол Secure \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="fc010-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="fc010-449">Можно использовать протокол TLS 1,2.</span><span class="sxs-lookup"><span data-stu-id="fc010-449">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="fc010-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_ \_ \_ Структура сертификата безопасности параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-451">Извлекает сертификат для сервера SSL/TLS в структуру [**\_ \_ сведений о сертификате WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="fc010-451">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="fc010-452">Приложение должно освободить члены **лпсзсубжектинфо** и **Лпсзиссуеринфо** с помощью [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span><span class="sxs-lookup"><span data-stu-id="fc010-452">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_ \_ Флаги безопасности для параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-454">Задает или получает длинное целое число без знака, содержащее флаги безопасности для маркера.</span><span class="sxs-lookup"><span data-stu-id="fc010-454">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="fc010-455">Это может быть сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fc010-455">It can be a combination of these values:</span></span>

| <span data-ttu-id="fc010-456">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-456">Term</span></span> | <span data-ttu-id="fc010-457">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-457">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>\_флаг безопасности \_ игнорирует \_ \_ недопустимое общее имя сертификата \_</span><span class="sxs-lookup"><span data-stu-id="fc010-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="fc010-459">Разрешает недопустимое общее имя в сертификате; то есть имя сервера, указанное приложением, не соответствует общему имени в сертификате.</span><span class="sxs-lookup"><span data-stu-id="fc010-459">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="fc010-460">Если этот флаг установлен, приложение не получает **\_ флаг состояния обратного вызова WinHTTP \_ \_ \_ \_ \_ Недопустимый** обратный вызов для сертификата.</span><span class="sxs-lookup"><span data-stu-id="fc010-460">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="fc010-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>\_ \_ \_ \_ Недопустимый срок игнорирования даты сертификата \_ для флага безопасности</span><span class="sxs-lookup"><span data-stu-id="fc010-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="fc010-462">Разрешает недействительную дату сертификата, то есть просроченный или еще не действующий сертификат.</span><span class="sxs-lookup"><span data-stu-id="fc010-462">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="fc010-463">Если этот флаг установлен, приложение не получает **\_ \_ \_ \_ \_ \_ Недопустимый обратный вызов для флага состояния обратного вызова WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="fc010-463">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="fc010-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_ \_ пропуск \_ неизвестного \_ ЦС в качестве флага безопасности</span><span class="sxs-lookup"><span data-stu-id="fc010-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="fc010-465">Разрешает недопустимый центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="fc010-465">Allows an invalid certificate authority.</span></span> <span data-ttu-id="fc010-466">Если этот флаг установлен, приложение не получает **\_ флаг состояния обратного вызова WinHTTP \_ \_ \_ Недопустимый \_** обратный вызов CA.</span><span class="sxs-lookup"><span data-stu-id="fc010-466">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="fc010-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>\_флаг безопасности \_ игнорирует \_ \_ неправильный способ \_ использования сертификата</span><span class="sxs-lookup"><span data-stu-id="fc010-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="fc010-468">Позволяет установить удостоверение сервера с помощью сертификата, не являющегося сервером (например, сертификата клиента).</span><span class="sxs-lookup"><span data-stu-id="fc010-468">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="fc010-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_флаг безопасности \_ игнорирует \_ слабую \_ подпись</span><span class="sxs-lookup"><span data-stu-id="fc010-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="fc010-470">Позволяет игнорировать слабую подпись.</span><span class="sxs-lookup"><span data-stu-id="fc010-470">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="fc010-471">Этот флаг доступен в обновлении свертки для каждой ОС, начиная с Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fc010-471">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="fc010-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_безопасный флаг \_ безопасности</span><span class="sxs-lookup"><span data-stu-id="fc010-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="fc010-473">Использует безопасные передачи.</span><span class="sxs-lookup"><span data-stu-id="fc010-473">Uses secure transfers.</span></span> <span data-ttu-id="fc010-474">Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="fc010-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="fc010-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>уровень \_ стойкости флага безопасности \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc010-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="fc010-476">Использует среднее (56-разрядное) шифрование.</span><span class="sxs-lookup"><span data-stu-id="fc010-476">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="fc010-477">Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="fc010-477">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="fc010-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_сильная стойкость флага безопасности \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc010-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="fc010-479">Использует стойкое (128-разрядное) шифрование.</span><span class="sxs-lookup"><span data-stu-id="fc010-479">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="fc010-480">Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="fc010-480">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="fc010-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>\_ \_ слабая стойкость ФЛАГа безопасности \_</span><span class="sxs-lookup"><span data-stu-id="fc010-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="fc010-482">Использует слабое (40-разрядное) шифрование.</span><span class="sxs-lookup"><span data-stu-id="fc010-482">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="fc010-483">Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="fc010-483">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="fc010-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**\_ \_ сведения о безопасности параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-485">Извлекает подключение SChannel и сведения о шифрах для запроса.</span><span class="sxs-lookup"><span data-stu-id="fc010-485">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**\_ \_ \_ разрядность ключа безопасности параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-487">Извлекает длинное целое значение без знака, содержащее стойкость шифра ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="fc010-487">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="fc010-488">Большее число означает более надежное шифрование стойкости шифра.</span><span class="sxs-lookup"><span data-stu-id="fc010-488">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_ \_ время ожидания отправки для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-490">Задает или получает длинное целое число без знака, содержащее значение времени ожидания (в миллисекундах) для отправки запроса или записи некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="fc010-490">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="fc010-491">Если отправка запроса длится дольше, чем время ожидания, операция отправки отменяется.</span><span class="sxs-lookup"><span data-stu-id="fc010-491">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="fc010-492">По умолчанию время ожидания составляет 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="fc010-492">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**\_ \_ CBT сервера параметров \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-494">Возвращает указатель на структуру [**\_ привязок секпкгконтекст**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) , указывающую маркер привязки канала (CBT).</span><span class="sxs-lookup"><span data-stu-id="fc010-494">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="fc010-495">Токен привязки канала — это свойство защищенного канала транспорта, которое используется для привязки канала проверки подлинности к защищенному каналу транспорта.</span><span class="sxs-lookup"><span data-stu-id="fc010-495">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="fc010-496">Этот маркер может быть получен только этим параметром после установки SSL-соединения.</span><span class="sxs-lookup"><span data-stu-id="fc010-496">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="fc010-497">При передаче этого параметра и значения **null** для *лпбуффер* в [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) будет возвращена ошибка \_ , недостаточная для буфера \_ , и необходимый размер в байтах для буфера в параметре *лпдвбуфферленгс* .</span><span class="sxs-lookup"><span data-stu-id="fc010-497">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="fc010-498">Возвращаемое значение размера буфера можно передать при последующем вызове запроса для маркера привязки канала.</span><span class="sxs-lookup"><span data-stu-id="fc010-498">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="fc010-499">Эти действия необходимы при обработке \_ запроса состояния обратного вызова WinHTTP, \_ \_ Если требуется изменить заголовки запроса на основе токена привязки канала.</span><span class="sxs-lookup"><span data-stu-id="fc010-499">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="fc010-500">Обратите внимание, что Windows XP и Vista не поддерживают изменение заголовков запросов во время этого обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fc010-500">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**\_параметр WinHTTP \_ \_ \_ контекст цепочки сертификатов сервера \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-502">Извлекает контекст цепочки сертификатов сервера.</span><span class="sxs-lookup"><span data-stu-id="fc010-502">Retrieves the server certification chain context.</span></span> <span data-ttu-id="fc010-503">Служба **WinHTTP \_ \_ \_ \_ \_ Контекст цепочки сертификатов сервера** может быть передан для получения повторяющегося указателя на **\_ \_ контекст цепочки** сертификатов для цепочки сертификата сервера, полученной во время согласованного SSL-соединения.</span><span class="sxs-lookup"><span data-stu-id="fc010-503">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="fc010-504">Клиент должен вызвать [**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) для возвращенного \_ указателя контекста пкцерт, который заполнен в буфере.</span><span class="sxs-lookup"><span data-stu-id="fc010-504">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_ \_ \_ контекст сертификата сервера параметров \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-506">Получает контекст сертификации сервера.</span><span class="sxs-lookup"><span data-stu-id="fc010-506">Retrieves the server certification context.</span></span> <span data-ttu-id="fc010-507">Служба **WinHTTP \_ Для получения повторяющегося указателя на контекст сертификата сервера, полученного во время согласованного SSL-соединения, можно передать параметр \_ \_ \_ контекстного сертификата сервера** . [](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)</span><span class="sxs-lookup"><span data-stu-id="fc010-507">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="fc010-508">Клиент должен вызвать [**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) для возвращенного \_ указателя контекста пкцерт, который заполнен в буфере.</span><span class="sxs-lookup"><span data-stu-id="fc010-508">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**\_ \_ \_ используемое имя субъекта-службы сервера параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-510">Возвращает имя участника серверного сервера, которое WinHTTP было передано в SSPI во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="fc010-510">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="fc010-511">Это строковое значение может быть передано в [**сспипромптфоркредентиалс**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) после сбоя проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="fc010-511">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**\_ \_ имя субъекта-службы для параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-513">Включает или удаляет номер порта сервера, если имя участника-службы (SPN) создано для проверки подлинности Kerberos или Negotiate.</span><span class="sxs-lookup"><span data-stu-id="fc010-513">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="fc010-514">Этот флаг имеет одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fc010-514">This flag is one of the following values:</span></span>

| <span data-ttu-id="fc010-515">Термин</span><span class="sxs-lookup"><span data-stu-id="fc010-515">Term</span></span> | <span data-ttu-id="fc010-516">Описание</span><span class="sxs-lookup"><span data-stu-id="fc010-516">Description</span></span> |
|-|-|
| <span data-ttu-id="fc010-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ отключение \_ \_ порта сервера \_ SPN</span><span class="sxs-lookup"><span data-stu-id="fc010-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="fc010-518">Удаляет номер порта сервера.</span><span class="sxs-lookup"><span data-stu-id="fc010-518">Removes the server port number.</span></span> |
| <span data-ttu-id="fc010-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>\_ \_ \_ порт сервера службы WinHTTP Enable SPN \_</span><span class="sxs-lookup"><span data-stu-id="fc010-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="fc010-520">Включает номер порта сервера.</span><span class="sxs-lookup"><span data-stu-id="fc010-520">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="fc010-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**\_ \_ код ошибки в потоке параметров WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="fc010-522">Этот параметр можно запросить в обработчике запросов WinHttp и будет возвращать код ошибки, указанный RST_STREAM кадром, полученным в HTTP-потоке.</span><span class="sxs-lookup"><span data-stu-id="fc010-522">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_параметр WinHTTP \_ TCP \_ fast \_ Open**</span><span class="sxs-lookup"><span data-stu-id="fc010-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-524">Включает TCP Fast Open для подключения.</span><span class="sxs-lookup"><span data-stu-id="fc010-524">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_параметр WinHTTP \_ \_ KeepAlive TCP**</span><span class="sxs-lookup"><span data-stu-id="fc010-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-526">Этот параметр можно задать для обработчика сеанса WinHttp, чтобы включить поведение проверки активности TCP на базовом сокете.</span><span class="sxs-lookup"><span data-stu-id="fc010-526">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="fc010-527">Принимает структуру [**TCP \_ KeepAlive**](/windows/win32/winsock/sio-keepalive-vals) .</span><span class="sxs-lookup"><span data-stu-id="fc010-527">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**\_Запуск параметра WinHTTP \_ TLS \_ false \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-529">Включает для соединения параметр TLS false.</span><span class="sxs-lookup"><span data-stu-id="fc010-529">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**\_небезопасный \_ \_ \_ \_ откат протокола TLS с параметром WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-531">Этот параметр можно задать для обработчика сеанса WinHttp, чтобы указать, разрешен ли переход на TLS 1,0 в случае сбоя подтверждения TLS с более новой версией протокола.</span><span class="sxs-lookup"><span data-stu-id="fc010-531">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**\_ \_ \_ событие уведомления о ВЫгрузке параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-533">Принимает событие, которое будет задано после завершения последнего обратного вызова для определенного сеанса.</span><span class="sxs-lookup"><span data-stu-id="fc010-533">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="fc010-534">Этот флаг должен быть использован для обработчика сеанса.</span><span class="sxs-lookup"><span data-stu-id="fc010-534">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="fc010-535">Событие не может быть закрыто до тех пор, пока оно не будет установлено WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="fc010-535">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**\_ \_ \_ синтаксический анализ ненадежного заголовка для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-537">Этот параметр зарезервирован для внутреннего использования и не должен вызываться.</span><span class="sxs-lookup"><span data-stu-id="fc010-537">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_Обновление параметра \_ WinHTTP \_ до \_ веб- \_ сокета**</span><span class="sxs-lookup"><span data-stu-id="fc010-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-539">Указывает стеку запустить процесс подтверждения соединения WebSocket с [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="fc010-539">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="fc010-540">Этот параметр не принимает параметров.</span><span class="sxs-lookup"><span data-stu-id="fc010-540">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_ \_ URL-адрес параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-542">Извлекает строковое значение, содержащее полный URL-адрес скачанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc010-542">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="fc010-543">Если исходный URL-адрес содержал дополнительные данные, например строки поиска или привязки, или если вызов был перенаправлен, то возвращаемый URL-адрес отличается от исходного.</span><span class="sxs-lookup"><span data-stu-id="fc010-543">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="fc010-544">Приложение должно передать в буфер размер в байтах, достаточно большой для хранения возвращенного URL-адреса в расширенном символе.</span><span class="sxs-lookup"><span data-stu-id="fc010-544">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера**</span><span class="sxs-lookup"><span data-stu-id="fc010-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-546">Принимает **логическое** значение и может устанавливать только обработчик сеанса.</span><span class="sxs-lookup"><span data-stu-id="fc010-546">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="fc010-547">Она будет распространяться только на дескрипторы, созданные из дескриптора сеанса после установки параметра.</span><span class="sxs-lookup"><span data-stu-id="fc010-547">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="fc010-548">Если **значение — true**, этот параметр приводит к тому, что в качестве последнего средства используется учетные данные глобального сервера, которые были отправлены из wininet.</span><span class="sxs-lookup"><span data-stu-id="fc010-548">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="fc010-549">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="fc010-549">The default for this option is **FALSE**.</span></span> <span data-ttu-id="fc010-550">Для этого параметра требуется раздел реестра **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet параметры Интернета! Шарекредсвисвинхттп**.</span><span class="sxs-lookup"><span data-stu-id="fc010-550">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="fc010-551">Этот раздел реестра отсутствует по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc010-551">This registry key is not present by default.</span></span> <span data-ttu-id="fc010-552">Когда она задана, WinINet отправит учетные данные на WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="fc010-552">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="fc010-553">Всякий раз, когда WinHttp получает запрос проверки подлинности и если для текущего обработчика не заданы учетные данные, он будет использовать учетные данные, предоставляемые WinINet.</span><span class="sxs-lookup"><span data-stu-id="fc010-553">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_ \_ Агент пользователя для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-555">Задает или получает строку [*агента пользователя*](glossary.md) для дескрипторов, предоставляемых [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) , и используется в последующих функциях [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) , если она не переопределяется заголовком, добавленным [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) или **WinHttpSendRequest**.</span><span class="sxs-lookup"><span data-stu-id="fc010-555">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="fc010-556">При извлечении агента пользователя приложение должно передать в буфер размер в байтах, достаточно большой для хранения возвращенного URL-адреса в расширенном символе.</span><span class="sxs-lookup"><span data-stu-id="fc010-556">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="fc010-557">При задании агента пользователя размер буфера — это длина строки в символах и знак завершения **null** .</span><span class="sxs-lookup"><span data-stu-id="fc010-557">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_имя пользователя для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-559">Задает или получает строку, содержащую имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc010-559">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_ \_ \_ \_ время ожидания закрытия веб-СОКЕТа для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-561">Задает время в миллисекундах, которое [**винхттпвебсоккетклосе**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) должно ожидать завершения подтверждения закрытия.</span><span class="sxs-lookup"><span data-stu-id="fc010-561">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="fc010-562">Значение по умолчанию — 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="fc010-562">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_интервал проверки \_ активности веб- \_ сокета для \_ параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-564">Задает интервал (в миллисекундах) отправки пакета проверки активности через соединение.</span><span class="sxs-lookup"><span data-stu-id="fc010-564">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="fc010-565">Интервал по умолчанию — 30000 (30 секунд).</span><span class="sxs-lookup"><span data-stu-id="fc010-565">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="fc010-566">Минимальный интервал — 15000 (15 секунд).</span><span class="sxs-lookup"><span data-stu-id="fc010-566">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="fc010-567">Использование [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) для установки значения ниже 15000 будет возвращать ошибку с **\_ недопустимым \_ параметром**.</span><span class="sxs-lookup"><span data-stu-id="fc010-567">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="fc010-568">Значение по умолчанию **для \_ параметра \_ WinHTTP \_ \_ \_ интервал проверки активности веб-сокета** считывается из раздела **HKLM: \\ Software \\ Microsoft \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="fc010-568">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="fc010-569">Если значение не задано, будет использоваться значение по умолчанию 30000.</span><span class="sxs-lookup"><span data-stu-id="fc010-569">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="fc010-570">Более низкий интервал активности не может превышать 15000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="fc010-570">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**\_параметр WinHTTP \_ \_ \_ \_ Размер буфера получения веб-сокета \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-572">Задает или получает значение типа DWORD, указывающее размер буфера приема, используемый для подключений WebSocket.</span><span class="sxs-lookup"><span data-stu-id="fc010-572">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**\_ \_ \_ \_ \_ Размер буфера отправки для веб-сокета параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-574">Задает или получает значение типа DWORD, указывающее размер буфера отправки, используемый для подключений WebSocket.</span><span class="sxs-lookup"><span data-stu-id="fc010-574">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_ \_ \_ число рабочих потоков \_ параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-576">Задает длинное целочисленное значение без знака, указывающее количество рабочих потоков, которые пул потоков должен использовать для асинхронных завершений.</span><span class="sxs-lookup"><span data-stu-id="fc010-576">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="fc010-577">Значение этого параметра по умолчанию равно нулю, что указывает, что количество рабочих потоков равно числу процессоров в системе.</span><span class="sxs-lookup"><span data-stu-id="fc010-577">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="fc010-578">Этот параметр может быть установлен только для [хинтернетного](hinternet-handles-in-winhttp.md) маркера **до выполнения** асинхронной операции.  </span><span class="sxs-lookup"><span data-stu-id="fc010-578">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="fc010-579">Этот параметр можно задать только один раз.</span><span class="sxs-lookup"><span data-stu-id="fc010-579">This option can only be set once.</span></span>

<span data-ttu-id="fc010-580">**Windows Server 2008 R2 и Windows 7:** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="fc010-580">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc010-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_ \_ \_ Размер буфера записи параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc010-582">Этот параметр является устаревшим; Он не действует.</span><span class="sxs-lookup"><span data-stu-id="fc010-582">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc010-583">Remarks</span><span class="sxs-lookup"><span data-stu-id="fc010-583">Remarks</span></span>

<span data-ttu-id="fc010-584">В следующей таблице перечислены флаги параметров, указывающие, какие дескрипторы могут действовать, можно ли запрашивать и задавать их, а также использовать тип данных.</span><span class="sxs-lookup"><span data-stu-id="fc010-584">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="fc010-585">"X" означает, что флаг параметра является допустимым для использования с функцией или обработчиком, а "-" указывает на недопустимый флаг параметра.</span><span class="sxs-lookup"><span data-stu-id="fc010-585">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="fc010-586">Попытка задать или запросить флаг параметра в версии Windows, где она не поддерживается, приведет к **ошибке \_ \_ "Недопустимый WinHTTP \_ "**.</span><span class="sxs-lookup"><span data-stu-id="fc010-586">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="fc010-587">Флаг параметра и тип данных</span><span class="sxs-lookup"><span data-stu-id="fc010-587">Option flag, and data type</span></span> | <span data-ttu-id="fc010-588">Обработчик сеанса</span><span class="sxs-lookup"><span data-stu-id="fc010-588">Session handle</span></span> | <span data-ttu-id="fc010-589">Маркер запроса</span><span class="sxs-lookup"><span data-stu-id="fc010-589">Request handle</span></span> | <span data-ttu-id="fc010-590">Параметр запросов</span><span class="sxs-lookup"><span data-stu-id="fc010-590">Query option</span></span> | <span data-ttu-id="fc010-591">Параметр SET</span><span class="sxs-lookup"><span data-stu-id="fc010-591">Set option</span></span> | <span data-ttu-id="fc010-592">Минимальная версия Windows</span><span class="sxs-lookup"><span data-stu-id="fc010-592">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="fc010-593">\_параметр WinHTTP \_ — \_ \_ неблокирующие \_ обратные вызовы</span><span class="sxs-lookup"><span data-stu-id="fc010-593">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="fc010-594">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-594">**BOOL**</span></span> | <span data-ttu-id="fc010-595">X</span><span class="sxs-lookup"><span data-stu-id="fc010-595">X</span></span> | \- | \- | <span data-ttu-id="fc010-596">X</span><span class="sxs-lookup"><span data-stu-id="fc010-596">X</span></span> | \- |
| <span data-ttu-id="fc010-597">\_ \_ политика автоматического входа в службу WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-597">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="fc010-598">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-598">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-599">X</span><span class="sxs-lookup"><span data-stu-id="fc010-599">X</span></span> | \- | <span data-ttu-id="fc010-600">X</span><span class="sxs-lookup"><span data-stu-id="fc010-600">X</span></span> | \- |
| <span data-ttu-id="fc010-601">\_Параметры WinHTTP \_ фоновых \_ подключений</span><span class="sxs-lookup"><span data-stu-id="fc010-601">WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS</span></span><br/><span data-ttu-id="fc010-602">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-602">**DWORD**</span></span> | <span data-ttu-id="fc010-603">X</span><span class="sxs-lookup"><span data-stu-id="fc010-603">X</span></span> | \- | \- | <span data-ttu-id="fc010-604">X</span><span class="sxs-lookup"><span data-stu-id="fc010-604">X</span></span> | <span data-ttu-id="fc010-605">Windows 10 версии 21H1</span><span class="sxs-lookup"><span data-stu-id="fc010-605">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="fc010-606">\_ \_ обратный вызов параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-606">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="fc010-607">**лпвоид**</span><span class="sxs-lookup"><span data-stu-id="fc010-607">**LPVOID**</span></span> | <span data-ttu-id="fc010-608">X</span><span class="sxs-lookup"><span data-stu-id="fc010-608">X</span></span> | <span data-ttu-id="fc010-609">X</span><span class="sxs-lookup"><span data-stu-id="fc010-609">X</span></span> | <span data-ttu-id="fc010-610">X</span><span class="sxs-lookup"><span data-stu-id="fc010-610">X</span></span> | <span data-ttu-id="fc010-611">X</span><span class="sxs-lookup"><span data-stu-id="fc010-611">X</span></span> | \- |
| <span data-ttu-id="fc010-612">\_ \_ \_ контекст сертификата клиента для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-612">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="fc010-613">**\_контекст сертификата**</span><span class="sxs-lookup"><span data-stu-id="fc010-613">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="fc010-614">X</span><span class="sxs-lookup"><span data-stu-id="fc010-614">X</span></span> | \- | <span data-ttu-id="fc010-615">X</span><span class="sxs-lookup"><span data-stu-id="fc010-615">X</span></span> | <span data-ttu-id="fc010-616">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc010-616">Windows Vista</span></span> |
| <span data-ttu-id="fc010-617">\_ \_ \_ \_ список поставщиков сертификатов клиента для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-617">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="fc010-618">**Секпкгконтекст \_ иссуерлистинфоекс**</span><span class="sxs-lookup"><span data-stu-id="fc010-618">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="fc010-619">X</span><span class="sxs-lookup"><span data-stu-id="fc010-619">X</span></span> | <span data-ttu-id="fc010-620">X</span><span class="sxs-lookup"><span data-stu-id="fc010-620">X</span></span> | \- | <span data-ttu-id="fc010-621">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc010-621">Windows Vista</span></span> |
| <span data-ttu-id="fc010-622">\_ \_ кодовая страница параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-622">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="fc010-623">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-623">**DWORD**</span></span> | <span data-ttu-id="fc010-624">X</span><span class="sxs-lookup"><span data-stu-id="fc010-624">X</span></span> | \- | \- | <span data-ttu-id="fc010-625">X</span><span class="sxs-lookup"><span data-stu-id="fc010-625">X</span></span> | \- |
| <span data-ttu-id="fc010-626">\_параметр WinHTTP \_ Настройка \_ \_ проверки подлинности паспорта</span><span class="sxs-lookup"><span data-stu-id="fc010-626">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="fc010-627">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-627">**DWORD**</span></span> | <span data-ttu-id="fc010-628">X</span><span class="sxs-lookup"><span data-stu-id="fc010-628">X</span></span> | \- | \- | <span data-ttu-id="fc010-629">X</span><span class="sxs-lookup"><span data-stu-id="fc010-629">X</span></span> | \- |
| <span data-ttu-id="fc010-630">\_ \_ повторные попытки соединения с ПАРАМЕТРом WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-630">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="fc010-631">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-631">**DWORD**</span></span> | <span data-ttu-id="fc010-632">X</span><span class="sxs-lookup"><span data-stu-id="fc010-632">X</span></span> | <span data-ttu-id="fc010-633">X</span><span class="sxs-lookup"><span data-stu-id="fc010-633">X</span></span> | <span data-ttu-id="fc010-634">X</span><span class="sxs-lookup"><span data-stu-id="fc010-634">X</span></span> | <span data-ttu-id="fc010-635">X</span><span class="sxs-lookup"><span data-stu-id="fc010-635">X</span></span> | \- |
| <span data-ttu-id="fc010-636">\_ \_ время ожидания соединения для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-636">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="fc010-637">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-637">**DWORD**</span></span> | <span data-ttu-id="fc010-638">X</span><span class="sxs-lookup"><span data-stu-id="fc010-638">X</span></span> | <span data-ttu-id="fc010-639">X</span><span class="sxs-lookup"><span data-stu-id="fc010-639">X</span></span> | <span data-ttu-id="fc010-640">X</span><span class="sxs-lookup"><span data-stu-id="fc010-640">X</span></span> | <span data-ttu-id="fc010-641">X</span><span class="sxs-lookup"><span data-stu-id="fc010-641">X</span></span> | \- |
| <span data-ttu-id="fc010-642">\_ \_ сведения о соединении параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-642">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="fc010-643">**\_сведения о подключении к WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-643">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="fc010-644">X</span><span class="sxs-lookup"><span data-stu-id="fc010-644">X</span></span> | <span data-ttu-id="fc010-645">X</span><span class="sxs-lookup"><span data-stu-id="fc010-645">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-646">\_Параметр WinHTTP \_ Connection \_ stats \_ v0</span><span class="sxs-lookup"><span data-stu-id="fc010-646">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="fc010-647">**\_V0 сведения о TCP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-647">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="fc010-648">X</span><span class="sxs-lookup"><span data-stu-id="fc010-648">X</span></span> | <span data-ttu-id="fc010-649">X</span><span class="sxs-lookup"><span data-stu-id="fc010-649">X</span></span> | \- | <span data-ttu-id="fc010-650">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="fc010-650">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="fc010-651">\_Параметр WinHTTP \_ Connection \_ stats \_ v1</span><span class="sxs-lookup"><span data-stu-id="fc010-651">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="fc010-652">**\_Сведения о TCP \_ v1**</span><span class="sxs-lookup"><span data-stu-id="fc010-652">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="fc010-653">X</span><span class="sxs-lookup"><span data-stu-id="fc010-653">X</span></span> | <span data-ttu-id="fc010-654">X</span><span class="sxs-lookup"><span data-stu-id="fc010-654">X</span></span> | \- | <span data-ttu-id="fc010-655">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="fc010-655">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="fc010-656">\_ \_ значение контекста WinHTTP для параметра \_</span><span class="sxs-lookup"><span data-stu-id="fc010-656">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="fc010-657">**DWORD \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="fc010-657">**DWORD\_PTR**</span></span> | <span data-ttu-id="fc010-658">X</span><span class="sxs-lookup"><span data-stu-id="fc010-658">X</span></span> | <span data-ttu-id="fc010-659">X</span><span class="sxs-lookup"><span data-stu-id="fc010-659">X</span></span> | <span data-ttu-id="fc010-660">X</span><span class="sxs-lookup"><span data-stu-id="fc010-660">X</span></span> | <span data-ttu-id="fc010-661">X</span><span class="sxs-lookup"><span data-stu-id="fc010-661">X</span></span> | \- |
| <span data-ttu-id="fc010-662">\_ \_ распаковка параметров WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-662">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="fc010-663">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-663">**DWORD**</span></span> | <span data-ttu-id="fc010-664">X</span><span class="sxs-lookup"><span data-stu-id="fc010-664">X</span></span> | <span data-ttu-id="fc010-665">X</span><span class="sxs-lookup"><span data-stu-id="fc010-665">X</span></span> | \- | <span data-ttu-id="fc010-666">X</span><span class="sxs-lookup"><span data-stu-id="fc010-666">X</span></span> | <span data-ttu-id="fc010-667">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fc010-667">Windows 8.1</span></span> |
| <span data-ttu-id="fc010-668">\_параметр WinHTTP \_ Отключить \_ \_ Построение цепочки сертификатов \_</span><span class="sxs-lookup"><span data-stu-id="fc010-668">WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING</span></span><br/><span data-ttu-id="fc010-669">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-669">**BOOL**</span></span> | <span data-ttu-id="fc010-670">X</span><span class="sxs-lookup"><span data-stu-id="fc010-670">X</span></span> | \- | \- | <span data-ttu-id="fc010-671">X</span><span class="sxs-lookup"><span data-stu-id="fc010-671">X</span></span> | <span data-ttu-id="fc010-672">Windows 10 версии 21H1</span><span class="sxs-lookup"><span data-stu-id="fc010-672">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="fc010-673">\_ \_ функция отключения параметров \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-673">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="fc010-674">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-674">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-675">X</span><span class="sxs-lookup"><span data-stu-id="fc010-675">X</span></span> | \- | <span data-ttu-id="fc010-676">X</span><span class="sxs-lookup"><span data-stu-id="fc010-676">X</span></span> | \- |
| <span data-ttu-id="fc010-677">\_параметр WinHTTP \_ Отключить \_ откат безопасных \_ протоколов \_</span><span class="sxs-lookup"><span data-stu-id="fc010-677">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="fc010-678">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-678">**BOOL**</span></span> | <span data-ttu-id="fc010-679">X</span><span class="sxs-lookup"><span data-stu-id="fc010-679">X</span></span> | \- | \- | <span data-ttu-id="fc010-680">X</span><span class="sxs-lookup"><span data-stu-id="fc010-680">X</span></span> | <span data-ttu-id="fc010-681">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="fc010-681">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="fc010-682">\_параметр WinHTTP \_ Отключить \_ \_ очередь потока</span><span class="sxs-lookup"><span data-stu-id="fc010-682">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="fc010-683">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-683">**BOOL**</span></span> | <span data-ttu-id="fc010-684">X</span><span class="sxs-lookup"><span data-stu-id="fc010-684">X</span></span> | <span data-ttu-id="fc010-685">X</span><span class="sxs-lookup"><span data-stu-id="fc010-685">X</span></span> | \- | <span data-ttu-id="fc010-686">X</span><span class="sxs-lookup"><span data-stu-id="fc010-686">X</span></span> | <span data-ttu-id="fc010-687">Windows 10, версия 1809</span><span class="sxs-lookup"><span data-stu-id="fc010-687">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="fc010-688">\_ \_ Включение \_ функции WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-688">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="fc010-689">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-689">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="fc010-690">X</span><span class="sxs-lookup"><span data-stu-id="fc010-690">X</span></span> | \- |
| <span data-ttu-id="fc010-691">\_параметр WinHTTP \_ Включение \_ \_ протокола HTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-691">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="fc010-692">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-692">**DWORD**</span></span> | <span data-ttu-id="fc010-693">X</span><span class="sxs-lookup"><span data-stu-id="fc010-693">X</span></span> | <span data-ttu-id="fc010-694">X</span><span class="sxs-lookup"><span data-stu-id="fc010-694">X</span></span> | \- | <span data-ttu-id="fc010-695">X</span><span class="sxs-lookup"><span data-stu-id="fc010-695">X</span></span> | <span data-ttu-id="fc010-696">Windows 10 версии 1607</span><span class="sxs-lookup"><span data-stu-id="fc010-696">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="fc010-697">\_Параметр WinHTTP \_ включить \_ \_ \_ \_ контекст сертификата клиента \_ HTTP2 Plus</span><span class="sxs-lookup"><span data-stu-id="fc010-697">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="fc010-698">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-698">**BOOL**</span></span> | <span data-ttu-id="fc010-699">X</span><span class="sxs-lookup"><span data-stu-id="fc010-699">X</span></span> | \- | \- | <span data-ttu-id="fc010-700">X</span><span class="sxs-lookup"><span data-stu-id="fc010-700">X</span></span> | <span data-ttu-id="fc010-701">Windows 10 версии 21H1</span><span class="sxs-lookup"><span data-stu-id="fc010-701">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="fc010-702">\_параметр WinHTTP \_ енаблетраЦинг</span><span class="sxs-lookup"><span data-stu-id="fc010-702">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="fc010-703">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-703">**DWORD**</span></span> | \- | \- | <span data-ttu-id="fc010-704">X</span><span class="sxs-lookup"><span data-stu-id="fc010-704">X</span></span> | <span data-ttu-id="fc010-705">X</span><span class="sxs-lookup"><span data-stu-id="fc010-705">X</span></span> | \- |
| <span data-ttu-id="fc010-706">\_ \_ добавочная кодировка параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-706">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="fc010-707">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-707">**BOOL**</span></span> | <span data-ttu-id="fc010-708">X</span><span class="sxs-lookup"><span data-stu-id="fc010-708">X</span></span> | <span data-ttu-id="fc010-709">X</span><span class="sxs-lookup"><span data-stu-id="fc010-709">X</span></span> | \- | <span data-ttu-id="fc010-710">X</span><span class="sxs-lookup"><span data-stu-id="fc010-710">X</span></span> | <span data-ttu-id="fc010-711">Windows 10, версия 1803</span><span class="sxs-lookup"><span data-stu-id="fc010-711">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="fc010-712">\_ \_ срок действия соединения для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-712">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="fc010-713">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fc010-713">N/A</span></span> | \- | <span data-ttu-id="fc010-714">X</span><span class="sxs-lookup"><span data-stu-id="fc010-714">X</span></span> | \- | <span data-ttu-id="fc010-715">X</span><span class="sxs-lookup"><span data-stu-id="fc010-715">X</span></span> | <span data-ttu-id="fc010-716">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="fc010-716">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="fc010-717">\_ \_ Расширенная ошибка при выборе WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-717">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="fc010-718">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-718">**DWORD**</span></span> | <span data-ttu-id="fc010-719">X</span><span class="sxs-lookup"><span data-stu-id="fc010-719">X</span></span> | <span data-ttu-id="fc010-720">X</span><span class="sxs-lookup"><span data-stu-id="fc010-720">X</span></span> | <span data-ttu-id="fc010-721">X</span><span class="sxs-lookup"><span data-stu-id="fc010-721">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-722">\_параметр WinHTTP \_ первое \_ доступное \_ подключение</span><span class="sxs-lookup"><span data-stu-id="fc010-722">WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION</span></span><br/><span data-ttu-id="fc010-723">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-723">**BOOL**</span></span> | <span data-ttu-id="fc010-724">X</span><span class="sxs-lookup"><span data-stu-id="fc010-724">X</span></span> | \- | \- | <span data-ttu-id="fc010-725">X</span><span class="sxs-lookup"><span data-stu-id="fc010-725">X</span></span> | <span data-ttu-id="fc010-726">Windows 10 версии 21H1</span><span class="sxs-lookup"><span data-stu-id="fc010-726">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="fc010-727">\_ \_ \_ учетные записи глобального прокси-сервера параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-727">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="fc010-728">**учетные учетные \_ службы WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-728">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="fc010-729">X</span><span class="sxs-lookup"><span data-stu-id="fc010-729">X</span></span> | <span data-ttu-id="fc010-730">X</span><span class="sxs-lookup"><span data-stu-id="fc010-730">X</span></span> | \- | <span data-ttu-id="fc010-731">X</span><span class="sxs-lookup"><span data-stu-id="fc010-731">X</span></span> | \- |
| <span data-ttu-id="fc010-732">Параметры WINHTTP глобальные учетные значения \_ \_ \_ сервера \_</span><span class="sxs-lookup"><span data-stu-id="fc010-732">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="fc010-733">**учетные учетные службы WINHTTP, \_ \_ пример**</span><span class="sxs-lookup"><span data-stu-id="fc010-733">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="fc010-734">X</span><span class="sxs-lookup"><span data-stu-id="fc010-734">X</span></span> | <span data-ttu-id="fc010-735">X</span><span class="sxs-lookup"><span data-stu-id="fc010-735">X</span></span> | \- | <span data-ttu-id="fc010-736">X</span><span class="sxs-lookup"><span data-stu-id="fc010-736">X</span></span> | \- |
| <span data-ttu-id="fc010-737">\_ \_ тип обработчика параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-737">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="fc010-738">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-738">**DWORD**</span></span> | <span data-ttu-id="fc010-739">X</span><span class="sxs-lookup"><span data-stu-id="fc010-739">X</span></span> | <span data-ttu-id="fc010-740">X</span><span class="sxs-lookup"><span data-stu-id="fc010-740">X</span></span> | <span data-ttu-id="fc010-741">X</span><span class="sxs-lookup"><span data-stu-id="fc010-741">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-742">\_ \_ \_ требуется протокол HTTP для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-742">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="fc010-743">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-743">**BOOL**</span></span> | <span data-ttu-id="fc010-744">X</span><span class="sxs-lookup"><span data-stu-id="fc010-744">X</span></span> | <span data-ttu-id="fc010-745">X</span><span class="sxs-lookup"><span data-stu-id="fc010-745">X</span></span> | \- | <span data-ttu-id="fc010-746">X</span><span class="sxs-lookup"><span data-stu-id="fc010-746">X</span></span> | <span data-ttu-id="fc010-747">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="fc010-747">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="fc010-748">\_ \_ \_ используемый протокол HTTP \_ для параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-748">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="fc010-749">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-749">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-750">X</span><span class="sxs-lookup"><span data-stu-id="fc010-750">X</span></span> | <span data-ttu-id="fc010-751">X</span><span class="sxs-lookup"><span data-stu-id="fc010-751">X</span></span> | \- | <span data-ttu-id="fc010-752">Windows 10 версии 1607</span><span class="sxs-lookup"><span data-stu-id="fc010-752">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="fc010-753">\_ \_ Версия HTTP параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-753">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="fc010-754">**\_ \_ сведения о версии HTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-754">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="fc010-755">X</span><span class="sxs-lookup"><span data-stu-id="fc010-755">X</span></span> | <span data-ttu-id="fc010-756">X</span><span class="sxs-lookup"><span data-stu-id="fc010-756">X</span></span> | <span data-ttu-id="fc010-757">X</span><span class="sxs-lookup"><span data-stu-id="fc010-757">X</span></span> | <span data-ttu-id="fc010-758">X</span><span class="sxs-lookup"><span data-stu-id="fc010-758">X</span></span> | \- |
| <span data-ttu-id="fc010-759">\_Параметр WinHTTP \_ HTTP2 \_ KeepAlive</span><span class="sxs-lookup"><span data-stu-id="fc010-759">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="fc010-760">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-760">**DWORD**</span></span> | <span data-ttu-id="fc010-761">X</span><span class="sxs-lookup"><span data-stu-id="fc010-761">X</span></span> | \- | \- | <span data-ttu-id="fc010-762">X</span><span class="sxs-lookup"><span data-stu-id="fc010-762">X</span></span> | <span data-ttu-id="fc010-763">Windows 10 версии 21H1</span><span class="sxs-lookup"><span data-stu-id="fc010-763">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="fc010-764">\_Параметр WinHTTP \_ HTTP2 \_ и \_ \_ Кодировка перемещения</span><span class="sxs-lookup"><span data-stu-id="fc010-764">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="fc010-765">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-765">**BOOL**</span></span> | <span data-ttu-id="fc010-766">X</span><span class="sxs-lookup"><span data-stu-id="fc010-766">X</span></span> | <span data-ttu-id="fc010-767">X</span><span class="sxs-lookup"><span data-stu-id="fc010-767">X</span></span> | \- | <span data-ttu-id="fc010-768">X</span><span class="sxs-lookup"><span data-stu-id="fc010-768">X</span></span> | <span data-ttu-id="fc010-769">Windows 10 версии 21H1</span><span class="sxs-lookup"><span data-stu-id="fc010-769">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="fc010-770">\_параметр WinHTTP \_ игнорировать \_ отзыв сертификата в \_ \_ автономном режиме</span><span class="sxs-lookup"><span data-stu-id="fc010-770">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="fc010-771">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-771">**BOOL**</span></span> | \- | <span data-ttu-id="fc010-772">X</span><span class="sxs-lookup"><span data-stu-id="fc010-772">X</span></span> | \- | <span data-ttu-id="fc010-773">X</span><span class="sxs-lookup"><span data-stu-id="fc010-773">X</span></span> | <span data-ttu-id="fc010-774">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="fc010-774">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="fc010-775">\_ \_ \_ Быстрый откат параметров WinHTTP \_ IPv6</span><span class="sxs-lookup"><span data-stu-id="fc010-775">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="fc010-776">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-776">**BOOL**</span></span> | <span data-ttu-id="fc010-777">X</span><span class="sxs-lookup"><span data-stu-id="fc010-777">X</span></span> | \- | \- | <span data-ttu-id="fc010-778">X</span><span class="sxs-lookup"><span data-stu-id="fc010-778">X</span></span> | <span data-ttu-id="fc010-779">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="fc010-779">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="fc010-780">\_параметр WinHTTP \_ — \_ ответ прокси- \_ подключения \_</span><span class="sxs-lookup"><span data-stu-id="fc010-780">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="fc010-781">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-781">**BOOL**</span></span> | <span data-ttu-id="fc010-782">X</span><span class="sxs-lookup"><span data-stu-id="fc010-782">X</span></span> | <span data-ttu-id="fc010-783">X</span><span class="sxs-lookup"><span data-stu-id="fc010-783">X</span></span> | <span data-ttu-id="fc010-784">X</span><span class="sxs-lookup"><span data-stu-id="fc010-784">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-785">\_Параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ \_ \_ сервер 1 0</span><span class="sxs-lookup"><span data-stu-id="fc010-785">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="fc010-786">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-786">**DWORD**</span></span> | <span data-ttu-id="fc010-787">X</span><span class="sxs-lookup"><span data-stu-id="fc010-787">X</span></span> | \- | <span data-ttu-id="fc010-788">X</span><span class="sxs-lookup"><span data-stu-id="fc010-788">X</span></span> | <span data-ttu-id="fc010-789">X</span><span class="sxs-lookup"><span data-stu-id="fc010-789">X</span></span> | \- |
| <span data-ttu-id="fc010-790">\_параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ сервер</span><span class="sxs-lookup"><span data-stu-id="fc010-790">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="fc010-791">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-791">**DWORD**</span></span> | <span data-ttu-id="fc010-792">X</span><span class="sxs-lookup"><span data-stu-id="fc010-792">X</span></span> | \- | <span data-ttu-id="fc010-793">X</span><span class="sxs-lookup"><span data-stu-id="fc010-793">X</span></span> | <span data-ttu-id="fc010-794">X</span><span class="sxs-lookup"><span data-stu-id="fc010-794">X</span></span> | \- |
| <span data-ttu-id="fc010-795">\_параметр WinHTTP \_ Максимальное \_ число \_ автоматических \_ перенаправлений HTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-795">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="fc010-796">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-796">**DWORD**</span></span> | <span data-ttu-id="fc010-797">X</span><span class="sxs-lookup"><span data-stu-id="fc010-797">X</span></span> | <span data-ttu-id="fc010-798">X</span><span class="sxs-lookup"><span data-stu-id="fc010-798">X</span></span> | <span data-ttu-id="fc010-799">X</span><span class="sxs-lookup"><span data-stu-id="fc010-799">X</span></span> | <span data-ttu-id="fc010-800">X</span><span class="sxs-lookup"><span data-stu-id="fc010-800">X</span></span> | \- |
| <span data-ttu-id="fc010-801">\_продолжение параметра \_ максимального \_ \_ состояния HTTP \_ для WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-801">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="fc010-802">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-802">**DWORD**</span></span> | <span data-ttu-id="fc010-803">X</span><span class="sxs-lookup"><span data-stu-id="fc010-803">X</span></span> | <span data-ttu-id="fc010-804">X</span><span class="sxs-lookup"><span data-stu-id="fc010-804">X</span></span> | <span data-ttu-id="fc010-805">X</span><span class="sxs-lookup"><span data-stu-id="fc010-805">X</span></span> | <span data-ttu-id="fc010-806">X</span><span class="sxs-lookup"><span data-stu-id="fc010-806">X</span></span> | \- |
| <span data-ttu-id="fc010-807">параметр WINHTTP — \_ \_ максимальный \_ \_ Размер очистки ответа \_</span><span class="sxs-lookup"><span data-stu-id="fc010-807">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="fc010-808">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-808">**DWORD**</span></span> | <span data-ttu-id="fc010-809">X</span><span class="sxs-lookup"><span data-stu-id="fc010-809">X</span></span> | <span data-ttu-id="fc010-810">X</span><span class="sxs-lookup"><span data-stu-id="fc010-810">X</span></span> | <span data-ttu-id="fc010-811">X</span><span class="sxs-lookup"><span data-stu-id="fc010-811">X</span></span> | <span data-ttu-id="fc010-812">X</span><span class="sxs-lookup"><span data-stu-id="fc010-812">X</span></span> | \- |
| <span data-ttu-id="fc010-813">\_параметр WinHTTP \_ максимальный \_ \_ размер заголовка \_ ответа</span><span class="sxs-lookup"><span data-stu-id="fc010-813">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="fc010-814">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-814">**DWORD**</span></span> | <span data-ttu-id="fc010-815">X</span><span class="sxs-lookup"><span data-stu-id="fc010-815">X</span></span> | <span data-ttu-id="fc010-816">X</span><span class="sxs-lookup"><span data-stu-id="fc010-816">X</span></span> | <span data-ttu-id="fc010-817">X</span><span class="sxs-lookup"><span data-stu-id="fc010-817">X</span></span> | <span data-ttu-id="fc010-818">X</span><span class="sxs-lookup"><span data-stu-id="fc010-818">X</span></span> | \- |
| <span data-ttu-id="fc010-819">\_ \_ родительский маркер параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-819">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="fc010-820">хинтернет</span><span class="sxs-lookup"><span data-stu-id="fc010-820">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="fc010-821">X</span><span class="sxs-lookup"><span data-stu-id="fc010-821">X</span></span> | <span data-ttu-id="fc010-822">X</span><span class="sxs-lookup"><span data-stu-id="fc010-822">X</span></span> | <span data-ttu-id="fc010-823">X</span><span class="sxs-lookup"><span data-stu-id="fc010-823">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-824">\_параметр WinHTTP \_ , \_ софирменный текст в паспорте \_</span><span class="sxs-lookup"><span data-stu-id="fc010-824">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="fc010-825">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-825">**LPWSTR**</span></span> | \- | <span data-ttu-id="fc010-826">X</span><span class="sxs-lookup"><span data-stu-id="fc010-826">X</span></span> | <span data-ttu-id="fc010-827">X</span><span class="sxs-lookup"><span data-stu-id="fc010-827">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-828">\_ \_ \_ URL-адрес КОфирменной символики для службы WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-828">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="fc010-829">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-829">**LPWSTR**</span></span> | \- | <span data-ttu-id="fc010-830">X</span><span class="sxs-lookup"><span data-stu-id="fc010-830">X</span></span> | <span data-ttu-id="fc010-831">X</span><span class="sxs-lookup"><span data-stu-id="fc010-831">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-832">\_ \_ \_ \_ URL-адрес возврата паспорта с параметром WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-832">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="fc010-833">**лпвоид**</span><span class="sxs-lookup"><span data-stu-id="fc010-833">**LPVOID**</span></span> | \- | <span data-ttu-id="fc010-834">X</span><span class="sxs-lookup"><span data-stu-id="fc010-834">X</span></span> | <span data-ttu-id="fc010-835">X</span><span class="sxs-lookup"><span data-stu-id="fc010-835">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-836">\_команда WinHTTP \_ выход \_ \_ из паспорта</span><span class="sxs-lookup"><span data-stu-id="fc010-836">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="fc010-837">**лпвоид**</span><span class="sxs-lookup"><span data-stu-id="fc010-837">**LPVOID**</span></span> | <span data-ttu-id="fc010-838">X</span><span class="sxs-lookup"><span data-stu-id="fc010-838">X</span></span> | \- | \- | <span data-ttu-id="fc010-839">X</span><span class="sxs-lookup"><span data-stu-id="fc010-839">X</span></span> | \- |
| <span data-ttu-id="fc010-840">\_пароль для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-840">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="fc010-841">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-841">**LPWSTR**</span></span> | \- | <span data-ttu-id="fc010-842">X</span><span class="sxs-lookup"><span data-stu-id="fc010-842">X</span></span> | <span data-ttu-id="fc010-843">X</span><span class="sxs-lookup"><span data-stu-id="fc010-843">X</span></span> | <span data-ttu-id="fc010-844">X</span><span class="sxs-lookup"><span data-stu-id="fc010-844">X</span></span> | \- |
| <span data-ttu-id="fc010-845">\_ \_ прокси-сервер параметров WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-845">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="fc010-846">**\_сведения о прокси-сервере WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-846">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="fc010-847">X</span><span class="sxs-lookup"><span data-stu-id="fc010-847">X</span></span> | <span data-ttu-id="fc010-848">X</span><span class="sxs-lookup"><span data-stu-id="fc010-848">X</span></span> | <span data-ttu-id="fc010-849">X</span><span class="sxs-lookup"><span data-stu-id="fc010-849">X</span></span> | <span data-ttu-id="fc010-850">X</span><span class="sxs-lookup"><span data-stu-id="fc010-850">X</span></span> | \- |
| <span data-ttu-id="fc010-851">\_ \_ пароль прокси-сервера для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-851">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="fc010-852">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-852">**LPWSTR**</span></span> | \- | <span data-ttu-id="fc010-853">X</span><span class="sxs-lookup"><span data-stu-id="fc010-853">X</span></span> | <span data-ttu-id="fc010-854">X</span><span class="sxs-lookup"><span data-stu-id="fc010-854">X</span></span> | <span data-ttu-id="fc010-855">X</span><span class="sxs-lookup"><span data-stu-id="fc010-855">X</span></span> | \- |
| <span data-ttu-id="fc010-856">\_используется параметр WinHTTP \_ прокси- \_ службы \_</span><span class="sxs-lookup"><span data-stu-id="fc010-856">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="fc010-857">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-857">**LPWSTR**</span></span> | \- | <span data-ttu-id="fc010-858">X</span><span class="sxs-lookup"><span data-stu-id="fc010-858">X</span></span> | <span data-ttu-id="fc010-859">X</span><span class="sxs-lookup"><span data-stu-id="fc010-859">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-860">\_параметр WinHTTP \_ \_ имя пользователя-посредника</span><span class="sxs-lookup"><span data-stu-id="fc010-860">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="fc010-861">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-861">**LPWSTR**</span></span> | \- | <span data-ttu-id="fc010-862">X</span><span class="sxs-lookup"><span data-stu-id="fc010-862">X</span></span> | <span data-ttu-id="fc010-863">X</span><span class="sxs-lookup"><span data-stu-id="fc010-863">X</span></span> | <span data-ttu-id="fc010-864">X</span><span class="sxs-lookup"><span data-stu-id="fc010-864">X</span></span> | \- |
| <span data-ttu-id="fc010-865">\_ \_ \_ Размер буфера чтения параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-865">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="fc010-866">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-866">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-867">X</span><span class="sxs-lookup"><span data-stu-id="fc010-867">X</span></span> | <span data-ttu-id="fc010-868">X</span><span class="sxs-lookup"><span data-stu-id="fc010-868">X</span></span> | <span data-ttu-id="fc010-869">X</span><span class="sxs-lookup"><span data-stu-id="fc010-869">X</span></span> | \- |
| <span data-ttu-id="fc010-870">\_параметр WinHTTP \_ Получение \_ ответа прокси-сервера \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc010-870">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="fc010-871">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-871">**BOOL**</span></span> | <span data-ttu-id="fc010-872">X</span><span class="sxs-lookup"><span data-stu-id="fc010-872">X</span></span> | <span data-ttu-id="fc010-873">X</span><span class="sxs-lookup"><span data-stu-id="fc010-873">X</span></span> | \- | <span data-ttu-id="fc010-874">X</span><span class="sxs-lookup"><span data-stu-id="fc010-874">X</span></span> | \- |
| <span data-ttu-id="fc010-875">\_ \_ \_ время ожидания ответа для получения параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-875">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="fc010-876">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-876">**DWORD**</span></span> | <span data-ttu-id="fc010-877">X</span><span class="sxs-lookup"><span data-stu-id="fc010-877">X</span></span> | <span data-ttu-id="fc010-878">X</span><span class="sxs-lookup"><span data-stu-id="fc010-878">X</span></span> | <span data-ttu-id="fc010-879">X</span><span class="sxs-lookup"><span data-stu-id="fc010-879">X</span></span> | <span data-ttu-id="fc010-880">X</span><span class="sxs-lookup"><span data-stu-id="fc010-880">X</span></span> | \- |
| <span data-ttu-id="fc010-881">\_ \_ время ожидания получения параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-881">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="fc010-882">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-882">**DWORD**</span></span> | <span data-ttu-id="fc010-883">X</span><span class="sxs-lookup"><span data-stu-id="fc010-883">X</span></span> | <span data-ttu-id="fc010-884">X</span><span class="sxs-lookup"><span data-stu-id="fc010-884">X</span></span> | <span data-ttu-id="fc010-885">X</span><span class="sxs-lookup"><span data-stu-id="fc010-885">X</span></span> | <span data-ttu-id="fc010-886">X</span><span class="sxs-lookup"><span data-stu-id="fc010-886">X</span></span> | \- |
| <span data-ttu-id="fc010-887">\_ \_ политика перенаправления для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-887">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="fc010-888">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-888">**DWORD**</span></span> | <span data-ttu-id="fc010-889">X</span><span class="sxs-lookup"><span data-stu-id="fc010-889">X</span></span> | <span data-ttu-id="fc010-890">X</span><span class="sxs-lookup"><span data-stu-id="fc010-890">X</span></span> | <span data-ttu-id="fc010-891">X</span><span class="sxs-lookup"><span data-stu-id="fc010-891">X</span></span> | <span data-ttu-id="fc010-892">X</span><span class="sxs-lookup"><span data-stu-id="fc010-892">X</span></span> | \- |
| <span data-ttu-id="fc010-893">\_параметр WinHTTP \_ отклонять \_ усерпвд \_ в \_ URL-адресе</span><span class="sxs-lookup"><span data-stu-id="fc010-893">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="fc010-894">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-894">**BOOL**</span></span> | \- | <span data-ttu-id="fc010-895">X</span><span class="sxs-lookup"><span data-stu-id="fc010-895">X</span></span> | \- | <span data-ttu-id="fc010-896">X</span><span class="sxs-lookup"><span data-stu-id="fc010-896">X</span></span> | \- |
| <span data-ttu-id="fc010-897">\_ \_ приоритет запроса параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-897">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="fc010-898">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-898">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-899">X</span><span class="sxs-lookup"><span data-stu-id="fc010-899">X</span></span> | <span data-ttu-id="fc010-900">X</span><span class="sxs-lookup"><span data-stu-id="fc010-900">X</span></span> | <span data-ttu-id="fc010-901">X</span><span class="sxs-lookup"><span data-stu-id="fc010-901">X</span></span> | \- |
| <span data-ttu-id="fc010-902">\_ \_ Статистика запросов параметров \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-902">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="fc010-903">**\_Статистика запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-903">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="fc010-904">X</span><span class="sxs-lookup"><span data-stu-id="fc010-904">X</span></span> | <span data-ttu-id="fc010-905">X</span><span class="sxs-lookup"><span data-stu-id="fc010-905">X</span></span> | \- | <span data-ttu-id="fc010-906">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="fc010-906">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="fc010-907">\_ \_ время запроса параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-907">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="fc010-908">**\_время запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="fc010-908">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="fc010-909">X</span><span class="sxs-lookup"><span data-stu-id="fc010-909">X</span></span> | <span data-ttu-id="fc010-910">X</span><span class="sxs-lookup"><span data-stu-id="fc010-910">X</span></span> | \- | <span data-ttu-id="fc010-911">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="fc010-911">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="fc010-912">\_параметр WinHTTP \_ требует \_ \_ завершения потока</span><span class="sxs-lookup"><span data-stu-id="fc010-912">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="fc010-913">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-913">**BOOL**</span></span> | <span data-ttu-id="fc010-914">X</span><span class="sxs-lookup"><span data-stu-id="fc010-914">X</span></span> | <span data-ttu-id="fc010-915">X</span><span class="sxs-lookup"><span data-stu-id="fc010-915">X</span></span> | \- | <span data-ttu-id="fc010-916">X</span><span class="sxs-lookup"><span data-stu-id="fc010-916">X</span></span> | <span data-ttu-id="fc010-917">Windows 10 версии 21H1</span><span class="sxs-lookup"><span data-stu-id="fc010-917">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="fc010-918">\_ \_ имя узла для разрешения параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-918">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="fc010-919">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-919">**LPWSTR**</span></span> | \- | <span data-ttu-id="fc010-920">X</span><span class="sxs-lookup"><span data-stu-id="fc010-920">X</span></span> | \- | <span data-ttu-id="fc010-921">X</span><span class="sxs-lookup"><span data-stu-id="fc010-921">X</span></span> | <span data-ttu-id="fc010-922">Windows 10 версии 21H1</span><span class="sxs-lookup"><span data-stu-id="fc010-922">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="fc010-923">\_ \_ время ожидания разрешения параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-923">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="fc010-924">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-924">**DWORD**</span></span> | <span data-ttu-id="fc010-925">X</span><span class="sxs-lookup"><span data-stu-id="fc010-925">X</span></span> | <span data-ttu-id="fc010-926">X</span><span class="sxs-lookup"><span data-stu-id="fc010-926">X</span></span> | <span data-ttu-id="fc010-927">X</span><span class="sxs-lookup"><span data-stu-id="fc010-927">X</span></span> | <span data-ttu-id="fc010-928">X</span><span class="sxs-lookup"><span data-stu-id="fc010-928">X</span></span> | \- |
| <span data-ttu-id="fc010-929">Параметры WINHTTP для \_ \_ защищенных \_ протоколов</span><span class="sxs-lookup"><span data-stu-id="fc010-929">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="fc010-930">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-930">**DWORD**</span></span> | <span data-ttu-id="fc010-931">X</span><span class="sxs-lookup"><span data-stu-id="fc010-931">X</span></span> | \- | \- | <span data-ttu-id="fc010-932">X</span><span class="sxs-lookup"><span data-stu-id="fc010-932">X</span></span> | \- |
| <span data-ttu-id="fc010-933">\_ \_ \_ Структура сертификата безопасности параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-933">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="fc010-934">**\_сведения о сертификате WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fc010-934">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="fc010-935">X</span><span class="sxs-lookup"><span data-stu-id="fc010-935">X</span></span> | <span data-ttu-id="fc010-936">X</span><span class="sxs-lookup"><span data-stu-id="fc010-936">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-937">\_ \_ Флаги безопасности для параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-937">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="fc010-938">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-938">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-939">X</span><span class="sxs-lookup"><span data-stu-id="fc010-939">X</span></span> | <span data-ttu-id="fc010-940">X</span><span class="sxs-lookup"><span data-stu-id="fc010-940">X</span></span> | <span data-ttu-id="fc010-941">X</span><span class="sxs-lookup"><span data-stu-id="fc010-941">X</span></span> | \- |
| <span data-ttu-id="fc010-942">\_ \_ сведения о безопасности параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-942">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="fc010-943">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="fc010-943">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="fc010-944">X</span><span class="sxs-lookup"><span data-stu-id="fc010-944">X</span></span> | <span data-ttu-id="fc010-945">X</span><span class="sxs-lookup"><span data-stu-id="fc010-945">X</span></span> | \- | <span data-ttu-id="fc010-946">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="fc010-946">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="fc010-947">\_ \_ \_ разрядность ключа безопасности параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-947">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="fc010-948">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-948">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-949">X</span><span class="sxs-lookup"><span data-stu-id="fc010-949">X</span></span> | <span data-ttu-id="fc010-950">X</span><span class="sxs-lookup"><span data-stu-id="fc010-950">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-951">\_ \_ время ожидания отправки для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-951">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="fc010-952">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-952">**DWORD**</span></span> | <span data-ttu-id="fc010-953">X</span><span class="sxs-lookup"><span data-stu-id="fc010-953">X</span></span> | <span data-ttu-id="fc010-954">X</span><span class="sxs-lookup"><span data-stu-id="fc010-954">X</span></span> | <span data-ttu-id="fc010-955">X</span><span class="sxs-lookup"><span data-stu-id="fc010-955">X</span></span> | <span data-ttu-id="fc010-956">X</span><span class="sxs-lookup"><span data-stu-id="fc010-956">X</span></span> | \- |
| <span data-ttu-id="fc010-957">\_ \_ CBT сервера параметров \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-957">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="fc010-958">[**\_Привязки секпкгконтекст**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="fc010-958">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="fc010-959">X</span><span class="sxs-lookup"><span data-stu-id="fc010-959">X</span></span> | <span data-ttu-id="fc010-960">X</span><span class="sxs-lookup"><span data-stu-id="fc010-960">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-961">\_параметр WinHTTP \_ \_ \_ контекст цепочки сертификатов сервера \_</span><span class="sxs-lookup"><span data-stu-id="fc010-961">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="fc010-962">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="fc010-962">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="fc010-963">X</span><span class="sxs-lookup"><span data-stu-id="fc010-963">X</span></span> | <span data-ttu-id="fc010-964">X</span><span class="sxs-lookup"><span data-stu-id="fc010-964">X</span></span> | \- | <span data-ttu-id="fc010-965">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="fc010-965">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="fc010-966">\_ \_ \_ контекст сертификата сервера параметров \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-966">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="fc010-967">**КОНТЕКСТ СЕРТИФИКАТА**</span><span class="sxs-lookup"><span data-stu-id="fc010-967">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="fc010-968">X</span><span class="sxs-lookup"><span data-stu-id="fc010-968">X</span></span> | <span data-ttu-id="fc010-969">X</span><span class="sxs-lookup"><span data-stu-id="fc010-969">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-970">\_ \_ \_ используемое имя субъекта-службы сервера параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-970">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="fc010-971">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-971">**LPWSTR**</span></span> | \- | <span data-ttu-id="fc010-972">X</span><span class="sxs-lookup"><span data-stu-id="fc010-972">X</span></span> | <span data-ttu-id="fc010-973">X</span><span class="sxs-lookup"><span data-stu-id="fc010-973">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-974">\_ \_ имя субъекта-службы для параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-974">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="fc010-975">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-975">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-976">X</span><span class="sxs-lookup"><span data-stu-id="fc010-976">X</span></span> | \- | <span data-ttu-id="fc010-977">X</span><span class="sxs-lookup"><span data-stu-id="fc010-977">X</span></span> | \- |
| <span data-ttu-id="fc010-978">\_ \_ код ошибки в потоке параметров WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc010-978">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="fc010-979">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-979">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-980">X</span><span class="sxs-lookup"><span data-stu-id="fc010-980">X</span></span> | <span data-ttu-id="fc010-981">X</span><span class="sxs-lookup"><span data-stu-id="fc010-981">X</span></span> | \- | <span data-ttu-id="fc010-982">Windows 10 версии 21H1</span><span class="sxs-lookup"><span data-stu-id="fc010-982">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="fc010-983">\_параметр WinHTTP \_ TCP \_ fast \_ Open</span><span class="sxs-lookup"><span data-stu-id="fc010-983">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="fc010-984">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-984">**BOOL**</span></span> | <span data-ttu-id="fc010-985">X</span><span class="sxs-lookup"><span data-stu-id="fc010-985">X</span></span> | \- | \- | <span data-ttu-id="fc010-986">X</span><span class="sxs-lookup"><span data-stu-id="fc010-986">X</span></span> | <span data-ttu-id="fc010-987">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="fc010-987">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="fc010-988">\_параметр WinHTTP \_ \_ KeepAlive TCP</span><span class="sxs-lookup"><span data-stu-id="fc010-988">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="fc010-989">**\_KeepAlive TCP**</span><span class="sxs-lookup"><span data-stu-id="fc010-989">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="fc010-990">X</span><span class="sxs-lookup"><span data-stu-id="fc010-990">X</span></span> | \- | \- | <span data-ttu-id="fc010-991">X</span><span class="sxs-lookup"><span data-stu-id="fc010-991">X</span></span> | <span data-ttu-id="fc010-992">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="fc010-992">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="fc010-993">\_Запуск параметра WinHTTP \_ TLS \_ false \_</span><span class="sxs-lookup"><span data-stu-id="fc010-993">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="fc010-994">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-994">**BOOL**</span></span> | <span data-ttu-id="fc010-995">X</span><span class="sxs-lookup"><span data-stu-id="fc010-995">X</span></span> | \- | \- | <span data-ttu-id="fc010-996">X</span><span class="sxs-lookup"><span data-stu-id="fc010-996">X</span></span> | <span data-ttu-id="fc010-997">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="fc010-997">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="fc010-998">\_небезопасный \_ \_ \_ \_ откат протокола TLS с параметром WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-998">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="fc010-999">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-999">**BOOL**</span></span> | <span data-ttu-id="fc010-1000">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1000">X</span></span> | \- | \- | <span data-ttu-id="fc010-1001">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1001">X</span></span> | <span data-ttu-id="fc010-1002">Windows 10 версии 21H1</span><span class="sxs-lookup"><span data-stu-id="fc010-1002">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="fc010-1003">\_ \_ \_ событие уведомления о ВЫгрузке параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-1003">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="fc010-1004">хинтернет</span><span class="sxs-lookup"><span data-stu-id="fc010-1004">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="fc010-1005">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1005">X</span></span> | \- | \- | <span data-ttu-id="fc010-1006">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1006">X</span></span> | \- |
| <span data-ttu-id="fc010-1007">\_ \_ \_ синтаксический анализ ненадежного заголовка для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-1007">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="fc010-1008">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-1008">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-1009">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1009">X</span></span> | \- | <span data-ttu-id="fc010-1010">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1010">X</span></span> | \- |
| <span data-ttu-id="fc010-1011">\_Обновление параметра \_ WinHTTP \_ до \_ веб- \_ сокета</span><span class="sxs-lookup"><span data-stu-id="fc010-1011">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="fc010-1012">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fc010-1012">N/A</span></span> | \- | <span data-ttu-id="fc010-1013">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1013">X</span></span> | \- | <span data-ttu-id="fc010-1014">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1014">X</span></span> | \- |
| <span data-ttu-id="fc010-1015">\_ \_ URL-адрес параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-1015">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="fc010-1016">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-1016">**LPWSTR**</span></span> | \- | <span data-ttu-id="fc010-1017">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1017">X</span></span> | <span data-ttu-id="fc010-1018">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1018">X</span></span> | \- | \- |
| <span data-ttu-id="fc010-1019">\_параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера</span><span class="sxs-lookup"><span data-stu-id="fc010-1019">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="fc010-1020">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="fc010-1020">**BOOL**</span></span> | <span data-ttu-id="fc010-1021">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1021">X</span></span> | <span data-ttu-id="fc010-1022">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1022">X</span></span> | \- | <span data-ttu-id="fc010-1023">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1023">X</span></span> | \- |
| <span data-ttu-id="fc010-1024">\_ \_ Агент пользователя для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-1024">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="fc010-1025">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-1025">**LPWSTR**</span></span> | <span data-ttu-id="fc010-1026">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1026">X</span></span> | \- | <span data-ttu-id="fc010-1027">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1027">X</span></span> | <span data-ttu-id="fc010-1028">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1028">X</span></span> | \- |
| <span data-ttu-id="fc010-1029">\_имя пользователя для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-1029">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="fc010-1030">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="fc010-1030">**LPWSTR**</span></span> | \- | <span data-ttu-id="fc010-1031">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1031">X</span></span> | <span data-ttu-id="fc010-1032">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1032">X</span></span> | <span data-ttu-id="fc010-1033">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1033">X</span></span> | \- |
| <span data-ttu-id="fc010-1034">\_ \_ \_ \_ время ожидания закрытия веб-СОКЕТа для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-1034">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="fc010-1035">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-1035">**DWORD**</span></span> | \- | \- | <span data-ttu-id="fc010-1036">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1036">X</span></span> | <span data-ttu-id="fc010-1037">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1037">X</span></span> | \- |
| <span data-ttu-id="fc010-1038">\_интервал проверки \_ активности веб- \_ сокета для \_ параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-1038">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="fc010-1039">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-1039">**DWORD**</span></span> | \- | \- | <span data-ttu-id="fc010-1040">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1040">X</span></span> | <span data-ttu-id="fc010-1041">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1041">X</span></span> | \- |
| <span data-ttu-id="fc010-1042">\_параметр WinHTTP \_ \_ \_ \_ Размер буфера получения веб-сокета \_</span><span class="sxs-lookup"><span data-stu-id="fc010-1042">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="fc010-1043">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-1043">**DWORD**</span></span> | <span data-ttu-id="fc010-1044">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1044">X</span></span> | <span data-ttu-id="fc010-1045">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1045">X</span></span> | <span data-ttu-id="fc010-1046">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1046">X</span></span> | <span data-ttu-id="fc010-1047">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1047">X</span></span> | <span data-ttu-id="fc010-1048">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fc010-1048">Windows 8.1</span></span> |
| <span data-ttu-id="fc010-1049">\_ \_ \_ \_ \_ Размер буфера отправки для веб-сокета параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="fc010-1049">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="fc010-1050">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-1050">**DWORD**</span></span> | <span data-ttu-id="fc010-1051">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1051">X</span></span> | <span data-ttu-id="fc010-1052">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1052">X</span></span> | <span data-ttu-id="fc010-1053">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1053">X</span></span> | <span data-ttu-id="fc010-1054">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1054">X</span></span> | <span data-ttu-id="fc010-1055">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fc010-1055">Windows 8.1</span></span> |
| <span data-ttu-id="fc010-1056">\_ \_ \_ число рабочих потоков \_ параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-1056">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="fc010-1057">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-1057">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="fc010-1058">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1058">X</span></span> | \- |
| <span data-ttu-id="fc010-1059">\_ \_ \_ Размер буфера записи параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-1059">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="fc010-1060">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc010-1060">**DWORD**</span></span> | \- | <span data-ttu-id="fc010-1061">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1061">X</span></span> | <span data-ttu-id="fc010-1062">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1062">X</span></span> | <span data-ttu-id="fc010-1063">X</span><span class="sxs-lookup"><span data-stu-id="fc010-1063">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="fc010-1064">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="fc010-1064">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc010-1065">Требования</span><span class="sxs-lookup"><span data-stu-id="fc010-1065">Requirements</span></span>

| <span data-ttu-id="fc010-1066">Требование</span><span class="sxs-lookup"><span data-stu-id="fc010-1066">Requirement</span></span> | <span data-ttu-id="fc010-1067">Значение</span><span class="sxs-lookup"><span data-stu-id="fc010-1067">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="fc010-1068">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc010-1068">Minimum supported client</span></span> | <span data-ttu-id="fc010-1069">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc010-1069">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="fc010-1070">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc010-1070">Minimum supported server</span></span> | <span data-ttu-id="fc010-1071">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc010-1071">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="fc010-1072">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="fc010-1072">Redistributable</span></span>          | <span data-ttu-id="fc010-1073">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fc010-1073">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="fc010-1074">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fc010-1074">Header</span></span>                   | <span data-ttu-id="fc010-1075">WinHTTP. h</span><span class="sxs-lookup"><span data-stu-id="fc010-1075">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="fc010-1076">См. также</span><span class="sxs-lookup"><span data-stu-id="fc010-1076">See also</span></span>

[<span data-ttu-id="fc010-1077">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fc010-1077">WinHTTP Versions</span></span>](winhttp-versions.md)
