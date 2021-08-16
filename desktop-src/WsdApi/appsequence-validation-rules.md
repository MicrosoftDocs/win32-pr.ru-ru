---
description: AppSequence сведения, содержащиеся в сообщениях WS-Discovery объявлений и ответах (Привет, ProbeMatch и Ресолвематчес).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Правила проверки AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f2acec9d9d3858b5d68b0240499d95dba059ac1bcac745f1dc69bebc2056a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738648"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[шаблоны сообщений обнаружения и метаданных Exchange](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



