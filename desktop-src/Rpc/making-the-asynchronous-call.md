---
title: Выполнение асинхронного вызова
description: Прежде чем он сможет выполнить асинхронный удаленный вызов, клиент должен инициализировать асинхронный обработчик. В клиентских и серверных программах \_ \_ для асинхронных дескрипторов используются указатели на структуру асинхронного состояния RPC.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- Удаленный вызов процедур RPC, задачи, выполнение асинхронных вызовов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa06f60b43a7dff3a29223ff1d8e9ad726c0e938
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672345"
---
# <a name="making-the-asynchronous-call"></a><span data-ttu-id="08164-105">Выполнение асинхронного вызова</span><span class="sxs-lookup"><span data-stu-id="08164-105">Making the Asynchronous Call</span></span>

<span data-ttu-id="08164-106">Прежде чем он сможет выполнить асинхронный удаленный вызов, клиент должен инициализировать асинхронный обработчик.</span><span class="sxs-lookup"><span data-stu-id="08164-106">Before it can make an asynchronous remote call, the client must initialize the asynchronous handle.</span></span> <span data-ttu-id="08164-107">В клиентских и серверных программах для асинхронных дескрипторов используются указатели на структуру асинхронного [**\_ \_ состояния RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) .</span><span class="sxs-lookup"><span data-stu-id="08164-107">Client and server programs use pointers to the [**RPC\_ASYNC\_STATE**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) structure for asynchronous handles.</span></span>

<span data-ttu-id="08164-108">Каждый необработанный вызов должен иметь собственный уникальный асинхронный обработчик.</span><span class="sxs-lookup"><span data-stu-id="08164-108">Every outstanding call must have its own unique asynchronous handle.</span></span> <span data-ttu-id="08164-109">Клиент создает этот обработчик и передает его в функцию [**рпкасинЦинитиализехандле**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) .</span><span class="sxs-lookup"><span data-stu-id="08164-109">The client creates the handle and passes it to the [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) function.</span></span> <span data-ttu-id="08164-110">Для правильного выполнения вызова клиент должен убедиться, что память для этого маркера не освобождена, пока не получит асинхронный ответ сервера.</span><span class="sxs-lookup"><span data-stu-id="08164-110">For the call to complete correctly, the client must ensure that the memory for the handle is not released until it receives the server's asynchronous reply.</span></span> <span data-ttu-id="08164-111">Кроме того, перед выполнением другого вызова в существующем асинхронном обработчике клиент должен повторно инициализировать этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="08164-111">Also, before making another call on an existing asynchronous handle, the client must reinitialize the handle.</span></span> <span data-ttu-id="08164-112">Невыполнение этого действия может привести к тому, что клиентская заглушка вызовет исключение во время вызова.</span><span class="sxs-lookup"><span data-stu-id="08164-112">Failure to do this can cause the client stub to raise an exception during the call.</span></span> <span data-ttu-id="08164-113">Клиент должен также убедиться, что буферы, предоставляемые для \[ [**исходящих**](/windows/desktop/Midl/out-idl) \] параметров и \[ [**в**](/windows/desktop/Midl/in), **выходные** \] параметры для асинхронной удаленной процедуры остаются выделенными до получения ответа от сервера.</span><span class="sxs-lookup"><span data-stu-id="08164-113">The client must also ensure that the buffers it supplies for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters and \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to an asynchronous remote procedure remain allocated until it has received the reply from the server.</span></span>

<span data-ttu-id="08164-114">При вызове асинхронной удаленной процедуры клиент должен выбрать метод, который библиотека времени выполнения RPC будет использовать для уведомления о завершении вызова.</span><span class="sxs-lookup"><span data-stu-id="08164-114">When it invokes an asynchronous remote procedure, the client must select the method that the RPC run-time library will use to notify it of the call's completion.</span></span> <span data-ttu-id="08164-115">Клиент может получить это уведомление одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="08164-115">The client can receive this notification in any one of the following ways:</span></span>

