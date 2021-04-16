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
# <a name="using-one-time-initialization"></a><span data-ttu-id="a187c-103">Использование инициализации One-Time</span><span class="sxs-lookup"><span data-stu-id="a187c-103">Using One-Time Initialization</span></span>

<span data-ttu-id="a187c-104">В следующих примерах демонстрируется использование функций одноразовой инициализации.</span><span class="sxs-lookup"><span data-stu-id="a187c-104">The following examples demonstrate the use of the one-time initialization functions.</span></span>

## <a name="synchronous-example"></a><span data-ttu-id="a187c-105">Синхронный пример</span><span class="sxs-lookup"><span data-stu-id="a187c-105">Synchronous Example</span></span>

<span data-ttu-id="a187c-106">В этом примере `g_InitOnce` Глобальная переменная является структурой однократной инициализации.</span><span class="sxs-lookup"><span data-stu-id="a187c-106">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="a187c-107">Он инициализируется статически с помощью команды **init \_ после \_ статической \_ инициализации**.</span><span class="sxs-lookup"><span data-stu-id="a187c-107">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="a187c-108">`OpenEventHandleSync`Функция возвращает маркер для события, созданного только один раз.</span><span class="sxs-lookup"><span data-stu-id="a187c-108">The `OpenEventHandleSync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="a187c-109">Он вызывает функцию [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) для выполнения кода инициализации, содержащегося в `InitHandleFunction` функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="a187c-109">It calls the [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) function to execute the initialization code contained in the `InitHandleFunction` callback function.</span></span> <span data-ttu-id="a187c-110">Если функция обратного вызова завершается удачно, `OpenEventHandleSync` возвращает маркер события, возвращенный в *lpContext*; в противном случае возвращается **недопустимое \_ \_ значение Handle**.</span><span class="sxs-lookup"><span data-stu-id="a187c-110">If the callback function succeeds, `OpenEventHandleSync` returns the event handle returned in *lpContext*; otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="a187c-111">`InitHandleFunction`Функция является [функцией обратного вызова однократной инициализации](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span><span class="sxs-lookup"><span data-stu-id="a187c-111">The `InitHandleFunction` function is the [one-time initialization callback function](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span></span> <span data-ttu-id="a187c-112">`InitHandleFunction` вызывает функцию [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) для создания события и возвращает маркер события в параметре *lpContext* .</span><span class="sxs-lookup"><span data-stu-id="a187c-112">`InitHandleFunction` calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and returns the event handle in the *lpContext* parameter.</span></span>


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



## <a name="asynchronous-example"></a><span data-ttu-id="a187c-113">Асинхронный пример</span><span class="sxs-lookup"><span data-stu-id="a187c-113">Asynchronous Example</span></span>

<span data-ttu-id="a187c-114">В этом примере `g_InitOnce` Глобальная переменная является структурой однократной инициализации.</span><span class="sxs-lookup"><span data-stu-id="a187c-114">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="a187c-115">Он инициализируется статически с помощью команды **init \_ после \_ статической \_ инициализации**.</span><span class="sxs-lookup"><span data-stu-id="a187c-115">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="a187c-116">`OpenEventHandleAsync`Функция возвращает маркер для события, созданного только один раз.</span><span class="sxs-lookup"><span data-stu-id="a187c-116">The `OpenEventHandleAsync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="a187c-117">`OpenEventHandleAsync` вызывает функцию [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) для входа в состояние инициализации.</span><span class="sxs-lookup"><span data-stu-id="a187c-117">`OpenEventHandleAsync` calls the [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) function to enter the initializing state.</span></span>

<span data-ttu-id="a187c-118">Если вызов завершился удачно, код проверяет значение параметра *fPending* , чтобы определить, следует ли создавать событие или просто возвращать маркер для события, созданного другим потоком.</span><span class="sxs-lookup"><span data-stu-id="a187c-118">If the call succeeds, the code checks the value of the *fPending* parameter to determine whether to create the event or simply return a handle to the event created by another thread.</span></span> <span data-ttu-id="a187c-119">Если *fPending* имеет **значение false**, инициализация уже завершена, поэтому `OpenEventHandleAsync` возвращает маркер события, возвращенный в параметре *lpContext* .</span><span class="sxs-lookup"><span data-stu-id="a187c-119">If *fPending* is **FALSE**, initialization has already completed so `OpenEventHandleAsync` returns the event handle returned in the *lpContext* parameter.</span></span> <span data-ttu-id="a187c-120">В противном случае вызывается функция [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) для создания события и функции [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) для завершения инициализации.</span><span class="sxs-lookup"><span data-stu-id="a187c-120">Otherwise, it calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and the [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) function to complete the initialization.</span></span>

<span data-ttu-id="a187c-121">Если вызов [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) завершается, `OpenEventHandleAsync` возвращает новый обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="a187c-121">If the call to [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) succeeds, `OpenEventHandleAsync` returns the new event handle.</span></span> <span data-ttu-id="a187c-122">В противном случае он закрывает обработчик событий и вызывает [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) с параметром **init \_ \_ \_ только после проверки** , чтобы определить, завершилась ли инициализация неудачей или завершилась другим потоком.</span><span class="sxs-lookup"><span data-stu-id="a187c-122">Otherwise, it closes the event handle and calls [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) with **INIT\_ONCE\_CHECK\_ONLY** to determine whether initialization failed or was completed by another thread.</span></span>

<span data-ttu-id="a187c-123">Если инициализация была выполнена другим потоком, `OpenEventHandleAsync` возвращает маркер события, возвращенный в *lpContext*.</span><span class="sxs-lookup"><span data-stu-id="a187c-123">If the initialization was completed by another thread, `OpenEventHandleAsync` returns the event handle returned in *lpContext*.</span></span> <span data-ttu-id="a187c-124">В противном случае возвращается **недопустимое \_ \_ значение Handle**.</span><span class="sxs-lookup"><span data-stu-id="a187c-124">Otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a187c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a187c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a187c-126">Однократная инициализация</span><span class="sxs-lookup"><span data-stu-id="a187c-126">One-Time Initialization</span></span>](one-time-initialization.md)
</dt> </dl>

 

 
