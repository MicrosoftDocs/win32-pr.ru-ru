---
description: Сообщение WS-Discovery, отправляемое в ответ на клиенты, разрешают сообщение с помощью соответствующей службы.
ms.assetid: 0eaa4348-968e-4b45-9509-8b15476edaa1
title: Сообщение Ресолвематчес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140d279a5e66835b7754e3f501732263dff430f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883639"
---
# <a name="resolvematches-message"></a>Сообщение Ресолвематчес

Сообщение Ресолвематчес — это WS-Discovery сообщение, отправленное в ответ на сообщение [разрешения](resolve-message.md) клиента соответствующей службой. Дополнительные сведения о сообщениях Ресолвематчес см. в разделе 6,2 [спецификации WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Сообщение Ресолвематчес отправляется по адресу UDP через порт 3702 (порт, из которого было отправлено сообщение [разрешения](resolve-message.md) клиента). Ресолвематчес должен быть отправлен в течение 4 секунд из сообщения разрешения; в противном случае Windows брандмауэр может удалить пакет.

Любое приложение DPWS, отправляющее сообщения с [разрешением](resolve-message.md) , получит сообщения ресолвематчес.

> [!Note]  
> В этом разделе показан пример сообщения DPWS, созданного WSDAPI-клиентами и узлами. WSDAPI будет анализировать и принимать другие сообщения, соответствующие DPWS, которые не соответствуют этому примеру. Не используйте этот пример для проверки взаимодействия DPWS. Используйте вместо него [базовое средство взаимодействия WSDAPI (всдбит)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

В следующем сообщении SOAP показан пример сообщения Ресолвематчес.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:64ddd01c-b0d6-4afd-aba6-6f1f161ce9d4
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="6">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ResolveMatches>
        <wsd:ResolveMatch>
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
        </wsd:ResolveMatch>
    </wsd:ResolveMatches>
</soap:Body>
</soap:Envelope>
```

Сообщение Ресолвематчес имеет следующие фокусы.



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
<td>ресолвематчес</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
&lt;/wsa:Action&gt;</code></pre></td>
<td>Действие SOAP Ресолвематчес определяет сообщение как сообщение Ресолвематчес.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:RelatesTo&gt;
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
&lt;/wsa:RelatesTo&gt;</code></pre></td>
<td>Идентификатор сообщения, на которое отвечает служба. Этот заголовок соответствует идентификатору MessageId в сообщении <a href="resolve-message.md">разрешения</a> .</td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;6&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>Содержит сведения о последовательности приложений, которые помогают поддерживать последовательность сообщений, даже если они получены не по порядку. AppSequence проверяется, как описано в <a href="appsequence-validation-rules.md">правилах проверки AppSequence</a>.</td>
</tr>
<tr class="even">
<td>Адрес</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>Содержит адрес разрешенной конечной точки.</td>
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

[Разрешить сообщение](resolve-message.md)
</dt> </dl>

 

 



