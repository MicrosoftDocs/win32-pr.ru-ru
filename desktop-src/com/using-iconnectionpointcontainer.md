---
title: Использование IConnectionPointContainer
description: Использование IConnectionPointContainer
ms.assetid: a87afb25-4d45-4ce2-9b27-840da5107bce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a8d53e9051796cafa4a8c7825d810b18784d58a4dd5d531eb38872b87cb32c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992034"
---
# <a name="using-iconnectionpointcontainer"></a>Использование IConnectionPointContainer

Подключаемый объект реализует [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (и предоставляет его через [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) для указания существования исходящих интерфейсов. Для каждого исходящего интерфейса объект, который подсоединяется, управляет подобъектом точки соединения, который сам реализует [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint). Таким образом, подключаемый объект содержит точки подключения, поэтому именование **IConnectionPointContainer** и **IConnectionPoint**.

С помощью [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer)клиент может выполнять две операции. Во первых, если у клиента уже есть IID для исходящего интерфейса, который он поддерживает, он может разместить соответствующую точку соединения для IID с помощью [**IConnectionPointContainer:: финдконнектионпоинт**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint). Клиент не может запросить точку соединения напрямую из-за наличия контейнера или вложенной связи между подключаемым объектом и содержащимися в нем точками соединения. По сути, **финдконнектионпоинт** — это [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) для исходящих ИНТЕРФЕЙСОВ, когда идентификатор IID известен клиенту.

Во-вторых, клиент может перечислить все точки подключения в объекте, доступном для подключения, с помощью [**IConnectionPointContainer:: енумконнектионпоинтс**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Этот метод возвращает указатель интерфейса [**иенумконнектионпоинтс**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) для отдельного объекта перечислителя. С помощью [**иенумконнектионпоинтс:: Next**](/windows/desktop/api/ocidl/nf-ocidl-ienumconnectionpoints-next)клиент может получить указатели интерфейса [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) на каждую точку подключения.

После того как клиент получит интерфейс [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) , он должен вызвать метод [**IConnectionPoint:: жетконнектионинтерфаце**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) , чтобы определить IID исходящего интерфейса, поддерживаемого каждой точкой подключения. Если клиент уже поддерживает этот исходящий интерфейс, он может установить соединение. В противном случае он по-прежнему может поддерживать исходящий интерфейс, используя сведения из библиотеки типов подключаемого объекта, чтобы обеспечить поддержку во время выполнения. Для этого метода требуется, чтобы подключаемый объект поддерживал интерфейс [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) . (См. раздел [Использование IProvideClassInfo](using-iprovideclassinfo.md).)

Поскольку перечислитель является отдельным объектом, клиент должен вызвать **иенумконнектионпоинтс:: Release** , если перечислитель больше не нужен. Кроме того, каждая точка соединения является объектом с отдельным числом ссылок из содержащего объекта, доступного для соединения. Таким образом, клиент должен также вызвать метод IConnectionPoint:: Release для каждой точки подключения, доступ к которой осуществляется через перечислитель или через [**финдконнектионпоинт**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Подключаемые интерфейсы объектов](connectable-object-interfaces.md)
</dt> </dl>

 

 




