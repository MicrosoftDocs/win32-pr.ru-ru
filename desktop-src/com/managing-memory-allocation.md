---
title: Управление выделением памяти
description: Управление выделением памяти
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413881"
---
# <a name="managing-memory-allocation"></a><span data-ttu-id="53c6e-103">Управление выделением памяти</span><span class="sxs-lookup"><span data-stu-id="53c6e-103">Managing Memory Allocation</span></span>

<span data-ttu-id="53c6e-104">В модели COM многие, если не большинство из них, методы интерфейса вызываются кодом, написанным одной организацией программирования, и реализуются кодом, написанным другим.</span><span class="sxs-lookup"><span data-stu-id="53c6e-104">In COM, many, if not most, interface methods are called by code written by one programming organization and implemented by code written by another.</span></span> <span data-ttu-id="53c6e-105">Многие параметры и возвращаемые значения этих функций имеют типы, которые могут передаваться по значению.</span><span class="sxs-lookup"><span data-stu-id="53c6e-105">Many of the parameters and return values of these functions are of types that can be passed around by value.</span></span> <span data-ttu-id="53c6e-106">Однако иногда необходимо передать структуры данных, для которых это не так, поэтому необходимо, чтобы вызывающий и вызывался совместимая политика выделения и отмены распределения.</span><span class="sxs-lookup"><span data-stu-id="53c6e-106">Sometimes, however, it is necessary to pass data structures for which this is not the case, so it is necessary for both caller and called to have a compatible allocation and de-allocation policy.</span></span> <span data-ttu-id="53c6e-107">COM определяет универсальное соглашение о выделении памяти, так как оно является более разумным, чем определение правил с учетом регистра, а реализация удаленного вызова процедур COM может правильно управлять памятью.</span><span class="sxs-lookup"><span data-stu-id="53c6e-107">COM defines a universal convention for memory allocation, because it is more reasonable than defining case-by-case rules and so that the COM remote procedure call implementation can correctly manage memory.</span></span>

<span data-ttu-id="53c6e-108">Методы COM-интерфейса всегда обеспечивают управление памятью указателей на интерфейс путем вызова функций [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) и [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , находящихся в интерфейсе [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , от которого наследуются все остальные COM-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="53c6e-108">The methods of a COM interface always provide memory management of pointers to the interface by calling the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) functions found in the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, from which all other COM interfaces derive.</span></span> <span data-ttu-id="53c6e-109">(Дополнительные сведения см. в разделе [правила управления счетчиками ссылок](rules-for-managing-reference-counts.md) .)</span><span class="sxs-lookup"><span data-stu-id="53c6e-109">(See [Rules for Managing Reference Counts](rules-for-managing-reference-counts.md) for more information.)</span></span>

<span data-ttu-id="53c6e-110">В этом разделе описывается, как выделить память для параметров, которые не передаются по значению, а не указатели на интерфейсы, но более рутинные вещи, такие как строки, указатели на структуры и т. д.</span><span class="sxs-lookup"><span data-stu-id="53c6e-110">This section describes only how to allocate memory for parameters that are not passed by value — not pointers to interfaces, but more mundane things like strings, pointers to structures, and so forth.</span></span>

<span data-ttu-id="53c6e-111">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="53c6e-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="53c6e-112">Распределитель памяти OLE</span><span class="sxs-lookup"><span data-stu-id="53c6e-112">The OLE Memory Allocator</span></span>](the-ole-memory-allocator.md)
-   [<span data-ttu-id="53c6e-113">Правила управления памятью</span><span class="sxs-lookup"><span data-stu-id="53c6e-113">Memory Management Rules</span></span>](memory-management-rules.md)
-   [<span data-ttu-id="53c6e-114">Отладка выделения памяти</span><span class="sxs-lookup"><span data-stu-id="53c6e-114">Debugging Memory Allocations</span></span>](debugging-memory-allocations.md)

 

 