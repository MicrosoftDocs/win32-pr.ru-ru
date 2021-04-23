---
title: Ожидание асинхронного ответа
description: Клиент, выполняющий ожидание получения уведомления от сервера, зависит от механизма уведомления, который он выбирает.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- Удаленный вызов процедур RPC, задачи, ожидание асинхронных ответов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0890b3024a05bb704f7b5a803c4b1e517c65ee21
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338476"
---
# <a name="waiting-for-the-asynchronous-reply"></a><span data-ttu-id="0b161-104">Ожидание асинхронного ответа</span><span class="sxs-lookup"><span data-stu-id="0b161-104">Waiting for the Asynchronous Reply</span></span>

<span data-ttu-id="0b161-105">Клиент, выполняющий ожидание получения уведомления от сервера, зависит от механизма уведомления, который он выбирает.</span><span class="sxs-lookup"><span data-stu-id="0b161-105">What the client does while it waits to be notified of a reply from the server depends on the notification mechanism it selects.</span></span>

<span data-ttu-id="0b161-106">Если клиент использует событие для уведомления, обычно вызывается функция [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) или функция [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) .</span><span class="sxs-lookup"><span data-stu-id="0b161-106">If the client uses an event for notification, it will typically call the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function or the [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) function.</span></span> <span data-ttu-id="0b161-107">Клиент переходит в состояние блокировки при вызове любой из этих функций.</span><span class="sxs-lookup"><span data-stu-id="0b161-107">The client enters a blocked state when it calls either of these functions.</span></span> <span data-ttu-id="0b161-108">Это эффективно, так как клиент не потребляет циклы выполнения ЦП, пока он заблокирован.</span><span class="sxs-lookup"><span data-stu-id="0b161-108">This is efficient because the client does not consume CPU run cycles while it is blocked.</span></span>

