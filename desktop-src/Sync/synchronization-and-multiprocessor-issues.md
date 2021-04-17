---
description: Приложения могут столкнуться с проблемами при запуске в многопроцессорных системах из-за допущений, которые они допускаются только в однопроцессорных системах.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Проблемы синхронизации и многопроцессорности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "105664783"
---
# <a name="synchronization-and-multiprocessor-issues"></a><span data-ttu-id="ce4b5-103">Проблемы синхронизации и многопроцессорности</span><span class="sxs-lookup"><span data-stu-id="ce4b5-103">Synchronization and Multiprocessor Issues</span></span>

<span data-ttu-id="ce4b5-104">Приложения могут столкнуться с проблемами при запуске в многопроцессорных системах из-за допущений, которые они допускаются только в однопроцессорных системах.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-104">Applications may encounter problems when run on multiprocessor systems due to assumptions they make which are valid only on single-processor systems.</span></span>

## <a name="thread-priorities"></a><span data-ttu-id="ce4b5-105">Приоритеты потоков</span><span class="sxs-lookup"><span data-stu-id="ce4b5-105">Thread Priorities</span></span>

<span data-ttu-id="ce4b5-106">Рассмотрим программу с двумя потоками, одна с более высоким приоритетом, чем другая.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-106">Consider a program with two threads, one with a higher priority than the other.</span></span> <span data-ttu-id="ce4b5-107">В системе с одним процессором поток с более высоким приоритетом не будет предоставлять управление потоку с более низким приоритетом, так как планировщик дает предпочтение потокам с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-107">On a single-processor system, the higher priority thread will not relinquish control to the lower priority thread because the scheduler gives preference to higher priority threads.</span></span> <span data-ttu-id="ce4b5-108">В многопроцессорной системе оба потока могут выполняться одновременно, каждый на собственном процессоре.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-108">On a multiprocessor system, both threads can run simultaneously, each on its own processor.</span></span>

<span data-ttu-id="ce4b5-109">Приложения должны синхронизировать доступ к структурам данных, чтобы избежать конкуренции.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-109">Applications should synchronize access to data structures to avoid race conditions.</span></span> <span data-ttu-id="ce4b5-110">Код, который предполагает, что потоки с более высоким приоритетом выполняются без помех в потоках с более низким приоритетом, завершатся сбоем в многопроцессорных системах.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-110">Code that assumes that higher priority threads run without interference from lower priority threads will fail on multiprocessor systems.</span></span>

## <a name="memory-ordering"></a><span data-ttu-id="ce4b5-111">Упорядочение памяти</span><span class="sxs-lookup"><span data-stu-id="ce4b5-111">Memory Ordering</span></span>

<span data-ttu-id="ce4b5-112">Когда процессор записывает данные в место в памяти, значение кэшируется для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-112">When a processor writes to a memory location, the value is cached to improve performance.</span></span> <span data-ttu-id="ce4b5-113">Аналогичным образом, процессор пытается удовлетворить запросы чтения из кэша, чтобы повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-113">Similarly, the processor attempts to satisfy read requests from the cache to improve performance.</span></span> <span data-ttu-id="ce4b5-114">Более того, процессоры начинают извлекать значения из памяти до того, как они запрашиваются приложением.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-114">Furthermore, processors begin to fetch values from memory before they are requested by the application.</span></span> <span data-ttu-id="ce4b5-115">Это может произойти в рамках гипотетического выполнения или из-за проблем, связанных со строками кэша.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-115">This can happen as part of speculative execution or due to cache line issues.</span></span>

<span data-ttu-id="ce4b5-116">Кэш ЦП можно секционировать на банки, к которым можно получить доступ параллельно.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-116">CPU caches can be partitioned into banks that can be accessed in parallel.</span></span> <span data-ttu-id="ce4b5-117">Это означает, что операции с памятью могут выполняться не по порядку.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-117">This means that memory operations can be completed out of order.</span></span> <span data-ttu-id="ce4b5-118">Чтобы гарантировать, что операции с памятью выполняются по порядку, большинство процессоров предоставляет инструкции по барьеру памяти.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-118">To ensure that memory operations are completed in order, most processors provide memory-barrier instructions.</span></span> <span data-ttu-id="ce4b5-119">*Переполнение памяти* гарантирует, что операции чтения и записи памяти, которые отображаются перед инструкцией барьера памяти, фиксируются в памяти до выполнения операций чтения и записи в памяти, появляющихся после инструкции барьера памяти.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-119">A *full memory barrier* ensures that memory read and write operations that appear before the memory barrier instruction are committed to memory before any memory read and write operations that appear after the memory barrier instruction.</span></span> <span data-ttu-id="ce4b5-120">*Барьер памяти для чтения* упорядочивает только операции чтения памяти, а *барьер памяти для записи* упорядочивает только операции записи в память.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-120">A *read memory barrier* orders only the memory read operations and a *write memory barrier* orders only the memory write operations.</span></span> <span data-ttu-id="ce4b5-121">Эти инструкции также гарантируют, что компилятор отключает любые оптимизации, которые могут переупорядочивать операции с памятью во всех барьерах.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-121">These instructions also ensure that the compiler disables any optimizations that could reorder memory operations across the barriers.</span></span>

