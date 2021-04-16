---
description: В следующих примерах демонстрируется использование функций одноразовой инициализации.
ms.assetid: 47e68fbb-29f8-4930-beba-01d44263eb1e
title: Использование инициализации One-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f89cbe0e2d3e7c45d4f18863533c8c161037ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546383"
---
# <a name="using-one-time-initialization"></a>Использование инициализации One-Time

В следующих примерах демонстрируется использование функций одноразовой инициализации.

## <a name="synchronous-example"></a>Синхронный пример

В этом примере `g_InitOnce` Глобальная переменная является структурой однократной инициализации. Он инициализируется статически с помощью команды **init \_ после \_ статической \_ инициализации**.

`OpenEventHandleSync`Функция возвращает маркер для события, созданного только один раз. Он вызывает функцию [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) для выполнения кода инициализации, содержащегося в `InitHandleFunction` функции обратного вызова. Если функция обратного вызова завершается удачно, `OpenEventHandleSync` возвращает маркер события, возвращенный в *lpContext*; в противном случае возвращается **недопустимое \_ \_ значение Handle**.

`InitHandleFunction`Функция является [функцией обратного вызова однократной инициализации](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn). `InitHandleFunction` вызывает функцию [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) для создания события и возвращает маркер события в параметре *lpContext* .


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Initialization callback function 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        
    PVOID Parameter,            
    PVOID *lpContext);           

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleSync()
{
  PVOID lpContext;
  BOOL  bStatus;
  
  // Execute the initialization callback function 
  bStatus = InitOnceExecuteOnce(&g_InitOnce,          // One-time initialization structure
                                InitHandleFunction,   // Pointer to initialization callback function
                                NULL,                 // Optional parameter to callback function (not used)
                                &lpContext);          // Receives pointer to event object stored in g_InitOnce

  // InitOnceExecuteOnce function succeeded. Return event object.
  if (bStatus)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return (INVALID_HANDLE_VALUE);
  }
}

// Initialization callback function that creates the event object 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        // Pointer to one-time initialization structure        
    PVOID Parameter,            // Optional parameter passed by InitOnceExecuteOnce            
    PVOID *lpContext)           // Receives pointer to event object           
{
  HANDLE hEvent;

  // Create event object
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return FALSE;
  }
  // Event object creation succeeded.
  else
  {
    *lpContext = hEvent;
    return TRUE;
  }
}
```



## <a name="asynchronous-example"></a>Асинхронный пример

В этом примере `g_InitOnce` Глобальная переменная является структурой однократной инициализации. Он инициализируется статически с помощью команды **init \_ после \_ статической \_ инициализации**.

`OpenEventHandleAsync`Функция возвращает маркер для события, созданного только один раз. `OpenEventHandleAsync` вызывает функцию [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) для входа в состояние инициализации.

Если вызов завершился удачно, код проверяет значение параметра *fPending* , чтобы определить, следует ли создавать событие или просто возвращать маркер для события, созданного другим потоком. Если *fPending* имеет **значение false**, инициализация уже завершена, поэтому `OpenEventHandleAsync` возвращает маркер события, возвращенный в параметре *lpContext* . В противном случае вызывается функция [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) для создания события и функции [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) для завершения инициализации.

Если вызов [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) завершается, `OpenEventHandleAsync` возвращает новый обработчик событий. В противном случае он закрывает обработчик событий и вызывает [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) с параметром **init \_ \_ \_ только после проверки** , чтобы определить, завершилась ли инициализация неудачей или завершилась другим потоком.

Если инициализация была выполнена другим потоком, `OpenEventHandleAsync` возвращает маркер события, возвращенный в *lpContext*. В противном случае возвращается **недопустимое \_ \_ значение Handle**.


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleAsync()
{
  PVOID  lpContext;
  BOOL   fStatus;
  BOOL   fPending;
  HANDLE hEvent;
  
  // Begin one-time initialization
  fStatus = InitOnceBeginInitialize(&g_InitOnce,       // Pointer to one-time initialization structure
                                    INIT_ONCE_ASYNC,   // Asynchronous one-time initialization
                                    &fPending,         // Receives initialization status
                                    &lpContext);       // Receives pointer to data in g_InitOnce  

  // InitOnceBeginInitialize function failed.
  if (!fStatus)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Initialization has already completed and lpContext contains event object.
  if (!fPending)
  {
    return (HANDLE)lpContext;
  }

  // Create event object for one-time initialization.
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Complete one-time initialization.
  fStatus = InitOnceComplete(&g_InitOnce,             // Pointer to one-time initialization structure
                             INIT_ONCE_ASYNC,         // Asynchronous initialization
                             (PVOID)hEvent);          // Pointer to event object to be stored in g_InitOnce

  // InitOnceComplete function succeeded. Return event object.
  if (fStatus)
  {
    return hEvent;
  }
  
  // Initialization has already completed. Free the local event.
  CloseHandle(hEvent);


  // Retrieve the final context data.
  fStatus = InitOnceBeginInitialize(&g_InitOnce,            // Pointer to one-time initialization structure
                                    INIT_ONCE_CHECK_ONLY,   // Check whether initialization is complete
                                    &fPending,              // Receives initialization status
                                    &lpContext);            // Receives pointer to event object in g_InitOnce
  
  // Initialization is complete. Return handle.
  if (fStatus && !fPending)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return INVALID_HANDLE_VALUE;
  }
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Однократная инициализация](one-time-initialization.md)
</dt> </dl>

 

 
