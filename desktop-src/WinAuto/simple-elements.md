---
title: Простые элементы
description: Простой элемент — это элемент пользовательского интерфейса, который использует объект IAccessible совместно с другими элементами и зависит от этого объекта IAccessible (как правило, его родителя) для предоставления его свойств.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691364"
---
# <a name="simple-elements"></a><span data-ttu-id="c9f8f-103">Простые элементы</span><span class="sxs-lookup"><span data-stu-id="c9f8f-103">Simple Elements</span></span>

<span data-ttu-id="c9f8f-104">*Простой элемент* — это элемент пользовательского интерфейса, который использует объект [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) совместно с другими элементами и зависит от этого объекта **IAccessible** (как правило, его родителя) для предоставления его свойств.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-104">A *simple element* is a UI element that shares an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with other elements and relies on that **IAccessible** object (typically its parent) to expose its properties.</span></span> <span data-ttu-id="c9f8f-105">Для различения элементов, совместно использующих объект **IAccessible** , сервер присваивает каждому простому элементу уникальный, положительный дочерний идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-105">To differentiate between the elements sharing an **IAccessible** object, the server assigns a unique, positive child identifier to each simple element.</span></span> <span data-ttu-id="c9f8f-106">Это назначение выполняется отдельно для каждого экземпляра интерфейса, поэтому идентификаторы должны быть уникальными в пределах этого контекста.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-106">This assignment is done on a per-instance-of-interface basis, so the IDs must be unique within that context.</span></span> <span data-ttu-id="c9f8f-107">Многие реализации присваивают эти идентификаторы последовательно, начиная с 1.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-107">Many implementations assign these IDs sequentially, beginning with 1.</span></span> <span data-ttu-id="c9f8f-108">Эта схема не позволяет простым элементам иметь собственные дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-108">This scheme does not allow simple elements to have children of their own.</span></span> <span data-ttu-id="c9f8f-109">Простые элементы также называются *дочерними* элементами.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-109">Simple elements are also known as *children*.</span></span>

<span data-ttu-id="c9f8f-110">Для однозначного определения и предоставления простого элемента требуется объект [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и идентификатор дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-110">To be uniquely identified and exposed, a simple element requires an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span> <span data-ttu-id="c9f8f-111">Поэтому при взаимодействии с объектом **IAccessible** клиенты должны предоставить соответствующий идентификатор дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-111">Therefore, when communicating with an **IAccessible** object, the clients must supply the appropriate child ID.</span></span> <span data-ttu-id="c9f8f-112">Специальный идентификатор ( **чилдид \_ Self**) можно использовать для ссылки на сам доступный объект, а не на один из его дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-112">A special identifier, **CHILDID\_SELF**, can be used to refer to the accessible object itself, instead of one of its children.</span></span>

<span data-ttu-id="c9f8f-113">Объект [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , совместно используемый простыми элементами, часто соответствует общему родительскому объекту в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-113">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object shared among simple elements often corresponds to a common parent object in the user interface.</span></span> <span data-ttu-id="c9f8f-114">Например, окна системных списков предоставляют доступный объект для общего списка и простые элементы для каждого элемента списка.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-114">For example, system list boxes expose an accessible object for the overall list box and simple elements for each list box item.</span></span> <span data-ttu-id="c9f8f-115">В этом случае объект **IAccessible** для списка также является родительским или контейнером элементов списка.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-115">In this case, the **IAccessible** object for the list box is also the parent or container of the list items.</span></span>

<span data-ttu-id="c9f8f-116">Дополнительные сведения о доступных объектах см. в разделе [Доступные объекты](accessible-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c9f8f-116">For more information about accessible objects, see [Accessible Objects](accessible-objects.md).</span></span>

 

 