<span data-ttu-id="ce4b5-122">Процессоры могут поддерживать инструкции для барьеров памяти с семантикой получения, выпуска и ограждения.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-122">Processors can support instructions for memory barriers with acquire, release, and fence semantics.</span></span> <span data-ttu-id="ce4b5-123">Эти семантики описывают порядок, в котором результаты операции становятся доступными.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-123">These semantics describe the order in which results of an operation become available.</span></span> <span data-ttu-id="ce4b5-124">При использовании семантики получения результаты операции доступны до результатов любой операции, которая отображается после нее в коде.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-124">With acquire semantics, the results of the operation are available before the results of any operation that appears after it in code.</span></span> <span data-ttu-id="ce4b5-125">При использовании семантики выпуска результаты операции становятся доступными после выполнения любой операции, которая отображается перед ней в коде.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-125">With release semantics, the results of the operation are available after the results of any operation that appears before it in code.</span></span> <span data-ttu-id="ce4b5-126">Семантика ограждения сочетает семантику получения и освобождения.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-126">Fence semantics combine acquire and release semantics.</span></span> <span data-ttu-id="ce4b5-127">Результаты операции с семантикой ограждения доступны до тех пор, пока они не появятся в коде и после любой операции, которая отображается перед ней.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-127">The results of an operation with fence semantics are available before those of any operation that appears after it in code and after those of any operation that appears before it.</span></span>

<span data-ttu-id="ce4b5-128">В процессорах x86 и x64, поддерживающих SSE2, инструкции **мфенце** (ограждение памяти), **лфенце** (Load забор) и **сфенце** (ограждение хранилища).</span><span class="sxs-lookup"><span data-stu-id="ce4b5-128">On x86 and x64 processors that support SSE2, the instructions are **mfence** (memory fence), **lfence** (load fence), and **sfence** (store fence).</span></span> <span data-ttu-id="ce4b5-129">В процессорах ARM инструтионс — это **ДМБ** и **ДСБ**.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-129">On ARM processors, the instrutions are **dmb** and **dsb**.</span></span> <span data-ttu-id="ce4b5-130">Дополнительные сведения см. в документации к процессору.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-130">For more information, see the documentation for the processor.</span></span>

<span data-ttu-id="ce4b5-131">Следующие функции синхронизации используют соответствующие барьеры для обеспечения упорядочения памяти:</span><span class="sxs-lookup"><span data-stu-id="ce4b5-131">The following synchronization functions use the appropriate barriers to ensure memory ordering:</span></span>

-   <span data-ttu-id="ce4b5-132">Функции, которые вводят или оставляют критические секции</span><span class="sxs-lookup"><span data-stu-id="ce4b5-132">Functions that enter or leave critical sections</span></span>
-   <span data-ttu-id="ce4b5-133">Функции, которые получают или освобождают блокировки SRW</span><span class="sxs-lookup"><span data-stu-id="ce4b5-133">Functions that acquire or release SRW locks</span></span>
-   <span data-ttu-id="ce4b5-134">Начало и завершение однократной инициализации</span><span class="sxs-lookup"><span data-stu-id="ce4b5-134">One-time initialization begin and completion</span></span>
-   <span data-ttu-id="ce4b5-135">Функция **ентерсинчронизатионбарриер**</span><span class="sxs-lookup"><span data-stu-id="ce4b5-135">**EnterSynchronizationBarrier** function</span></span>
-   <span data-ttu-id="ce4b5-136">Функции, которые сообщают об объектах синхронизации</span><span class="sxs-lookup"><span data-stu-id="ce4b5-136">Functions that signal synchronization objects</span></span>
-   <span data-ttu-id="ce4b5-137">Функции Wait</span><span class="sxs-lookup"><span data-stu-id="ce4b5-137">Wait functions</span></span>
-   <span data-ttu-id="ce4b5-138">Блокируемые функции (за исключением функций с суффиксом " _ограждения_ " или встроенных компонентов с суффиксом _\_ NF_ )</span><span class="sxs-lookup"><span data-stu-id="ce4b5-138">Interlocked functions (except functions with _NoFence_ suffix, or intrinsics with _\_nf_ suffix)</span></span>

