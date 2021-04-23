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
# <a name="using-iprovideclassinfo"></a><span data-ttu-id="d8515-103">Использование IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="d8515-103">Using IProvideClassInfo</span></span>

<span data-ttu-id="d8515-104">Подключаемый объект может предложить интерфейсы [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) и [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) , чтобы клиенты могли легко исследовать сведения о типе.</span><span class="sxs-lookup"><span data-stu-id="d8515-104">A connectable object can offer the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) interfaces so that its clients can easily examine its type information.</span></span> <span data-ttu-id="d8515-105">Эта возможность важна при работе с исходящими интерфейсами, которые, по определению, определяются объектом, но реализуются клиентом на собственном объекте приемника.</span><span class="sxs-lookup"><span data-stu-id="d8515-105">This capability is important when dealing with outgoing interfaces, which, by definition, are defined by an object but implemented by a client on its own sink object.</span></span> <span data-ttu-id="d8515-106">В некоторых случаях исходящий интерфейс известен во время компиляции как для подключаемого объекта, так и для объекта приемника. Например, с [**ипропертинотифисинк**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span><span class="sxs-lookup"><span data-stu-id="d8515-106">In some cases, an outgoing interface is known at compile time to both the connectable object and the sink object; such is the case with [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span></span>

<span data-ttu-id="d8515-107">Однако в других случаях только подключаемый объект знает определения исходящих интерфейсов во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="d8515-107">In other cases, however, only the connectable object knows its outgoing interface definitions at compile time.</span></span> <span data-ttu-id="d8515-108">В таких случаях клиент должен получить сведения о типе для исходящего интерфейса, чтобы он мог динамически предоставлять приемник, поддерживающий правильные точки входа, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d8515-108">In these cases, the client must obtain the type information for the outgoing interface so that it can dynamically provide a sink supporting the right entry points, as follows:</span></span>

1.  <span data-ttu-id="d8515-109">Клиент перечисляет точки подключения, а затем для получения идентификаторов IID исходящих интерфейсов, поддерживаемых объектом, который можно подключить, вызывает метод [**IConnectionPoint:: жетконнектионинтерфаце**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) для каждой точки подключения.</span><span class="sxs-lookup"><span data-stu-id="d8515-109">The client enumerates the connection points and then, to obtain the IIDs of outgoing interfaces supported by the connectable object, calls [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) for each connection point.</span></span>
2.  <span data-ttu-id="d8515-110">Клиент запрашивает доступ к подключаемому объекту для одного из интерфейсов [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .</span><span class="sxs-lookup"><span data-stu-id="d8515-110">The client queries the connectable object for one of the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces.</span></span>
3.  <span data-ttu-id="d8515-111">Клиент вызывает методы в интерфейсах [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) для получения сведений о типе для исходящего интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d8515-111">The client calls methods in the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces to get the type information for the outgoing interface.</span></span>
4.  <span data-ttu-id="d8515-112">Клиент создает объект приемника, поддерживающий исходящий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d8515-112">The client creates a sink object supporting the outgoing interface.</span></span>
5.  <span data-ttu-id="d8515-113">Процесс продолжится, и клиент вызывает метод [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) для подключения своего приемника к точке подключения.</span><span class="sxs-lookup"><span data-stu-id="d8515-113">The process continues, and the client calls [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) to connect its sink to the connection point.</span></span>

<span data-ttu-id="d8515-114">В сведениях о типе [**источник**](/windows/desktop/Midl/source) атрибута помечает [**интерфейс**](/windows/desktop/Midl/interface) или [**DISP**](/windows/desktop/Midl/dispinterface) , указанный в [**компоненте coclass**](/windows/desktop/Midl/coclass) , как исходящий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d8515-114">In the type information, the attribute [**source**](/windows/desktop/Midl/source) marks an [**interface**](/windows/desktop/Midl/interface) or [**dispinterface**](/windows/desktop/Midl/dispinterface) listed under a [**coclass**](/windows/desktop/Midl/coclass) as an outgoing interface.</span></span> <span data-ttu-id="d8515-115">Указанные в списке без этого атрибута считаются входящими интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="d8515-115">Those listed without this attribute are considered incoming interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8515-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d8515-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8515-117">Подключаемые интерфейсы объектов</span><span class="sxs-lookup"><span data-stu-id="d8515-117">Connectable Object Interfaces</span></span>](connectable-object-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d8515-118">Предоставление сведений о классе</span><span class="sxs-lookup"><span data-stu-id="d8515-118">Providing Class Information</span></span>](providing-class-information.md)
</dt> </dl>

 

 