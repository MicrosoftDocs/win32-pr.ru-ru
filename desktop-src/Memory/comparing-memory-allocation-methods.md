---
Description: Ниже приведено краткое сравнение различных методов выделения памяти.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Сравнение методов выделения памяти
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104000295"
---
# <a name="comparing-memory-allocation-methods"></a><span data-ttu-id="846c8-103">Сравнение методов выделения памяти</span><span class="sxs-lookup"><span data-stu-id="846c8-103">Comparing Memory Allocation Methods</span></span>

<span data-ttu-id="846c8-104">Ниже приведено краткое сравнение различных методов выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="846c8-104">The following is a brief comparison of the various memory allocation methods:</span></span>

-   [<span data-ttu-id="846c8-105">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="846c8-105">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [<span data-ttu-id="846c8-106">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="846c8-106">**GlobalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [<span data-ttu-id="846c8-107">**хеапаллок**</span><span class="sxs-lookup"><span data-stu-id="846c8-107">**HeapAlloc**</span></span>](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [<span data-ttu-id="846c8-108">**локалаллок**</span><span class="sxs-lookup"><span data-stu-id="846c8-108">**LocalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   <span data-ttu-id="846c8-109">**malloc**</span><span class="sxs-lookup"><span data-stu-id="846c8-109">**malloc**</span></span>
-   <span data-ttu-id="846c8-110">**new**</span><span class="sxs-lookup"><span data-stu-id="846c8-110">**new**</span></span>
-   [<span data-ttu-id="846c8-111">**VirtualAlloc**</span><span class="sxs-lookup"><span data-stu-id="846c8-111">**VirtualAlloc**</span></span>](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

<span data-ttu-id="846c8-112">Хотя функции [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**локалаллок**](/windows/desktop/api/WinBase/nf-winbase-localalloc)и [**хеапаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) в конечном итоге выделяют память из той же кучи, каждая из них предоставляет слегка отличающийся набор функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="846c8-112">Although the [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), and [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) functions ultimately allocate memory from the same heap, each provides a slightly different set of functionality.</span></span> <span data-ttu-id="846c8-113">Например, **хеапаллок** может дать указание создавать исключение, если память не может быть выделена, возможность недоступна для **локалаллок**.</span><span class="sxs-lookup"><span data-stu-id="846c8-113">For example, **HeapAlloc** can be instructed to raise an exception if memory could not be allocated, a capability not available with **LocalAlloc**.</span></span> <span data-ttu-id="846c8-114">**Локалаллок** поддерживает выделение дескрипторов, позволяющих перемещать базовую память при перераспределении без изменения значения дескриптора, возможность недоступна для **хеапаллок**.</span><span class="sxs-lookup"><span data-stu-id="846c8-114">**LocalAlloc** supports allocation of handles which permit the underlying memory to be moved by a reallocation without changing the handle value, a capability not available with **HeapAlloc**.</span></span>

<span data-ttu-id="846c8-115">Начиная с 32-разрядных Windows, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) и [**локалаллок**](/windows/desktop/api/WinBase/nf-winbase-localalloc) реализуются как функции-оболочки, которые вызывают [**хеапаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) с помощью обработчика для кучи процесса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="846c8-115">Starting with 32-bit Windows, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) and [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) are implemented as wrapper functions that call [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) using a handle to the process's default heap.</span></span> <span data-ttu-id="846c8-116">Таким образом, **GlobalAlloc** и **локалаллок** имеют большие издержки, чем **хеапаллок**.</span><span class="sxs-lookup"><span data-stu-id="846c8-116">Therefore, **GlobalAlloc** and **LocalAlloc** have greater overhead than **HeapAlloc**.</span></span>

<span data-ttu-id="846c8-117">Так как различные распределительы кучи обеспечивают различенную функциональность с помощью различных механизмов, необходимо освободить память с правильной функцией.</span><span class="sxs-lookup"><span data-stu-id="846c8-117">Because the different heap allocators provide distinctive functionality by using different mechanisms, you must free memory with the correct function.</span></span> <span data-ttu-id="846c8-118">Например, память, выделенная с помощью [**хеапаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) , должна быть освобождена с помощью [**хеапфри**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) , а не [**функции LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) или [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span><span class="sxs-lookup"><span data-stu-id="846c8-118">For example, memory allocated with [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) must be freed with [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) and not [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) or [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span></span> <span data-ttu-id="846c8-119">Память, выделенная с помощью [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) или [**локалаллок**](/windows/desktop/api/WinBase/nf-winbase-localalloc) , должна быть запрошена, проверена и освобождена с помощью соответствующей глобальной или локальной функции.</span><span class="sxs-lookup"><span data-stu-id="846c8-119">Memory allocated with [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) or [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) must be queried, validated, and released with the corresponding global or local function.</span></span>

<span data-ttu-id="846c8-120">Функция [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) позволяет указать дополнительные параметры для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="846c8-120">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function allows you to specify additional options for memory allocation.</span></span> <span data-ttu-id="846c8-121">Однако при выделении ресурсов используется гранулярность страницы, поэтому использование **VirtualAlloc** может привести к увеличению использования памяти.</span><span class="sxs-lookup"><span data-stu-id="846c8-121">However, its allocations use a page granularity, so using **VirtualAlloc** can result in higher memory usage.</span></span>

<span data-ttu-id="846c8-122">Функция **malloc** имеет недостатки, зависящие от времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="846c8-122">The **malloc** function has the disadvantage of being run-time dependent.</span></span> <span data-ttu-id="846c8-123">У оператора **New** есть недостатки, зависящие от компилятора и зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="846c8-123">The **new** operator has the disadvantage of being compiler dependent and language dependent.</span></span>

<span data-ttu-id="846c8-124">Функция [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) имеет преимущество при работе с C, C++ или Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="846c8-124">The [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function has the advantage of working well in either C, C++, or Visual Basic.</span></span> <span data-ttu-id="846c8-125">Это также единственный способ совместного использования памяти в приложении на основе COM, поскольку MIDL использует **CoTaskMemAlloc** и [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) для маршалирования памяти.</span><span class="sxs-lookup"><span data-stu-id="846c8-125">It is also the only way to share memory in a COM-based application, since MIDL uses **CoTaskMemAlloc** and [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to marshal memory.</span></span>


## <a name="examples"></a><span data-ttu-id="846c8-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="846c8-126">Examples</span></span>

* [<span data-ttu-id="846c8-127">Резервирование и фиксация памяти</span><span class="sxs-lookup"><span data-stu-id="846c8-127">Reserving and Committing Memory</span></span>](./reserving-and-committing-memory.md)

* [<span data-ttu-id="846c8-128">Пример расширений AWE</span><span class="sxs-lookup"><span data-stu-id="846c8-128">AWE Example</span></span>](./awe-example.md)

## <a name="related-topics"></a><span data-ttu-id="846c8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="846c8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="846c8-130">Глобальные и локальные функции</span><span class="sxs-lookup"><span data-stu-id="846c8-130">Global and Local Functions</span></span>](global-and-local-functions.md)
</dt> <dt>

[<span data-ttu-id="846c8-131">Функции кучи</span><span class="sxs-lookup"><span data-stu-id="846c8-131">Heap Functions</span></span>](heap-functions.md)
</dt> <dt>

[<span data-ttu-id="846c8-132">Функции виртуальной памяти</span><span class="sxs-lookup"><span data-stu-id="846c8-132">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
</dt> </dl>

 

 