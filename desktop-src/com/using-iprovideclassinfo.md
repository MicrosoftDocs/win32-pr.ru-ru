---
title: Использование IProvideClassInfo
description: Использование IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070693"
---
# <a name="using-iprovideclassinfo"></a>Использование IProvideClassInfo

Подключаемый объект может предложить интерфейсы [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) и [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) , чтобы клиенты могли легко исследовать сведения о типе. Эта возможность важна при работе с исходящими интерфейсами, которые, по определению, определяются объектом, но реализуются клиентом на собственном объекте приемника. В некоторых случаях исходящий интерфейс известен во время компиляции как для подключаемого объекта, так и для объекта приемника. Например, с [**ипропертинотифисинк**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).

Однако в других случаях только подключаемый объект знает определения исходящих интерфейсов во время компиляции. В таких случаях клиент должен получить сведения о типе для исходящего интерфейса, чтобы он мог динамически предоставлять приемник, поддерживающий правильные точки входа, следующим образом:

1.  Клиент перечисляет точки подключения, а затем для получения идентификаторов IID исходящих интерфейсов, поддерживаемых объектом, который можно подключить, вызывает метод [**IConnectionPoint:: жетконнектионинтерфаце**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) для каждой точки подключения.
2.  Клиент запрашивает доступ к подключаемому объекту для одного из интерфейсов [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .
3.  Клиент вызывает методы в интерфейсах [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) для получения сведений о типе для исходящего интерфейса.
4.  Клиент создает объект приемника, поддерживающий исходящий интерфейс.
5.  Процесс продолжится, и клиент вызывает метод [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) для подключения своего приемника к точке подключения.

В сведениях о типе [**источник**](/windows/desktop/Midl/source) атрибута помечает [**интерфейс**](/windows/desktop/Midl/interface) или [**DISP**](/windows/desktop/Midl/dispinterface) , указанный в [**компоненте coclass**](/windows/desktop/Midl/coclass) , как исходящий интерфейс. Указанные в списке без этого атрибута считаются входящими интерфейсами.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Подключаемые интерфейсы объектов](connectable-object-interfaces.md)
</dt> <dt>

[Предоставление сведений о классе](providing-class-information.md)
</dt> </dl>

 

 