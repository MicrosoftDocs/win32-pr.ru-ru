---
description: Включает параметры, которые могут быть установлены или получены для текущего сеанса служб Microsoft Windows HTTP (WinHTTP).
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: Перечисление Винхттпрекуестоптион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: 32ae65f43cd04027027e43d29c49ed0f68f29c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541674"
---
# <a name="winhttprequestoption-enumeration"></a><span data-ttu-id="b2913-103">Перечисление Винхттпрекуестоптион</span><span class="sxs-lookup"><span data-stu-id="b2913-103">WinHttpRequestOption enumeration</span></span>

<span data-ttu-id="b2913-104">Перечисление **винхттпрекуестоптион** включает параметры, которые могут быть установлены или получены для текущего сеанса служб Microsoft Windows HTTP (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="b2913-104">The **WinHttpRequestOption** enumeration includes options that can be set or retrieved for the current Microsoft Windows HTTP Services (WinHTTP) session.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2913-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2913-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a><span data-ttu-id="b2913-106">Константы</span><span class="sxs-lookup"><span data-stu-id="b2913-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b2913-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**Винхттпрекуестоптион \_ усеражентстринг**</span><span class="sxs-lookup"><span data-stu-id="b2913-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption\_UserAgentString**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-108">Задает или получает **значение типа Variant** , содержащее строку [*агента пользователя*](glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="b2913-108">Sets or retrieves a **VARIANT** that contains the [*user agent*](glossary.md) string.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**\_URL-адрес винхттпрекуестоптион**</span><span class="sxs-lookup"><span data-stu-id="b2913-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**WinHttpRequestOption\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-110">Извлекает **значение типа Variant** , содержащее URL-адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2913-110">Retrieves a **VARIANT** that contains the URL of the resource.</span></span> <span data-ttu-id="b2913-111">Это значение доступно только для чтения; задать URL-адрес с помощью этого свойства нельзя.</span><span class="sxs-lookup"><span data-stu-id="b2913-111">This value is read-only; you cannot set the URL using this property.</span></span> <span data-ttu-id="b2913-112">Невозможно прочитать URL-адрес до вызова метода [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="b2913-112">The URL cannot be read until the [**Open**](iwinhttprequest-open.md) method is called.</span></span> <span data-ttu-id="b2913-113">Этот параметр полезен для проверки URL-адреса после завершения метода [**Send**](iwinhttprequest-send.md) , чтобы проверить, не произошло ли перенаправление.</span><span class="sxs-lookup"><span data-stu-id="b2913-113">This option is useful for checking the URL after the [**Send**](iwinhttprequest-send.md) method is finished to verify that any redirection occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**Винхттпрекуестоптион \_ урлкодепаже**</span><span class="sxs-lookup"><span data-stu-id="b2913-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption\_URLCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-115">Задает или получает **значение типа Variant** , идентифицирующее [*кодовую страницу*](glossary.md) для строки URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b2913-115">Sets or retrieves a **VARIANT** that identifies the [*code page*](glossary.md) for the URL string.</span></span> <span data-ttu-id="b2913-116">Значение по умолчанию — кодовая страница UTF-8.</span><span class="sxs-lookup"><span data-stu-id="b2913-116">The default value is the UTF-8 code page.</span></span> <span data-ttu-id="b2913-117">Кодовая страница используется для преобразования строки URL-адреса Юникода, передаваемой в метод [**Open**](iwinhttprequest-open.md) , в однобайтовое строковое представление.</span><span class="sxs-lookup"><span data-stu-id="b2913-117">The code page is used to convert the Unicode URL string, passed in the [**Open**](iwinhttprequest-open.md) method, to a single-byte string representation.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**Винхттпрекуестоптион \_ ескапеперцентинурл**</span><span class="sxs-lookup"><span data-stu-id="b2913-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption\_EscapePercentInURL**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-119">Задает или получает **значение типа Variant** , которое указывает, преобразуются ли символы процента в строке URL-адреса в управляющую последовательность.</span><span class="sxs-lookup"><span data-stu-id="b2913-119">Sets or retrieves a **VARIANT** that indicates whether percent characters in the URL string are converted to an escape sequence.</span></span> <span data-ttu-id="b2913-120">По умолчанию этот параметр имеет значение **Variant \_ true** , которое указывает, что все ненадежные символы американский национальный институт стандартов (ANSI) (ANSI), за исключением символа процента, преобразуются в escape-последовательность.</span><span class="sxs-lookup"><span data-stu-id="b2913-120">The default value of this option is **VARIANT\_TRUE** which specifies all unsafe American National Standards Institute (ANSI) characters except the percent symbol are converted to an escape sequence.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**Винхттпрекуестоптион \_ сслерроригнорефлагс**</span><span class="sxs-lookup"><span data-stu-id="b2913-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption\_SslErrorIgnoreFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-122">Задает или получает **значение типа Variant** , указывающее, какие ошибки сертификата сервера следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="b2913-122">Sets or retrieves a **VARIANT** that indicates which server certificate errors should be ignored.</span></span> <span data-ttu-id="b2913-123">Это может быть сочетание одного или нескольких из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="b2913-123">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="b2913-124">Ошибка</span><span class="sxs-lookup"><span data-stu-id="b2913-124">Error</span></span>                                                  | <span data-ttu-id="b2913-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b2913-125">Value</span></span>  |
|--------------------------------------------------------|--------|
| <span data-ttu-id="b2913-126">Неизвестный центр сертификации (ЦС) или недоверенный корень</span><span class="sxs-lookup"><span data-stu-id="b2913-126">Unknown certification authority (CA) or untrusted root</span></span> | <span data-ttu-id="b2913-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="b2913-127">0x0100</span></span> |
| <span data-ttu-id="b2913-128">Неправильное использование</span><span class="sxs-lookup"><span data-stu-id="b2913-128">Wrong usage</span></span>                                            | <span data-ttu-id="b2913-129">0x0200</span><span class="sxs-lookup"><span data-stu-id="b2913-129">0x0200</span></span> |
| <span data-ttu-id="b2913-130">Недопустимое общее имя (CN)</span><span class="sxs-lookup"><span data-stu-id="b2913-130">Invalid common name (CN)</span></span>                               | <span data-ttu-id="b2913-131">0x1000</span><span class="sxs-lookup"><span data-stu-id="b2913-131">0x1000</span></span> |
| <span data-ttu-id="b2913-132">Срок действия недействительной даты или сертификата истек</span><span class="sxs-lookup"><span data-stu-id="b2913-132">Invalid date or certificate expired</span></span>                    | <span data-ttu-id="b2913-133">0x2000</span><span class="sxs-lookup"><span data-stu-id="b2913-133">0x2000</span></span> |



 

<span data-ttu-id="b2913-134">Значение этого параметра по умолчанию в версии 5,1 WinHTTP равно нулю, что не приводит к игнорированию ошибок.</span><span class="sxs-lookup"><span data-stu-id="b2913-134">The default value of this option in Version 5.1 of WinHTTP is zero, which results in no errors being ignored.</span></span> <span data-ttu-id="b2913-135">В более ранних версиях WinHTTP параметр по умолчанию был 0x3300, что привело к тому, что по умолчанию все ошибки сертификата сервера игнорировались.</span><span class="sxs-lookup"><span data-stu-id="b2913-135">In earlier versions of WinHTTP, the default setting was 0x3300, which resulted in all server certificate errors being ignored by default.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**Винхттпрекуестоптион \_ селектцертификате**</span><span class="sxs-lookup"><span data-stu-id="b2913-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption\_SelectCertificate**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-137">Задает **значение типа Variant** , указывающее сертификат клиента, который отправляется на сервер для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b2913-137">Sets a **VARIANT** that specifies the client certificate that is sent to a server for authentication.</span></span> <span data-ttu-id="b2913-138">Этот параметр указывает расположение, [*хранилище сертификатов*](glossary.md)и субъект сертификата клиента, разделенные символами обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="b2913-138">This option indicates the location, [*certificate store*](glossary.md), and subject of a client certificate delimited with backslashes.</span></span> <span data-ttu-id="b2913-139">Дополнительные сведения о выборе сертификата клиента см. в разделе [SSL в WinHTTP](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="b2913-139">For more information about selecting a client certificate, see [SSL in WinHTTP](ssl-in-winhttp.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2913-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**Винхттпрекуестоптион \_ енаблередиректс**</span><span class="sxs-lookup"><span data-stu-id="b2913-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption\_EnableRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-141">Задает или получает **значение типа Variant** , указывающее, будут ли запросы автоматически перенаправляться, когда сервер указывает новое расположение для ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2913-141">Sets or retrieves a **VARIANT** that indicates whether requests are automatically redirected when the server specifies a new location for the resource.</span></span> <span data-ttu-id="b2913-142">Значение этого параметра по умолчанию — **Variant \_ true** , указывающее, что запросы перенаправляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="b2913-142">The default value of this option is **VARIANT\_TRUE** to indicate that requests are automatically redirected.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**Винхттпрекуестоптион \_ урлескапедисабле**</span><span class="sxs-lookup"><span data-stu-id="b2913-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption\_UrlEscapeDisable**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-144">Задает или получает **значение типа Variant** , указывающее, преобразуются ли незащищенные символы в пути и компонентах запроса URL-адреса в управляющие последовательности.</span><span class="sxs-lookup"><span data-stu-id="b2913-144">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the path and query components of a URL are converted to escape sequences.</span></span> <span data-ttu-id="b2913-145">Значение этого параметра по умолчанию — **Variant \_ true**, которое указывает, что символы в пути и запросе преобразованы.</span><span class="sxs-lookup"><span data-stu-id="b2913-145">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the path and query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**Винхттпрекуестоптион \_ урлескапедисаблекуери**</span><span class="sxs-lookup"><span data-stu-id="b2913-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption\_UrlEscapeDisableQuery**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-147">Задает или получает **значение типа Variant** , указывающее, преобразуются ли незащищенные символы в компоненте запроса URL-адреса в управляющие последовательности.</span><span class="sxs-lookup"><span data-stu-id="b2913-147">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the query component of the URL are converted to escape sequences.</span></span> <span data-ttu-id="b2913-148">Значение этого параметра по умолчанию — **Variant \_ true**, которое указывает, что символы в запросе преобразованы.</span><span class="sxs-lookup"><span data-stu-id="b2913-148">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**Винхттпрекуестоптион \_ секурепротоколс**</span><span class="sxs-lookup"><span data-stu-id="b2913-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption\_SecureProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-150">Задает или получает **значение типа Variant** , указывающее, какие безопасные протоколы можно использовать.</span><span class="sxs-lookup"><span data-stu-id="b2913-150">Sets or retrieves a **VARIANT** that indicates which secure protocols can be used.</span></span> <span data-ttu-id="b2913-151">Этот параметр позволяет выбрать протоколы, приемлемые для клиента.</span><span class="sxs-lookup"><span data-stu-id="b2913-151">This option selects the protocols acceptable to the client.</span></span> <span data-ttu-id="b2913-152">Протокол согласовывается во время согласования SSL (SSL).</span><span class="sxs-lookup"><span data-stu-id="b2913-152">The protocol is negotiated during the Secure Sockets Layer (SSL) handshake.</span></span> <span data-ttu-id="b2913-153">Это может быть сочетание одного или нескольких из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="b2913-153">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="b2913-154">Протокол</span><span class="sxs-lookup"><span data-stu-id="b2913-154">Protocol</span></span>                           | <span data-ttu-id="b2913-155">Значение</span><span class="sxs-lookup"><span data-stu-id="b2913-155">Value</span></span>  |
|------------------------------------|--------|
| <span data-ttu-id="b2913-156">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="b2913-156">SSL 2.0</span></span>                            | <span data-ttu-id="b2913-157">0x0008</span><span class="sxs-lookup"><span data-stu-id="b2913-157">0x0008</span></span> |
| <span data-ttu-id="b2913-158">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="b2913-158">SSL 3.0</span></span>                            | <span data-ttu-id="b2913-159">0x0020</span><span class="sxs-lookup"><span data-stu-id="b2913-159">0x0020</span></span> |
| <span data-ttu-id="b2913-160">Безопасность транспортного уровня (TLS) 1,0</span><span class="sxs-lookup"><span data-stu-id="b2913-160">Transport Layer Security (TLS) 1.0</span></span> | <span data-ttu-id="b2913-161">0x0080</span><span class="sxs-lookup"><span data-stu-id="b2913-161">0x0080</span></span> |



 

<span data-ttu-id="b2913-162">Значение этого параметра по умолчанию — 0x0028, которое указывает, что можно использовать SSL 2,0 или SSL 3,0.</span><span class="sxs-lookup"><span data-stu-id="b2913-162">The default value of this option is 0x0028, which indicates that SSL 2.0 or SSL 3.0 can be used.</span></span> <span data-ttu-id="b2913-163">Если этот параметр имеет значение 0, клиент и сервер не могут определить приемлемый протокол безопасности, а следующая [**Отправка**](iwinhttprequest-send.md) приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b2913-163">If this option is set to zero, the client and server are not able to determine an acceptable security protocol and the next [**Send**](iwinhttprequest-send.md) results in an error.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**Винхттпрекуестоптион \_ енаблетраЦинг**</span><span class="sxs-lookup"><span data-stu-id="b2913-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption\_EnableTracing**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-165">Задает или получает **значение типа Variant** , указывающее, включена ли трассировка в данный момент.</span><span class="sxs-lookup"><span data-stu-id="b2913-165">Sets or retrieves a **VARIANT** that indicates whether tracing is currently enabled.</span></span> <span data-ttu-id="b2913-166">Дополнительные сведения о средстве трассировки в службах Microsoft Windows HTTP (WinHTTP) см. в разделе Служба [трассировки WinHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="b2913-166">For more information about the trace facility in Microsoft Windows HTTP Services (WinHTTP), see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2913-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**Винхттпрекуестоптион \_ ревертимперсонатионоверссл**</span><span class="sxs-lookup"><span data-stu-id="b2913-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption\_RevertImpersonationOverSsl**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-168">Определяет, будет ли объект [**WinHttpRequest**](winhttprequest.md) временно отменять олицетворение клиента на время операций проверки подлинности SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="b2913-168">Controls whether the [**WinHttpRequest**](winhttprequest.md) object temporarily reverts client impersonation for the duration of the SSL certificate authentication operations.</span></span> <span data-ttu-id="b2913-169">Значение по умолчанию для объекта **WinHttpRequest** — **true**.</span><span class="sxs-lookup"><span data-stu-id="b2913-169">The default setting for the **WinHttpRequest** object is **TRUE**.</span></span> <span data-ttu-id="b2913-170">Установите этот параметр в **значение false** , чтобы при выполнении операций проверки подлинности с помощью сертификата сохранение олицетворения выполнялось.</span><span class="sxs-lookup"><span data-stu-id="b2913-170">Set this option to **FALSE** to keep impersonation while performing certificate authentication operations.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**Винхттпрекуестоптион \_ енаблехттпстохттпредиректс**</span><span class="sxs-lookup"><span data-stu-id="b2913-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption\_EnableHttpsToHttpRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-172">Определяет, допускает ли служба WinHTTP перенаправление.</span><span class="sxs-lookup"><span data-stu-id="b2913-172">Controls whether or not WinHTTP allows redirects.</span></span> <span data-ttu-id="b2913-173">По умолчанию все перенаправления выполняются автоматически, за исключением тех, которые передаются с защищенного URL-адреса (HTTPS) на небезопасный (http) URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b2913-173">By default, all redirects are automatically followed, except those that transfer from a secure (https) URL to an non-secure (http) URL.</span></span> <span data-ttu-id="b2913-174">Установите для этого параметра **значение true** , чтобы включить перенаправления по протоколу HTTPS в HTTP.</span><span class="sxs-lookup"><span data-stu-id="b2913-174">Set this option to **TRUE** to enable HTTPS to HTTP redirects.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**Винхттпрекуестоптион \_ енаблепасспортаусентикатион**</span><span class="sxs-lookup"><span data-stu-id="b2913-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption\_EnablePassportAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-176">Включает или отключает поддержку проверки подлинности Passport.</span><span class="sxs-lookup"><span data-stu-id="b2913-176">Enables or disables support for Passport authentication.</span></span> <span data-ttu-id="b2913-177">По умолчанию автоматическая поддержка проверки подлинности Passport отключена. Установите для этого параметра **значение true** , чтобы включить поддержку проверки подлинности паспорта.</span><span class="sxs-lookup"><span data-stu-id="b2913-177">By default, automatic support for Passport authentication is disabled; set this option to **TRUE** to enable Passport authentication support.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**Винхттпрекуестоптион \_ максаутоматикредиректс**</span><span class="sxs-lookup"><span data-stu-id="b2913-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption\_MaxAutomaticRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-179">Задает или получает максимальное число перенаправлений, которое следует за WinHTTP. значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="b2913-179">Sets or retrieves the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="b2913-180">Это ограничение не позволяет неавторизованным сайтам сделать клиент WinHTTP остановленным после большого числа перенаправлений.</span><span class="sxs-lookup"><span data-stu-id="b2913-180">This limit prevents unauthorized sites from making the WinHTTP client stall following a large number of redirects.</span></span>

<span data-ttu-id="b2913-181">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Это значение перечисления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b2913-181">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**Винхттпрекуестоптион \_ максреспонсехеадерсизе**</span><span class="sxs-lookup"><span data-stu-id="b2913-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption\_MaxResponseHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-183">Задает или получает связанный набор на максимальный размер заголовка ответа сервера.</span><span class="sxs-lookup"><span data-stu-id="b2913-183">Sets or retrieves a bound set on the maximum size of the header portion of the server's response.</span></span> <span data-ttu-id="b2913-184">Эта привязка защищает клиента от вредоносного сервера, пытающегося приостановки работы клиента, отправив ответ с бесконечным объемом данных заголовка.</span><span class="sxs-lookup"><span data-stu-id="b2913-184">This bound protects the client from a malicious server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="b2913-185">Значение по умолчанию — 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="b2913-185">The default value is 64 KB.</span></span>

<span data-ttu-id="b2913-186">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Это значение перечисления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b2913-186">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**Винхттпрекуестоптион \_ максреспонседраинсизе**</span><span class="sxs-lookup"><span data-stu-id="b2913-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption\_MaxResponseDrainSize**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-188">Задает или получает ограничение на объем данных, которые будут передаваться из ответов для повторного использования соединения.</span><span class="sxs-lookup"><span data-stu-id="b2913-188">Sets or retrieves a bound on the amount of data that will be drained from responses in order to reuse a connection.</span></span> <span data-ttu-id="b2913-189">По умолчанию установлено значение 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="b2913-189">The default is 1 MB.</span></span>

<span data-ttu-id="b2913-190">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Это значение перечисления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b2913-190">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**Винхттпрекуестоптион \_ EnableHttp1 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b2913-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption\_EnableHttp1\_1**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-192">Задает или получает логическое значение, указывающее, следует ли использовать HTTP/1.1 или HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="b2913-192">Sets or retrieves a boolean value that indicates whether HTTP/1.1 or HTTP/1.0 should be used.</span></span> <span data-ttu-id="b2913-193">Значение по умолчанию — **true**, поэтому по умолчанию используется HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="b2913-193">The default is **TRUE**, so that HTTP/1.1 is used by default.</span></span>

<span data-ttu-id="b2913-194">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Это значение перечисления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b2913-194">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b2913-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**Винхттпрекуестоптион \_ енаблецертификатеревокатиончекк**</span><span class="sxs-lookup"><span data-stu-id="b2913-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption\_EnableCertificateRevocationCheck**</span></span>
</dt> <dd>

<span data-ttu-id="b2913-196">Включает проверку отзыва сертификатов сервера во время согласования SSL.</span><span class="sxs-lookup"><span data-stu-id="b2913-196">Enables server certificate revocation checking during SSL negotiation.</span></span> <span data-ttu-id="b2913-197">Если сервер представляет сертификат, выполняется проверка, чтобы определить, отозван ли сертификат его издателем.</span><span class="sxs-lookup"><span data-stu-id="b2913-197">When the server presents a certificate, a check is performed to determine whether the certificate has been revoked by its issuer.</span></span> <span data-ttu-id="b2913-198">Если сертификат действительно отозван или проверка отзыва не удалась из-за невозможности загрузить список отзыва сертификатов (CRL), запрос завершится ошибкой. такие ошибки отзыва не могут быть подавлены.</span><span class="sxs-lookup"><span data-stu-id="b2913-198">If the certificate is indeed revoked, or the revocation check fails because the Certificate Revocation List (CRL) cannot be downloaded, the request fails; such revocation errors cannot be suppressed.</span></span>

<span data-ttu-id="b2913-199">**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Это значение перечисления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b2913-199">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2913-200">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2913-200">Remarks</span></span>

<span data-ttu-id="b2913-201">Задайте параметр, указав одну из предыдущих констант в качестве параметра свойства [**Option**](iwinhttprequest-option.md) .</span><span class="sxs-lookup"><span data-stu-id="b2913-201">Set an option by specifying one of the preceding constants as the parameter of the [**Option**](iwinhttprequest-option.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="b2913-202">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b2913-202">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2913-203">Требования</span><span class="sxs-lookup"><span data-stu-id="b2913-203">Requirements</span></span>



| <span data-ttu-id="b2913-204">Требование</span><span class="sxs-lookup"><span data-stu-id="b2913-204">Requirement</span></span> | <span data-ttu-id="b2913-205">Значение</span><span class="sxs-lookup"><span data-stu-id="b2913-205">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2913-206">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2913-206">Minimum supported client</span></span><br/> | <span data-ttu-id="b2913-207">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2913-207">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="b2913-208">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2913-208">Minimum supported server</span></span><br/> | <span data-ttu-id="b2913-209">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2913-209">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="b2913-210">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b2913-210">Redistributable</span></span><br/>          | <span data-ttu-id="b2913-211">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b2913-211">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="b2913-212">IDL</span><span class="sxs-lookup"><span data-stu-id="b2913-212">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b2913-213"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b2913-213"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2913-214">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2913-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2913-215">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b2913-215">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




