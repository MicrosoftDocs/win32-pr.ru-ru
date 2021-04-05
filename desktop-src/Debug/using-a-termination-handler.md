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
# <a name="using-a-termination-handler"></a>Использование обработчика завершения

В следующем примере показано, как обработчик завершения используется, чтобы обеспечить освобождение ресурсов при завершении выполнения защищенного текста кода. В этом случае поток использует функцию [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) для ожидания владения объектом критической секции. Когда поток завершит исполнение кода, защищенного критической секцией, он должен вызвать функцию [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) , чтобы сделать объект критического раздела доступным другим потокам. Использование обработчика завершения гарантирует, что это произойдет. Дополнительные сведения см. в разделе [объекты критических секций](../sync/critical-section-objects.md).


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



 

 
