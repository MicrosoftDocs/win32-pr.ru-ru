---
description: Сообщение WS-Discovery, отправленное службой в ответ на сообщение проверки клиентов.
ms.assetid: 58d3d016-ae29-4090-9b88-e1125db59c95
title: Сообщение ProbeMatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813549091edc6cbb1202d746c7a7f62ecf3e03b5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882004"
---
# <a name="probematches-message"></a>Сообщение ProbeMatch

Сообщение ProbeMatch — это WS-Discovery сообщение, отправленное службой в ответ на сообщение [пробы](probe-message.md) клиента. Дополнительные сведения о сообщениях ProbeMatch см. в разделе 5,3 [спецификации WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Сообщение ProbeMatch отправляется по адресу UDP на порт, из которого было отправлено сообщение [пробы](probe-message.md) клиента. ProbeMatch должен отправляться в течение 4 секунд сообщения пробы; в противном случае Windows брандмауэр может удалить пакет.

Если в сообщение ProbeMatch не включены Ксаддрс, клиент может отправить сообщение с [разрешением](resolve-message.md) по многоадресной рассылке UDP на порт 3702. Клиент будет отправлять сообщение с разрешением, только когда будет отправлено HTTP-сообщение (например, запрос на [Получение](get--metadata-exchange--http-request-and-message.md) метаданных или сообщение службы).

Любое приложение DPWS, которое отправляет [пробные](probe-message.md) сообщения, получит сообщения ProbeMatch.

> [!Note]  
> В этом разделе показан пример сообщения DPWS, созданного WSDAPI-клиентами и узлами. WSDAPI будет анализировать и принимать другие сообщения, соответствующие DPWS, которые не соответствуют этому примеру. Не используйте этот пример для проверки взаимодействия DPWS. Используйте вместо него [базовое средство взаимодействия WSDAPI (всдбит)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

В следующем сообщении SOAP показан пример сообщения ProbeMatch.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:967d0036-fe69-40ad-8191-dd1fc8ef64ab
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="9">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ProbeMatches>
        <wsd:ProbeMatch>
            <wsa:EndpointReference>
                <wsa:Address>
                    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                </wsa:Address>
            </wsa:EndpointReference>
            <wsd:Types>wsdp:Device</wsd:Types>
            <wsd:XAddrs>
                https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsd:XAddrs>
            <wsd:MetadataVersion>2</wsd:MetadataVersion>
        </wsd:ProbeMatch>
    </wsd:ProbeMatches>
</soap:Body>
</soap:Envelope>
```

Сообщение ProbeMatch имеет следующие фокусы.



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
<td>ProbeMatch</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
&lt;/wsa:Action&gt;</code></pre></td>
<td>Действие SOAP ProbeMatch определяет сообщение как сообщение ProbeMatch.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:RelatesTo&gt;
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
&lt;/wsa:RelatesTo&gt;</code></pre></td>
<td>Идентификатор сообщения, на которое отвечает служба. Этот заголовок соответствует идентификатору MessageId в сообщении <a href="probe-message.md">пробы</a> .</td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;9&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>Содержит сведения о последовательности приложений, которые помогают поддерживать последовательность сообщений, даже если они получены не по порядку. AppSequence проверяется, как описано в <a href="appsequence-validation-rules.md">правилах проверки AppSequence</a>.</td>
</tr>
<tr class="even">
<td>Адрес</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>Содержит адрес конечной точки. На это обращение можно ссылаться в сообщении с <a href="resolve-message.md">разрешением</a> .</td>
</tr>
<tr class="odd">
<td>ксаддрс</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsd:XAddrs&gt;
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsd:XAddrs&gt;</code></pre></td>
<td>Ксаддрс — это транспортные адреса, которые могут использоваться для обмена данными между клиентом и службой. Адреса подтверждаются, как описано в <a href="xaddr-validation-rules.md">правилах проверки ксаддр</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[обнаружение и метаданные Exchange сообщения](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Сообщение пробы](probe-message.md)
</dt> </dl>

 

 