-   <span data-ttu-id="08164-116">Журнале.</span><span class="sxs-lookup"><span data-stu-id="08164-116">Event.</span></span> <span data-ttu-id="08164-117">Клиент может указать событие, которое должно запускаться по завершении вызова.</span><span class="sxs-lookup"><span data-stu-id="08164-117">The client can specify an event to be fired when the call has completed.</span></span> <span data-ttu-id="08164-118">Дополнительные сведения см. в разделе [объекты событий](/windows/desktop/Sync/event-objects).</span><span class="sxs-lookup"><span data-stu-id="08164-118">For details, see [Event Objects](/windows/desktop/Sync/event-objects).</span></span>
-   <span data-ttu-id="08164-119">опрос;</span><span class="sxs-lookup"><span data-stu-id="08164-119">Polling.</span></span> <span data-ttu-id="08164-120">Клиент может многократно вызывать [**рпкасинкжеткаллстатус**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span><span class="sxs-lookup"><span data-stu-id="08164-120">The client can repeatedly call [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="08164-121">Если возвращаемое значение отличается \_ \_ от асинхронного вызова RPC S \_ \_ , вызов завершен.</span><span class="sxs-lookup"><span data-stu-id="08164-121">If the return value is anything other than RPC\_S\_ASYNC\_CALL\_PENDING, the call is complete.</span></span> <span data-ttu-id="08164-122">Этот метод использует больше времени ЦП, чем другие методы, описанные здесь.</span><span class="sxs-lookup"><span data-stu-id="08164-122">This method uses more CPU time than the other methods described here.</span></span>
-   <span data-ttu-id="08164-123">APC.</span><span class="sxs-lookup"><span data-stu-id="08164-123">APC.</span></span> <span data-ttu-id="08164-124">Клиент может указать [асинхронный вызов процедуры (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) , который вызывается по завершении вызова.</span><span class="sxs-lookup"><span data-stu-id="08164-124">The client can specify an [asynchronous procedure call (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) that gets called when the call completes.</span></span> <span data-ttu-id="08164-125">Прототип функции APC см. в разделе [**\_ подпрограммы рпкнотификатион**](/previous-versions/aa375808(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="08164-125">For the prototype of the APC function, see [**RPCNOTIFICATION\_ROUTINE**](/previous-versions/aa375808(v=vs.80)).</span></span> <span data-ttu-id="08164-126">Метод APC вызывается с параметром Event, имеющим значение Рпккаллкомплете.</span><span class="sxs-lookup"><span data-stu-id="08164-126">The APC is called with its Event parameter set to RpcCallComplete.</span></span> <span data-ttu-id="08164-127">Чтобы APC можно было отправить, клиентский поток должен находиться в состоянии ожидания с оповещением.</span><span class="sxs-lookup"><span data-stu-id="08164-127">For APCs to get dispatched, the client thread must be in an alertable wait state.</span></span>

    <span data-ttu-id="08164-128">Если поле **хсреад** в асинхронном обработчике имеет значение 0, APC помещаются в очередь в потоке, который выполнил асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="08164-128">If the **hThread** field in the asynchronous handle is set to 0, the APCs are queued on the thread that made the asynchronous call.</span></span> <span data-ttu-id="08164-129">Если он не равен нулю, APC помещается в очередь в потоке, заданном параметром m.</span><span class="sxs-lookup"><span data-stu-id="08164-129">If it is nonzero, the APCs are queued on the thread specified by m.</span></span>

-   <span data-ttu-id="08164-130">Инфраструктур.</span><span class="sxs-lookup"><span data-stu-id="08164-130">IOC.</span></span> <span data-ttu-id="08164-131">Порт завершения ввода-вывода получает уведомление с параметрами, указанными в асинхронном обработчике.</span><span class="sxs-lookup"><span data-stu-id="08164-131">The I/O completion port is notified with the parameters specified in the asynchronous handle.</span></span> <span data-ttu-id="08164-132">Дополнительные сведения см. в разделе [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span><span class="sxs-lookup"><span data-stu-id="08164-132">For more information, see [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span></span>
-   <span data-ttu-id="08164-133">Маркер Windows.</span><span class="sxs-lookup"><span data-stu-id="08164-133">Windows handle.</span></span> <span data-ttu-id="08164-134">Сообщение отправляется в указанный дескриптор окна (HWND).</span><span class="sxs-lookup"><span data-stu-id="08164-134">A message is posted to the specified window handle (HWND).</span></span>

<span data-ttu-id="08164-135">В следующем фрагменте кода показаны необходимые шаги для инициализации асинхронного обработчика и его использования для выполнения асинхронного вызова удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="08164-135">The following code fragment shows the essential steps required for initializing an asynchronous handle and using it to make an asynchronous remote procedure call.</span></span>


```C++
RPC_ASYNC_STATE Async;
RPC_STATUS status;
 
// Initialize the handle.
status = RpcAsyncInitializeHandle(&Async, sizeof(RPC_ASYNC_STATE));
if (status)
{
    // Code to handle the error goes here.
}
 
Async.UserInfo = NULL;
Async.NotificationType = RpcNotificationTypeEvent;
 
Async.u.hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (Async.u.hEvent == 0)
{
    // Code to handle the error goes here.
}
// Call an asynchronous RPC routine here
RpcTryExcept
{
    printf("\nCalling the remote procedure 'AsyncFunc'\n");
    AsyncFunc(&Async, AsyncRPC_ClientIfHandle, nAsychDelay);
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("AsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
 
// Call a synchronous routine while
// the asynchronous procedure is still running
RpcTryExcept
{
    printf("\nCalling the remote procedure 'NonAsyncFunc'\n");
    NonAsyncFunc(AsyncRPC_ClientIfHandle, pszMessage);
    fprintf(stderr, 
            "While 'AsyncFunc' is running asynchronously,\n"
            "we still can send message to the server in the mean "
            "time.\n\n");
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("NonAsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
```



<span data-ttu-id="08164-136">Как показано в этом примере, клиентская программа может выполнять синхронные удаленные вызовы процедур, пока асинхронный вызов процедуры все еще находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="08164-136">As this example demonstrates, your client program can execute synchronous remote procedure calls while an asynchronous procedure call is still pending.</span></span> <span data-ttu-id="08164-137">Этот клиент создает объект события для библиотеки времени выполнения RPC, который используется для уведомления о завершении асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="08164-137">This client creates an event object for the RPC run-time library to use to notify it when the asynchronous call completes.</span></span>

> [!Note]  
> <span data-ttu-id="08164-138">Уведомление о завершении не будет возвращено из асинхронной подпрограммы RPC, если во время асинхронного вызова возникает исключение RPC.</span><span class="sxs-lookup"><span data-stu-id="08164-138">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during an asynchronous call.</span></span>

 

 

 