<span data-ttu-id="0b161-109">При использовании опроса для ожидания его результатов клиентская программа вводит цикл, который многократно вызывает функцию [**рпкасинкжеткаллстатус**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span><span class="sxs-lookup"><span data-stu-id="0b161-109">When it uses polling to wait for its results, the client program enters a loop that repeatedly calls the function [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="0b161-110">Это эффективный метод ожидания, если клиентская программа выполняет другую обработку в цикле опроса.</span><span class="sxs-lookup"><span data-stu-id="0b161-110">This is an efficient method of waiting if your client program does other processing in the polling loop.</span></span> <span data-ttu-id="0b161-111">Например, он может подготовить данные в небольших блоках для последующего асинхронного вызова удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="0b161-111">For instance, it can prepare data in small chunks for a subsequent asynchronous remote procedure call.</span></span> <span data-ttu-id="0b161-112">После завершения каждого фрагмента клиент может опросить необработанный асинхронный вызов удаленной процедуры, чтобы убедиться, что он завершен.</span><span class="sxs-lookup"><span data-stu-id="0b161-112">After each chunk is finished, your client can poll the outstanding asynchronous remote procedure call to see if it is complete.</span></span>

<span data-ttu-id="0b161-113">Клиентская программа может предоставить асинхронный вызов процедур (APC), который представляет собой тип функции обратного вызова, которая будет вызываться библиотекой времени выполнения RPC при завершении асинхронного вызова удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="0b161-113">Your client program can provide an asynchronous procedure call (APC), which is a type of callback function that the RPC run-time library will invoke when the asynchronous remote procedure call completes.</span></span> <span data-ttu-id="0b161-114">Клиентская программа должна находиться в состоянии ожидания с оповещением.</span><span class="sxs-lookup"><span data-stu-id="0b161-114">Your client program must be in an alertable wait state.</span></span> <span data-ttu-id="0b161-115">Обычно это означает, что клиент вызывает функцию Windows API, чтобы перевести себя в заблокированное состояние.</span><span class="sxs-lookup"><span data-stu-id="0b161-115">This typically means that the client calls a Windows API function to put itself in a blocked state.</span></span> <span data-ttu-id="0b161-116">Дополнительные сведения см. в разделе [асинхронные вызовы процедур](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="0b161-116">For more information, see [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span>

> [!Note]  
> <span data-ttu-id="0b161-117">Уведомление о завершении не будет возвращено из асинхронной подпрограммы RPC, если во время асинхронного вызова возникает исключение RPC.</span><span class="sxs-lookup"><span data-stu-id="0b161-117">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during a asynchronous call.</span></span>

 

<span data-ttu-id="0b161-118">Если клиентская программа использует порт завершения ввода-вывода для получения уведомлений о завершении, он должен вызвать функцию [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="0b161-118">If your client program uses an I/O completion port to receive completion notification, it must call the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="0b161-119">В этом случае он может либо подождать неограниченное время ответа, либо продолжить обработку.</span><span class="sxs-lookup"><span data-stu-id="0b161-119">When it does, it can either wait indefinitely for a response or continue to do other processing.</span></span> <span data-ttu-id="0b161-120">Если он выполняет другие операции обработки, ожидая ответа, он должен опросить порт завершения с помощью функции **жеткуеуедкомплетионстатус** .</span><span class="sxs-lookup"><span data-stu-id="0b161-120">If it does other processing while it waits for a reply, it must poll the completion port with the **GetQueuedCompletionStatus** function.</span></span> <span data-ttu-id="0b161-121">В этом случае, как правило, необходимо установить *dwMilliseconds* в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0b161-121">In this case, it typically needs to set the *dwMilliseconds* to zero.</span></span> <span data-ttu-id="0b161-122">Это приводит к тому, что **жеткуеуедкомплетионстатус** будет возвращаться немедленно, даже если асинхронный вызов не завершен.</span><span class="sxs-lookup"><span data-stu-id="0b161-122">This causes **GetQueuedCompletionStatus** to return immediately, even if the asynchronous call has not completed.</span></span>

<span data-ttu-id="0b161-123">Клиентские программы также могут получить уведомление о завершении через очереди сообщений окна.</span><span class="sxs-lookup"><span data-stu-id="0b161-123">Client programs can also receive completion notification through their window message queues.</span></span> <span data-ttu-id="0b161-124">В этом случае они просто обрабатывают сообщение о завершении, как и любое сообщение Windows.</span><span class="sxs-lookup"><span data-stu-id="0b161-124">In this situation, they simply process the completion message as they would any Windows message.</span></span>

<span data-ttu-id="0b161-125">В многопоточном приложении асинхронный вызов может быть отменен Клиентом только после того, как поток, порожденный вызов, успешно возвращался из вызова.</span><span class="sxs-lookup"><span data-stu-id="0b161-125">In a multithreaded application, an asynchronous call can be canceled by the client only after the thread that originated the call has returned successfully from the call.</span></span> <span data-ttu-id="0b161-126">Это гарантирует, что вызов не будет асинхронно отменен другим потоком после сбоя синхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="0b161-126">This ensures that the call is not canceled asynchronously by another thread after it failed a synchronous call.</span></span> <span data-ttu-id="0b161-127">По стандартной практике асинхронный вызов, который завершается сбоем синхронно, не должен быть отменен асинхронно.</span><span class="sxs-lookup"><span data-stu-id="0b161-127">As standard practice, an asynchronous call that fails synchronously should not be canceled asynchronously.</span></span> <span data-ttu-id="0b161-128">Клиентское приложение должно наблюдать за этим поведением, если вызовы могут быть выданы и отменены в разных потоках.</span><span class="sxs-lookup"><span data-stu-id="0b161-128">The client application must observe this behavior if calls may be issued and canceled on different threads.</span></span> <span data-ttu-id="0b161-129">Кроме того, после отмены вызова клиентский код должен ждать уведомления о завершении и завершить вызов.</span><span class="sxs-lookup"><span data-stu-id="0b161-129">Also, after the call is canceled, the client code must wait for the completion notification and complete the call.</span></span> <span data-ttu-id="0b161-130">Функция [**рпкасинкканцелкалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) просто пропускует уведомление о завершении; Это не является заменой выполнению вызова.</span><span class="sxs-lookup"><span data-stu-id="0b161-130">The [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) function simply rushes the completion notification; it is not a substitute for completing the call.</span></span>

<span data-ttu-id="0b161-131">В следующем фрагменте кода показано, как клиентская программа может использовать событие для ожидания асинхронного ответа.</span><span class="sxs-lookup"><span data-stu-id="0b161-131">The following code fragment illustrates how a client program can use an event to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="0b161-132">Клиентские программы, использующие APC для получения уведомлений об асинхронном ответе, обычно переводят себя в заблокированное состояние.</span><span class="sxs-lookup"><span data-stu-id="0b161-132">Client programs that use an APC to receive notification of an asynchronous reply typically put themselves into a blocked state.</span></span> <span data-ttu-id="0b161-133">Это показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="0b161-133">The following code fragment shows this.</span></span>


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="0b161-134">В этом случае клиентская программа переходит в спящий режим, использующий циклы ЦП, пока библиотека времени выполнения RPC не вызовет APC (не показано).</span><span class="sxs-lookup"><span data-stu-id="0b161-134">In this case, the client program goes to sleep, consuming no CPU cycles, until the RPC run-time library calls the APC (not shown).</span></span>

<span data-ttu-id="0b161-135">В следующем примере демонстрируется клиент, использующий порт завершения ввода-вывода для ожидания асинхронного ответа.</span><span class="sxs-lookup"><span data-stu-id="0b161-135">The next example demonstrates a client that uses an I/O completion port to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (!GetQueuedCompletionStatus(
         Async.u.IOC.hIOPort,
         &Async.u.IOC.dwNumberOfBytesTransferred,
         &Async.u.IOC.dwCompletionKey,
         &Async.u.IOC.lpOverlapped,
         INFINITE))
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="0b161-136">В предыдущем примере вызов [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ожидает неограниченного времени до завершения асинхронного вызова удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="0b161-136">In the preceding example, the call to [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) waits indefinitely until the asynchronous remote procedure call completes.</span></span>

<span data-ttu-id="0b161-137">При написании многопоточных приложений возникает одна потенциальная ловушка.</span><span class="sxs-lookup"><span data-stu-id="0b161-137">One potential pitfall occurs when writing multithreaded applications.</span></span> <span data-ttu-id="0b161-138">Если поток вызывает удаленный вызов процедуры, а затем завершается перед получением уведомления о завершении отправки, вызов удаленной процедуры может завершиться ошибкой, и клиентская заглушка может закрыть соединение с сервером.</span><span class="sxs-lookup"><span data-stu-id="0b161-138">If a thread invokes a remote procedure call and then terminates before it receives notification that the send completed, the remote procedure call may fail and the client stub may close the connection to the server.</span></span> <span data-ttu-id="0b161-139">Поэтому потоки, вызывающие удаленную процедуру, не должны завершаться до завершения или отмены вызова, если поведение нежелательно.</span><span class="sxs-lookup"><span data-stu-id="0b161-139">Therefore, threads that call a remote procedure should not terminate before the call is completed or canceled when behavior is undesirable.</span></span>

 

 