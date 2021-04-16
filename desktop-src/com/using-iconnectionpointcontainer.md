---
title: Использование IConnectionPointContainer
description: Использование IConnectionPointContainer
ms.assetid: a87afb25-4d45-4ce2-9b27-840da5107bce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d0b7c691e1ba6a8445af56978b43a2ccbf33e7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "105710227"
---
# <a name="using-iconnectionpointcontainer"></a>Использование IConnectionPointContainer

Подключаемый объект реализует [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (и предоставляет его через [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) для указания существования исходящих интерфейсов. Для каждого исходящего интерфейса объект, который подсоединяется, управляет подобъектом точки соединения, который сам реализует [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint). Таким образом, подключаемый объект содержит точки подключения, поэтому именование **IConnectionPointContainer** и **IConnectionPoint**.

С помощью [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer)клиент может выполнять две операции. Во первых, если у клиента уже есть IID для исходящего интерфейса, который он поддерживает, он может разместить соответствующую точку соединения для IID с помощью [**IConnectionPointContainer:: финдконнектионпоинт**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint). Клиент не может запросить точку соединения напрямую из-за наличия контейнера или вложенной связи между подключаемым объектом и содержащимися в нем точками соединения. По сути, **финдконнектионпоинт** — это [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) для исходящих ИНТЕРФЕЙСОВ, когда идентификатор IID известен клиенту.

Во-вторых, клиент может перечислить все точки подключения в объекте, доступном для подключения, с помощью [**IConnectionPointContainer:: енумконнектионпоинтс**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Этот метод возвращает указатель интерфейса [**иенумконнектионпоинтс**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) для отдельного объекта перечислителя. С помощью [**иенумконнектионпоинтс:: Next**](/windows/desktop/api/ocidl/nf-ocidl-ienumconnectionpoints-next)клиент может получить указатели интерфейса [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) на каждую точку подключения.

После того как клиент получит интерфейс [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) , он должен вызвать метод [**IConnectionPoint:: жетконнектионинтерфаце**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) , чтобы определить IID исходящего интерфейса, поддерживаемого каждой точкой подключения. Если клиент уже поддерживает этот исходящий интерфейс, он может установить соединение. В противном случае он по-прежнему может поддерживать исходящий интерфейс, используя сведения из библиотеки типов подключаемого объекта, чтобы обеспечить поддержку во время выполнения. Для этого метода требуется, чтобы подключаемый объект поддерживал интерфейс [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) . (См. раздел [Использование IProvideClassInfo](using-iprovideclassinfo.md).)

Поскольку перечислитель является отдельным объектом, клиент должен вызвать **иенумконнектионпоинтс:: Release** , если перечислитель больше не нужен. Кроме того, каждая точка соединения является объектом с отдельным числом ссылок из содержащего объекта, доступного для соединения. Таким образом, клиент должен также вызвать метод IConnectionPoint:: Release для каждой точки подключения, доступ к которой осуществляется через перечислитель или через [**финдконнектионпоинт**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Подключаемые интерфейсы объектов](connectable-object-interfaces.md)
</dt> </dl>

 

 




