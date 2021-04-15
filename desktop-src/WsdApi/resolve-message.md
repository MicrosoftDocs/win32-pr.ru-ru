---
description: WS-Discovery сообщение, используемое клиентом для поиска служб в сети по имени.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Разрешить сообщение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3390d97aad972f001b98587c6b5e7cd7ac708b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702039"
---
# <a name="resolve-message"></a>Разрешить сообщение

Сообщение с разрешением — это WS-Discovery сообщение, используемое клиентом для поиска служб в сети по имени. Клиент будет отправлять сообщение с разрешением, только когда будет отправлено HTTP-сообщение (например, запрос на [Получение](get--metadata-exchange--http-request-and-message.md) метаданных или сообщение службы). Дополнительные сведения о разрешении сообщений см. в разделе 6,1 [спецификации WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Сообщение с разрешением отправляется многоадресной передачей UDP на порт 3702. Одноадресные сообщения разрешения не поддерживаются.

Клиенты DPWS отправляют сообщения разрешения. В следующем списке приведены сценарии, в которых WSDAPI отправляет сообщение с разрешением.

-   Клиент обнаружения функции отправляет сообщение разрешения, если в сообщение [ProbeMatch](probematches-message.md) не включены ксаддрс.
-   Клиент, вызывающий методы [**ивсдисковерипровидер:: сеарчбид**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) , отправит сообщение с разрешением.
-   Клиент, вызывающий [**всдкреатедевицепрокси**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) , может отправить сообщение разрешения, если адрес логического устройства передается в *псздевицеид*.
-   Клиент, вызывающий [**всдкреатедевицепроксядванцед**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) , отправит сообщение с разрешением, если функция вызывается с параметром пдевицеаддресс, установленным в **значение NULL**.

> [!Note]  
> В этом разделе показан пример сообщения DPWS, созданного WSDAPI-клиентами и узлами. WSDAPI будет анализировать и принимать другие сообщения, соответствующие DPWS, которые не соответствуют этому примеру. Не используйте этот пример для проверки взаимодействия DPWS. Используйте вместо него [базовое средство взаимодействия WSDAPI (всдбит)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

В следующем сообщении SOAP показан пример сообщения о разрешении.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery">
<soap:Header>
    <wsa:To>
urn:schemas-xmlsoap-org:ws:2005:04:discovery
</wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Resolve>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Resolve>
</soap:Body>
</soap:Envelope>
```

Сообщение с разрешением имеет следующие фокусы.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>точка фокусировки;</th>
<th>XML</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Разрешить</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td>Действие "разрешить SOAP" определяет сообщение как сообщение для разрешения.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>Содержит идентификатор сообщения, на который ссылается сообщение <a href="resolvematches-message.md">ресолвематчес</a> .</td>
</tr>
<tr class="odd">
<td>Адрес</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Содержит адрес разрешенной конечной точки.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сообщения обнаружения и обмена метаданными](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Сообщение Ресолвематчес](resolvematches-message.md)
</dt> </dl>

 

 