## <a name="fixing-a-race-condition"></a><span data-ttu-id="ce4b5-139">Исправление состояния гонки</span><span class="sxs-lookup"><span data-stu-id="ce4b5-139">Fixing a Race Condition</span></span>

<span data-ttu-id="ce4b5-140">Следующий код имеет состояние гонки в многопроцессорных системах, так как процессор, который выполняет `CacheComputedValue` первый раз, может записывать `fValueHasBeenComputed` в основную память перед записью `iValue` в основную память.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-140">The following code has a race condition on a multiprocessor systems because the processor that executes `CacheComputedValue` the first time may write `fValueHasBeenComputed` to main memory before writing `iValue` to main memory.</span></span> <span data-ttu-id="ce4b5-141">Следовательно, второй процессор, выполняющийся в `FetchComputedValue` то же время `fValueHasBeenComputed` , считывает значение **true**, но новое значение `iValue` остается в кэше первого процессора и не записывается в память.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-141">Consequently, a second processor executing `FetchComputedValue` at the same time reads `fValueHasBeenComputed` as **TRUE**, but the new value of `iValue` is still in the first processor's cache and has not been written to memory.</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="ce4b5-142">Приведенное выше состояние гонки можно исправить с помощью ключевого слова **volatile** или функции [**интерлоккедексчанже**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) , чтобы гарантировать, что значение `iValue` обновляется для всех процессоров, прежде чем значение `fValueHasBeenComputed` будет равно **true**.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-142">This race condition above can be repaired by using the **volatile** keyword or the [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) function to ensure that the value of `iValue` is updated for all processors before the value of `fValueHasBeenComputed` is set to **TRUE**.</span></span>

<span data-ttu-id="ce4b5-143">Запуск Visual Studio 2005, если скомпилирован в режиме **/volatile: MS** , компилятор использует семантику получения для операций чтения с **временными** переменными и семантику выпуска для операций записи **в переменных с переменными** (если они поддерживаются ЦП).</span><span class="sxs-lookup"><span data-stu-id="ce4b5-143">Starting Visual Studio 2005, if compiled in **/volatile:ms** mode, the compiler uses acquire semantics for read operations on **volatile** variables and release semantics for write operations on **volatile** variables (when supported by the CPU).</span></span> <span data-ttu-id="ce4b5-144">Таким образом, можно исправить пример следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ce4b5-144">Therefore, you can correct the example as follows:</span></span>

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="ce4b5-145">В Visual Studio 2003 упорядочиваются **временные ссылки на** **переменные** . компилятор не будет изменять порядок доступа к переменным с **постоянным** доступом.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-145">With Visual Studio 2003, **volatile** to **volatile** references are ordered; the compiler will not re-order **volatile** variable access.</span></span> <span data-ttu-id="ce4b5-146">Однако эти операции могут быть переупорядочены процессором.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-146">However, these operations could be re-ordered by the processor.</span></span> <span data-ttu-id="ce4b5-147">Таким образом, можно исправить пример следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ce4b5-147">Therefore, you can correct the example as follows:</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a><span data-ttu-id="ce4b5-148">См. также</span><span class="sxs-lookup"><span data-stu-id="ce4b5-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce4b5-149">Объекты критических секций</span><span class="sxs-lookup"><span data-stu-id="ce4b5-149">Critical Section Objects</span></span>](critical-section-objects.md)
</dt> <dt>

[<span data-ttu-id="ce4b5-150">Доступ к блокируемым переменным</span><span class="sxs-lookup"><span data-stu-id="ce4b5-150">Interlocked Variable Access</span></span>](interlocked-variable-access.md)
</dt> <dt>

[<span data-ttu-id="ce4b5-151">Функции Wait</span><span class="sxs-lookup"><span data-stu-id="ce4b5-151">Wait Functions</span></span>](wait-functions.md)
</dt> </dl>

 

 



