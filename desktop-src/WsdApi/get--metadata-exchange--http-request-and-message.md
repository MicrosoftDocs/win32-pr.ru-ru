---
description: WS-Transfer сообщение, используемое для запроса метаданных.
ms.assetid: 18bf27aa-6ae5-4419-ae68-6df9eda10cd4
title: получение HTTP-запроса и сообщения об ошибке (метаданные Exchange)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994e02b990dc87cf8551e215bc7eae94dbcf7852
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632072"
---
# <a name="get-metadata-exchange-http-request-and-message"></a>получение HTTP-запроса и сообщения об ошибке (метаданные Exchange)

Сообщение Get — это WS-Transfer сообщение, используемое для запроса метаданных. Дополнительные сведения о получении сообщений см. в разделе 3,1 [спецификации WS-передач](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf). Так как обмен метаданными выполняется по протоколу HTTP, сообщение Get — это полезная нагрузка HTTP-запроса.

Клиенты DPWS отправляют сообщения Get. Клиенты обнаружения функций, клиенты WSDAPI, вызывающие [**всдкреатедевицепрокси**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)и WSDAPI клиенты, вызывающие [**всдкреатедевицепроксядванцед**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) отправить это сообщение.

> [!Note]  
> В этом разделе показан пример сообщения DPWS, созданного WSDAPI-клиентами и узлами. WSDAPI будет анализировать и принимать другие сообщения, соответствующие DPWS, которые не соответствуют этому примеру. Не используйте этот пример для проверки взаимодействия DPWS. Используйте вместо него [базовое средство взаимодействия WSDAPI (всдбит)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

В следующем примере показан пример HTTP-запроса GET.

``` syntax
POST /37f86d35-e6ac-4241-964f-1d9ae46fb366
HTTP/1.1
Content-Type: application/soap+xml
User-Agent: WSDAPI
Host: 192.168.0.2:5357
Content-Length: 658
Connection: Keep-Alive
Cache-Control: no-cache
Pragma: no-cache
```

Запрос HTTP GET имеет следующие фокусы.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>точка фокусировки;</th>
<th>Строка заголовка</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>путь_URL-адреса</td>
<td><pre class="syntax" data-space="preserve"><code>POST /37f86d35-e6ac-4241-964f-1d9ae46fb366</code></pre></td>
<td>URL-путь, по которому был отправлен запрос GET HTTP.</td>
</tr>
<tr class="even">
<td>Узел и порт</td>
<td><pre class="syntax" data-space="preserve"><code>Host: 192.168.0.2:5357</code></pre></td>
<td>Узел и порт, куда был направлен HTTP-запрос GET.</td>
</tr>
</tbody>
</table>



 

В следующем сообщении SOAP показан пример сообщения Get.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing">
<soap:Header>
    <wsa:To>
        urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:MessageID>
    <wsa:ReplyTo>
        <wsa:Address>
            https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        </wsa:Address>
    </wsa:ReplyTo>
    <wsa:From>
        <wsa:Address>
            urn:uuid:49e131df-351a-4ece-9a6f-6a862d31cffa
        </wsa:Address>
    </wsa:From>
</soap:Header>
<soap:Body>
</soap:Body>
```

Сообщение Get имеет следующие фокусы.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Кому</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:To>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:To></code></pre></td>
<td>Идентификатор устройства, запрашиваемого для метаданных.</td>
</tr>
<tr class="even">
<td>Получить</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
</wsa:Action</code></pre></td>
<td>Действие Get SOAP определяет сообщение как сообщение get.</td>
</tr>
<tr class="odd">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:MessageID></code></pre></td>
<td>Содержит идентификатор сообщения, на который имеется ссылка в сообщении <a href="getresponse--metadata-exchange--message.md">GetResponse</a> .</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[обнаружение и метаданные Exchange сообщения](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Сообщение с ответом](getresponse--metadata-exchange--message.md)
</dt> </dl>

 

 



