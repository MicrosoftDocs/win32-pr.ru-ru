---
description: С помощью предупреждений I/O потоки приложений обрабатывают асинхронные запросы ввода-вывода только в том случае, если они находятся в состоянии оповещения.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: Ввод-вывод с оповещением
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683047"
---
# <a name="alertable-io"></a><span data-ttu-id="f9c6f-103">Ввод-вывод с оповещением</span><span class="sxs-lookup"><span data-stu-id="f9c6f-103">Alertable I/O</span></span>

<span data-ttu-id="f9c6f-104">С помощью предупреждений I/O потоки приложений обрабатывают асинхронные запросы ввода-вывода только в том случае, если они находятся в состоянии оповещения.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-104">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span>

<span data-ttu-id="f9c6f-105">Чтобы понять, когда поток находится в состоянии оповещения, рассмотрим следующий сценарий:</span><span class="sxs-lookup"><span data-stu-id="f9c6f-105">To understand when a thread is in an alertable state, consider the following scenario:</span></span>

1.  <span data-ttu-id="f9c6f-106">Поток инициирует асинхронный запрос на чтение путем вызова [**реадфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) с указателем на функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-106">A thread initiates an asynchronous read request by calling [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) with a pointer to a callback function.</span></span>
2.  <span data-ttu-id="f9c6f-107">Поток инициирует асинхронный запрос на запись путем вызова [**вритефиликс**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) с указателем на функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-107">The thread initiates an asynchronous write request by calling [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) with a pointer to a callback function.</span></span>
3.  <span data-ttu-id="f9c6f-108">Поток вызывает функцию, которая извлекает строку данных с удаленного сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-108">The thread calls a function that fetches a row of data from a remote database server.</span></span>

<span data-ttu-id="f9c6f-109">В этом сценарии вызовы [**реадфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) и [**вритефиликс**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) , скорее всего, будут возвращаться перед вызовом функции на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-109">In this scenario, the calls to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) will most likely return before the function call in step 3.</span></span> <span data-ttu-id="f9c6f-110">В этом случае ядро размещает указатели на функции обратного вызова в очереди асинхронного вызова процедур (APC) потока.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-110">When they do, the kernel places the pointers to the callback functions on the thread's Asynchronous Procedure Call (APC) queue.</span></span> <span data-ttu-id="f9c6f-111">Ядро поддерживает эту очередь специально для хранения возвращенных данных запроса ввода-вывода до тех пор, пока они не будут обработаны соответствующим потоком.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-111">The kernel maintains this queue specifically to hold returned I/O request data until it can be processed by the corresponding thread.</span></span>

<span data-ttu-id="f9c6f-112">Когда выборка строки завершается и поток возвращается из функции, его наивысший приоритет заключается в обработке возвращенных запросов ввода-вывода в очереди путем вызова функций обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-112">When the row fetch is complete and the thread returns from the function, its highest priority is to process the returned I/O requests on the queue by calling the callback functions.</span></span> <span data-ttu-id="f9c6f-113">Для этого необходимо ввести оповещенное состояние.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-113">To do this, it must enter an alertable state.</span></span> <span data-ttu-id="f9c6f-114">Поток может сделать это, вызвав одну из следующих функций с соответствующими флагами:</span><span class="sxs-lookup"><span data-stu-id="f9c6f-114">A thread can only do this by calling one of the following functions with the appropriate flags:</span></span>

