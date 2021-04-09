---
title: Привязки безопасности
description: Привязка безопасности — это спецификация маркера безопасности, которая указывает среде выполнения, как получить и использовать маркер безопасности для обеспечения безопасности канала.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Веб-службы привязки безопасности для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104134795"
---
# <a name="security-bindings"></a>Привязки безопасности

Привязка безопасности — это спецификация маркера безопасности, которая указывает среде выполнения, как получить и использовать маркер безопасности для обеспечения безопасности канала. Маркер безопасности содержит сведения, подтверждающие право доступа к ресурсам. Он также может иметь связанный криптографический ключ для выполнения подписей и шифрования.


Каждая привязка безопасности содержит собственную коллекцию дополнительных [параметров привязки безопасности](security-binding-settings.md) , область действия которой определяется маркером безопасности, который он определяет. Он также содержит [учетные данные безопасности](security-credentials.md), представляющие доказательства безопасности (например, имя пользователя и пароли или сертификаты), необходимые для создания маркеров безопасности.

Следующие обратные вызовы являются частью привязки безопасности:

-   [**\_ \_ \_ обратный вызов функции WS Validate SAML**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

Следующие перечисления являются частью привязки безопасности:

-   [**\_ \_ Использование безопасности сообщений \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [**\_ \_ тип аутентификации WS \_ SAML**](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [**\_ \_ тип привязки безопасности \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [**\_ \_ \_ тип маркера ключа безопасности WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

Следующие функции являются частью привязки безопасности:

-   [**вскреатексмлсекурититокен**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [**всфрисекурититокен**](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

Следующие структуры являются частью привязки безопасности:

-   [**\_ \_ маркер асимметричного \_ \_ ключа безопасности \_ WS CAPI**](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [**\_ \_ \_ \_ Проверка подлинности SAML с подписью сертификата WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [**\_ \_ \_ Привязка безопасности для проверки подлинности заголовка WS \_ HTTP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [**\_ \_ \_ \_ Привязка безопасности сообщений WS Kerberos \_ апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [**\_ \_ \_ \_ Привязка безопасности транспорта WS помощью канала NamedPipe \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**\_ \_ маркер асимметричного \_ \_ ключа безопасности \_ WS NCRYPT**](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [**\_ \_ маркер симметричного \_ \_ ключа безопасности \_ (необработанный) WS**](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [**\_ \_ удостоверение WS SAML Authenticator**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [**\_ \_ \_ Привязка безопасности сообщения SAML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [**\_Привязка безопасности \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [**\_ \_ \_ \_ Привязка безопасности сообщений контекста безопасности \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [**\_ \_ маркер ключа безопасности \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [**\_ \_ \_ Привязка безопасности транспорта WS \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [**\_ \_ \_ \_ Привязка безопасности транспорта WS TCP \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [**\_ \_ \_ Привязка безопасности сообщений имени пользователя WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [**\_ \_ \_ \_ Привязка безопасности сообщений для токена WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




