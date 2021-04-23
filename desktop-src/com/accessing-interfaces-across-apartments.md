---
title: Доступ к интерфейсам в разных апартаментах
description: Доступ к интерфейсам в разных апартаментах
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774795"
---
# <a name="accessing-interfaces-across-apartments"></a><span data-ttu-id="a9c08-103">Доступ к интерфейсам в разных апартаментах</span><span class="sxs-lookup"><span data-stu-id="a9c08-103">Accessing Interfaces Across Apartments</span></span>

<span data-ttu-id="a9c08-104">COM позволяет любому подразделению в процессе получить доступ к интерфейсу, реализованному для объекта в любом другом апартаменте в процессе.</span><span class="sxs-lookup"><span data-stu-id="a9c08-104">COM provides a way for any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.</span></span> <span data-ttu-id="a9c08-105">Это делается через интерфейс [**иглобалинтерфацетабле**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="a9c08-105">This is done through the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="a9c08-106">Этот интерфейс имеет три метода, которые позволяют выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a9c08-106">This interface has three methods, which allow you to do the following:</span></span>

-   <span data-ttu-id="a9c08-107">Зарегистрируйте интерфейс как *глобальный* интерфейс (процессвиде).</span><span class="sxs-lookup"><span data-stu-id="a9c08-107">Register an interface as a *global* (processwide) interface.</span></span>
-   <span data-ttu-id="a9c08-108">Получение указателя на этот интерфейс из любого другого подразделения через файл cookie.</span><span class="sxs-lookup"><span data-stu-id="a9c08-108">Get a pointer to that interface from any other apartment through a cookie.</span></span>
-   <span data-ttu-id="a9c08-109">Отозвать глобальную регистрацию интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a9c08-109">Revoke the global registration of an interface.</span></span>

<span data-ttu-id="a9c08-110">Интерфейс [**иглобалинтерфацетабле**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) — это эффективный способ хранения указателя интерфейса в памяти, доступ к которому можно получить из нескольких подконтейнеров внутри процесса, таких как переменные на уровне процесса и *гибкие* объекты (объекты с поддержкой свободных потоков), содержащие указатели интерфейсов на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="a9c08-110">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface is an efficient way for a process to store an interface pointer in a memory location that can be accessed from multiple apartments within the process, such as process-wide variables and *agile* objects (free-threaded, marshaled objects) containing interface pointers to other objects.</span></span>

<span data-ttu-id="a9c08-111">Объект Agile не знает о базовой инфраструктуре COM, в которой она выполняется. Иными словами, подразделение, контекст и поток, на котором он выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9c08-111">An agile object is unaware of the underlying COM infrastructure in which it runs; in other words, what apartment, context, and thread it is executing on.</span></span> <span data-ttu-id="a9c08-112">Объект может храниться в интерфейсах, относящихся к подразделению или контексту.</span><span class="sxs-lookup"><span data-stu-id="a9c08-112">The object may be holding on to interfaces that are specific to an apartment or context.</span></span> <span data-ttu-id="a9c08-113">По этой причине вызов этих интерфейсов из любого места, где выполняется компонент Agile, может не всегда работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="a9c08-113">For this reason, calling these interfaces from wherever the agile component is executing might not always work properly.</span></span> <span data-ttu-id="a9c08-114">Глобальная таблица интерфейса позволяет избежать этой проблемы, гарантируя, что используется допустимый прокси-сервер (или прямой указатель) для объекта, основанный на месте, где работает объект Agile.</span><span class="sxs-lookup"><span data-stu-id="a9c08-114">The global interface table avoids this problem by guaranteeing that a valid proxy (or direct pointer) to the object is used, based on where the agile object is executing.</span></span>

> [!Note]  
> <span data-ttu-id="a9c08-115">Глобальная таблица интерфейса не переносима между процессами или границами машин, поэтому ее нельзя использовать вместо обычного механизма передачи параметров.</span><span class="sxs-lookup"><span data-stu-id="a9c08-115">The global interface table is not portable across process or machine boundaries, so it cannot be used in place of the normal parameter-passing mechanism.</span></span>

 

<span data-ttu-id="a9c08-116">Сведения о создании и использовании глобальной таблицы интерфейса см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a9c08-116">For information about creating and using a global interface table, see the following topics:</span></span>

-   [<span data-ttu-id="a9c08-117">Создание глобальной таблицы интерфейса</span><span class="sxs-lookup"><span data-stu-id="a9c08-117">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
-   [<span data-ttu-id="a9c08-118">Когда следует использовать глобальную таблицу интерфейса</span><span class="sxs-lookup"><span data-stu-id="a9c08-118">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a><span data-ttu-id="a9c08-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a9c08-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9c08-120">Выбор потоковой модели</span><span class="sxs-lookup"><span data-stu-id="a9c08-120">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="a9c08-121">Многопоточные подразделения</span><span class="sxs-lookup"><span data-stu-id="a9c08-121">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="a9c08-122">Проблемы потоковой обработки в процессе сервера</span><span class="sxs-lookup"><span data-stu-id="a9c08-122">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="a9c08-123">Процессы, потоки и подразделения</span><span class="sxs-lookup"><span data-stu-id="a9c08-123">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="a9c08-124">Однопотоковое и многопоточное взаимодействие</span><span class="sxs-lookup"><span data-stu-id="a9c08-124">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="a9c08-125">Подразделения с одним потоком</span><span class="sxs-lookup"><span data-stu-id="a9c08-125">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




