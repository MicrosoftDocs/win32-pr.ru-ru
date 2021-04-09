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
# <a name="connectable-object-interfaces"></a><span data-ttu-id="f8269-103">Подключаемые интерфейсы объектов</span><span class="sxs-lookup"><span data-stu-id="f8269-103">Connectable Object Interfaces</span></span>

<span data-ttu-id="f8269-104">Для поддержки подключаемых объектов требуется поддержка четырех интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="f8269-104">Support for connectable objects requires support for four interfaces:</span></span>

-   <span data-ttu-id="f8269-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) для подключаемого объекта</span><span class="sxs-lookup"><span data-stu-id="f8269-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) on the connectable object</span></span>
-   <span data-ttu-id="f8269-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) в объекте точки подключения</span><span class="sxs-lookup"><span data-stu-id="f8269-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) on the connection point object</span></span>
-   <span data-ttu-id="f8269-107">[**Иенумконнектионпоинтс**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) для объекта Enumerator</span><span class="sxs-lookup"><span data-stu-id="f8269-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) on an enumerator object</span></span>
-   <span data-ttu-id="f8269-108">[**Иенумконнектионс**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) для объекта Enumerator</span><span class="sxs-lookup"><span data-stu-id="f8269-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) on an enumerator object</span></span>

<span data-ttu-id="f8269-109">Последние два определяются как стандартные перечислители для типов **IConnectionPoint \*** и [**коннектдата**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span><span class="sxs-lookup"><span data-stu-id="f8269-109">The latter two are defined as standard enumerators for the types **IConnectionPoint \*** and [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span></span>

<span data-ttu-id="f8269-110">Кроме того, подключаемый объект может дополнительно поддерживать интерфейс [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) и [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) , чтобы предоставить клиенту достаточно информации, чтобы клиент мог обеспечить поддержку исходящего интерфейса во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f8269-110">Additionally, the connectable object can optionally support [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) to provide enough information to a client so that the client can provide support for the outgoing interface at run time.</span></span>

<span data-ttu-id="f8269-111">Наконец, клиент должен предоставить объект приемника, реализующий исходящий интерфейс, который является настраиваемым COM-интерфейсом, определенным подключаемым объектом.</span><span class="sxs-lookup"><span data-stu-id="f8269-111">Finally, the client must provide a sink object that implements the outgoing interface, which is a custom COM interface defined by the connectable object.</span></span>

<span data-ttu-id="f8269-112">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="f8269-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f8269-113">Использование IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="f8269-113">Using IConnectionPointContainer</span></span>](using-iconnectionpointcontainer.md)
-   [<span data-ttu-id="f8269-114">Использование IConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="f8269-114">Using IConnectionPoint</span></span>](using-iconnectionpoint.md)
-   [<span data-ttu-id="f8269-115">Использование IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="f8269-115">Using IProvideClassInfo</span></span>](using-iprovideclassinfo.md)

## <a name="related-topics"></a><span data-ttu-id="f8269-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f8269-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8269-117">Архитектура подключаемых объектов</span><span class="sxs-lookup"><span data-stu-id="f8269-117">Architecture of Connectable Objects</span></span>](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




