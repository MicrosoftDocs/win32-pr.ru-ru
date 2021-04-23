---
title: Сдвоенные интерфейсы (COM)
description: Сдвоенные интерфейсы
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070732"
---
# <a name="dual-interfaces"></a><span data-ttu-id="66287-103">Сдвоенные интерфейсы</span><span class="sxs-lookup"><span data-stu-id="66287-103">Dual Interfaces</span></span>

<span data-ttu-id="66287-104">OLE-автоматизация позволяет объекту предоставлять набор методов двумя способами: через интерфейс **IDispatch** и через прямую привязку OLE vtable.</span><span class="sxs-lookup"><span data-stu-id="66287-104">OLE Automation enables an object to expose a set of methods in two ways: via the **IDispatch** interface, and through direct OLE VTable binding.</span></span> <span data-ttu-id="66287-105">Интерфейс **IDispatch** используется большинством доступных в настоящее время средств и обеспечивает поддержку позднего связывания с свойствами и методами.</span><span class="sxs-lookup"><span data-stu-id="66287-105">**IDispatch** is used by most tools available today, and offers support for late binding to properties and methods.</span></span>

<span data-ttu-id="66287-106">Привязка VTable обеспечивает более высокую производительность, так как этот метод вызывается напрямую, а не через **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="66287-106">VTable binding offers much higher performance because this method is called directly instead of through **IDispatch::Invoke**.</span></span> <span data-ttu-id="66287-107">**IDispatch** обеспечивает поддержку поздних границ, где прямая привязка vtable обеспечивает значительное увеличение производительности. Оба метода полезны и важны в различных сценариях.</span><span class="sxs-lookup"><span data-stu-id="66287-107">**IDispatch** offers late bound support, where direct VTable binding offers a significant performance gain; both techniques are valuable and important in different scenarios.</span></span> <span data-ttu-id="66287-108">Если пометить интерфейс как \[ [**сдвоенный**](/windows/desktop/Midl/dual) \] в библиотеке типов, то интерфейс OLE Automation можно использовать либо через **IDispatch**, либо с прямым связыванием.</span><span class="sxs-lookup"><span data-stu-id="66287-108">By labeling an interface as \[[**dual**](/windows/desktop/Midl/dual)\] in the type library, an OLE Automation interface can be used either via **IDispatch**, or it can be bound to directly.</span></span> <span data-ttu-id="66287-109">Таким образом, контейнеры могут выбирать наиболее подходящий способ.</span><span class="sxs-lookup"><span data-stu-id="66287-109">Containers can thus choose the most appropriate technique.</span></span> <span data-ttu-id="66287-110">Для элементов управления и контейнеров настоятельно рекомендуется поддержка сдвоенных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="66287-110">Support for dual interfaces is strongly recommended for both controls and containers.</span></span>

 

 