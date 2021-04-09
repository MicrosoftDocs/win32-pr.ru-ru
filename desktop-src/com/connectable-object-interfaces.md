---
title: Подключаемые интерфейсы объектов
description: Подключаемые интерфейсы объектов
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889144"
---
# <a name="connectable-object-interfaces"></a>Подключаемые интерфейсы объектов

Для поддержки подключаемых объектов требуется поддержка четырех интерфейсов:

-   [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) для подключаемого объекта
-   [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) в объекте точки подключения
-   [**Иенумконнектионпоинтс**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) для объекта Enumerator
-   [**Иенумконнектионс**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) для объекта Enumerator

Последние два определяются как стандартные перечислители для типов **IConnectionPoint \*** и [**коннектдата**](/windows/win32/api/ocidl/ns-ocidl-connectdata).

Кроме того, подключаемый объект может дополнительно поддерживать интерфейс [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) и [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) , чтобы предоставить клиенту достаточно информации, чтобы клиент мог обеспечить поддержку исходящего интерфейса во время выполнения.

Наконец, клиент должен предоставить объект приемника, реализующий исходящий интерфейс, который является настраиваемым COM-интерфейсом, определенным подключаемым объектом.

Дополнительные сведения см. в следующих разделах:

-   [Использование IConnectionPointContainer](using-iconnectionpointcontainer.md)
-   [Использование IConnectionPoint](using-iconnectionpoint.md)
-   [Использование IProvideClassInfo](using-iprovideclassinfo.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Архитектура подключаемых объектов](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




