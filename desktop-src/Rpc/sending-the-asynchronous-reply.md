---
title: Отправка асинхронного ответа
description: По завершении асинхронного вызова сервер отправляет клиенту ответ, вызывая функцию Рпкасинккомплетекалл и передавая ей асинхронный обработчик.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f861c3f2a1befdb85435f5275176c82e23bb06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068425"
---
# <a name="sending-the-asynchronous-reply"></a><span data-ttu-id="529e1-103">Отправка асинхронного ответа</span><span class="sxs-lookup"><span data-stu-id="529e1-103">Sending the Asynchronous Reply</span></span>

<span data-ttu-id="529e1-104">По завершении асинхронного вызова сервер отправляет клиенту ответ, вызывая функцию [**рпкасинккомплетекалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) и передавая ей асинхронный обработчик.</span><span class="sxs-lookup"><span data-stu-id="529e1-104">When the asynchronous call is complete, the server sends a reply to the client by calling the [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) function and passing it the asynchronous handle.</span></span> <span data-ttu-id="529e1-105">Этот вызов необходим, даже если асинхронный вызов имеет возвращаемое значение void и не \[ имеет \] параметров out.</span><span class="sxs-lookup"><span data-stu-id="529e1-105">This call is necessary even if the asynchronous call has a void return value and no \[out\] parameters.</span></span> <span data-ttu-id="529e1-106">Если функция имеет возвращаемое значение, она передается по ссылке на **рпкасинккомплетекалл**.</span><span class="sxs-lookup"><span data-stu-id="529e1-106">If the function has a return value, it is passed by reference to **RpcAsyncCompleteCall**.</span></span>

<span data-ttu-id="529e1-107">Когда сервер вызывает [**рпкасинккомплетекалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) или **рпкасинкаборткалл** или вызов завершается, поскольку в подпрограммы диспетчера сервера возникло исключение, Библиотека времени выполнения RPC автоматически уничтожает асинхронный обработчик сервера.</span><span class="sxs-lookup"><span data-stu-id="529e1-107">When the server calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) or **RpcAsyncAbortCall**, or a call completes because an exception was raised in the server-manager routine, the RPC run-time library automatically destroys the server's asynchronous handle.</span></span>

> [!Note]  
> <span data-ttu-id="529e1-108">\[ \] \[ \] Перед вызовом **рпкасинккомплетекалл** сервер должен завершить обновление параметров In, out и out.</span><span class="sxs-lookup"><span data-stu-id="529e1-108">The server must finish updating the \[in, out\] and \[out\] parameters before calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="529e1-109">Невозможно внести изменения в эти параметры или асинхронный обработчик после вызова **рпкасинккомплетекалл**.</span><span class="sxs-lookup"><span data-stu-id="529e1-109">No changes can be made to those parameters or to the asynchronous handle after calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="529e1-110">Если вызов функции **рпкасинккомплетекалл** завершается ошибкой, среда выполнения RPC освобождает параметры.</span><span class="sxs-lookup"><span data-stu-id="529e1-110">If the **RpcAsyncCompleteCall** function call fails, the RPC runtime frees the parameters.</span></span>

 

<span data-ttu-id="529e1-111">В следующем примере демонстрируется простой асинхронный вызов процедуры.</span><span class="sxs-lookup"><span data-stu-id="529e1-111">The following example demonstrates a simple asynchronous procedure call.</span></span>


