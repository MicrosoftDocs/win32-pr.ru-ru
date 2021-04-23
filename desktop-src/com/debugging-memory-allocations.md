---
title: Отладка выделения памяти
description: Отладка выделения памяти
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339329"
---
# <a name="debugging-memory-allocations"></a><span data-ttu-id="b1be1-103">Отладка выделения памяти</span><span class="sxs-lookup"><span data-stu-id="b1be1-103">Debugging Memory Allocations</span></span>

<span data-ttu-id="b1be1-104">COM предоставляет разработчикам интерфейс [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) для отладки выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="b1be1-104">COM provides the [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) interface for developers to use to debug their memory allocations.</span></span> <span data-ttu-id="b1be1-105">Для каждого метода нахождения [**в**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)интерфейсе **IMallocSpy** есть два метода: «Pre» и «POST».</span><span class="sxs-lookup"><span data-stu-id="b1be1-105">For each method in [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), there are two methods in **IMallocSpy**, a "pre" method and a "post" method.</span></span> <span data-ttu-id="b1be1-106">После того, как разработчик реализовал его и опубликует в системе, система вызывает метод **IMallocSpy** "Pre" непосредственно **перед соответствующим методом** освобождения, фактически позволяя коду отладки "Spy" в операции выделения памяти и вызову метода POST для освобождения Spy.</span><span class="sxs-lookup"><span data-stu-id="b1be1-106">After a developer implements it and publishes it to the system, the system calls the **IMallocSpy** "pre" method just before the corresponding **IMalloc** method, effectively allowing the debug code to "spy" on the allocation operation, and calls the "post" method to release the spy.</span></span>

<span data-ttu-id="b1be1-107">Например, когда COM обнаруживает, что следующий вызов является вызовом метода [**unalloc:: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), он вызывает метод [**IMallocSpy::P перераспределения**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), выполняя все операции отладки, необходимые разработчику во время выполнения **выделения** , а затем, когда вызывается метод **выделения** , вызывает интерфейс [**IMallocSpy::P осталлок**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) для освобождения Spy и возврата управления в код.</span><span class="sxs-lookup"><span data-stu-id="b1be1-107">For example, when COM detects that the next call is a call to [**IMalloc::Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), it calls [**IMallocSpy::PreAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), executing whatever debug operations the developer wants during the **Alloc** execution, and then, when the **Alloc** call returns, calls [**IMallocSpy::PostAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) to release the spy and return control to the code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1be1-108">См. также</span><span class="sxs-lookup"><span data-stu-id="b1be1-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1be1-109">Управление выделением памяти</span><span class="sxs-lookup"><span data-stu-id="b1be1-109">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> </dl>

 

 