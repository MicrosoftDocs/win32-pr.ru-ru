---
title: Сопоставление метаданных
description: Содержимое схемы документа метаданных в API метаданных описано в следующих разделах.
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- Веб-службы сопоставления метаданных для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9da067768569e78ba6bb98ee219e11917d3201
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105691712"
---
# <a name="metadata-mapping"></a><span data-ttu-id="09324-106">Сопоставление метаданных</span><span class="sxs-lookup"><span data-stu-id="09324-106">Metadata Mapping</span></span>

<span data-ttu-id="09324-107">Содержимое схемы документа метаданных в API метаданных описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="09324-107">The contents of a metadata document map to the metadata API in the ways explained in the following sections.</span></span>


<span data-ttu-id="09324-108">В этой документации используются следующие префиксы пространств имен:</span><span class="sxs-lookup"><span data-stu-id="09324-108">The following namespace prefixes are used throughout this documentation:</span></span>

``` syntax
wsdl   => http://schemas.xmlsoap.org/wsdl/
soap11 => http://schemas.xmlsoap.org/wsdl/soap/
soap12 => http://schemas.xmlsoap.org/wsdl/soap12/
wsa09  => http://schemas.xmlsoap.org/ws/2004/08/addressing
wsa10  => http://www.w3.org/2005/08/addressing
wsa09p => http://schemas.xmlsoap.org/ws/2004/08/addressing/policy
wsa10p => http://www.w3.org/2006/05/addressing/wsdl
binp   => http://schemas.microsoft.com/ws/06/2004/mspolicy/netbinary1
mtomp  => http://schemas.xmlsoap.org/ws/2004/09/policy/optimizedmimeserialization
sp     => http://schemas.xmlsoap.org/ws/2005/07/securitypolicy
wsp    => http://schemas.xmlsoap.org/ws/2004/09/policy
netf   => http://schemas.microsoft.com/ws/2006/05/framing/policy
httpp  => http://schemas.microsoft.com/ws/06/2004/policy/http
wst10  => http://schemas.xmlsoap.org/ws/2005/02/trust
wsi    => http://schemas.xmlsoap.org/ws/2005/05/identity
```

<span data-ttu-id="09324-109">В последующих разделах описываются конструкции API вместе с какими конструкциями метаданных (WSDL или Policy), к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="09324-109">The subsequent sections describe API constructs along with what metadata constructs (WSDL or Policy) they correspond to.</span></span>

<span data-ttu-id="09324-110">Знание таких спецификаций метаданных, как WSDL и политика, поможет понять этот раздел.</span><span class="sxs-lookup"><span data-stu-id="09324-110">Familiarity with metadata specifications such as WSDL and Policy will aid in understanding this section.</span></span>

## <a name="endpoint-address"></a><span data-ttu-id="09324-111">Адрес конечной точки</span><span class="sxs-lookup"><span data-stu-id="09324-111">Endpoint address</span></span>

