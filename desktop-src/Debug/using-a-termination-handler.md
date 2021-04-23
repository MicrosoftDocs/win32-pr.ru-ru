---
description: В следующем примере показано, как обработчик завершения используется, чтобы обеспечить освобождение ресурсов при завершении выполнения защищенного текста кода.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Использование обработчика завершения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbe73eda8533ed5805159d5386b69daa4d03194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990560"
---
# <a name="using-a-termination-handler"></a><span data-ttu-id="f8f8b-103">Использование обработчика завершения</span><span class="sxs-lookup"><span data-stu-id="f8f8b-103">Using a Termination Handler</span></span>

<span data-ttu-id="f8f8b-104">В следующем примере показано, как обработчик завершения используется, чтобы обеспечить освобождение ресурсов при завершении выполнения защищенного текста кода.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-104">The following example shows how a termination handler is used to ensure that resources are released when execution of a guarded body of code terminates.</span></span> <span data-ttu-id="f8f8b-105">В этом случае поток использует функцию [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) для ожидания владения объектом критической секции.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-105">In this case, a thread uses the [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) function to wait for ownership of a critical section object.</span></span> <span data-ttu-id="f8f8b-106">Когда поток завершит исполнение кода, защищенного критической секцией, он должен вызвать функцию [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) , чтобы сделать объект критического раздела доступным другим потокам.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-106">When the thread is finished executing the code that is protected by the critical section, it must call the [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) function to make the critical section object available to other threads.</span></span> <span data-ttu-id="f8f8b-107">Использование обработчика завершения гарантирует, что это произойдет.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-107">Using a termination handler guarantees that this will happen.</span></span> <span data-ttu-id="f8f8b-108">Дополнительные сведения см. в разделе [объекты критических секций](../sync/critical-section-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f8f8b-108">For more information, see [critical section objects](../sync/critical-section-objects.md).</span></span>


```C++
LPTSTR lpBuffer = NULL; 
CRITICAL_SECTION CriticalSection; 

// EnterCriticalSection synchronizes code with other threads. 
EnterCriticalSection(&CriticalSection); 
 
__try 
{ 
    // Perform a task that may cause an exception. 
    lpBuffer = (LPTSTR) LocalAlloc(LPTR, 10); 
    StringCchCopy(lpBuffer, 10, TEXT("Hello"));

    _tprintf(TEXT("%s\n"),lpBuffer); 
    LocalFree(lpBuffer); 
} 
__finally 
{ 
    // LeaveCriticalSection is called even if an exception occurred. 
    LeaveCriticalSection(&CriticalSection); 
}
```



 

 
