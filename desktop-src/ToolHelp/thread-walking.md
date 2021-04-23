---
title: Потоковый проход
description: Моментальный снимок, включающий список потоков, содержит сведения о каждом потоке каждого выполняющегося процесса.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- перечисление
- Перечисление, потоки
- потоки
- потоки, перечисление потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681665"
---
# <a name="thread-walking"></a><span data-ttu-id="8af47-107">Потоковый проход</span><span class="sxs-lookup"><span data-stu-id="8af47-107">Thread Walking</span></span>

<span data-ttu-id="8af47-108">Моментальный снимок, включающий список потоков, содержит сведения о каждом потоке каждого выполняющегося процесса.</span><span class="sxs-lookup"><span data-stu-id="8af47-108">A snapshot that includes the thread list contains information about each thread of each currently executing process.</span></span> <span data-ttu-id="8af47-109">Сведения для первого потока в списке можно получить с помощью функции [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) .</span><span class="sxs-lookup"><span data-stu-id="8af47-109">You can retrieve information for the first thread in the list by using the [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) function.</span></span> <span data-ttu-id="8af47-110">После получения первого потока в списке можно получить сведения для последующих потоков с помощью функции [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) .</span><span class="sxs-lookup"><span data-stu-id="8af47-110">After retrieving the first thread in the list, you can retrieve information for subsequent threads by using the [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) function.</span></span> <span data-ttu-id="8af47-111">**Thread32First** и **Thread32Next** заполняют структуру [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) информацией об отдельных потоках в моментальном снимке.</span><span class="sxs-lookup"><span data-stu-id="8af47-111">**Thread32First** and **Thread32Next** fill a [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) structure with information about individual threads in the snapshot.</span></span>

<span data-ttu-id="8af47-112">Вы можете перечислить потоки определенного процесса, используя моментальный снимок, включающий потоки, а затем продвигаясь по списку потоков, сохранив сведения о потоках, имеющих тот же идентификатор процесса, что и указанный процесс.</span><span class="sxs-lookup"><span data-stu-id="8af47-112">You can enumerate the threads of a specific process by taking a snapshot that includes the threads and then by traversing the thread list, keeping information about the threads that have the same process identifier as the specified process.</span></span>

<span data-ttu-id="8af47-113">Код расширенного состояния ошибки для [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) и [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) можно получить с помощью функции [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="8af47-113">You can retrieve an extended error status code for [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) and [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="8af47-114">Содержимое элемента **th32ThreadID** объекта [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) является идентификатором потока и может использоваться любыми функциями, которым требуется идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="8af47-114">The contents of the **th32ThreadID** member of [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) is a thread identifier and can be used by any functions that require a thread identifier.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8af47-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8af47-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8af47-116">Обход списка потоков</span><span class="sxs-lookup"><span data-stu-id="8af47-116">Traversing the Thread List</span></span>](traversing-the-thread-list.md)
</dt> </dl>

 

 