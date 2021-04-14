---
title: Метаданные службы
description: Узел службы ВВСАПИ поддерживает WS-MetadataExchange для своих конечных точек.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Собственные метаданные службы — веб-службы
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488568"
---
# <a name="service-metadata"></a>Метаданные службы

Узел службы ВВСАПИ поддерживает WS-MetadataExchange для своих конечных точек. Включить такой обмен метаданными на узле службы можно следующим образом:

-   Укажите документы метаданных в свойстве [**\_ \_ метаданных службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) на [ \_ \_ узле службы WS](ws-service-host.md).
-   Укажите имя службы в свойстве [**\_ \_ метаданных службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) на [ \_ \_ узле службы WS](ws-service-host.md).
-   Укажите порт для отдельных конечных точек с помощью [**свойства \_ \_ метаданных для \_ свойства \_ конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) WS в [**\_ \_ конечной точке службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).
-   Включите одну или несколько [**структур \_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) для обслуживания запросов WS-MetadataExchange.
-   При необходимости укажите **\_ \_ \_ \_ \_ \_ \_ суффикс URL-адреса обмена метаданных свойств конечной точки службы WS** в перечислении [**\_ \_ \_ \_ идентификаторов свойств конечной точки службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) для обслуживания Ws-MetadataExchange запросов по определенному адресу.


Указание метаданных и имен службы на узле службы

Первым шагом является указание документов метаданных на узле службы. Для этого необходимо собрать отдельные документы в виде массива \_ строк WS XML \_ \* . Эти строки могут быть XML-схемой, WSDL или WS-Policy документом. Это указывается с помощью свойства [**\_ \_ \_ метаданных свойства службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .

При необходимости приложение может также указать имя службы и пространство имен как часть [**\_ \_ метаданных службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata). Если в документе метаданных не указан элемент службы для данного имени службы, то модель службы создаст элемент службы с соответствующими портами WSDL для службы.

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

Обратите внимание, что для документов не выполняется проверка отдельных документов метаданных. Приложение проверяет содержимое документов и гарантирует, что все пути импорта являются относительно определенными.

Указанное пространство имен используется для нахождение документа, в котором элемент службы будет добавлен узлом службы.

Добавление элемента службы в документ WSDL

Узел службы предоставляет приложению средство для добавления элемента службы от его имени, если он еще не указан. Чтобы обеспечить такое поведение, приложение должно указать поля Серивценаме и Сервиценс в структуре [**\_ \_ метаданных службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) . Если serviceName и Сервиценс равны **null** , в документ WSDL не добавляется элемент Service. Оба они используются для указания документа, в котором будет добавлен serviceElement.

Если [**свойство \_ \_ \_ метаданных свойства службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) не указано, метаданные ексханже не будут выполняться на узле службы.

Указание порта в \_ конечной точке службы WS \_

Чтобы [**\_ \_ Конечная точка службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) была доступна в качестве порта внутри элемента Service в документе WSDL, приложение должно указать свойство метаданных для [**\_ \_ \_ свойства \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) .

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

Предполагается, что ссылка на имя привязки и пространство имен существует в документах, указанных на узле службы как часть \_ \_ метаданных свойства службы WS \_ . Среда выполнения не проверяет это от имени приложения.

Включение обслуживания WS-MetadataExchange в \_ \_ конечной точке службы WS

Чтобы обслуживать запросы WS-MetadataExchange, на узле службы должна быть включена хотя бы одна конечная точка для обслуживания запросов WS-MetadataExchange. Для этого необходимо задать соответствующую версию для WS-MetadataExchange в [**\_ \_ конечной точке службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Включение обслуживания HTTP GET в \_ \_ конечной точке службы WS

Чтобы Сервицехттп запросы GET, на узле службы должна быть включена хотя бы одна конечная точка для обслуживания запросов WS-MetadataExchange. Для этого необходимо задать соответствующую версию для WS-MetadataExchange в [**\_ \_ конечной точке службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Указание суффикса URL-адреса для запросов Ws-MetadataExchange

Приложение может при необходимости включить прием запросов только для WS-MetadataExchange по определенному пути. Это делается путем указания суффикса для заданной \_ \_ конечной точки службы WS. Этот суффикс объединяется "как есть" с фактическим URL-адресом \_ \_ конечной точки службы WS. Объединенная строка используется в качестве соответствующего URL-адреса для полученного заголовка "to".

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

Следующие элементы API относятся к службе метаданных.

| Перечисление                                                       | Описание                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_тип обмена метаданными WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | Включает или отключает WS-MetadataExchange и HTTP GET для обслуживания конечной точки. |



 



| Структура                                                               | Описание                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**\_ \_ метаданные конечной точки службы WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | Представляет элемент порта для конечной точки.                         |
| [**\_метаданные службы \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | Указывает массив документов метаданных службы.                       |
| [**\_ \_ документ МЕТАДАННЫХ службы \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | Указывает отдельные документы, составляющие метаданные службы. |



 

 

 




