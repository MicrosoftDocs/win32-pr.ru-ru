---
title: Свойства и методы навигации по объектам
description: Клиенты переходят от одного объекта к другому с помощью таких методов, как IAccessible Аккнавигате и IAccessible Акчиттест.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986373"
---
# <a name="object-navigation-properties-and-methods"></a><span data-ttu-id="de916-103">Свойства и методы навигации по объектам</span><span class="sxs-lookup"><span data-stu-id="de916-103">Object Navigation Properties and Methods</span></span>

<span data-ttu-id="de916-104">Клиенты *переходят* от одного объекта к другому с помощью таких методов, как [**IAccessible:: аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) и [**IAccessible:: акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span><span class="sxs-lookup"><span data-stu-id="de916-104">Clients *navigate* from one object to another using methods such as [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span></span> <span data-ttu-id="de916-105">Эти методы позволяют клиентам извлекать либо дочерний идентификатор, либо адрес интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) другого объекта.</span><span class="sxs-lookup"><span data-stu-id="de916-105">These methods allow clients to retrieve either a child ID or the address of another object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="de916-106">Навигация позволяет клиентам исследовать взаимосвязь между объектами.</span><span class="sxs-lookup"><span data-stu-id="de916-106">Navigation allows clients to explore how objects are related to each other.</span></span> <span data-ttu-id="de916-107">Обратите внимание, что переход к другому объекту не изменяет выделенный фрагмент или фокус.</span><span class="sxs-lookup"><span data-stu-id="de916-107">Note that navigating to another object does not change the selection or focus.</span></span>

<span data-ttu-id="de916-108">Интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) предоставляет свойства и методы, поддерживающие следующие виды навигации:</span><span class="sxs-lookup"><span data-stu-id="de916-108">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides properties and methods that support the following kinds of navigation:</span></span>

-   [<span data-ttu-id="de916-109">Иерархическая навигация</span><span class="sxs-lookup"><span data-stu-id="de916-109">Hierarchical Navigation</span></span>](hierarchical-navigation.md)
-   [<span data-ttu-id="de916-110">Пространственное и логическое перемещение</span><span class="sxs-lookup"><span data-stu-id="de916-110">Spatial and Logical Navigation</span></span>](spatial-and-logical-navigation.md)
-   [<span data-ttu-id="de916-111">Навигация с помощью проверки попадания и расположения на экране</span><span class="sxs-lookup"><span data-stu-id="de916-111">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)

 

 




