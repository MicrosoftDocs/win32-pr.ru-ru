---
title: Импорт метаданных
description: ВВСАПИ включает элементы API, которые можно использовать для обработки WSDL и политики из конечной точки с целью извлечения сведений, которые можно использовать для связи с конечной точкой.
ms.assetid: 77738bf1-ef8b-4fd6-a36a-43f1932868dd
keywords:
- Веб-службы импорта метаданных для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c36ffdf9bcbf0d63bdef473cc52cd4d545e5a3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797394"
---
# <a name="metadata-import"></a>Импорт метаданных

ВВСАПИ включает элементы API, которые можно использовать для обработки WSDL и политики из конечной точки с целью извлечения сведений, которые можно использовать для связи с конечной точкой. Эти API обычно используются, когда протокол связи, поддерживаемый конечной точкой, еще не известен.


Для обработки метаданных используйте следующую последовательность:

``` syntax
WsCreateMetadata    // create a metadata object

while there are metadata documents to add
{
    // retrieve the metadata document from it's location
    // (download, read from file, etc)

    // add the document to the metadata object
    WsReadMetadata

    // optionally query the metadata object for any missing documents
    WsGetMissingMetadataDocumentAddress?
}

// get the endpoints from the metadata object
WsGetMetadataEndpoints

for each endpoint
{            
    // examine the endpoint information to see if 
    // the endpoint is relevant for the particular scenario

    if the endpoint is relevant
    {
        // get the policy object from the endpoint

        // get the number of policy alternatives in the policy
        WsGetPolicyAlternativeCount

        for each policy alternative
        {
            // construct a policy constraints structure that specifies
            // what policy is acceptable and what information to extract
            // from the policy

            // see if the policy alternative matches the constraints
            WsMatchPolicyAlternative

            // if there is a match, then use it

            // if there is not a match, then it is also possible to 
            // try with a different constraint structure
        }
    }
}

// If reusing the metadata object for a different set of documents
WsResetMetadata? // reset metadata object, which removes all documents

WsFreeMetadata // free the metadata object
```

сведения о том, как утверждения WSDL и WS-Policy соответствуют API, см. в разделе [Сопоставление метаданных](metadata-mapping.md) .

## <a name="security"></a>Безопасность

Скачанные метаданные — это так же хорошо, как адрес, используемый для его скачивания. Приложение должно обеспечить доверие к адресу. Кроме того, приложение должно обеспечить использование протокола безопасности для загрузки документов метаданных, которые не допускают фальсификации с помощью метаданных.

Приложение должно проверять адреса служб, предоставляемых метаданными. По умолчанию среда выполнения гарантирует, что имя узла службы совпадает с исходным URL-адресом, используемым для загрузки метаданных, но приложение может захотеть выполнить дополнительные проверки. Приложение может отключить проверку имени узла, перезаписав свойство [**метаданных WS \_ \_ проверить имя \_ \_ узла \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) . Если проверка имени узла, выполненная по умолчанию, отключена, приложение должно защищать себя от документов метаданных, содержащих адрес службы, от другой стороны, которая не доверяет каким-либо другим способом.

По умолчанию максимальный объем памяти, используемый средой выполнения метаданных для десериализации и обработки метаданных, составляет 256 КБ, а максимальное число документов, которое можно добавить, — 32. Эти значения по умолчанию могут быть перезаписаны в свойствах [**\_ \_ \_ \_ запрошенного \_ размера кучи свойств метаданных**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) и свойств **\_ метаданных \_ \_ \_ WS** . Эти границы предназначены для ограничения объема загружаемых файлов и ограничивают объем выделяемой памяти для накопления метаданных. Увеличение этих значений может привести к чрезмерному потреблению памяти, использованию ЦП или пропускной способности сети. Обратите внимание, что из-за расширения строк словаря в двоичном формате небольшое сообщение может привести к значительному объему десериализованной формы, поэтому использование небольших сообщений для ограничения выделения памяти метаданных недостаточно при использовании двоичного формата.

По умолчанию максимальное количество альтернативных политик — 32, хотя оно может быть перезаписано свойством " [**\_ \_ \_ Максимальное \_ альтернативное свойство политики WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) ". Если приложение просматривает каждую альтернативу в поисках совпадения, может потребоваться выполнить поиск во всех вариантах, прежде чем искать соответствие. Увеличение максимального числа альтернатив может привести к чрезмерному использованию ЦП.

Следующие перечисления являются частью импорта метаданных:

-   [**\_ \_ идентификатор свойства метаданных \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [**\_состояние МЕТАДАННЫХ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [**\_ \_ тип расширения политики \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [**\_ \_ идентификатор свойства политики \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [**\_состояние политики \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [**\_ \_ \_ тип ограничения привязки безопасности \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

В импорт метаданных входят следующие функции:

-   [**вскреатеметадата**](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [**всфриметадата**](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [**всжетметадатаендпоинтс**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [**всжетметадатапроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [**всжетмиссингметадатадокументаддресс**](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [**всжетполициалтернативекаунт**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [**всжетполиципроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [**всматчполициалтернативе**](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [**всреадметадата**](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [**всресетметадата**](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

В импорт метаданных входят следующие дескрипторы:

-   [\_метаданные WS](ws-metadata.md)
-   [\_политика WS](ws-policy.md)

В импорт метаданных входят следующие структуры:

-   [**\_ \_ \_ \_ ограничение привязки безопасности сообщений сертификата \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_ \_ ограничение свойства канала \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [**\_расширение политики конечных точек WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности проверки подлинности заголовка WS HTTP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений \_ о выданных маркерах WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений WS Kerberos \_ апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_ \_ Конечная точка метаданных WS**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [**\_ \_ конечные точки метаданных WS**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [**\_свойство МЕТАДАННЫХ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [**\_ограничения политики \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [**\_расширение политики \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [**\_Свойства политики \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [**\_свойство политики \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [**\_ \_ \_ ограничение свойства токена \_ безопасности \_ WS Request**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [**\_ \_ ограничение привязки безопасности \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [**\_ \_ \_ ограничение свойства привязки безопасности \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [**\_ограничения безопасности \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений контекста \_ безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [**\_ \_ ограничение свойства безопасности \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [**\_ \_ \_ \_ ограничение привязки безопасности транспорта WS SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [**\_ \_ \_ \_ \_ ограничение привязки безопасности транспорта WS TCP \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [**\_ \_ \_ \_ ограничение привязки безопасности сообщений имени пользователя WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