-   [<span data-ttu-id="f9c6f-115">**слипекс**</span><span class="sxs-lookup"><span data-stu-id="f9c6f-115">**SleepEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [<span data-ttu-id="f9c6f-116">**WaitForSingleObjectEx**</span><span class="sxs-lookup"><span data-stu-id="f9c6f-116">**WaitForSingleObjectEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [<span data-ttu-id="f9c6f-117">**ваитформултиплеобжектсекс**</span><span class="sxs-lookup"><span data-stu-id="f9c6f-117">**WaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [<span data-ttu-id="f9c6f-118">**сигналобжектандваит**</span><span class="sxs-lookup"><span data-stu-id="f9c6f-118">**SignalObjectAndWait**</span></span>](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [<span data-ttu-id="f9c6f-119">**мсгваитформултиплеобжектсекс**</span><span class="sxs-lookup"><span data-stu-id="f9c6f-119">**MsgWaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

<span data-ttu-id="f9c6f-120">Когда поток попадает в состояние оповещения, происходят следующие события:</span><span class="sxs-lookup"><span data-stu-id="f9c6f-120">When the thread enters an alertable state, the following events occur:</span></span>

1.  <span data-ttu-id="f9c6f-121">Ядро проверяет очередь APC потока.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-121">The kernel checks the thread's APC queue.</span></span> <span data-ttu-id="f9c6f-122">Если очередь содержит указатели на функцию обратного вызова, ядро удаляет указатель из очереди и отправляет его в поток.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-122">If the queue contains callback function pointers, the kernel removes the pointer from the queue and sends it to the thread.</span></span>
2.  <span data-ttu-id="f9c6f-123">Поток выполняет функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-123">The thread executes the callback function.</span></span>
3.  <span data-ttu-id="f9c6f-124">Шаги 1 и 2 повторяются для каждого указателя, оставшегося в очереди.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-124">Steps 1 and 2 are repeated for each pointer remaining in the queue.</span></span>
4.  <span data-ttu-id="f9c6f-125">Если очередь пуста, поток возвращается из функции, которая поместила ее в состояние оповещения.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-125">When the queue is empty, the thread returns from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="f9c6f-126">В этом сценарии, когда поток переходит в состояние оповещения, он вызывает функции обратного вызова, отправленные в [**реадфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) и [**вритефиликс**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), а затем возвращает из функции, которая поместила ее в оповещенное состояние.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-126">In this scenario, once the thread enters an alertable state it will call the callback functions sent to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), then return from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="f9c6f-127">Если поток переходит в состояние оповещения, когда очередь APC пуста, выполнение потока будет приостановлено ядром до тех пор, пока не произойдет одно из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="f9c6f-127">If a thread enters an alertable state while its APC queue is empty, the thread's execution will be suspended by the kernel until one of the following occurs:</span></span>

-   <span data-ttu-id="f9c6f-128">Объект ядра, который находится в состоянии ожидания, получает сигнал.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-128">The kernel object that is being waited on becomes signaled.</span></span>
-   <span data-ttu-id="f9c6f-129">Указатель функции обратного вызова помещается в очередь APC.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-129">A callback function pointer is placed in the APC queue.</span></span>

<span data-ttu-id="f9c6f-130">Поток, использующий обработанные операции ввода-вывода, обрабатывает асинхронные запросы ввода-вывода более эффективно, чем при простом ожидании установленного флага события в структуре [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , а механизм с оповещением ввода-вывода менее сложен по сравнению с [портами завершения ввода-вывода](i-o-completion-ports.md) .</span><span class="sxs-lookup"><span data-stu-id="f9c6f-130">A thread that uses alertable I/O processes asynchronous I/O requests more efficiently than when they simply wait on the event flag in the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure to be set, and the alertable I/O mechanism is less complicated than [I/O completion ports](i-o-completion-ports.md) to use.</span></span> <span data-ttu-id="f9c6f-131">Однако при этом операция ввода-вывода с оповещением возвращает результат запроса ввода-вывода только в поток, который инициировал его.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-131">However, alertable I/O returns the result of the I/O request only to the thread that initiated it.</span></span> <span data-ttu-id="f9c6f-132">Порты завершения ввода-вывода не имеют этого ограничения.</span><span class="sxs-lookup"><span data-stu-id="f9c6f-132">I/O completion ports do not have this limitation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9c6f-133">См. также</span><span class="sxs-lookup"><span data-stu-id="f9c6f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9c6f-134">Асинхронные вызовы процедур</span><span class="sxs-lookup"><span data-stu-id="f9c6f-134">Asynchronous Procedure Calls</span></span>](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
