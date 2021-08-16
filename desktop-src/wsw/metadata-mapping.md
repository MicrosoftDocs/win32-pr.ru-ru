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
ms.openlocfilehash: 57e6577e05f1d51ec13cc917465c306b94c403827149b086f252a38964997ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841494"
---
# <a name="metadata-mapping"></a>Сопоставление метаданных

Содержимое схемы документа метаданных в API метаданных описано в следующих разделах.


В этой документации используются следующие префиксы пространств имен:

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

В последующих разделах описываются конструкции API вместе с какими конструкциями метаданных (WSDL или Policy), к которым они относятся.

Знание таких спецификаций метаданных, как WSDL и политика, поможет понять этот раздел.

## <a name="endpoint-address"></a>Адрес конечной точки

Адрес конечной точки (см. [**\_ \_ адрес конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) получен из элемента расширения в элементе WSDL: Port документа WSDL. Для указания адреса поддерживаются следующие элементы расширяемости:

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

## <a name="ws_channel_binding"></a>\_Привязка канала \_ WS

Привязка канала (см. [**раздел \_ \_ Привязка канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) определяется транспортом, используемым привязкой SOAP, следующим образом:

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a>\_ \_ \_ Версия конверта свойства канала WS \_

Версия конверта (см [**. \_ \_ \_ \_ версию конверта свойства WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) определяется используемой привязкой SOAP следующим образом.

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

## <a name="addressing-version"></a>Версия адресации

Версия адресации (см. сведения о [**\_ \_ \_ \_ версии адресации свойства WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) определяется следующими утверждениями в политике конечных точек:

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

Если утверждение адресации отсутствует, предполагается [**\_ \_ \_ транспортировка версии WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .

## <a name="message-encoding"></a>Message Encoding

Кодировка сообщения (см. раздел [**\_ \_ \_ Кодировка свойства WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) определяется следующими утверждениями в политике конечных точек:

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

Обратите внимание, что утверждение политики двоичной кодировки не включает сведения о том, является ли двоичная кодировка сеансом или без сеанса. Это определяется ограничением свойства Encoding (которое должно быть соответствующим в зависимости от того, используется ли [**\_ \_ Тип канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) в качестве сеанса или нет).

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

Если ни одно из указанных выше утверждений не задано, используется кодировка текста: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ Encoding \_ XML \_ UTF16LE**, **WS \_ Encoding \_ XML \_ UTF16BE**.

Обратите внимание, что политика не включает в себя сведения о кодировке MTOM или текста (например, UTF8, UTF16LE или UTF16BE). Фактическое используемое значение кодировки определяется ограничением свойства Encoding.

## <a name="constraints-with-http-header-authentication"></a>Ограничения с проверкой подлинности заголовка HTTP

Этот раздел применим, если задано ограничение привязки безопасности для проверки привязки безопасности [**\_ \_ заголовка \_ \_ \_ \_ WS HTTP**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) .

Эта привязка безопасности указывается в политике различными утверждениями, которые указывают, что должна использоваться проверка подлинности HTTP-заголовка, и должна использоваться определенная схема проверки подлинности. Утверждения политики соответствуют значениям [**\_ \_ \_ \_ \_ \_ \_ схемы проверки подлинности заголовка HTTP для свойства привязки безопасности WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) следующим образом:

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

## <a name="constraints-with-sll-transport-security"></a>Ограничения с безопасностью транспорта СЛЛ

Этот раздел относится к определению ограничения привязки безопасности [**WS \_ SSL \_ Transport \_ Security \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) . В этом случае используются следующие утверждения политики:

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

## <a name="constraints-with-sspi-transport-security"></a>Ограничения с безопасностью транспорта SSPI

Этот раздел применим, если задано ограничение привязки безопасности для [**\_ \_ \_ \_ \_ \_ ограничения привязки безопасности транспорта WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) . В этом случае используются следующие утверждения политики:

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

## <a name="constrains-with-transport-security"></a>Ограничения безопасности транспорта

Ограничение [**свойства \_ \_ \_ \_ \_ уровня защиты транспорта свойства WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) можно указать, если указаны какие либо ограничения привязки безопасности:

-   [**\_ \_ \_ \_ ограничение привязки безопасности транспорта WS SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    Значение из политики всегда равно [**WS- \_ \_ уровню защиты \_ Sign \_ и \_ Encrypt**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности транспорта WS TCP \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    Значение из параметра Policy указывается как часть утверждения Виндовстранспортсекурити следующим образом:

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности проверки подлинности заголовка WS HTTP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    Значением из политики всегда является [**\_ уровень защиты WS \_ \_ None**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

## <a name="constraints-with-kerberos-apreq-security-binding"></a>Ограничения с привязкой безопасности Kerberos АПРЕК

Этот раздел применим, если задано ограничение привязки безопасности для ограничения привязки безопасности [**\_ сообщений WS Kerberos \_ апрек \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) . В этом случае используются следующие утверждения политики:

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a>Ограничения с привязкой безопасности сообщений

Этот раздел применяется при указании ограничения привязки безопасности для ограничения привязки безопасности [**\_ \_ сообщений \_ \_ \_ пользователя WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) . В этом случае используются следующие утверждения политики:

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a>\_ \_ \_ \_ ограничение привязки безопасности сообщений сертификата \_ WS

Этот раздел применим, если задано ограничение привязки безопасности для [**\_ \_ \_ \_ \_ ограничения привязки сообщений WS CERT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) . В этом случае используются следующие утверждения политики:

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a>\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений \_ о выданных маркерах WS

Этот раздел применяется, если задано ограничение привязки безопасности для сообщения о привязке защиты [**\_ \_ \_ сообщений \_ \_ \_ токена WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) . В этом случае используются следующие утверждения политики:

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

Ниже описывается сопоставление полей [**\_ \_ \_ \_ \_ \_ ограничения привязки безопасности сообщений о выданном маркере WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) с указанной выше политикой.

-   Поле Клаимконстраинтс используется для проверки набора URI типа утверждения, который отображается в элементе ВСИ: Typ выше.

-   Поле Иссуераддресс соответствует элементу WSP: Issuer выше, который является [**\_ \_ адресом конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) службы, которая может выдать маркер.

-   Поле Рекуестсекурититокентемплате соответствует дочерним элементам элемента wsp: Рекуестсекурититокентемплате.

## <a name="ws_security_context_message_security_binding_constraint"></a>\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений контекста \_ безопасности WS

Этот раздел относится к определению ограничения привязки безопасности для [**\_ \_ \_ сообщения \_ \_ \_ контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) . В этом случае используются следующие утверждения политики:

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

Режим энтропии определяется с помощью утверждения <SP: Trust10>. <SP: Рекуиреклиентентропи/> и <SP: Рекуиресерверентропи/> => [**WS \_ Security \_ Key с \_ \_ режимом энтропии \_ Объединенный**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP: рекуиреклиентентропи/> => рекуиресерверентропи:/<= >, **\_ \_ \_ \_ \_ \_ только сервер в режиме энтропии** **\_ \_ \_ \_ \_ \_**

## <a name="ws_request_security_token_property_trust_version"></a>\_ \_ \_ \_ \_ версия доверия свойства маркера безопасности запроса WS \_

Этот раздел применяется, если задано ограничение привязки безопасности для сообщения о привязке защиты [**\_ \_ \_ сообщений \_ \_ \_ токена WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) . Следующие утверждения политики используются для задания [**\_ \_ версии доверия WS**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) и связанных параметров.

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

Версию доверия можно указать с помощью [**\_ \_ \_ \_ \_ ограничения свойства маркера безопасности WS Request**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) с идентификатором свойства [**\_ \_ \_ \_ \_ \_ версии доверия свойства токена безопасности WS**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).

## <a name="ws_security_property_security_header_version"></a>\_ \_ \_ \_ версия заголовка безопасности свойства WS Security \_

Этот раздел применяется при использовании любого из следующих ограничений привязки:

-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений WS Kerberos \_ апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_ \_ \_ \_ ограничение привязки безопасности сообщений имени пользователя WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_ \_ \_ \_ ограничение привязки безопасности сообщений сертификата \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений \_ о выданных маркерах WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Версия безопасности заголовка (как указано в [**\_ \_ \_ \_ заголовке \_ безопасности свойства WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) определяется одним из следующих утверждений политики:

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a>Ограничения с макетом безопасности заголовка

Этот раздел применяется при использовании любого из следующих ограничений привязки:

-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений WS Kerberos \_ апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_ \_ \_ \_ ограничение привязки безопасности сообщений имени пользователя WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_ \_ \_ \_ ограничение привязки безопасности сообщений сертификата \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений \_ о выданных маркерах WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Макет заголовка безопасности (заданный в [**\_ \_ \_ \_ \_ макете заголовка безопасности свойства безопасности WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) определяется одним из следующих утверждений политики:

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

## <a name="constraints-with-timestamp-security"></a>Ограничения с защитой меток времени

Этот раздел применяется при использовании любого из следующих ограничений привязки:

-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений WS Kerberos \_ апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_ \_ \_ \_ ограничение привязки безопасности сообщений имени пользователя WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_ \_ \_ \_ ограничение привязки безопасности сообщений сертификата \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений \_ о выданных маркерах WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Независимо от того, включена ли отметка времени в заголовок безопасности (как указано [**в \_ \_ свойстве \_ « \_ Использование метки времени» свойства WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)), определяется наличием параметра SP: инклудетиместамп в следующем расположении:

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

При наличии утверждения SP: Инклудетиместамп значение параметра Policy равно [**WS \_ Security \_ timestamp \_ \_ Always**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

Если утверждение SP: Инклудетиместамп отсутствует, значение параметра Policy равно [**WS \_ Security \_ timestamp \_ \_ никогда не**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)используется.

 

 




