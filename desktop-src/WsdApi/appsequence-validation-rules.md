---
description: AppSequence сведения, содержащиеся в сообщениях WS-Discovery объявлений и ответах (Привет, ProbeMatch и Ресолвематчес).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Правила проверки AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544815"
---
# <a name="appsequence-validation-rules"></a>Правила проверки AppSequence

AppSequence сведения, содержащиеся в сообщениях WS-Discovery объявлений и ответах ([Привет](hello-message.md), [ProbeMatch](probematches-message.md)и [ресолвематчес](resolvematches-message.md)). Эти сведения обрабатываются и проверяются WSDAPI, прежде чем эти сообщения передаются в компоненты выше стека (например, сетевой обозреватель или приложение, вызывающее в WSDAPI).

В следующем коде XML показан пример элемента AppSequence. Префикс WSD ссылается на пространство имен `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

WSDAPI игнорирует устаревшие сообщения. Для каждого устройства (уникально идентифицируемого адресом конечной точки в теле SOAP) протокол WSDAPI игнорирует все сообщения с AppSequence MessageNumber ниже последнего отображаемого сообщения.

WSDAPI игнорирует устаревшие объявления Ксаддр. Если значение InstanceId AppSequence меньше, чем последний замеченный InstanceId, то WSDAPI игнорирует Ксаддрс, объявленный в теле SOAP. Кроме того, если InstanceId совпадает с предыдущим, но Метадатаверсион меньше, чем последний Метадатаверсион, то WSDAPI игнорирует Ксаддрс.

WSDAPI игнорирует дублирующиеся WS-Discovery сообщения. Если в WSDAPI отправляется два одинаковых WS-Discovery сообщений, то обрабатываются только первые полученные. Обычно это относится только к приложениям, которые напрямую вызывают интерфейсы [**ивсдисковерипублишер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) или [**ивсдисковерипровидер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Шаблоны сообщений обнаружения и обмена метаданными](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



