---
description: WS-Discovery сообщение, используемое для объявления о присутствии устройства или службы в сети.
ms.assetid: a7402e02-9bdc-49ec-ba93-8a32f55b9dd8
title: Сообщение Hello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3fe850c4df51fba75c33e202a0bd742226cfb38
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882564"
---
# <a name="hello-message"></a>Сообщение Hello

Сообщение Hello — это WS-Discovery сообщение, используемое для объявления о присутствии устройства или службы в сети. Сообщения Hello также отправляются в других сценариях. Дополнительные сведения о сообщениях Hello см. в разделе 4,1 [спецификации WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Многоадресная рассылка UDP отправляет сообщение Hello на порт 3702. Это сообщение не запрошено.

> [!Note]  
> В этом разделе показан пример сообщения DPWS, созданного WSDAPI-клиентами и узлами. WSDAPI будет анализировать и принимать другие сообщения, соответствующие DPWS, которые не соответствуют этому примеру. Не используйте этот пример для проверки взаимодействия DPWS. Используйте вместо него [базовое средство взаимодействия WSDAPI (всдбит)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

В следующем сообщении SOAP отображается пример сообщения Hello.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        urn:schemas-xmlsoap-org:ws:2005:04:discovery
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:0f5d604c-81ac-4abc-8010-51dbffad55f2
    </wsa:MessageID>
    <wsd:AppSequence InstanceId="2"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="14">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:Hello>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
        <wsd:Types>wsdp:Device</wsd:Types>
        <wsd:MetadataVersion>2</wsd:MetadataVersion>
    </wsd:Hello>
</soap:Body>
```

Сообщение Hello имеет следующие фокусы.



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
<td>Привет</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
&lt;/wsa:Action&gt;</code></pre></td>
<td>Действие Hello SOAP идентифицирует сообщение как сообщение Hello.</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;14&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>Содержит сведения о последовательности приложений, которые помогают поддерживать последовательность сообщений, даже если они получены не по порядку. AppSequence проверяется, как описано в <a href="appsequence-validation-rules.md">правилах проверки AppSequence</a>.</td>
</tr>
<tr class="odd">
<td>Адрес</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>Содержит адрес конечной точки. На это обращение можно ссылаться в сообщении с <a href="resolve-message.md">разрешением</a> .</td>
</tr>
<tr class="even">
<td>Типы</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsd:Types&gt;wsdp:Device</wsd:Types></code></pre></td>
<td>Содержит типы WS-Discovery, объявленные узлом.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[обнаружение и метаданные Exchange сообщения](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Сообщение Bye](bye-message.md)
</dt> </dl>

 

 



