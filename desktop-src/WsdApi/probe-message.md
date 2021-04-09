---
description: WS-Discovery сообщение, используемое клиентом для поиска служб в сети по типу службы.
ms.assetid: a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7
title: Сообщение пробы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913c163be8d82297a642b1a97a7d28e0c403ca08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155982"
---
# <a name="probe-message"></a>Сообщение пробы

Сообщение пробы — это WS-Discovery сообщение, используемое клиентом для поиска служб в сети по типу службы. Дополнительные сведения о сообщениях пробы см. в разделе 5,2 [спецификации WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Сообщение пробы отправляется многоадресной передачей UDP на порт 3702. Сообщения пробы одноадресной проверки не поддерживаются.

Клиенты DPWS отправляют пробные сообщения. В следующем списке приведены сценарии, в которых WSDAPI будет отсылать сообщение пробы.

-   Клиенты обнаружения функций отправляют проверочные сообщения.
-   Клиенты WSDAPI, вызывающие [**ивсдисковерипровидер:: сеарчбяддресс**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress) , отправляют пробные сообщения.
-   Клиенты WSDAPI, вызывающие [**ивсдисковерипровидер:: сеарчбитипе**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) , отправляют пробные сообщения.
-   Приложения, использующие направленное обнаружение, отправляют сообщения проверки по протоколу HTTP или HTTPS.

> [!Note]  
> В этом разделе показан пример сообщения DPWS, созданного WSDAPI-клиентами и узлами. WSDAPI будет анализировать и принимать другие сообщения, соответствующие DPWS, которые не соответствуют этому примеру. Не используйте этот пример для проверки взаимодействия DPWS. Используйте вместо него [базовое средство взаимодействия WSDAPI (всдбит)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

В следующем сообщении SOAP показан образец сообщения пробы.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Probe>
        <wsd:Types>wsdp:Device</wsd:Types>
    </wsd:Probe>
</soap:Body>
```

Сообщение пробы имеет следующие фокусы.



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
<td>Проба</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
</wsa:Action></code></pre></td>
<td>Действие проверки SOAP определяет сообщение как сообщение пробы.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
</wsa:MessageID></code></pre></td>
<td>Содержит идентификатор сообщения, на который ссылается элемент «текст сообщения об ошибке» в сообщении <a href="probematches-message.md">ProbeMatch</a> .</td>
</tr>
<tr class="odd">
<td>Типы</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:Types>wsdp:Device</wsd:Types></code></pre></td>
<td>Содержит типы WS-Discovery, для которых клиент выполняет поиск. Этот элемент не должен быть пустым.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сообщения обнаружения и обмена метаданными](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Сообщение ProbeMatch](probematches-message.md)
</dt> </dl>

 

 