<span data-ttu-id="09324-112">Адрес конечной точки (см. [**\_ \_ адрес конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) получен из элемента расширения в элементе WSDL: Port документа WSDL.</span><span class="sxs-lookup"><span data-stu-id="09324-112">The address of an endpoint (see [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) is obtained from an extensibility element within the wsdl:port element of the WSDL document.</span></span> <span data-ttu-id="09324-113">Для указания адреса поддерживаются следующие элементы расширяемости:</span><span class="sxs-lookup"><span data-stu-id="09324-113">The following extensibility elements are supported for specifying the address:</span></span>

``` syntax
<wsdl:port...>
    <soap11:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <soap12:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa09:EndpointReference.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa10:EndpointReference.../>
</wsdl:port>
```

## <a name="ws_channel_binding"></a><span data-ttu-id="09324-114">\_Привязка канала \_ WS</span><span class="sxs-lookup"><span data-stu-id="09324-114">WS\_CHANNEL\_BINDING</span></span>

<span data-ttu-id="09324-115">Привязка канала (см. [**раздел \_ \_ Привязка канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) определяется транспортом, используемым привязкой SOAP, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="09324-115">The channel binding (see [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) is determined by the transport the soap binding used, as follows:</span></span>

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a><span data-ttu-id="09324-116">\_ \_ \_ Версия конверта свойства канала WS \_</span><span class="sxs-lookup"><span data-stu-id="09324-116">WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION</span></span>

<span data-ttu-id="09324-117">Версия конверта (см [**. \_ \_ \_ \_ версию конверта свойства WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) определяется используемой привязкой SOAP следующим образом.</span><span class="sxs-lookup"><span data-stu-id="09324-117">The envelope version (see [**WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by which soap binding is used, as follows:</span></span>

``` syntax
<wsdl:binding...>
    <soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

``` syntax
<wsdl:binding...>
    <soap12:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_2
</wsdl:binding>
```

## <a name="addressing-version"></a><span data-ttu-id="09324-118">Версия адресации</span><span class="sxs-lookup"><span data-stu-id="09324-118">Addressing Version</span></span>

<span data-ttu-id="09324-119">Версия адресации (см. сведения о [**\_ \_ \_ \_ версии адресации свойства WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) определяется следующими утверждениями в политике конечных точек:</span><span class="sxs-lookup"><span data-stu-id="09324-119">The addressing version (see [**WS\_CHANNEL\_PROPERTY\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <wsa09p:UsingAddressing.../> => WS_ADDRESSING_VERSION_0_9
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <wsa10p:UsingAddressing.../> => WS_ADDRESSING_VERSION_1_0
</wsp:Policy>
```

<span data-ttu-id="09324-120">Если утверждение адресации отсутствует, предполагается [**\_ \_ \_ транспортировка версии WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .</span><span class="sxs-lookup"><span data-stu-id="09324-120">If an addressing assertion is not present, then [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) is assumed.</span></span>

## <a name="message-encoding"></a><span data-ttu-id="09324-121">Message Encoding</span><span class="sxs-lookup"><span data-stu-id="09324-121">Message Encoding</span></span>

<span data-ttu-id="09324-122">Кодировка сообщения (см. раздел [**\_ \_ \_ Кодировка свойства WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) определяется следующими утверждениями в политике конечных точек:</span><span class="sxs-lookup"><span data-stu-id="09324-122">The encoding of the message (see [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

<span data-ttu-id="09324-123">Обратите внимание, что утверждение политики двоичной кодировки не включает сведения о том, является ли двоичная кодировка сеансом или без сеанса.</span><span class="sxs-lookup"><span data-stu-id="09324-123">Note that the binary encoding policy assertion does not include information about whether the binary encoding is sessionful or sessionless.</span></span> <span data-ttu-id="09324-124">Это определяется ограничением свойства Encoding (которое должно быть соответствующим в зависимости от того, используется ли [**\_ \_ Тип канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) в качестве сеанса или нет).</span><span class="sxs-lookup"><span data-stu-id="09324-124">This is determined by the encoding property constraint (which should be appropriate according to whether or not the [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) being used is sessionful or not).</span></span>

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

<span data-ttu-id="09324-125">Если ни одно из указанных выше утверждений не задано, используется кодировка текста: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ Encoding \_ XML \_ UTF16LE**, **WS \_ Encoding \_ XML \_ UTF16BE**.</span><span class="sxs-lookup"><span data-stu-id="09324-125">If neither of the above assertions are present, then a text encoding is used: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS\_ENCODING\_XML\_UTF16LE**, **WS\_ENCODING\_XML\_UTF16BE**.</span></span>

<span data-ttu-id="09324-126">Обратите внимание, что политика не включает в себя сведения о кодировке MTOM или текста (например, UTF8, UTF16LE или UTF16BE).</span><span class="sxs-lookup"><span data-stu-id="09324-126">Note that policy does not include information about the character set for MTOM or text encodings (whether it is UTF8, UTF16LE or UTF16BE).</span></span> <span data-ttu-id="09324-127">Фактическое используемое значение кодировки определяется ограничением свойства Encoding.</span><span class="sxs-lookup"><span data-stu-id="09324-127">The actual character set value used is determined by the encoding property constraint.</span></span>

## <a name="constraints-with-http-header-authentication"></a><span data-ttu-id="09324-128">Ограничения с проверкой подлинности заголовка HTTP</span><span class="sxs-lookup"><span data-stu-id="09324-128">Constraints with HTTP Header Authentication</span></span>

<span data-ttu-id="09324-129">Этот раздел применим, если задано ограничение привязки безопасности для проверки привязки безопасности [**\_ \_ заголовка \_ \_ \_ \_ WS HTTP**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="09324-129">This section applies when the [**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) security binding constraint is specified.</span></span>

<span data-ttu-id="09324-130">Эта привязка безопасности указывается в политике различными утверждениями, которые указывают, что должна использоваться проверка подлинности HTTP-заголовка, и должна использоваться определенная схема проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="09324-130">This security binding is indicated in the policy by different assertions that states both that HTTP header authentication should be used, and that a particular authentication scheme should be used.</span></span> <span data-ttu-id="09324-131">Утверждения политики соответствуют значениям [**\_ \_ \_ \_ \_ \_ \_ схемы проверки подлинности заголовка HTTP для свойства привязки безопасности WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="09324-131">The policy assertions correspond to the values of the [**WS\_SECURITY\_BINDING\_PROPERTY\_HTTP\_HEADER\_AUTH\_SCHEME**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) as follows:</span></span>

``` syntax
<wsp:Policy...>
    <httpp:BasicAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_BASIC
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NegotiateAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NtlmAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NTLM
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:DigestAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_DIGEST
</wsp:Policy>
```

## <a name="constraints-with-sll-transport-security"></a><span data-ttu-id="09324-132">Ограничения с безопасностью транспорта СЛЛ</span><span class="sxs-lookup"><span data-stu-id="09324-132">Constraints with SLL Transport Security</span></span>

<span data-ttu-id="09324-133">Этот раздел относится к определению ограничения привязки безопасности [**WS \_ SSL \_ Transport \_ Security \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="09324-133">This section applies when the [**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="09324-134">В этом случае используются следующие утверждения политики:</span><span class="sxs-lookup"><span data-stu-id="09324-134">The following policy assertions are used in this case:</span></span>

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <sp:HttpsToken.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constraints-with-sspi-transport-security"></a><span data-ttu-id="09324-135">Ограничения с безопасностью транспорта SSPI</span><span class="sxs-lookup"><span data-stu-id="09324-135">Constraints with SSPI Transport Security</span></span>

<span data-ttu-id="09324-136">Этот раздел применим, если задано ограничение привязки безопасности для [**\_ \_ \_ \_ \_ \_ ограничения привязки безопасности транспорта WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="09324-136">This section applies when the [**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="09324-137">В этом случае используются следующие утверждения политики:</span><span class="sxs-lookup"><span data-stu-id="09324-137">The following policy assertions are used in this case:</span></span>

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <netf:WindowsTransportSecurity.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constrains-with-transport-security"></a><span data-ttu-id="09324-138">Ограничения безопасности транспорта</span><span class="sxs-lookup"><span data-stu-id="09324-138">Constrains with Transport Security</span></span>

<span data-ttu-id="09324-139">Ограничение [**свойства \_ \_ \_ \_ \_ уровня защиты транспорта свойства WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) можно указать, если указаны какие либо ограничения привязки безопасности:</span><span class="sxs-lookup"><span data-stu-id="09324-139">The [**WS\_SECURITY\_PROPERTY\_TRANSPORT\_PROTECTION\_LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) property constraint can be specified if any of the security binding constraints are specified:</span></span>

-   [<span data-ttu-id="09324-140">**\_ \_ \_ \_ ограничение привязки безопасности транспорта WS SSL \_**</span><span class="sxs-lookup"><span data-stu-id="09324-140">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    <span data-ttu-id="09324-141">Значение из политики всегда равно [**WS- \_ \_ уровню защиты \_ Sign \_ и \_ Encrypt**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="09324-141">The value from policy is always [**WS\_PROTECTION\_LEVEL\_SIGN\_AND\_ENCRYPT**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

-   [<span data-ttu-id="09324-142">**\_ \_ \_ \_ \_ ограничение привязки безопасности транспорта WS TCP \_ SSPI**</span><span class="sxs-lookup"><span data-stu-id="09324-142">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    <span data-ttu-id="09324-143">Значение из параметра Policy указывается как часть утверждения Виндовстранспортсекурити следующим образом:</span><span class="sxs-lookup"><span data-stu-id="09324-143">The value from policy is specified as part of the WindowsTransportSecurity assertion, as follows:</span></span>

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [<span data-ttu-id="09324-144">**\_ \_ \_ \_ \_ ограничение привязки безопасности проверки подлинности заголовка WS HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="09324-144">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    <span data-ttu-id="09324-145">Значением из политики всегда является [**\_ уровень защиты WS \_ \_ None**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="09324-145">The value from policy is always [**WS\_PROTECTION\_LEVEL\_NONE**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

## <a name="constraints-with-kerberos-apreq-security-binding"></a><span data-ttu-id="09324-146">Ограничения с привязкой безопасности Kerberos АПРЕК</span><span class="sxs-lookup"><span data-stu-id="09324-146">Constraints with Kerberos APREQ Security Binding</span></span>

<span data-ttu-id="09324-147">Этот раздел применим, если задано ограничение привязки безопасности для ограничения привязки безопасности [**\_ сообщений WS Kerberos \_ апрек \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="09324-147">This section applies when the [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="09324-148">В этом случае используются следующие утверждения политики:</span><span class="sxs-lookup"><span data-stu-id="09324-148">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a><span data-ttu-id="09324-149">Ограничения с привязкой безопасности сообщений</span><span class="sxs-lookup"><span data-stu-id="09324-149">Constraints with Message Security Binding</span></span>

<span data-ttu-id="09324-150">Этот раздел применяется при указании ограничения привязки безопасности для ограничения привязки безопасности [**\_ \_ сообщений \_ \_ \_ пользователя WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="09324-150">This section applies when the [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="09324-151">В этом случае используются следующие утверждения политики:</span><span class="sxs-lookup"><span data-stu-id="09324-151">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a><span data-ttu-id="09324-152">\_ \_ \_ \_ ограничение привязки безопасности сообщений сертификата \_ WS</span><span class="sxs-lookup"><span data-stu-id="09324-152">WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="09324-153">Этот раздел применим, если задано ограничение привязки безопасности для [**\_ \_ \_ \_ \_ ограничения привязки сообщений WS CERT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="09324-153">This section applies when the [**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="09324-154">В этом случае используются следующие утверждения политики:</span><span class="sxs-lookup"><span data-stu-id="09324-154">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a><span data-ttu-id="09324-155">\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений \_ о выданных маркерах WS</span><span class="sxs-lookup"><span data-stu-id="09324-155">WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="09324-156">Этот раздел применяется, если задано ограничение привязки безопасности для сообщения о привязке защиты [**\_ \_ \_ сообщений \_ \_ \_ токена WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="09324-156">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="09324-157">В этом случае используются следующие утверждения политики:</span><span class="sxs-lookup"><span data-stu-id="09324-157">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:IssuedToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:RequestSecurityTokenTemplate TrustVersion='xs:anyURI&quot;?>
                ...
                <wst10:Claims>
                    <wsi:ClaimType Optional='xs:boolean'?>xs:anyURI<wt:ClaimType>*
                </wst10:Claims>
                ...
            </wsp:RequestSecurityTokenTemplate>
            <wsp:Policy>
                <sp:RequireDerivedKeys/> ?
                <sp:RequireExternalReference/> ?
                <sp:RequireInternalReference/> ?
            </wsp:Policy> ?
        </sp:IssuedToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

<span data-ttu-id="09324-158">Ниже описывается сопоставление полей [**\_ \_ \_ \_ \_ \_ ограничения привязки безопасности сообщений о выданном маркере WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) с указанной выше политикой.</span><span class="sxs-lookup"><span data-stu-id="09324-158">The following describes the mapping of fields of the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) to the above policy:</span></span>

-   <span data-ttu-id="09324-159">Поле Клаимконстраинтс используется для проверки набора URI типа утверждения, который отображается в элементе ВСИ: Typ выше.</span><span class="sxs-lookup"><span data-stu-id="09324-159">The claimConstraints field is used to verify the set of claim type URIs that appear within the wsi:ClaimType element above.</span></span>

-   <span data-ttu-id="09324-160">Поле Иссуераддресс соответствует элементу WSP: Issuer выше, который является [**\_ \_ адресом конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) службы, которая может выдать маркер.</span><span class="sxs-lookup"><span data-stu-id="09324-160">The issuerAddress field corresponds to the wsp:Issuer element above, which is the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) of the service that can issue the token.</span></span>

-   <span data-ttu-id="09324-161">Поле Рекуестсекурититокентемплате соответствует дочерним элементам элемента wsp: Рекуестсекурититокентемплате.</span><span class="sxs-lookup"><span data-stu-id="09324-161">The requestSecurityTokenTemplate field corresponds to the child elements of the wsp:RequestSecurityTokenTemplate element.</span></span>

## <a name="ws_security_context_message_security_binding_constraint"></a><span data-ttu-id="09324-162">\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений контекста \_ безопасности WS</span><span class="sxs-lookup"><span data-stu-id="09324-162">WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="09324-163">Этот раздел относится к определению ограничения привязки безопасности для [**\_ \_ \_ сообщения \_ \_ \_ контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="09324-163">This section applies when the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="09324-164">В этом случае используются следующие утверждения политики:</span><span class="sxs-lookup"><span data-stu-id="09324-164">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:SecureConversationToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:Policy>
                <sp:RequireDerivedKeys.../>?
                <sp:RequireExternalUriReference.../>?
                <sp:SC10SecurityContextToken.../>? => WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005
                <sp:BootstrapPolicy... >?
                   <wsp:Policy> ...  </wsp:Policy> => WS_SECURITY_CONSTRAINTS
                </sp:BootstrapPolicy>
            </wsp:Policy>
        </wsp:SecureConversationToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

<span data-ttu-id="09324-165">Режим энтропии определяется с помощью утверждения <SP: Trust10>.</span><span class="sxs-lookup"><span data-stu-id="09324-165">The entropy mode is determined by the <sp:Trust10> assertion.</span></span> <span data-ttu-id="09324-166"><SP: Рекуиреклиентентропи/> и <SP: Рекуиресерверентропи/> => [**WS \_ Security \_ Key с \_ \_ режимом энтропии \_ Объединенный**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP: рекуиреклиентентропи/> => рекуиресерверентропи:/<= >, **\_ \_ \_ \_ \_ \_ только сервер в режиме энтропии** **\_ \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="09324-166"><sp:RequireClientEntropy/> and <sp:RequireServerEntropy/> => [**WS\_SECURITY\_KEY\_ENTROPY\_MODE\_COMBINED**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <sp:RequireClientEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_CLIENT\_ONLY** <sp:RequireServerEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_SERVER\_ONLY**</span></span>

## <a name="ws_request_security_token_property_trust_version"></a><span data-ttu-id="09324-167">\_ \_ \_ \_ \_ версия доверия свойства маркера безопасности запроса WS \_</span><span class="sxs-lookup"><span data-stu-id="09324-167">WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION</span></span>

<span data-ttu-id="09324-168">Этот раздел применяется, если задано ограничение привязки безопасности для сообщения о привязке защиты [**\_ \_ \_ сообщений \_ \_ \_ токена WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="09324-168">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="09324-169">Следующие утверждения политики используются для задания [**\_ \_ версии доверия WS**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) и связанных параметров.</span><span class="sxs-lookup"><span data-stu-id="09324-169">The following policy assertions are used to identify the [**WS\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) and associated options.</span></span>

``` syntax
<sp:Trust10> => WS_TRUST_VERSION_FEBRUARY_2005
    <sp:Policy>
        <sp:MustSupportClientChallenge/> ?
        <sp:MustSupportServerChallenge/> ?
        <sp:RequireClientEntropy/> ?
        <sp:RequireServerEntropy/> ?
        <sp:MustSupportIssuedTokens/> ?
    </sp:Policy>
</sp:Trust10>
```

<span data-ttu-id="09324-170">Версию доверия можно указать с помощью [**\_ \_ \_ \_ \_ ограничения свойства маркера безопасности WS Request**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) с идентификатором свойства [**\_ \_ \_ \_ \_ \_ версии доверия свойства токена безопасности WS**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span><span class="sxs-lookup"><span data-stu-id="09324-170">The trust version can be specified using the [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) with a property id of [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span></span>

## <a name="ws_security_property_security_header_version"></a><span data-ttu-id="09324-171">\_ \_ \_ \_ версия заголовка безопасности свойства WS Security \_</span><span class="sxs-lookup"><span data-stu-id="09324-171">WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION</span></span>

<span data-ttu-id="09324-172">Этот раздел применяется при использовании любого из следующих ограничений привязки:</span><span class="sxs-lookup"><span data-stu-id="09324-172">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="09324-173">**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений WS Kerberos \_ апрек**</span><span class="sxs-lookup"><span data-stu-id="09324-173">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="09324-174">**\_ \_ \_ \_ ограничение привязки безопасности сообщений имени пользователя WS \_**</span><span class="sxs-lookup"><span data-stu-id="09324-174">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="09324-175">**\_ \_ \_ \_ ограничение привязки безопасности сообщений сертификата \_ WS**</span><span class="sxs-lookup"><span data-stu-id="09324-175">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="09324-176">**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений \_ о выданных маркерах WS**</span><span class="sxs-lookup"><span data-stu-id="09324-176">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="09324-177">Версия безопасности заголовка (как указано в [**\_ \_ \_ \_ заголовке \_ безопасности свойства WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) определяется одним из следующих утверждений политики:</span><span class="sxs-lookup"><span data-stu-id="09324-177">The header security version (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a><span data-ttu-id="09324-178">Ограничения с макетом безопасности заголовка</span><span class="sxs-lookup"><span data-stu-id="09324-178">Constraints with Header Security Layout</span></span>

<span data-ttu-id="09324-179">Этот раздел применяется при использовании любого из следующих ограничений привязки:</span><span class="sxs-lookup"><span data-stu-id="09324-179">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="09324-180">**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений WS Kerberos \_ апрек**</span><span class="sxs-lookup"><span data-stu-id="09324-180">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="09324-181">**\_ \_ \_ \_ ограничение привязки безопасности сообщений имени пользователя WS \_**</span><span class="sxs-lookup"><span data-stu-id="09324-181">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="09324-182">**\_ \_ \_ \_ ограничение привязки безопасности сообщений сертификата \_ WS**</span><span class="sxs-lookup"><span data-stu-id="09324-182">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="09324-183">**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений \_ о выданных маркерах WS**</span><span class="sxs-lookup"><span data-stu-id="09324-183">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="09324-184">Макет заголовка безопасности (заданный в [**\_ \_ \_ \_ \_ макете заголовка безопасности свойства безопасности WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) определяется одним из следующих утверждений политики:</span><span class="sxs-lookup"><span data-stu-id="09324-184">The security header layout (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_LAYOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Lax.../> => WS_SECURITY_HEADER_LAYOUT_LAX
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Strict.../> => WS_SECURITY_HEADER_LAYOUT_STRICT
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsFirst.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsLast.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

## <a name="constraints-with-timestamp-security"></a><span data-ttu-id="09324-185">Ограничения с защитой меток времени</span><span class="sxs-lookup"><span data-stu-id="09324-185">Constraints with Timestamp Security</span></span>

<span data-ttu-id="09324-186">Этот раздел применяется при использовании любого из следующих ограничений привязки:</span><span class="sxs-lookup"><span data-stu-id="09324-186">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="09324-187">**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений WS Kerberos \_ апрек**</span><span class="sxs-lookup"><span data-stu-id="09324-187">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="09324-188">**\_ \_ \_ \_ ограничение привязки безопасности сообщений имени пользователя WS \_**</span><span class="sxs-lookup"><span data-stu-id="09324-188">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="09324-189">**\_ \_ \_ \_ ограничение привязки безопасности сообщений сертификата \_ WS**</span><span class="sxs-lookup"><span data-stu-id="09324-189">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="09324-190">**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений \_ о выданных маркерах WS**</span><span class="sxs-lookup"><span data-stu-id="09324-190">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="09324-191">Независимо от того, включена ли отметка времени в заголовок безопасности (как указано [**в \_ \_ свойстве \_ « \_ Использование метки времени» свойства WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)), определяется наличием параметра SP: инклудетиместамп в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="09324-191">Whether or not a timestamp is included in the security header (as specified by [**WS\_SECURITY\_PROPERTY\_TIMESTAMP\_USAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by the presence of the sp:IncludeTimestamp in the following location:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

<span data-ttu-id="09324-192">При наличии утверждения SP: Инклудетиместамп значение параметра Policy равно [**WS \_ Security \_ timestamp \_ \_ Always**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="09324-192">If the sp:IncludeTimestamp assertion is present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

<span data-ttu-id="09324-193">Если утверждение SP: Инклудетиместамп отсутствует, значение параметра Policy равно [**WS \_ Security \_ timestamp \_ \_ никогда не**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)используется.</span><span class="sxs-lookup"><span data-stu-id="09324-193">If the sp:IncludeTimestamp assertion is not present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

 

 




