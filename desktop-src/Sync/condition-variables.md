---
description: Переменные условия — это примитивы синхронизации, которые позволяют потокам ожидать выполнения определенного условия. Переменные условия — это объекты пользовательского режима, которые нельзя совместно использовать в процессах.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Переменные условия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fad7d80c1c5e06fc6e496198cd298b190daba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663887"
---
# <a name="condition-variables"></a><span data-ttu-id="e223b-104">Переменные условия</span><span class="sxs-lookup"><span data-stu-id="e223b-104">Condition Variables</span></span>

<span data-ttu-id="e223b-105">Переменные условия — это примитивы синхронизации, которые позволяют потокам ожидать выполнения определенного условия.</span><span class="sxs-lookup"><span data-stu-id="e223b-105">Condition variables are synchronization primitives that enable threads to wait until a particular condition occurs.</span></span> <span data-ttu-id="e223b-106">Переменные условия — это объекты пользовательского режима, которые нельзя совместно использовать в процессах.</span><span class="sxs-lookup"><span data-stu-id="e223b-106">Condition variables are user-mode objects that cannot be shared across processes.</span></span>

<span data-ttu-id="e223b-107">Переменные условия позволяют потокам атомарно освобождать блокировку и переходить в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="e223b-107">Condition variables enable threads to atomically release a lock and enter the sleeping state.</span></span> <span data-ttu-id="e223b-108">Их можно использовать с критическими секциями или с упрощенными блокировками потоков чтения/записи (SRW).</span><span class="sxs-lookup"><span data-stu-id="e223b-108">They can be used with critical sections or slim reader/writer (SRW) locks.</span></span> <span data-ttu-id="e223b-109">Переменные условия поддерживают операции, которые переводят ожидающие потоки в спящий режим или пробуждать все.</span><span class="sxs-lookup"><span data-stu-id="e223b-109">Condition variables support operations that "wake one" or "wake all" waiting threads.</span></span> <span data-ttu-id="e223b-110">После того как поток пробуждении, он повторно получает блокировку, освобожденную, когда поток перешел в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="e223b-110">After a thread is woken, it re-acquires the lock it released when the thread entered the sleeping state.</span></span>