```C++
#define DEFAULT_ASYNC_DELAY 20;
#define ASYNC_CANCEL_CHECK 100;

void AsyncFunc(IN PRPC_ASYNC_STATE pAsync,
               IN RPC_BINDING_HANDLE hBinding,
               IN OUT unsigned long nAsychDelay)
{
    int nReply = 1;
    RPC_STATUS status;
    unsigned long nTmpAsychDelay;
    int i;
 
    if (nAsychDelay < 0){
        nAsychDelay = DEFAULT_ASYNC_DELAY;
    }else if (nAsychDelay < 100){
        nAsychDelay = 100;
    }

    // We only call RpcServerTestCancel if the call
    // takes longer than ASYNC_CANCEL_CHECK ms
    if(nAsychDelay > ASYNC_CANCEL_CHECK){
        
        nTmpAsychDelay = nAsychDelay/100;
 
        for (i = 0; i < 100; i++){
            Sleep(nTmpAsychDelay);
 
            if (i%5 == 0){
                fprintf(stderr, 
                        "\rRunning AsyncFunc (%lu ms) (%d%c) ... ",
                        nAsychDelay, i+5, PERCENT);
 
                status = 
                    RpcServerTestCancel(
                        RpcAsyncGetCallHandle(pAsync));
                if (status == RPC_S_OK){
                    fprintf(stderr, 
                            "\nAsyncFunc has been canceled!!!\n");
                    break;
                }else if (status != RPC_S_CALL_IN_PROGRESS){
                    printf(
                        "RpcAsyncInitializeHandle returned 0x%x\n", 
                        status);
                    exit(status); 
                }
            }
        }
    }else{
        Sleep(nAsychDelay);
    }
 
    printf("\nCalling RpcAsyncCompleteCall\n");
    status = RpcAsyncCompleteCall(pAsync, &nReply);
    printf("RpcAsyncCompleteCall returned 0x%x\n", status);
    if (status){
        exit(status);
    }
}
```



<span data-ttu-id="529e1-112">Для простоты эта асинхронная Серверная процедура не обрабатывает фактические данные.</span><span class="sxs-lookup"><span data-stu-id="529e1-112">For the sake of simplicity, this asynchronous server routine does not process actual data.</span></span> <span data-ttu-id="529e1-113">Он просто помещает себя в спящий режим в течение некоторого времени.</span><span class="sxs-lookup"><span data-stu-id="529e1-113">It simply puts itself to sleep for awhile.</span></span>

> [!Note]  
> <span data-ttu-id="529e1-114">Функцию **рпкасинккомплетекалл** можно вызывать либо в потоке, который получил вызов, либо в любом другом потоке в процессе.</span><span class="sxs-lookup"><span data-stu-id="529e1-114">The **RpcAsyncCompleteCall** function can be called either on the thread that received the call, or on any other thread in the process.</span></span> <span data-ttu-id="529e1-115">Если все данные, необходимые для завершения вызова, доступны, сервер может заполнить их в одном потоке и вызвать **рпкасинккомплетекалл** в том же потоке.</span><span class="sxs-lookup"><span data-stu-id="529e1-115">If all the data necessary to complete the call are readily available, the server may fill them in on the same thread, and call the **RpcAsyncCompleteCall** on the same thread.</span></span> <span data-ttu-id="529e1-116">Этот подход позволяет сохранить некоторые контекстные переключения и повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="529e1-116">This approach saves some context switching and improves performance.</span></span> <span data-ttu-id="529e1-117">Такие вызовы называются рационально асинхронными.</span><span class="sxs-lookup"><span data-stu-id="529e1-117">Such calls are called opportunistically asynchronous.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="529e1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="529e1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="529e1-119">**\_асинхронное \_ Состояние RPC**</span><span class="sxs-lookup"><span data-stu-id="529e1-119">**RPC\_ASYNC\_STATE**</span></span>](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[<span data-ttu-id="529e1-120">**рпкасинккомплетекалл**</span><span class="sxs-lookup"><span data-stu-id="529e1-120">**RpcAsyncCompleteCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[<span data-ttu-id="529e1-121">**рпкасинкаборткалл**</span><span class="sxs-lookup"><span data-stu-id="529e1-121">**RpcAsyncAbortCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[<span data-ttu-id="529e1-122">**рпксервертестканцел**</span><span class="sxs-lookup"><span data-stu-id="529e1-122">**RpcServerTestCancel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




