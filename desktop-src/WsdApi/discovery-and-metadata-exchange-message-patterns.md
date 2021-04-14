---
description: Профиль устройства для узлов и клиентов веб-служб (DPWS) взаимодействует по сети, используя серию сообщений SOAP по протоколам UDP и HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Шаблоны сообщений обнаружения и обмена метаданными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104273216"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>Шаблоны сообщений обнаружения и обмена метаданными

Профиль устройства для узлов и клиентов веб-служб (DPWS) взаимодействует по сети, используя серию сообщений SOAP по протоколам UDP и HTTP.

На следующей диаграмме представлен обзор ожидаемого трафика UDP и HTTP между узлом DPWS и клиентом.

![Схема трафика UDP и HTTP между узлом DPWS и клиентом.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

Сообщения [Hello](hello-message.md), [Bye](bye-message.md), [зонд](probe-message.md), [Resolve](resolve-message.md)и [Get](get--metadata-exchange--http-request-and-message.md) создаются без запроса сети. Эти сообщения используются для объявления состояния устройства или для выдаче запроса на поиск. Сообщения [ProbeMatch](probematches-message.md), [ресолвематчес](resolvematches-message.md)и [GetResponse](getresponse--metadata-exchange--message.md) создаются в ответ на проверку, разрешение и получение сообщений.

Сообщения [Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md)и [ресолвематчес](resolvematches-message.md) всегда будут выполняться по протоколу UDP. Аналогичным образом, сообщения метаданных [Get](get--metadata-exchange--http-request-and-message.md) и [GetResponse](getresponse--metadata-exchange--message.md) всегда будут выполняться по протоколам HTTP или HTTPS. Сообщения [проверки](probe-message.md) и [ProbeMatch](probematches-message.md) обычно передаются по протоколу UDP, но выполняются по протоколу HTTP или HTTPS в сценарии направленного обнаружения. Дополнительные сведения о направленных шаблонах сообщений обнаружения см. в разделе [Устранение неполадок приложений с помощью](troubleshooting-applications-using-directed-discovery.md)управляемого обнаружения.

В следующем списке показана типичная последовательность сообщений, отправляемых по сети. Не все сообщения являются обязательными.

1.  [Привет](hello-message.md)
2.  [Проба](probe-message.md)
3.  [ProbeMatch](probematches-message.md)
4.  [Разрешить](resolve-message.md)
5.  [ресолвематчес](resolvematches-message.md)
6.  [Get](get--metadata-exchange--http-request-and-message.md) (запрос на обмен метаданными)
7.  [GetResponse](getresponse--metadata-exchange--message.md)
8.  [Пока](bye-message.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[О веб-службах на устройствах](about-web-services-for-devices.md)
</dt> </dl>

 

 



