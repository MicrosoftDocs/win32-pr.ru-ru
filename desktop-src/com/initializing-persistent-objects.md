---
title: Инициализация постоянных объектов
description: Инициализация постоянных объектов
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211d9d89b7a8f36ab06d9930e45f365e0fb5d4dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413817"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="b6944-103">Инициализация постоянных объектов</span><span class="sxs-lookup"><span data-stu-id="b6944-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="b6944-104">Несколько постоянных интерфейсов объектов, [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [иперсистмемори](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))и [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), позволяют клиентам инициализировать объекты в состоянии "новое" или "по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="b6944-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="b6944-105">Это начальное состояние отличается от вновь созданного объекта, который не имеет состояния.</span><span class="sxs-lookup"><span data-stu-id="b6944-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="b6944-106">Инициализация состояния объекта даже до состояния по умолчанию может быть операцией ресурсоемких вычислений или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6944-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="b6944-107">Разделив создание на основе инициализации, инициализацию можно выполнить только в том случае, если она действительно необходима, и клиенты могут избежать инициализации объектов до состояния по умолчанию только для немедленной загрузки ранее сохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="b6944-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6944-108">См. также</span><span class="sxs-lookup"><span data-stu-id="b6944-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6944-109">Постоянные интерфейсы объектов</span><span class="sxs-lookup"><span data-stu-id="b6944-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 