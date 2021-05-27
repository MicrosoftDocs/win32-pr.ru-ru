---
title: Инициализация постоянных объектов
description: Инициализация постоянных объектов
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549200"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="3c6a7-103">Инициализация постоянных объектов</span><span class="sxs-lookup"><span data-stu-id="3c6a7-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="3c6a7-104">Несколько постоянных интерфейсов объектов, [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [иперсистмемори](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))и [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), позволяют клиентам инициализировать объекты в состоянии "новое" или "по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="3c6a7-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="3c6a7-105">Это начальное состояние отличается от вновь созданного объекта, который не имеет состояния.</span><span class="sxs-lookup"><span data-stu-id="3c6a7-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="3c6a7-106">Инициализация состояния объекта даже до состояния по умолчанию может быть операцией ресурсоемких вычислений или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c6a7-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="3c6a7-107">Разделив создание на основе инициализации, инициализацию можно выполнить только в том случае, если она действительно необходима, и клиенты могут избежать инициализации объектов до состояния по умолчанию только для немедленной загрузки ранее сохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="3c6a7-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c6a7-108">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3c6a7-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c6a7-109">Постоянные интерфейсы объектов</span><span class="sxs-lookup"><span data-stu-id="3c6a7-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 