<span data-ttu-id="e223b-111">Обратите внимание, что вызывающий объект должен выделить структуру **\_ переменной условия** и инициализировать ее, вызвав [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (для динамической инициализации структуры) или присвоить переменной Structure значение **\_ \_ init переменной Condition** (для статической инициализации структуры).</span><span class="sxs-lookup"><span data-stu-id="e223b-111">Note that the caller must allocate a **CONDITION\_VARIABLE** structure and initialize it by either calling [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (to initialize the structure dynamically) or assign the constant **CONDITION\_VARIABLE\_INIT** to the structure variable (to initialize the structure statically).</span></span>

<span data-ttu-id="e223b-112">**Windows Server 2003 и Windows XP:** Переменные условия не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e223b-112">**Windows Server 2003 and Windows XP:** Condition variables are not supported.</span></span>

<span data-ttu-id="e223b-113">Ниже приведены функции переменных условия.</span><span class="sxs-lookup"><span data-stu-id="e223b-113">The following are the condition variable functions.</span></span>



| <span data-ttu-id="e223b-114">Переменная Condition, функция</span><span class="sxs-lookup"><span data-stu-id="e223b-114">Condition variable function</span></span>                                        | <span data-ttu-id="e223b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="e223b-115">Description</span></span>                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e223b-116">**InitializeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="e223b-116">**InitializeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | <span data-ttu-id="e223b-117">Инициализирует переменную условия.</span><span class="sxs-lookup"><span data-stu-id="e223b-117">Initializes a condition variable.</span></span>                                                                              |
| [<span data-ttu-id="e223b-118">**SleepConditionVariableCS**</span><span class="sxs-lookup"><span data-stu-id="e223b-118">**SleepConditionVariableCS**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | <span data-ttu-id="e223b-119">Закрывает указанную переменную условия и освобождает указанную критическую секцию как атомарную операцию.</span><span class="sxs-lookup"><span data-stu-id="e223b-119">Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.</span></span> |
| [<span data-ttu-id="e223b-120">**SleepConditionVariableSRW**</span><span class="sxs-lookup"><span data-stu-id="e223b-120">**SleepConditionVariableSRW**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | <span data-ttu-id="e223b-121">Закрывает указанную переменную условия и освобождает указанную блокировку SRW как атомарную операцию.</span><span class="sxs-lookup"><span data-stu-id="e223b-121">Sleeps on the specified condition variable and releases the specified SRW lock as an atomic operation.</span></span>         |
| [<span data-ttu-id="e223b-122">**WakeAllConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="e223b-122">**WakeAllConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | <span data-ttu-id="e223b-123">Пробуждает все потоки, ожидающие заданную переменную условия.</span><span class="sxs-lookup"><span data-stu-id="e223b-123">Wakes all threads waiting on the specified condition variable.</span></span>                                                 |
| [<span data-ttu-id="e223b-124">**WakeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="e223b-124">**WakeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | <span data-ttu-id="e223b-125">Пробуждает один поток, ожидающий заданную переменную условия.</span><span class="sxs-lookup"><span data-stu-id="e223b-125">Wakes a single thread waiting on the specified condition variable.</span></span>                                             |



 

<span data-ttu-id="e223b-126">В следующем псевдокоде показан типичный шаблон использования переменных условия.</span><span class="sxs-lookup"><span data-stu-id="e223b-126">The following pseudocode demonstrates the typical usage pattern of condition variables.</span></span>

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

<span data-ttu-id="e223b-127">Например, в реализации блокировки потоков чтения/записи `TestPredicate` функция проверяет, совместим ли текущий запрос на блокировку с существующими владельцами.</span><span class="sxs-lookup"><span data-stu-id="e223b-127">For example, in an implementation of a reader/writer lock, the `TestPredicate` function would verify that the current lock request is compatible with the existing owners.</span></span> <span data-ttu-id="e223b-128">Если это так, получите блокировку; в противном случае — спящий режим.</span><span class="sxs-lookup"><span data-stu-id="e223b-128">If it is, acquire the lock; otherwise, sleep.</span></span> <span data-ttu-id="e223b-129">Более подробный пример см. в разделе [Использование переменных условия](using-condition-variables.md).</span><span class="sxs-lookup"><span data-stu-id="e223b-129">For a more detailed example, see [Using Condition Variables](using-condition-variables.md).</span></span>

<span data-ttu-id="e223b-130">Переменные условия подчиняются ложным пробуждениям (не связанным с явной функцией пробуждения) и украденным пробуждениям (другой поток управляет выполнением до потока пробуждении).</span><span class="sxs-lookup"><span data-stu-id="e223b-130">Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread).</span></span> <span data-ttu-id="e223b-131">Поэтому следует проверить предикат (обычно в цикле **while** ) после возврата в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="e223b-131">Therefore, you should recheck a predicate (typically in a **while** loop) after a sleep operation returns.</span></span>

<span data-ttu-id="e223b-132">Можно пробудить другие потоки с помощью [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) или [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) внутри или вне блокировки, связанной с переменной Condition.</span><span class="sxs-lookup"><span data-stu-id="e223b-132">You can wake other threads using [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) or [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) either inside or outside the lock associated with the condition variable.</span></span> <span data-ttu-id="e223b-133">Обычно лучше снять блокировку перед пробуждением других потоков, чтобы уменьшить число переключений контекста.</span><span class="sxs-lookup"><span data-stu-id="e223b-133">It is usually better to release the lock before waking other threads to reduce the number of context switches.</span></span>

<span data-ttu-id="e223b-134">Часто удобно использовать более одной переменной условия с одной блокировкой.</span><span class="sxs-lookup"><span data-stu-id="e223b-134">It is often convenient to use more than one condition variable with the same lock.</span></span> <span data-ttu-id="e223b-135">Например, реализация блокировки потоков чтения/записи может использовать одну критическую секцию, но отдельные переменные условия для читателей и модулей записи.</span><span class="sxs-lookup"><span data-stu-id="e223b-135">For example, an implementation of a reader/writer lock might use a single critical section but separate condition variables for readers and writers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e223b-136">См. также</span><span class="sxs-lookup"><span data-stu-id="e223b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e223b-137">Использование переменных условия</span><span class="sxs-lookup"><span data-stu-id="e223b-137">Using Condition Variables</span></span>](using-condition-variables.md)
</dt> </dl>

 

 
