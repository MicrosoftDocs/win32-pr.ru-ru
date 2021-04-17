---
Description: В Винхттпкуерйоптион и Винхттпсетоптион поддерживаются следующие флаги параметров.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Флаги параметров (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 56eea8e528c445c5ce6f852ff8841073dd74d6a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718133"
---
# <a name="option-flags"></a><span data-ttu-id="a4a5c-103">Флаги параметров</span><span class="sxs-lookup"><span data-stu-id="a4a5c-103">Option Flags</span></span>

<span data-ttu-id="a4a5c-104">В [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) и [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)поддерживаются следующие флаги параметров.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="a4a5c-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_параметр WinHTTP \_ — \_ \_ неблокирующие \_ обратные вызовы**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-106">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-106">The default is FALSE.</span></span> <span data-ttu-id="a4a5c-107">Если задано значение TRUE, служба WinHTTP не гарантирует ход выполнения, если клиентское приложение блокирует обратные вызовы состояния.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="a4a5c-108">Клиентское приложение должно соблюдать особое внимание для выполнения минимальных операций в обратном вызове без блокировки, возврата как можно быстрее, а в частности не должен ждать последующего вызова WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="a4a5c-109">Если это не соответствует этим рекомендациям, вероятно, это отрицательное воздействие на производительность или зависание приложения.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="a4a5c-110">Если используется заранее, этот параметр может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**\_ \_ политика автоматического входа в службу WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-112">Задает длинное целочисленное значение без знака, определяющее [политику автоматического входа в систему](authentication-in-winhttp.md) с одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="a4a5c-113">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-113">Term</span></span> | <span data-ttu-id="a4a5c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-114">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>\_ \_ \_ высокий уровень безопасности автоматического входа \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="a4a5c-116">Учетные данные по умолчанию не используются.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-116">Default credentials are not used.</span></span> <span data-ttu-id="a4a5c-117">Обратите внимание, что этот флаг вступает в силу только в том случае, если сервер задается фактическим именем компьютера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="a4a5c-118">Он не вступит в силу, если сервер указывается как localhost или IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="a4a5c-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>\_ \_ \_ низкий уровень безопасности автоматического входа \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="a4a5c-120">Вход с проверкой подлинности с использованием учетных данных по умолчанию выполняется для всех запросов.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="a4a5c-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>\_уровень безопасности автоматического входа WinHTTP — \_ \_ \_ средний</span><span class="sxs-lookup"><span data-stu-id="a4a5c-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="a4a5c-122">Вход с проверкой подлинности с использованием учетных данных по умолчанию выполняется только для запросов в локальной интрасети.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4a5c-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_ \_ обратный вызов параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-124">Получает указатель на функцию обратного вызова, заданную с помощью [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_ \_ \_ контекст сертификата клиента для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-126">Задает контекст сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-126">Sets the client certificate context.</span></span> <span data-ttu-id="a4a5c-127">Если приложение получает [**сообщение об ошибке " \_ \_ \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP**](error-messages.md)", он должен вызвать [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) для предоставления сертификата, прежде чем повторять запрос.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="a4a5c-128">В ходе обработки этого параметра служба WinHttp вызывает [**цертдупликатецертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) в контексте сертификата, предоставленного вызывающим объектом, чтобы контекст сертификата можно было независимо освободить от вызывающего.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="a4a5c-129">Приложению не следует попытаться закрыть хранилище сертификатов с помощью \_ флага "Close" ( \_ \_ Сбросить флаг принудительного восстановления сертификата) \_ в вызове [**цертклосесторе**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) в хранилище сертификатов, из которого был получен контекст сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="a4a5c-130">Может произойти нарушение прав доступа.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-130">An access violation may occur.</span></span>

<span data-ttu-id="a4a5c-131">Когда сервер запрашивает сертификат клиента, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)или [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) возвращает [**ошибку, \_ \_ \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP**](error-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="a4a5c-132">Если сервер запрашивает сертификат, но не требует его, приложение может указать этот параметр, чтобы указать, что у него нет сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="a4a5c-133">Сервер может выбрать другую схему проверки подлинности или разрешить анонимный доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="a4a5c-134">Приложение предоставляет **\_ \_ \_ \_ Контекстный макрос WinHTTP No Client** Certificate в параметре *лпбуффер* объекта [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="a4a5c-135">Если серверу требуется сертификат клиента, он может отправить код состояния HTTP 403 в ответе.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="a4a5c-136">Дополнительные сведения см. в описании параметра **WinHTTP Certificate \_ \_ Client \_ CERT \_ Issuer \_** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_ \_ \_ \_ список поставщиков сертификатов клиента для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-138">Извлекает структуру [**\_ иссуерлистинфоекс секпкгконтекст**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , когда ошибка из [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) или [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) является **ошибкой \_ \_ \_ сертификата проверки подлинности \_ \_ клиента WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="a4a5c-139">Список издателей в структуре содержит список приемлемых центров сертификации (ЦС) с сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="a4a5c-140">Клиентское приложение может отфильтровать список центров сертификации, чтобы получить сертификат клиента для проверки подлинности SSL.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="a4a5c-141">Кроме того, если сервер запрашивает сертификат клиента, но не требует его, приложение может вызвать [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с параметром **\_ контекста WinHTTP параметр \_ \_ сертификата \_ клиента** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="a4a5c-142">Дополнительные сведения см. в описании параметра службы **WinHTTP \_ параметр \_ \_ \_ контекста сертификата клиента** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**\_ \_ кодовая страница параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-144">Задает [*кодовую страницу*](glossary.md) , используемую для обработки URL-адреса (то есть строки запроса).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="a4a5c-145">По умолчанию используется значение UTF8.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_параметр WinHTTP \_ Настройка \_ \_ проверки подлинности паспорта**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-147">Задает длинное целое число без знака, указывающее, включена ли [Проверка подлинности Passport при](passport-authentication-in-winhttp.md) проверке подлинности WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="a4a5c-148">Он может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a4a5c-148">The value can be one of the following:</span></span>

| <span data-ttu-id="a4a5c-149">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-149">Term</span></span> | <span data-ttu-id="a4a5c-150">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-150">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>\_Служба WinHTTP отключает проверку \_ \_ подлинности Passport</span><span class="sxs-lookup"><span data-stu-id="a4a5c-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="a4a5c-152">Microsoft Passport проверка подлинности отключена.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="a4a5c-153">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-153">This is the default.</span></span> |
| <span data-ttu-id="a4a5c-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ отключение \_ набора \_ ключей паспорта</span><span class="sxs-lookup"><span data-stu-id="a4a5c-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="a4a5c-155">Набор ключей паспорта отключен.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="a4a5c-156">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-156">This is the default.</span></span> |
| <span data-ttu-id="a4a5c-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>\_Служба WinHTTP включает проверку \_ \_ подлинности паспорта</span><span class="sxs-lookup"><span data-stu-id="a4a5c-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="a4a5c-158">Проверка подлинности паспорта включена.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="a4a5c-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>\_Служба WinHTTP включает набор \_ \_ ключей Passport</span><span class="sxs-lookup"><span data-stu-id="a4a5c-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="a4a5c-160">Набор ключей паспорта включен.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="a4a5c-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_ \_ повторные попытки соединения с ПАРАМЕТРом WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-162">Задает или получает длинное целое число без знака, которое содержит число попыток подключения к узлу Тимесвинхттп.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="a4a5c-163">Службы Microsoft Windows HTTP (WinHTTP) пытаются попытаться только один раз на IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="a4a5c-164">Например, при попытке подключиться к многосетевому узлу, имеющему 10 IP-адресов, а **\_ параметру WinHTTP \_ \_ попыток подключения** будет присвоено значение 7, служба WinHTTP попытается подключиться только к первым семи IP-адресам.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="a4a5c-165">Если один набор из 10 IP-адресов установлен в значение 20, то служба WinHTTP попытается выполнить каждую из 10 только один раз. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="a4a5c-166">Если попытка соединения по-прежнему завершается неудачей после указанного числа попыток или если время ожидания соединения истекло раньше, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="a4a5c-167">Значение по умолчанию **для \_ параметра \_ \_ WinHTTP** — пять попыток.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**\_ \_ время ожидания соединения для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-169">Задает или получает длинное целое число без знака, содержащее значение времени ожидания в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="a4a5c-170">Если установить для этого параметра значение Infinite (0xFFFFFFFF), этот таймер будет отключен.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="a4a5c-171">Если запрос на TCP-соединение длится дольше этого значения времени ожидания, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="a4a5c-172">Время ожидания по умолчанию — 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="a4a5c-173">При попытке подключения к нескольким IP-адресам для одного узла (многосетевой узел) для каждого отдельного соединения устанавливается ограничение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**\_ \_ сведения о соединении параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-175">Извлекает исходный и конечный IP-адрес и порт запроса, который создал ответ при возвращении [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="a4a5c-176">Приложение вызывает [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) с параметром **WinHTTP \_ \_ \_ сведения о соединении** и предоставляет структуру [**\_ \_ сведений о соединении WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) в параметре *лпбуффер* .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="a4a5c-177">Дополнительные сведения см. в **разделе \_ \_ сведения о подключении к WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="a4a5c-178">**Windows Server 2003 с пакетом обновления SP1 и Windows XP с пакетом обновления 2 (SP2):** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_Параметр WinHTTP \_ Connection \_ stats \_ v0**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-180">Извлекает структуру [**TCP \_ info \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) для базового соединения, используемого запросом.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="a4a5c-181">Возвращаемая структура может содержать статистику предыдущих запросов, отправленных по тому же соединению.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="a4a5c-182">Этот параметр был заменен **\_ параметром WinHTTP \_ Connection \_ stats \_ v1**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Параметр WinHTTP \_ Connection \_ stats \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-184">Извлекает структуру [**TCP \_ \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) для базового соединения, используемого запросом.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="a4a5c-185">Возвращаемая структура может содержать статистику предыдущих запросов, отправленных по тому же соединению.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_ \_ значение контекста WinHTTP для параметра \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-187">Задает или получает **двойное слово \_ типа DWORD** , содержащее указатель на значение контекста, связанное с этим [хинтернет](hinternet-handles-in-winhttp.md) -обработчиком.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="a4a5c-188">Используется значение, хранящееся в буфере, а для флага Option **\_ \_ \_ значения контекста WinHTTP** задано новое значение.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**\_ \_ распаковка параметров WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-190">Задает параметр DWORD флагов, который определяет, будет ли WinHTTP автоматически распаковывать текст ответа с сжатыми кодировками содержимого.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="a4a5c-191">WinHTTP также установит соответствующий заголовок Accept-Encoding, переопределив все, предоставленные вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="a4a5c-192">Поддерживаются значения:</span><span class="sxs-lookup"><span data-stu-id="a4a5c-192">Supported values are:</span></span>

| <span data-ttu-id="a4a5c-193">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-193">Term</span></span> | <span data-ttu-id="a4a5c-194">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-194">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_флаг распаковки \_ WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="a4a5c-196">Распаковка содержимого в кодировке: отклики gzip.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="a4a5c-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_ДЕуплотнение \_ ФЛАГа РАСПАКОВКи WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="a4a5c-198">Распаковка содержимого в кодировке: разворачивает ответы.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="a4a5c-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_ \_ все ФЛАГи РАСПАКОВКи WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="a4a5c-200">Распаковка ответов с любой поддерживаемой кодировкой содержимого.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="a4a5c-201">По умолчанию WinHTTP будет доставлять сжатые ответы вызывающему объекту без изменений.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**\_ \_ функция отключения параметров \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-203">Задает длинное целочисленное значение без знака, указывающее, какие функции отключены с помощью одного или нескольких из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="a4a5c-204">Имейте в виду, что эта функция должна передаваться только в [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) в дескрипторах запросов после создания дескриптора запроса с помощью [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)и перед отправкой запроса с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="a4a5c-205">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-205">Term</span></span> | <span data-ttu-id="a4a5c-206">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-206">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ отключение \_ проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="a4a5c-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="a4a5c-208">Автоматическая проверка подлинности отключена.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="a4a5c-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ отключение \_ файлов cookie</span><span class="sxs-lookup"><span data-stu-id="a4a5c-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="a4a5c-210">Автоматическое добавление заголовков файлов cookie в запросы отключено.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="a4a5c-211">Кроме того, возвращенные файлы cookie не добавляются автоматически в базу данных cookie.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="a4a5c-212">Отключение файлов cookie может привести к низкой производительности проверки подлинности Passport.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="a4a5c-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>\_отключение \_ поддержания \_ активности WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="a4a5c-214">Отключает семантику поддержания активности для соединения.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="a4a5c-215">Семантика проверки активности требуется для MSN, NTLM и других типов аутентификации.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="a4a5c-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>\_отключение \_ ПЕРЕнаправлений WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="a4a5c-217">Автоматическое перенаправление отключено при отправке запросов с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="a4a5c-218">Если автоматическое перенаправление отключено, приложение должно зарегистрировать функцию обратного вызова, чтобы обеспечить успешную проверку подлинности Passport.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4a5c-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_параметр WinHTTP \_ Отключить \_ откат безопасных \_ протоколов \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-220">Предотвращает повторное выполнение службой WinHTTP соединения с более ранней версией протокола безопасности при сбое согласования первоначального протокола.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**\_параметр WinHTTP \_ Отключить \_ \_ очередь потока**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-222">Позволяет новым запросам открывать дополнительное соединение HTTP/2 при достижении максимального количества одновременных потоков, а не ждать следующего доступного потока в существующем соединении.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**\_ \_ Включение \_ функции WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-224">Задает длинное целое число без знака, определяющее включенные в данный момент функции.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="a4a5c-225">Может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-225">Can be one of the following values.</span></span>

| <span data-ttu-id="a4a5c-226">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-226">Term</span></span> | <span data-ttu-id="a4a5c-227">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-227">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ Включение \_ \_ олицетворения при отмене SSL \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="a4a5c-229">Если параметр включен, WinHTTP временно восстанавливает олицетворение клиента на время выполнения операций аутентификации SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="a4a5c-230">Это значение может быть задано только в обработчике сеанса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="a4a5c-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ Включение \_ \_ отзыва SSL</span><span class="sxs-lookup"><span data-stu-id="a4a5c-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="a4a5c-232">Если этот режим включен, WinHTTP разрешает отзыв SSL.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="a4a5c-233">Это значение можно задать только в обработчике запроса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_параметр WinHTTP \_ Включение \_ \_ протокола HTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-235">Задает битовую маску DWORD допустимых расширенных версий HTTP.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="a4a5c-236">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a4a5c-236">Possible values are:</span></span>

| <span data-ttu-id="a4a5c-237">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-237">Term</span></span> | <span data-ttu-id="a4a5c-238">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-238">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_Флаг протокола \_ WinHTTP \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a4a5c-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="a4a5c-240">Включает HTTP/2 для запроса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="a4a5c-241">Нет (0x0)</span><span class="sxs-lookup"><span data-stu-id="a4a5c-241">None (0x0)</span></span> | <span data-ttu-id="a4a5c-242">Разрешает запрос в формате HTTP/1.1 и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="a4a5c-243">Устаревшие версии протокола HTTP (1,1 и более ранних версий) нельзя отключить с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="a4a5c-244">Значение по умолчанию — 0x0.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_параметр WinHTTP \_ енаблетраЦинг**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-246">Задает **логическое** значение, указывающее, включена ли трассировка в данный момент.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-246">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="a4a5c-247">Дополнительные сведения о средстве трассировки в WinHTTP см. в разделе [средство трассировки WinHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-247">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="a4a5c-248">Этот параметр можно задать только для **нулевого** маркера **хинтернет** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-248">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="a4a5c-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**\_ \_ добавочная кодировка параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-250">Включает кодировку URL в процентах для пути и строки запроса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-250">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="a4a5c-251">Кроме того, можно закодировать процент перед вызовом WinHttp.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-251">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="a4a5c-252"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ Расширенная ошибка при выборе WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-252"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-253">Извлекает длинное целое число без знака, содержащее код ошибки сокетов Microsoft Windows, сопоставленный с ошибкой сообщения WinHTTP, которые были \_ \_ \* возвращены в данном контексте потока.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-253">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="a4a5c-254">В качестве значения Handle можно передать значение **null** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-254">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-255"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**\_ \_ \_ учетные записи глобального прокси-сервера параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-255"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-256">Принимает указатель на структуру с указанием учетных данных [**\_ \_ WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) с параметром функции *хинтернет* , имеющим значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-256">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="a4a5c-257">Для этого параметра требуется раздел реестра **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet параметры Интернета! Шарекредсвисвинхттп**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-257">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a4a5c-258">Если этот раздел реестра не задан, служба WinHTTP вернет ошибку **Ошибка \_ WinHTTP \_ Недопустимый \_ параметр**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-258">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="a4a5c-259">Этот раздел реестра отсутствует по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-259">This registry key is not present by default.</span></span> <span data-ttu-id="a4a5c-260">Когда она задана, WinINet отправит учетные данные на WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-260">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a4a5c-261">Всякий раз, когда WinHttp получает запрос проверки подлинности и если для текущего обработчика не заданы учетные данные, он будет использовать учетные данные, предоставляемые WinINet.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-261">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="a4a5c-262">Чтобы предоставить общий доступ к учетным данным сервера в дополнение к учетным данным прокси-сервера, пользователям необходимо задать **\_ параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-262">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-263"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**Параметры WINHTTP глобальные учетные значения \_ \_ \_ сервера \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-263"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-264">Принимает указатель на структуру с указанием учетных данных [**\_ \_ WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) с параметром функции *хинтернет* , имеющим значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-264">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="a4a5c-265">Для этого параметра требуется раздел реестра **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet параметры Интернета! Шарекредсвисвинхттп**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-265">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a4a5c-266">Если этот раздел реестра не задан, служба WinHTTP вернет ошибку **Ошибка \_ WinHTTP \_ Недопустимый \_ параметр**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-266">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="a4a5c-267">Этот раздел реестра отсутствует по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-267">This registry key is not present by default.</span></span> <span data-ttu-id="a4a5c-268">Когда она задана, WinINet отправит учетные данные на WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-268">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a4a5c-269">Всякий раз, когда WinHttp получает запрос проверки подлинности и если для текущего обработчика не заданы учетные данные, он будет использовать учетные данные, предоставляемые WinINet.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-269">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="a4a5c-270">Чтобы предоставить общий доступ к учетным данным сервера в дополнение к учетным данным прокси-сервера, пользователям необходимо задать **\_ параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-270">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-271"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**\_ \_ тип обработчика параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-271"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-272">Извлекает длинное целочисленное значение без знака, содержащее тип переданного в [хинтернет](hinternet-handles-in-winhttp.md) маркера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-272">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="a4a5c-273">Может возвращаться одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a4a5c-273">The return value can be one of the following:</span></span>

| <span data-ttu-id="a4a5c-274">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-274">Term</span></span> | <span data-ttu-id="a4a5c-275">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-275">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-276"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_тип обработчика WinHTTP \_ \_ Connect</span><span class="sxs-lookup"><span data-stu-id="a4a5c-276"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="a4a5c-277">Этот маркер является маркером соединения.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-277">The handle is a connection handle.</span></span> |
| <span data-ttu-id="a4a5c-278"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_запрос типа для обработчика WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-278"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="a4a5c-279">Этот маркер является обработчиком запросов.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-279">The handle is a request handle.</span></span> |
| <span data-ttu-id="a4a5c-280"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_сеанс типа для обработчика WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-280"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="a4a5c-281">Этот обработчик является обработчиком сеанса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-281">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4a5c-282"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_ \_ \_ требуется протокол HTTP для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-282"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-283">Предотвращает использование в запросе версий протокола, отличных от, включенных **\_ параметром WinHTTP, \_ Включение \_ \_ протокола HTTP** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-283">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-284"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**\_ \_ \_ используемый протокол HTTP \_ для параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-284"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-285">Возвращает значение типа DWORD, указывающее, какая расширенная версия HTTP использовалась для данного запроса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-285">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="a4a5c-286">Список возможных значений см. в разделе **параметр WinHTTP \_ \_ включить \_ \_ протокол HTTP**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-286">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-287"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_ \_ Версия HTTP параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-287"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-288">Задает или получает структуру [**\_ \_ сведений о версии HTTP**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) , которая содержит поддерживаемую версию HTTP.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-288">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="a4a5c-289">Это параметр на уровне процесса; для этого маркера используйте **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-289">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-290"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_параметр WinHTTP \_ игнорировать \_ отзыв сертификата в \_ \_ автономном режиме**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-290"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-291">Позволяет защищенным подключениям использовать сертификаты безопасности, для которых не удалось скачать список отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-291">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-292"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_ \_ \_ Быстрый откат параметров WinHTTP \_ IPv6**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-292"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-293">Включает быстрое резервное восстановление IPv6 (более глаз) для подключения.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-293">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="a4a5c-294">Такое поведение аналогично поведению счастливого глаз, описанного в [RFC 6555](https://tools.ietf.org/html/rfc6555) , для повышения времени подключения в сетях, в которых IPv6 является ненадежным.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-294">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="a4a5c-295">Если адреса IPv6 и IPv4 разрешаются для данного узла, служба WinHttp начнет с подключения к первому разрешенному IPv6-адресу с коротким (300 мс) временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-295">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="a4a5c-296">Если соединение не будет выполнено, служба WinHttp попытается подключиться к первому разрешенному IPv4-адресу со стандартным временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-296">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="a4a5c-297">Если произойдет сбой второго подключения, служба WinHttp попытается повторить первый разрешенный IPv6-адрес со стандартным временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-297">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="a4a5c-298">В случае сбоя третьего подключения WinHttp вернется к поведению по умолчанию для оставшихся адресов, пытаясь подключиться к каждому из них со стандартным временем ожидания до тех пор, пока не будет установлено соединение или не останется ни одного адреса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-298">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-299"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**\_параметр WinHTTP \_ — \_ ответ прокси- \_ подключения \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-299"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-300">Возвращает значение, указывающее, может ли быть получен ответ на возвращаемое соединение прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-300">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-301"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_Параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ \_ \_ сервер 1 0**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-301"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-302">Задает или получает длинное целое число без знака, содержащее максимально допустимое количество подключений на сервер HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-302">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="a4a5c-303">Значение по умолчанию — **Infinite**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-303">The default value is **INFINITE**.</span></span>

<span data-ttu-id="a4a5c-304">**Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008:** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-304">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-305"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ сервер**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-305"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-306">Задает или получает длинное целое число без знака, содержащее максимально допустимое количество подключений на сервер.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-306">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="a4a5c-307">Значение по умолчанию — **Infinite**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-307">The default value is **INFINITE**.</span></span>

<span data-ttu-id="a4a5c-308">Если этот параметр имеет значение 0, WinHTTP устанавливает ограничение на число подключений равным 2.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-308">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-309"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**\_параметр WinHTTP \_ Максимальное \_ число \_ автоматических \_ перенаправлений HTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-309"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-310">Задает максимальное число перенаправлений, которые следует указать WinHTTP; значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-310">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="a4a5c-311">Это ограничение не позволяет неавторизованным сайтам сделать остановку клиента WinHTTP после большого числа перенаправлений.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-311">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="a4a5c-312">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-312">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-313"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_продолжение параметра \_ максимального \_ \_ состояния HTTP \_ для WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-313"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-314">Максимальное число ответов с кодом состояния 100-199, которые игнорируются перед возвратом окончательного кода состояния клиенту WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-314">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="a4a5c-315">Коды состояния 100-199 могут отправляться сервером перед окончательным кодом состояния и описаны в спецификации HTTP/1.1 (Дополнительные сведения см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-315">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="a4a5c-316">Значение по умолчанию равно 10.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-316">The default is 10.</span></span>

<span data-ttu-id="a4a5c-317">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-317">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-318"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**параметр WINHTTP — \_ \_ максимальный \_ \_ Размер очистки ответа \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-318"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-319">Объект, привязанный к объему данных, остановленных из ответов для повторного использования соединения, указанного в байтах.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-319">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="a4a5c-320">Значение по умолчанию — 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-320">The default is 1MB.</span></span>

<span data-ttu-id="a4a5c-321">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-321">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-322"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_параметр WinHTTP \_ максимальный \_ \_ размер заголовка \_ ответа**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-322"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-323">Ограничивающий набор для максимального размера части заголовка ответа сервера, указанного в байтах.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-323">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="a4a5c-324">Эта привязка защищает клиента от неавторизованного сервера, пытающегося приостановки работы клиента, отправив ответ с бесконечным объемом данных заголовка.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-324">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="a4a5c-325">Значение по умолчанию — 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-325">The default value is 64KB.</span></span>

<span data-ttu-id="a4a5c-326">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-327"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ родительский маркер параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-327"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-328">Получает родительский маркер для этого маркера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-328">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-329"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**\_параметр WinHTTP \_ , \_ софирменный текст в паспорте \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-329"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-330">Извлекает строку, содержащую [*фирменный*](glossary.md) текст, предоставленный сервером входа Passport.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-330">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="a4a5c-331">Этот параметр следует получать сразу после ответа сервера входа с кодом состояния 401.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-331">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="a4a5c-332">Приложение должно передавать размер буфера в байтах, достаточно большой для хранения возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-332">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-333"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_ \_ \_ URL-адрес КОфирменной символики для службы WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-333"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-334">Извлекает строку, содержащую URL-адрес [*фирменной символики*](glossary.md) , предоставляемой сервером входа Passport.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-334">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="a4a5c-335">Этот параметр следует получать сразу после ответа сервера входа с кодом состояния 401.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-335">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="a4a5c-336">Приложение должно передавать размер буфера в байтах, достаточно большой для хранения возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-336">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-337"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_ \_ \_ \_ URL-адрес возврата паспорта с параметром WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-337"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-338">Устанавливает параметр "только для чтения" для обработчика запроса, который получает URL-адрес возврата Passport.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-338">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-339"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**\_команда WinHTTP \_ выход \_ \_ из паспорта**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-339"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-340">Задает параметр в обработчике сеанса для выхода из любых имен входа Passport.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-340">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="a4a5c-341">Приложение должно передать URL-адрес возврата Passport, полученный с помощью **\_ функции WinHTTP \_ \_ \_ URL-адрес возврата Passport**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-341">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="a4a5c-342">Все файлы cookie, связанные с URL-адресом возврата, очищаются.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-342">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-343"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_пароль для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-343"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-344">Задает или получает строковое значение, содержащее пароль, связанный с обработчиком запроса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-344">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-345"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_ \_ прокси-сервер параметров WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-345"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-346">Задает или получает структуру [**\_ \_ сведений о прокси-сервере WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) , которая содержит данные прокси-сервера для существующего обработчика сеанса или обработчика запроса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-346">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="a4a5c-347">При получении данных прокси-сервера приложение должно освободить строки **лпсзпрокси** и **лпсзпроксибипасс** , содержащиеся в этой структуре (если они не **равны NULL**), с помощью функции [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-347">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="a4a5c-348">Приложение может запросить данные глобального прокси-сервера (прокси-сервер по умолчанию), передав маркер **null** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-348">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-349"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_ \_ пароль прокси-сервера для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-349"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-350">Задает или получает строковое значение, содержащее пароль, используемый для доступа к прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-350">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-351"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**\_используется параметр WinHTTP \_ прокси- \_ службы \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-351"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-352">Возвращает имя участника прокси-сервера, предоставляемое WinHTTP для SSPI во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-352">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="a4a5c-353">Это строковое значение является усефор передачей в [**сспипромптфоркредентиалс**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) после сбоя проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-353">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-354"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_параметр WinHTTP \_ \_ имя пользователя-посредника**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-354"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-355">Задает или получает строковое значение, содержащее имя пользователя, используемое для доступа к прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-355">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-356"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_ \_ \_ Размер буфера чтения параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-356"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-357">Этот параметр является устаревшим; Он не действует.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-357">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-358"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**\_параметр WinHTTP \_ Получение \_ ответа прокси-сервера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-358"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-359">Задает, может ли быть получена сущность ответа прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-359">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="a4a5c-360">Этот параметр отключен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-360">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-361"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**\_ \_ \_ время ожидания ответа для получения параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-361"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-362">Задает или получает длинное целое число без знака, которое содержит значение времени ожидания (в миллисекундах) ожидания получения всех заголовков ответа в запрос.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-362">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="a4a5c-363">Если служба WinHTTP не получает все заголовки в течение этого периода ожидания, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-363">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="a4a5c-364">Значение времени ожидания по умолчанию — 90 секунд.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-364">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="a4a5c-365">Это время ожидания проверяется только при получении данных от сокета.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-365">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="a4a5c-366">В результате, по истечении времени ожидания клиентское приложение не получает уведомления, пока не поступают дополнительные данные с сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-366">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="a4a5c-367">Если данные не поступают с сервера, задержка между истечением времени ожидания и уведомлением клиентского приложения может быть выше, чем значение времени ожидания, заданное с помощью параметра *дврецеиветимеаут* функции [**винхттпсеттимеаутс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-367">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-368"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_ \_ время ожидания получения параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-368"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-369">Задает или получает длинное целое число без знака, которое содержит значение времени ожидания (в миллисекундах) для получения частичного ответа на запрос или чтения некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-369">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="a4a5c-370">Если ответ длится дольше этого значения времени ожидания, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-370">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="a4a5c-371">По умолчанию время ожидания составляет 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-371">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-372"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_ \_ политика перенаправления для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-372"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-373">Задает поведение WinHTTP в отношении обработки кода состояния перенаправления HTTP повышалась.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-373">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="a4a5c-374">Этот параметр может быть установлен для сеанса или в обработчике запроса на одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a4a5c-374">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="a4a5c-375">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-375">Term</span></span> | <span data-ttu-id="a4a5c-376">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-376">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_параметр WinHTTP \_ политика перенаправления \_ \_ всегда</span><span class="sxs-lookup"><span data-stu-id="a4a5c-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="a4a5c-378">Все перенаправления выполняются автоматически.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-378">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="a4a5c-379"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_ \_ политика перенаправления параметра WinHTTP \_ \_ запретить \_ HTTPS \_ для \_ http</span><span class="sxs-lookup"><span data-stu-id="a4a5c-379"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="a4a5c-380">Все перенаправления выполняются, за исключением тех, которые исходят от защищенного URL-адреса (HTTPS) на небезопасный (http) URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-380">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="a4a5c-381">Это параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-381">This is the default setting.</span></span> |
| <span data-ttu-id="a4a5c-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_параметр WinHTTP \_ Перенаправление \_ политики \_ никогда не</span><span class="sxs-lookup"><span data-stu-id="a4a5c-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="a4a5c-383">Перенаправления не идут.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-383">Redirects are never followed.</span></span> <span data-ttu-id="a4a5c-384">Состояние повышалась возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-384">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-385"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_параметр WinHTTP \_ отклонять \_ усерпвд \_ в \_ URL-адресе**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-385"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-386">Отклоняет URL-адреса, содержащие имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-386">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="a4a5c-387">Этот параметр также отклоняет URL-адреса, содержащие семантику *username: Password* , даже если имя пользователя или пароль не указаны.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-387">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="a4a5c-388">Например, " u:p@hostname ", " :@hostname ", " u:@hostname " и " :p@hostname " будут помечены как недопустимые.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-388">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="a4a5c-389">Если функции передан недопустимый URL-адрес, он возвращает [ошибку \_ WinHTTP \_ Недопустимый \_ URL-адрес](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-389">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="a4a5c-390">По умолчанию этот параметр выключен.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-390">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-391"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_ \_ приоритет запроса параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-391"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-392">Этот параметр является устаревшим; Он не действует.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-392">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-393"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_ \_ Статистика запросов параметров \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-393"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-394">Статистика извлекает для запроса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-394">Retreives statistics for the request.</span></span>  <span data-ttu-id="a4a5c-395">Список доступных статистических данных см. в разделе [**\_ \_ Статистика запросов WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-395">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-396"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_ \_ время запроса параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-396"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-397">Сведения о времени извлекает для запроса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-397">Retreives timing information for the request.</span></span> <span data-ttu-id="a4a5c-398">Список доступных времени см. в разделе [**\_ \_ время запроса WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-398">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-399"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**\_ \_ время ожидания разрешения параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-399"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-400">Задает или получает длинное целое число без знака, содержащее значение времени ожидания (в миллисекундах) для разрешения имени узла.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-400">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="a4a5c-401">Значение времени ожидания по умолчанию — **Infinite**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-401">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="a4a5c-402">Если указано значение, отличное от значения по умолчанию, то для разрешения имен создается дополнительная нагрузка на один поток.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-402">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-403"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**Параметры WINHTTP для \_ \_ защищенных \_ протоколов**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-403"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-404">Задает длинное целое число без знака, которое указывает, какие безопасные протоколы приемлемы.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-404">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="a4a5c-405">По умолчанию в Windows 7 и Windows 8 включены только SSL3 и TLS1.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-405">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="a4a5c-406">По умолчанию в Windows 8.1 и Windows 10 включены только SSL3, TLS 1.0, TLS 1.1 и TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-406">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="a4a5c-407">Значение может быть сочетанием одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-407">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="a4a5c-408">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-408">Term</span></span> | <span data-ttu-id="a4a5c-409">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-409">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-410"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_флаг WinHTTP \_ безопасный \_ протокол \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-410"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="a4a5c-411">Можно использовать протоколы SSL (SSL) 2,0, SSL 3,0 и TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-411">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="a4a5c-412"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>SSL2 протокола WINHTTP с \_ флагом \_ Secure \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-412"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="a4a5c-413">Можно использовать протокол SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-413">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="a4a5c-414"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>SSL3 протокола WINHTTP с \_ флагом \_ Secure \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-414"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="a4a5c-415">Можно использовать протокол SSL 3,0.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-415">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="a4a5c-416"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>TLS1 протокола WINHTTP с \_ флагом \_ Secure \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-416"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="a4a5c-417">Можно использовать протокол TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-417">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="a4a5c-418"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_Флаг WinHTTP \_ \_ протокол Secure \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a4a5c-418"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="a4a5c-419">Можно использовать протокол TLS 1,1.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-419">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="a4a5c-420"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_Флаг WinHTTP \_ \_ протокол Secure \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="a4a5c-420"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="a4a5c-421">Можно использовать протокол TLS 1,2.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-421">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4a5c-422"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_ \_ \_ Структура сертификата безопасности параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-422"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-423">Извлекает сертификат для сервера SSL/TLS в структуру [**\_ \_ сведений о сертификате WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-423">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="a4a5c-424">Приложение должно освободить члены **лпсзсубжектинфо** и **Лпсзиссуеринфо** с помощью [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-424">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-425"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_ \_ Флаги безопасности для параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-425"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-426">Задает или получает длинное целое число без знака, содержащее флаги безопасности для маркера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-426">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="a4a5c-427">Это может быть сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a4a5c-427">It can be a combination of these values:</span></span>

| <span data-ttu-id="a4a5c-428">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-428">Term</span></span> | <span data-ttu-id="a4a5c-429">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-429">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-430"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>\_флаг безопасности \_ игнорирует \_ \_ недопустимое общее имя сертификата \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-430"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="a4a5c-431">Разрешает недопустимое общее имя в сертификате; то есть имя сервера, указанное приложением, не соответствует общему имени в сертификате.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-431">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="a4a5c-432">Если этот флаг установлен, приложение не получает **\_ флаг состояния обратного вызова WinHTTP \_ \_ \_ \_ \_ Недопустимый** обратный вызов для сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-432">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="a4a5c-433"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>\_ \_ \_ \_ Недопустимый срок игнорирования даты сертификата \_ для флага безопасности</span><span class="sxs-lookup"><span data-stu-id="a4a5c-433"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="a4a5c-434">Разрешает недействительную дату сертификата, то есть просроченный или еще не действующий сертификат.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-434">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="a4a5c-435">Если этот флаг установлен, приложение не получает **\_ \_ \_ \_ \_ \_ Недопустимый обратный вызов для флага состояния обратного вызова WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-435">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="a4a5c-436"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_ \_ пропуск \_ неизвестного \_ ЦС в качестве флага безопасности</span><span class="sxs-lookup"><span data-stu-id="a4a5c-436"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="a4a5c-437">Разрешает недопустимый центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-437">Allows an invalid certificate authority.</span></span> <span data-ttu-id="a4a5c-438">Если этот флаг установлен, приложение не получает **\_ флаг состояния обратного вызова WinHTTP \_ \_ \_ Недопустимый \_** обратный вызов CA.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-438">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="a4a5c-439"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>\_флаг безопасности \_ игнорирует \_ \_ неправильный способ \_ использования сертификата</span><span class="sxs-lookup"><span data-stu-id="a4a5c-439"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="a4a5c-440">Позволяет установить удостоверение сервера с помощью сертификата, не являющегося сервером (например, сертификата клиента).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-440">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="a4a5c-441"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_флаг безопасности \_ игнорирует \_ слабую \_ подпись</span><span class="sxs-lookup"><span data-stu-id="a4a5c-441"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="a4a5c-442">Позволяет игнорировать слабую подпись.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-442">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="a4a5c-443">Этот флаг доступен в обновлении свертки для каждой ОС, начиная с Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-443">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="a4a5c-444"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_безопасный флаг \_ безопасности</span><span class="sxs-lookup"><span data-stu-id="a4a5c-444"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="a4a5c-445">Использует безопасные передачи.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-445">Uses secure transfers.</span></span> <span data-ttu-id="a4a5c-446">Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-446">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a4a5c-447"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>уровень \_ стойкости флага безопасности \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-447"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="a4a5c-448">Использует среднее (56-разрядное) шифрование.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-448">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="a4a5c-449">Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-449">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a4a5c-450"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_сильная стойкость флага безопасности \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-450"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="a4a5c-451">Использует стойкое (128-разрядное) шифрование.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-451">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="a4a5c-452">Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-452">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a4a5c-453"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>\_ \_ слабая стойкость ФЛАГа безопасности \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-453"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="a4a5c-454">Использует слабое (40-разрядное) шифрование.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-454">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="a4a5c-455">Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-455">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4a5c-456"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**\_ \_ сведения о безопасности параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-456"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-457">Извлекает подключение SChannel и сведения о шифрах для запроса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-457">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-458"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**\_ \_ \_ разрядность ключа безопасности параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-458"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-459">Извлекает длинное целое значение без знака, содержащее стойкость шифра ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-459">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="a4a5c-460">Большее число означает более надежное шифрование стойкости шифра.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-460">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-461"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_ \_ время ожидания отправки для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-461"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-462">Задает или получает длинное целое число без знака, содержащее значение времени ожидания (в миллисекундах) для отправки запроса или записи некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-462">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="a4a5c-463">Если отправка запроса длится дольше, чем время ожидания, операция отправки отменяется.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-463">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="a4a5c-464">По умолчанию время ожидания составляет 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-464">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-465"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**\_ \_ CBT сервера параметров \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-465"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-466">Возвращает указатель на структуру [**\_ привязок секпкгконтекст**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) , указывающую маркер привязки канала (CBT).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-466">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="a4a5c-467">Токен привязки канала — это свойство защищенного канала транспорта, которое используется для привязки канала проверки подлинности к защищенному каналу транспорта.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-467">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="a4a5c-468">Этот маркер может быть получен только этим параметром после установки SSL-соединения.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-468">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="a4a5c-469">При передаче этого параметра и значения **null** для *лпбуффер* в [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) будет возвращена ошибка \_ , недостаточная для буфера \_ , и необходимый размер в байтах для буфера в параметре *лпдвбуфферленгс* .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-469">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="a4a5c-470">Возвращаемое значение размера буфера можно передать при последующем вызове запроса для маркера привязки канала.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-470">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="a4a5c-471">Эти действия необходимы при обработке \_ запроса состояния обратного вызова WinHTTP, \_ \_ Если требуется изменить заголовки запроса на основе токена привязки канала.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-471">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="a4a5c-472">Обратите внимание, что Windows XP и Vista не поддерживают изменение заголовков запросов во время этого обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-472">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-473"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**\_параметр WinHTTP \_ \_ \_ контекст цепочки сертификатов сервера \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-473"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-474">Извлекает контекст цепочки сертификатов сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-474">Retrieves the server certification chain context.</span></span> <span data-ttu-id="a4a5c-475">Служба **WinHTTP \_ \_ \_ \_ \_ Контекст цепочки сертификатов сервера** может быть передан для получения повторяющегося указателя на **\_ \_ контекст цепочки** сертификатов для цепочки сертификата сервера, полученной во время согласованного SSL-соединения.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-475">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="a4a5c-476">Клиент должен вызвать [**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) для возвращенного \_ указателя контекста пкцерт, который заполнен в буфере.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-476">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-477"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_ \_ \_ контекст сертификата сервера параметров \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-477"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-478">Получает контекст сертификации сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-478">Retrieves the server certification context.</span></span> <span data-ttu-id="a4a5c-479">Служба **WinHTTP \_ Для получения повторяющегося указателя на контекст сертификата сервера, полученного во время согласованного SSL-соединения, можно передать параметр \_ \_ \_ контекстного сертификата сервера** . [](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)</span><span class="sxs-lookup"><span data-stu-id="a4a5c-479">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="a4a5c-480">Клиент должен вызвать [**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) для возвращенного \_ указателя контекста пкцерт, который заполнен в буфере.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-480">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-481"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**\_ \_ \_ используемое имя субъекта-службы сервера параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-481"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-482">Возвращает имя участника серверного сервера, которое WinHTTP было передано в SSPI во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-482">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="a4a5c-483">Это строковое значение может быть передано в [**сспипромптфоркредентиалс**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) после сбоя проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-483">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-484"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**\_ \_ имя субъекта-службы для параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-484"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-485">Включает или удаляет номер порта сервера, если имя участника-службы (SPN) создано для проверки подлинности Kerberos или Negotiate.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-485">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="a4a5c-486">Этот флаг имеет одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a4a5c-486">This flag is one of the following values:</span></span>

| <span data-ttu-id="a4a5c-487">Термин</span><span class="sxs-lookup"><span data-stu-id="a4a5c-487">Term</span></span> | <span data-ttu-id="a4a5c-488">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a5c-488">Description</span></span> |
|-|-|
| <span data-ttu-id="a4a5c-489"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ отключение \_ \_ порта сервера \_ SPN</span><span class="sxs-lookup"><span data-stu-id="a4a5c-489"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="a4a5c-490">Удаляет номер порта сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-490">Removes the server port number.</span></span> |
| <span data-ttu-id="a4a5c-491"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>\_ \_ \_ порт сервера службы WinHTTP Enable SPN \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-491"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="a4a5c-492">Включает номер порта сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-492">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4a5c-493"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_параметр WinHTTP \_ TCP \_ fast \_ Open**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-493"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-494">Включает TCP Fast Open для подключения.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-494">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-495"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**\_Запуск параметра WinHTTP \_ TLS \_ false \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-495"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-496">Включает для соединения параметр TLS false.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-496">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-497"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**\_ \_ \_ событие уведомления о ВЫгрузке параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-497"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-498">Принимает событие, которое будет задано после завершения последнего обратного вызова для определенного сеанса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-498">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="a4a5c-499">Этот флаг должен быть использован для обработчика сеанса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-499">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="a4a5c-500">Событие не может быть закрыто до тех пор, пока оно не будет установлено WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-500">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-501"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**\_ \_ \_ синтаксический анализ ненадежного заголовка для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-501"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-502">Этот параметр зарезервирован для внутреннего использования и не должен вызываться.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-502">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-503"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_Обновление параметра \_ WinHTTP \_ до \_ веб- \_ сокета**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-503"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-504">Указывает стеку запустить процесс подтверждения соединения WebSocket с [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-504">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="a4a5c-505">Этот параметр не принимает параметров.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-505">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-506"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_ \_ URL-адрес параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-506"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-507">Извлекает строковое значение, содержащее полный URL-адрес скачанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-507">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="a4a5c-508">Если исходный URL-адрес содержал дополнительные данные, например строки поиска или привязки, или если вызов был перенаправлен, то возвращаемый URL-адрес отличается от исходного.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-508">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="a4a5c-509">Приложение должно передать в буфер размер в байтах, достаточно большой для хранения возвращенного URL-адреса в расширенном символе.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-509">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-510"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-510"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-511">Принимает **логическое** значение и может устанавливать только обработчик сеанса.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-511">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="a4a5c-512">Она будет распространяться только на дескрипторы, созданные из дескриптора сеанса после установки параметра.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-512">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="a4a5c-513">Если **значение — true**, этот параметр приводит к тому, что в качестве последнего средства используется учетные данные глобального сервера, которые были отправлены из wininet.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-513">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="a4a5c-514">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-514">The default for this option is **FALSE**.</span></span> <span data-ttu-id="a4a5c-515">Для этого параметра требуется раздел реестра **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet параметры Интернета! Шарекредсвисвинхттп**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-515">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a4a5c-516">Этот раздел реестра отсутствует по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-516">This registry key is not present by default.</span></span> <span data-ttu-id="a4a5c-517">Когда она задана, WinINet отправит учетные данные на WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-517">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a4a5c-518">Всякий раз, когда WinHttp получает запрос проверки подлинности и если для текущего обработчика не заданы учетные данные, он будет использовать учетные данные, предоставляемые WinINet.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-518">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-519"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_ \_ Агент пользователя для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-519"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-520">Задает или получает строку [*агента пользователя*](glossary.md) для дескрипторов, предоставляемых [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) , и используется в последующих функциях [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) , если она не переопределяется заголовком, добавленным [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) или **WinHttpSendRequest**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-520">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="a4a5c-521">При извлечении агента пользователя приложение должно передать в буфер размер в байтах, достаточно большой для хранения возвращенного URL-адреса в расширенном символе.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-521">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="a4a5c-522">При задании агента пользователя размер буфера — это длина строки в символах и знак завершения **null** .</span><span class="sxs-lookup"><span data-stu-id="a4a5c-522">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-523"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_имя пользователя для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-523"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-524">Задает или получает строку, содержащую имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-524">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-525"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_ \_ \_ \_ время ожидания закрытия веб-СОКЕТа для параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-525"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-526">Задает время в миллисекундах, которое [**винхттпвебсоккетклосе**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) должно ожидать завершения подтверждения закрытия.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-526">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="a4a5c-527">Значение по умолчанию — 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-527">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-528"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_интервал проверки \_ активности веб- \_ сокета для \_ параметра WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-528"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-529">Задает интервал (в миллисекундах) отправки пакета проверки активности через соединение.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-529">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="a4a5c-530">Интервал по умолчанию — 30000 (30 секунд).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-530">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="a4a5c-531">Минимальный интервал — 15000 (15 секунд).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-531">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="a4a5c-532">Использование [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) для установки значения ниже 15000 будет возвращать ошибку с **\_ недопустимым \_ параметром**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-532">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="a4a5c-533">Значение по умолчанию **для \_ параметра \_ WinHTTP \_ \_ \_ интервал проверки активности веб-сокета** считывается из раздела **HKLM: \\ Software \\ Microsoft \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-533">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="a4a5c-534">Если значение не задано, будет использоваться значение по умолчанию 30000.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-534">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="a4a5c-535">Более низкий интервал активности не может превышать 15000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-535">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-536"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**\_параметр WinHTTP \_ \_ \_ \_ Размер буфера получения веб-сокета \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-536"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-537">Задает или получает значение типа DWORD, указывающее размер буфера приема, используемый для подключений WebSocket.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-537">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-538"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**\_ \_ \_ \_ \_ Размер буфера отправки для веб-сокета параметров WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-538"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-539">Задает или получает значение типа DWORD, указывающее размер буфера отправки, используемый для подключений WebSocket.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-539">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-540"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_ \_ \_ число рабочих потоков \_ параметра WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-540"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-541">Задает длинное целочисленное значение без знака, указывающее количество рабочих потоков, которые пул потоков должен использовать для асинхронных завершений.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-541">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="a4a5c-542">Значение этого параметра по умолчанию равно нулю, что указывает, что количество рабочих потоков равно числу процессоров в системе.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-542">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="a4a5c-543">Этот параметр может быть установлен только для [хинтернетного](hinternet-handles-in-winhttp.md) маркера **до выполнения** асинхронной операции.  </span><span class="sxs-lookup"><span data-stu-id="a4a5c-543">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="a4a5c-544">Этот параметр можно задать только один раз.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-544">This option can only be set once.</span></span>

<span data-ttu-id="a4a5c-545">**Windows Server 2008 R2 и Windows 7:** Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-545">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4a5c-546"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_ \_ \_ Размер буфера записи параметра \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-546"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4a5c-547">Этот параметр является устаревшим; Он не действует.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-547">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4a5c-548">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4a5c-548">Remarks</span></span>

<span data-ttu-id="a4a5c-549">В следующей таблице перечислены флаги параметров, указывающие, какие дескрипторы могут действовать, можно ли запрашивать и задавать их, а также использовать тип данных.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-549">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="a4a5c-550">"X" означает, что флаг параметра является допустимым для использования с функцией или обработчиком, а "-" указывает на недопустимый флаг параметра.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-550">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="a4a5c-551">Попытка задать или запросить флаг параметра в версии Windows, где она не поддерживается, приведет к **ошибке \_ \_ "Недопустимый WinHTTP \_ "**.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-551">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="a4a5c-552">Флаг параметра и тип данных</span><span class="sxs-lookup"><span data-stu-id="a4a5c-552">Option flag, and data type</span></span> | <span data-ttu-id="a4a5c-553">Обработчик сеанса</span><span class="sxs-lookup"><span data-stu-id="a4a5c-553">Session handle</span></span> | <span data-ttu-id="a4a5c-554">Маркер запроса</span><span class="sxs-lookup"><span data-stu-id="a4a5c-554">Request handle</span></span> | <span data-ttu-id="a4a5c-555">Параметр запросов</span><span class="sxs-lookup"><span data-stu-id="a4a5c-555">Query option</span></span> | <span data-ttu-id="a4a5c-556">Параметр SET</span><span class="sxs-lookup"><span data-stu-id="a4a5c-556">Set option</span></span> | <span data-ttu-id="a4a5c-557">Минимальная версия Windows</span><span class="sxs-lookup"><span data-stu-id="a4a5c-557">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="a4a5c-558">\_параметр WinHTTP \_ — \_ \_ неблокирующие \_ обратные вызовы</span><span class="sxs-lookup"><span data-stu-id="a4a5c-558">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="a4a5c-559">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-559">**BOOL**</span></span> | <span data-ttu-id="a4a5c-560">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-560">X</span></span> | \- | \- | <span data-ttu-id="a4a5c-561">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-561">X</span></span> | \- |
| <span data-ttu-id="a4a5c-562">\_ \_ политика автоматического входа в службу WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-562">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="a4a5c-563">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-563">**DWORD**</span></span> | \- | <span data-ttu-id="a4a5c-564">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-564">X</span></span> | \- | <span data-ttu-id="a4a5c-565">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-565">X</span></span> | \- |
| <span data-ttu-id="a4a5c-566">\_ \_ обратный вызов параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-566">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="a4a5c-567">**лпвоид**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-567">**LPVOID**</span></span> | <span data-ttu-id="a4a5c-568">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-568">X</span></span> | <span data-ttu-id="a4a5c-569">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-569">X</span></span> | <span data-ttu-id="a4a5c-570">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-570">X</span></span> | <span data-ttu-id="a4a5c-571">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-571">X</span></span> | \- |
| <span data-ttu-id="a4a5c-572">\_ \_ \_ контекст сертификата клиента для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-572">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="a4a5c-573">**\_контекст сертификата**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-573">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="a4a5c-574">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-574">X</span></span> | \- | <span data-ttu-id="a4a5c-575">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-575">X</span></span> | <span data-ttu-id="a4a5c-576">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4a5c-576">Windows Vista</span></span> |
| <span data-ttu-id="a4a5c-577">\_ \_ \_ \_ список поставщиков сертификатов клиента для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-577">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="a4a5c-578">**Секпкгконтекст \_ иссуерлистинфоекс**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-578">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="a4a5c-579">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-579">X</span></span> | <span data-ttu-id="a4a5c-580">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-580">X</span></span> | \- | <span data-ttu-id="a4a5c-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4a5c-581">Windows Vista</span></span> |
| <span data-ttu-id="a4a5c-582">\_ \_ кодовая страница параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-582">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="a4a5c-583">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-583">**DWORD**</span></span> | <span data-ttu-id="a4a5c-584">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-584">X</span></span> | \- | \- | <span data-ttu-id="a4a5c-585">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-585">X</span></span> | \- |
| <span data-ttu-id="a4a5c-586">\_параметр WinHTTP \_ Настройка \_ \_ проверки подлинности паспорта</span><span class="sxs-lookup"><span data-stu-id="a4a5c-586">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="a4a5c-587">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-587">**DWORD**</span></span> | <span data-ttu-id="a4a5c-588">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-588">X</span></span> | \- | \- | <span data-ttu-id="a4a5c-589">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-589">X</span></span> | \- |
| <span data-ttu-id="a4a5c-590">\_ \_ повторные попытки соединения с ПАРАМЕТРом WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-590">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="a4a5c-591">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-591">**DWORD**</span></span> | <span data-ttu-id="a4a5c-592">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-592">X</span></span> | <span data-ttu-id="a4a5c-593">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-593">X</span></span> | <span data-ttu-id="a4a5c-594">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-594">X</span></span> | <span data-ttu-id="a4a5c-595">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-595">X</span></span> | \- |
| <span data-ttu-id="a4a5c-596">\_ \_ время ожидания соединения для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-596">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="a4a5c-597">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-597">**DWORD**</span></span> | <span data-ttu-id="a4a5c-598">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-598">X</span></span> | <span data-ttu-id="a4a5c-599">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-599">X</span></span> | <span data-ttu-id="a4a5c-600">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-600">X</span></span> | <span data-ttu-id="a4a5c-601">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-601">X</span></span> | \- |
| <span data-ttu-id="a4a5c-602">\_ \_ сведения о соединении параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-602">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="a4a5c-603">**\_сведения о подключении к WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-603">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="a4a5c-604">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-604">X</span></span> | <span data-ttu-id="a4a5c-605">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-605">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-606">\_Параметр WinHTTP \_ Connection \_ stats \_ v0</span><span class="sxs-lookup"><span data-stu-id="a4a5c-606">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="a4a5c-607">**\_V0 сведения о TCP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-607">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="a4a5c-608">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-608">X</span></span> | <span data-ttu-id="a4a5c-609">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-609">X</span></span> | \- | <span data-ttu-id="a4a5c-610">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="a4a5c-610">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4a5c-611">\_Параметр WinHTTP \_ Connection \_ stats \_ v1</span><span class="sxs-lookup"><span data-stu-id="a4a5c-611">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="a4a5c-612">**\_Сведения о TCP \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-612">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="a4a5c-613">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-613">X</span></span> | <span data-ttu-id="a4a5c-614">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-614">X</span></span> | \- | <span data-ttu-id="a4a5c-615">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="a4a5c-615">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4a5c-616">\_ \_ значение контекста WinHTTP для параметра \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-616">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="a4a5c-617">**DWORD \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-617">**DWORD\_PTR**</span></span> | <span data-ttu-id="a4a5c-618">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-618">X</span></span> | <span data-ttu-id="a4a5c-619">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-619">X</span></span> | <span data-ttu-id="a4a5c-620">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-620">X</span></span> | <span data-ttu-id="a4a5c-621">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-621">X</span></span> | \- |
| <span data-ttu-id="a4a5c-622">\_ \_ распаковка параметров WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-622">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="a4a5c-623">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-623">**DWORD**</span></span> | <span data-ttu-id="a4a5c-624">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-624">X</span></span> | <span data-ttu-id="a4a5c-625">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-625">X</span></span> | \- | <span data-ttu-id="a4a5c-626">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-626">X</span></span> | <span data-ttu-id="a4a5c-627">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a4a5c-627">Windows 8.1</span></span> |
| <span data-ttu-id="a4a5c-628">\_ \_ функция отключения параметров \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-628">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="a4a5c-629">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-629">**DWORD**</span></span> | \- | <span data-ttu-id="a4a5c-630">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-630">X</span></span> | \- | <span data-ttu-id="a4a5c-631">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-631">X</span></span> | \- |
| <span data-ttu-id="a4a5c-632">\_параметр WinHTTP \_ Отключить \_ откат безопасных \_ протоколов \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-632">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="a4a5c-633">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-633">**BOOL**</span></span> | <span data-ttu-id="a4a5c-634">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-634">X</span></span> | \- | \- | <span data-ttu-id="a4a5c-635">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-635">X</span></span> | <span data-ttu-id="a4a5c-636">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="a4a5c-636">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4a5c-637">\_параметр WinHTTP \_ Отключить \_ \_ очередь потока</span><span class="sxs-lookup"><span data-stu-id="a4a5c-637">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="a4a5c-638">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-638">**BOOL**</span></span> | <span data-ttu-id="a4a5c-639">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-639">X</span></span> | <span data-ttu-id="a4a5c-640">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-640">X</span></span> | \- | <span data-ttu-id="a4a5c-641">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-641">X</span></span> | <span data-ttu-id="a4a5c-642">Windows 10, версия 1809</span><span class="sxs-lookup"><span data-stu-id="a4a5c-642">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="a4a5c-643">\_ \_ Включение \_ функции WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-643">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="a4a5c-644">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-644">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="a4a5c-645">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-645">X</span></span> | \- |
| <span data-ttu-id="a4a5c-646">\_параметр WinHTTP \_ Включение \_ \_ протокола HTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-646">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="a4a5c-647">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-647">**DWORD**</span></span> | <span data-ttu-id="a4a5c-648">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-648">X</span></span> | <span data-ttu-id="a4a5c-649">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-649">X</span></span> | \- | <span data-ttu-id="a4a5c-650">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-650">X</span></span> | <span data-ttu-id="a4a5c-651">Windows 10 версии 1607</span><span class="sxs-lookup"><span data-stu-id="a4a5c-651">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="a4a5c-652">\_параметр WinHTTP \_ енаблетраЦинг</span><span class="sxs-lookup"><span data-stu-id="a4a5c-652">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="a4a5c-653">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-653">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a4a5c-654">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-654">X</span></span> | <span data-ttu-id="a4a5c-655">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-655">X</span></span> | \- |
| <span data-ttu-id="a4a5c-656">\_ \_ добавочная кодировка параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-656">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="a4a5c-657">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-657">**BOOL**</span></span> | <span data-ttu-id="a4a5c-658">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-658">X</span></span> | <span data-ttu-id="a4a5c-659">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-659">X</span></span> | \- | <span data-ttu-id="a4a5c-660">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-660">X</span></span> | <span data-ttu-id="a4a5c-661">Windows 10, версия 1803</span><span class="sxs-lookup"><span data-stu-id="a4a5c-661">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="a4a5c-662">\_ \_ Расширенная ошибка при выборе WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-662">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="a4a5c-663">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-663">**DWORD**</span></span> | <span data-ttu-id="a4a5c-664">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-664">X</span></span> | <span data-ttu-id="a4a5c-665">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-665">X</span></span> | <span data-ttu-id="a4a5c-666">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-666">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-667">\_ \_ \_ учетные записи глобального прокси-сервера параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-667">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="a4a5c-668">**учетные учетные \_ службы WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-668">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="a4a5c-669">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-669">X</span></span> | <span data-ttu-id="a4a5c-670">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-670">X</span></span> | \- | <span data-ttu-id="a4a5c-671">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-671">X</span></span> | \- |
| <span data-ttu-id="a4a5c-672">Параметры WINHTTP глобальные учетные значения \_ \_ \_ сервера \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-672">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="a4a5c-673">**учетные учетные службы WINHTTP, \_ \_ пример**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-673">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="a4a5c-674">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-674">X</span></span> | <span data-ttu-id="a4a5c-675">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-675">X</span></span> | \- | <span data-ttu-id="a4a5c-676">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-676">X</span></span> | \- |
| <span data-ttu-id="a4a5c-677">\_ \_ тип обработчика параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-677">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="a4a5c-678">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-678">**DWORD**</span></span> | <span data-ttu-id="a4a5c-679">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-679">X</span></span> | <span data-ttu-id="a4a5c-680">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-680">X</span></span> | <span data-ttu-id="a4a5c-681">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-681">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-682">\_ \_ \_ требуется протокол HTTP для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-682">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="a4a5c-683">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-683">**BOOL**</span></span> | <span data-ttu-id="a4a5c-684">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-684">X</span></span> | <span data-ttu-id="a4a5c-685">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-685">X</span></span> | \- | <span data-ttu-id="a4a5c-686">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-686">X</span></span> | <span data-ttu-id="a4a5c-687">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="a4a5c-687">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4a5c-688">\_ \_ \_ используемый протокол HTTP \_ для параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-688">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="a4a5c-689">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-689">**DWORD**</span></span> | \- | <span data-ttu-id="a4a5c-690">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-690">X</span></span> | <span data-ttu-id="a4a5c-691">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-691">X</span></span> | \- | <span data-ttu-id="a4a5c-692">Windows 10 версии 1607</span><span class="sxs-lookup"><span data-stu-id="a4a5c-692">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="a4a5c-693">\_ \_ Версия HTTP параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-693">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="a4a5c-694">**\_ \_ сведения о версии HTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-694">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="a4a5c-695">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-695">X</span></span> | <span data-ttu-id="a4a5c-696">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-696">X</span></span> | <span data-ttu-id="a4a5c-697">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-697">X</span></span> | <span data-ttu-id="a4a5c-698">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-698">X</span></span> | \- |
| <span data-ttu-id="a4a5c-699">\_параметр WinHTTP \_ игнорировать \_ отзыв сертификата в \_ \_ автономном режиме</span><span class="sxs-lookup"><span data-stu-id="a4a5c-699">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="a4a5c-700">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-700">**BOOL**</span></span> | \- | <span data-ttu-id="a4a5c-701">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-701">X</span></span> | \- | <span data-ttu-id="a4a5c-702">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-702">X</span></span> | <span data-ttu-id="a4a5c-703">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="a4a5c-703">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4a5c-704">\_ \_ \_ Быстрый откат параметров WinHTTP \_ IPv6</span><span class="sxs-lookup"><span data-stu-id="a4a5c-704">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="a4a5c-705">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-705">**BOOL**</span></span> | <span data-ttu-id="a4a5c-706">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-706">X</span></span> | \- | \- | <span data-ttu-id="a4a5c-707">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-707">X</span></span> | <span data-ttu-id="a4a5c-708">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="a4a5c-708">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4a5c-709">\_параметр WinHTTP \_ — \_ ответ прокси- \_ подключения \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-709">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="a4a5c-710">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-710">**BOOL**</span></span> | <span data-ttu-id="a4a5c-711">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-711">X</span></span> | <span data-ttu-id="a4a5c-712">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-712">X</span></span> | <span data-ttu-id="a4a5c-713">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-713">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-714">\_Параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ \_ \_ сервер 1 0</span><span class="sxs-lookup"><span data-stu-id="a4a5c-714">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="a4a5c-715">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-715">**DWORD**</span></span> | <span data-ttu-id="a4a5c-716">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-716">X</span></span> | \- | <span data-ttu-id="a4a5c-717">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-717">X</span></span> | <span data-ttu-id="a4a5c-718">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-718">X</span></span> | \- |
| <span data-ttu-id="a4a5c-719">\_параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ сервер</span><span class="sxs-lookup"><span data-stu-id="a4a5c-719">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="a4a5c-720">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-720">**DWORD**</span></span> | <span data-ttu-id="a4a5c-721">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-721">X</span></span> | \- | <span data-ttu-id="a4a5c-722">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-722">X</span></span> | <span data-ttu-id="a4a5c-723">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-723">X</span></span> | \- |
| <span data-ttu-id="a4a5c-724">\_параметр WinHTTP \_ Максимальное \_ число \_ автоматических \_ перенаправлений HTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-724">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="a4a5c-725">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-725">**DWORD**</span></span> | <span data-ttu-id="a4a5c-726">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-726">X</span></span> | <span data-ttu-id="a4a5c-727">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-727">X</span></span> | <span data-ttu-id="a4a5c-728">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-728">X</span></span> | <span data-ttu-id="a4a5c-729">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-729">X</span></span> | \- |
| <span data-ttu-id="a4a5c-730">\_продолжение параметра \_ максимального \_ \_ состояния HTTP \_ для WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-730">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="a4a5c-731">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-731">**DWORD**</span></span> | <span data-ttu-id="a4a5c-732">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-732">X</span></span> | <span data-ttu-id="a4a5c-733">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-733">X</span></span> | <span data-ttu-id="a4a5c-734">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-734">X</span></span> | <span data-ttu-id="a4a5c-735">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-735">X</span></span> | \- |
| <span data-ttu-id="a4a5c-736">параметр WINHTTP — \_ \_ максимальный \_ \_ Размер очистки ответа \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-736">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="a4a5c-737">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-737">**DWORD**</span></span> | <span data-ttu-id="a4a5c-738">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-738">X</span></span> | <span data-ttu-id="a4a5c-739">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-739">X</span></span> | <span data-ttu-id="a4a5c-740">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-740">X</span></span> | <span data-ttu-id="a4a5c-741">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-741">X</span></span> | \- |
| <span data-ttu-id="a4a5c-742">\_параметр WinHTTP \_ максимальный \_ \_ размер заголовка \_ ответа</span><span class="sxs-lookup"><span data-stu-id="a4a5c-742">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="a4a5c-743">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-743">**DWORD**</span></span> | <span data-ttu-id="a4a5c-744">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-744">X</span></span> | <span data-ttu-id="a4a5c-745">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-745">X</span></span> | <span data-ttu-id="a4a5c-746">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-746">X</span></span> | <span data-ttu-id="a4a5c-747">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-747">X</span></span> | \- |
| <span data-ttu-id="a4a5c-748">\_ \_ родительский маркер параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-748">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="a4a5c-749">хинтернет</span><span class="sxs-lookup"><span data-stu-id="a4a5c-749">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="a4a5c-750">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-750">X</span></span> | <span data-ttu-id="a4a5c-751">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-751">X</span></span> | <span data-ttu-id="a4a5c-752">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-752">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-753">\_параметр WinHTTP \_ , \_ софирменный текст в паспорте \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-753">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="a4a5c-754">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-754">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4a5c-755">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-755">X</span></span> | <span data-ttu-id="a4a5c-756">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-756">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-757">\_ \_ \_ URL-адрес КОфирменной символики для службы WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-757">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="a4a5c-758">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-758">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4a5c-759">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-759">X</span></span> | <span data-ttu-id="a4a5c-760">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-760">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-761">\_ \_ \_ \_ URL-адрес возврата паспорта с параметром WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-761">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="a4a5c-762">**лпвоид**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-762">**LPVOID**</span></span> | \- | <span data-ttu-id="a4a5c-763">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-763">X</span></span> | <span data-ttu-id="a4a5c-764">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-764">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-765">\_команда WinHTTP \_ выход \_ \_ из паспорта</span><span class="sxs-lookup"><span data-stu-id="a4a5c-765">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="a4a5c-766">**лпвоид**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-766">**LPVOID**</span></span> | <span data-ttu-id="a4a5c-767">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-767">X</span></span> | \- | \- | <span data-ttu-id="a4a5c-768">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-768">X</span></span> | \- |
| <span data-ttu-id="a4a5c-769">\_пароль для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-769">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="a4a5c-770">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-770">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4a5c-771">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-771">X</span></span> | <span data-ttu-id="a4a5c-772">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-772">X</span></span> | <span data-ttu-id="a4a5c-773">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-773">X</span></span> | \- |
| <span data-ttu-id="a4a5c-774">\_ \_ прокси-сервер параметров WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-774">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="a4a5c-775">**\_сведения о прокси-сервере WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-775">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="a4a5c-776">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-776">X</span></span> | <span data-ttu-id="a4a5c-777">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-777">X</span></span> | <span data-ttu-id="a4a5c-778">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-778">X</span></span> | <span data-ttu-id="a4a5c-779">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-779">X</span></span> | \- |
| <span data-ttu-id="a4a5c-780">\_ \_ пароль прокси-сервера для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-780">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="a4a5c-781">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-781">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4a5c-782">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-782">X</span></span> | <span data-ttu-id="a4a5c-783">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-783">X</span></span> | <span data-ttu-id="a4a5c-784">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-784">X</span></span> | \- |
| <span data-ttu-id="a4a5c-785">\_используется параметр WinHTTP \_ прокси- \_ службы \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-785">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="a4a5c-786">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-786">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4a5c-787">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-787">X</span></span> | <span data-ttu-id="a4a5c-788">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-788">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-789">\_параметр WinHTTP \_ \_ имя пользователя-посредника</span><span class="sxs-lookup"><span data-stu-id="a4a5c-789">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="a4a5c-790">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-790">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4a5c-791">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-791">X</span></span> | <span data-ttu-id="a4a5c-792">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-792">X</span></span> | <span data-ttu-id="a4a5c-793">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-793">X</span></span> | \- |
| <span data-ttu-id="a4a5c-794">\_ \_ \_ Размер буфера чтения параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-794">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a4a5c-795">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-795">**DWORD**</span></span> | \- | <span data-ttu-id="a4a5c-796">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-796">X</span></span> | <span data-ttu-id="a4a5c-797">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-797">X</span></span> | <span data-ttu-id="a4a5c-798">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-798">X</span></span> | \- |
| <span data-ttu-id="a4a5c-799">\_параметр WinHTTP \_ Получение \_ ответа прокси-сервера \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-799">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="a4a5c-800">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-800">**BOOL**</span></span> | <span data-ttu-id="a4a5c-801">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-801">X</span></span> | <span data-ttu-id="a4a5c-802">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-802">X</span></span> | \- | <span data-ttu-id="a4a5c-803">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-803">X</span></span> | \- |
| <span data-ttu-id="a4a5c-804">\_ \_ \_ время ожидания ответа для получения параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-804">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="a4a5c-805">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-805">**DWORD**</span></span> | <span data-ttu-id="a4a5c-806">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-806">X</span></span> | <span data-ttu-id="a4a5c-807">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-807">X</span></span> | <span data-ttu-id="a4a5c-808">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-808">X</span></span> | <span data-ttu-id="a4a5c-809">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-809">X</span></span> | \- |
| <span data-ttu-id="a4a5c-810">\_ \_ время ожидания получения параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-810">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="a4a5c-811">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-811">**DWORD**</span></span> | <span data-ttu-id="a4a5c-812">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-812">X</span></span> | <span data-ttu-id="a4a5c-813">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-813">X</span></span> | <span data-ttu-id="a4a5c-814">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-814">X</span></span> | <span data-ttu-id="a4a5c-815">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-815">X</span></span> | \- |
| <span data-ttu-id="a4a5c-816">\_ \_ политика перенаправления для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-816">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="a4a5c-817">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-817">**DWORD**</span></span> | <span data-ttu-id="a4a5c-818">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-818">X</span></span> | <span data-ttu-id="a4a5c-819">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-819">X</span></span> | <span data-ttu-id="a4a5c-820">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-820">X</span></span> | <span data-ttu-id="a4a5c-821">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-821">X</span></span> | \- |
| <span data-ttu-id="a4a5c-822">\_параметр WinHTTP \_ отклонять \_ усерпвд \_ в \_ URL-адресе</span><span class="sxs-lookup"><span data-stu-id="a4a5c-822">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="a4a5c-823">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-823">**BOOL**</span></span> | \- | <span data-ttu-id="a4a5c-824">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-824">X</span></span> | \- | <span data-ttu-id="a4a5c-825">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-825">X</span></span> | \- |
| <span data-ttu-id="a4a5c-826">\_ \_ приоритет запроса параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-826">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="a4a5c-827">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-827">**DWORD**</span></span> | \- | <span data-ttu-id="a4a5c-828">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-828">X</span></span> | <span data-ttu-id="a4a5c-829">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-829">X</span></span> | <span data-ttu-id="a4a5c-830">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-830">X</span></span> | \- |
| <span data-ttu-id="a4a5c-831">\_ \_ Статистика запросов параметров \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-831">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="a4a5c-832">**\_Статистика запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-832">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="a4a5c-833">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-833">X</span></span> | <span data-ttu-id="a4a5c-834">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-834">X</span></span> | \- | <span data-ttu-id="a4a5c-835">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="a4a5c-835">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4a5c-836">\_ \_ время запроса параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-836">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="a4a5c-837">**\_время запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-837">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="a4a5c-838">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-838">X</span></span> | <span data-ttu-id="a4a5c-839">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-839">X</span></span> | \- | <span data-ttu-id="a4a5c-840">Windows 10, версия 1903</span><span class="sxs-lookup"><span data-stu-id="a4a5c-840">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4a5c-841">\_ \_ время ожидания разрешения параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-841">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="a4a5c-842">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-842">**DWORD**</span></span> | <span data-ttu-id="a4a5c-843">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-843">X</span></span> | <span data-ttu-id="a4a5c-844">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-844">X</span></span> | <span data-ttu-id="a4a5c-845">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-845">X</span></span> | <span data-ttu-id="a4a5c-846">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-846">X</span></span> | \- |
| <span data-ttu-id="a4a5c-847">Параметры WINHTTP для \_ \_ защищенных \_ протоколов</span><span class="sxs-lookup"><span data-stu-id="a4a5c-847">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="a4a5c-848">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-848">**DWORD**</span></span> | <span data-ttu-id="a4a5c-849">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-849">X</span></span> | \- | \- | <span data-ttu-id="a4a5c-850">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-850">X</span></span> | \- |
| <span data-ttu-id="a4a5c-851">\_ \_ \_ Структура сертификата безопасности параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-851">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="a4a5c-852">**\_сведения о сертификате WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-852">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="a4a5c-853">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-853">X</span></span> | <span data-ttu-id="a4a5c-854">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-854">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-855">\_ \_ Флаги безопасности для параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-855">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="a4a5c-856">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-856">**DWORD**</span></span> | \- | <span data-ttu-id="a4a5c-857">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-857">X</span></span> | <span data-ttu-id="a4a5c-858">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-858">X</span></span> | <span data-ttu-id="a4a5c-859">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-859">X</span></span> | \- |
| <span data-ttu-id="a4a5c-860">\_ \_ сведения о безопасности параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-860">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="a4a5c-861">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-861">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="a4a5c-862">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-862">X</span></span> | <span data-ttu-id="a4a5c-863">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-863">X</span></span> | \- | <span data-ttu-id="a4a5c-864">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="a4a5c-864">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4a5c-865">\_ \_ \_ разрядность ключа безопасности параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-865">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="a4a5c-866">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-866">**DWORD**</span></span> | \- | <span data-ttu-id="a4a5c-867">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-867">X</span></span> | <span data-ttu-id="a4a5c-868">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-868">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-869">\_ \_ время ожидания отправки для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-869">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="a4a5c-870">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-870">**DWORD**</span></span> | <span data-ttu-id="a4a5c-871">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-871">X</span></span> | <span data-ttu-id="a4a5c-872">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-872">X</span></span> | <span data-ttu-id="a4a5c-873">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-873">X</span></span> | <span data-ttu-id="a4a5c-874">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-874">X</span></span> | \- |
| <span data-ttu-id="a4a5c-875">\_ \_ CBT сервера параметров \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-875">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="a4a5c-876">[**\_Привязки секпкгконтекст**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="a4a5c-876">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="a4a5c-877">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-877">X</span></span> | <span data-ttu-id="a4a5c-878">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-878">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-879">\_параметр WinHTTP \_ \_ \_ контекст цепочки сертификатов сервера \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-879">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="a4a5c-880">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-880">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="a4a5c-881">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-881">X</span></span> | <span data-ttu-id="a4a5c-882">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-882">X</span></span> | \- | <span data-ttu-id="a4a5c-883">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="a4a5c-883">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4a5c-884">\_ \_ \_ контекст сертификата сервера параметров \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-884">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="a4a5c-885">**КОНТЕКСТ СЕРТИФИКАТА**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-885">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="a4a5c-886">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-886">X</span></span> | <span data-ttu-id="a4a5c-887">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-887">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-888">\_ \_ \_ используемое имя субъекта-службы сервера параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-888">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="a4a5c-889">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-889">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4a5c-890">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-890">X</span></span> | <span data-ttu-id="a4a5c-891">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-891">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-892">\_ \_ имя субъекта-службы для параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-892">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="a4a5c-893">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-893">**DWORD**</span></span> | \- | <span data-ttu-id="a4a5c-894">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-894">X</span></span> | \- | <span data-ttu-id="a4a5c-895">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-895">X</span></span> | \- |
| <span data-ttu-id="a4a5c-896">\_параметр WinHTTP \_ TCP \_ fast \_ Open</span><span class="sxs-lookup"><span data-stu-id="a4a5c-896">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="a4a5c-897">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-897">**BOOL**</span></span> | <span data-ttu-id="a4a5c-898">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-898">X</span></span> | \- | \- | <span data-ttu-id="a4a5c-899">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-899">X</span></span> | <span data-ttu-id="a4a5c-900">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="a4a5c-900">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4a5c-901">\_Запуск параметра WinHTTP \_ TLS \_ false \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-901">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="a4a5c-902">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-902">**BOOL**</span></span> | <span data-ttu-id="a4a5c-903">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-903">X</span></span> | \- | \- | <span data-ttu-id="a4a5c-904">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-904">X</span></span> | <span data-ttu-id="a4a5c-905">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="a4a5c-905">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4a5c-906">\_ \_ \_ событие уведомления о ВЫгрузке параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-906">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="a4a5c-907">хинтернет</span><span class="sxs-lookup"><span data-stu-id="a4a5c-907">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="a4a5c-908">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-908">X</span></span> | \- | \- | <span data-ttu-id="a4a5c-909">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-909">X</span></span> | \- |
| <span data-ttu-id="a4a5c-910">\_ \_ \_ синтаксический анализ ненадежного заголовка для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-910">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="a4a5c-911">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-911">**DWORD**</span></span> | \- | <span data-ttu-id="a4a5c-912">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-912">X</span></span> | \- | <span data-ttu-id="a4a5c-913">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-913">X</span></span> | \- |
| <span data-ttu-id="a4a5c-914">\_Обновление параметра \_ WinHTTP \_ до \_ веб- \_ сокета</span><span class="sxs-lookup"><span data-stu-id="a4a5c-914">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="a4a5c-915">Н/Д</span><span class="sxs-lookup"><span data-stu-id="a4a5c-915">N/A</span></span> | \- | <span data-ttu-id="a4a5c-916">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-916">X</span></span> | \- | <span data-ttu-id="a4a5c-917">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-917">X</span></span> | \- |
| <span data-ttu-id="a4a5c-918">\_ \_ URL-адрес параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-918">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="a4a5c-919">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-919">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4a5c-920">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-920">X</span></span> | <span data-ttu-id="a4a5c-921">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-921">X</span></span> | \- | \- |
| <span data-ttu-id="a4a5c-922">\_параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера</span><span class="sxs-lookup"><span data-stu-id="a4a5c-922">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="a4a5c-923">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-923">**BOOL**</span></span> | <span data-ttu-id="a4a5c-924">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-924">X</span></span> | <span data-ttu-id="a4a5c-925">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-925">X</span></span> | \- | <span data-ttu-id="a4a5c-926">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-926">X</span></span> | \- |
| <span data-ttu-id="a4a5c-927">\_ \_ Агент пользователя для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-927">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="a4a5c-928">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-928">**LPWSTR**</span></span> | <span data-ttu-id="a4a5c-929">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-929">X</span></span> | \- | <span data-ttu-id="a4a5c-930">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-930">X</span></span> | <span data-ttu-id="a4a5c-931">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-931">X</span></span> | \- |
| <span data-ttu-id="a4a5c-932">\_имя пользователя для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-932">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="a4a5c-933">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-933">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4a5c-934">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-934">X</span></span> | <span data-ttu-id="a4a5c-935">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-935">X</span></span> | <span data-ttu-id="a4a5c-936">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-936">X</span></span> | \- |
| <span data-ttu-id="a4a5c-937">\_ \_ \_ \_ время ожидания закрытия веб-СОКЕТа для параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-937">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="a4a5c-938">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-938">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a4a5c-939">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-939">X</span></span> | <span data-ttu-id="a4a5c-940">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-940">X</span></span> | \- |
| <span data-ttu-id="a4a5c-941">\_интервал проверки \_ активности веб- \_ сокета для \_ параметра WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-941">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="a4a5c-942">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-942">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a4a5c-943">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-943">X</span></span> | <span data-ttu-id="a4a5c-944">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-944">X</span></span> | \- |
| <span data-ttu-id="a4a5c-945">\_параметр WinHTTP \_ \_ \_ \_ Размер буфера получения веб-сокета \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-945">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a4a5c-946">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-946">**DWORD**</span></span> | <span data-ttu-id="a4a5c-947">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-947">X</span></span> | <span data-ttu-id="a4a5c-948">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-948">X</span></span> | <span data-ttu-id="a4a5c-949">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-949">X</span></span> | <span data-ttu-id="a4a5c-950">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-950">X</span></span> | <span data-ttu-id="a4a5c-951">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a4a5c-951">Windows 8.1</span></span> |
| <span data-ttu-id="a4a5c-952">\_ \_ \_ \_ \_ Размер буфера отправки для веб-сокета параметров WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a4a5c-952">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a4a5c-953">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-953">**DWORD**</span></span> | <span data-ttu-id="a4a5c-954">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-954">X</span></span> | <span data-ttu-id="a4a5c-955">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-955">X</span></span> | <span data-ttu-id="a4a5c-956">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-956">X</span></span> | <span data-ttu-id="a4a5c-957">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-957">X</span></span> | <span data-ttu-id="a4a5c-958">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a4a5c-958">Windows 8.1</span></span> |
| <span data-ttu-id="a4a5c-959">\_ \_ \_ число рабочих потоков \_ параметра WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-959">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="a4a5c-960">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-960">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="a4a5c-961">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-961">X</span></span> | \- |
| <span data-ttu-id="a4a5c-962">\_ \_ \_ Размер буфера записи параметра \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-962">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a4a5c-963">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4a5c-963">**DWORD**</span></span> | \- | <span data-ttu-id="a4a5c-964">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-964">X</span></span> | <span data-ttu-id="a4a5c-965">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-965">X</span></span> | <span data-ttu-id="a4a5c-966">X</span><span class="sxs-lookup"><span data-stu-id="a4a5c-966">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="a4a5c-967">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="a4a5c-967">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a5c-968">Требования</span><span class="sxs-lookup"><span data-stu-id="a4a5c-968">Requirements</span></span>

| <span data-ttu-id="a4a5c-969">Требование</span><span class="sxs-lookup"><span data-stu-id="a4a5c-969">Requirement</span></span> | <span data-ttu-id="a4a5c-970">Значение</span><span class="sxs-lookup"><span data-stu-id="a4a5c-970">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a4a5c-971">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4a5c-971">Minimum supported client</span></span> | <span data-ttu-id="a4a5c-972">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a4a5c-972">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="a4a5c-973">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4a5c-973">Minimum supported server</span></span> | <span data-ttu-id="a4a5c-974">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a4a5c-974">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="a4a5c-975">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a4a5c-975">Redistributable</span></span>          | <span data-ttu-id="a4a5c-976">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a4a5c-976">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="a4a5c-977">Header</span><span class="sxs-lookup"><span data-stu-id="a4a5c-977">Header</span></span>                   | <span data-ttu-id="a4a5c-978">WinHTTP. h</span><span class="sxs-lookup"><span data-stu-id="a4a5c-978">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="a4a5c-979">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4a5c-979">See also</span></span>

[<span data-ttu-id="a4a5c-980">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a4a5c-980">WinHTTP Versions</span></span>](winhttp-versions.md)
