---
title: Выполнение асинхронного вызова
description: Прежде чем он сможет выполнить асинхронный удаленный вызов, клиент должен инициализировать асинхронный обработчик. В клиентских и серверных программах \_ \_ для асинхронных дескрипторов используются указатели на структуру асинхронного состояния RPC.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- Удаленный вызов процедур RPC, задачи, выполнение асинхронных вызовов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d8399071cae6ea39aaac3f966e7e799b2c93b32a152048a7d18282b465f929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928380"
---
# <a name="making-the-asynchronous-call"></a>Выполнение асинхронного вызова

Прежде чем он сможет выполнить асинхронный удаленный вызов, клиент должен инициализировать асинхронный обработчик. В клиентских и серверных программах для асинхронных дескрипторов используются указатели на структуру асинхронного [**\_ \_ состояния RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) .

Каждый необработанный вызов должен иметь собственный уникальный асинхронный обработчик. Клиент создает этот обработчик и передает его в функцию [**рпкасинЦинитиализехандле**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) . Для правильного выполнения вызова клиент должен убедиться, что память для этого маркера не освобождена, пока не получит асинхронный ответ сервера. Кроме того, перед выполнением другого вызова в существующем асинхронном обработчике клиент должен повторно инициализировать этот обработчик. Невыполнение этого действия может привести к тому, что клиентская заглушка вызовет исключение во время вызова. Клиент должен также убедиться, что буферы, предоставляемые для \[ [**исходящих**](/windows/desktop/Midl/out-idl) \] параметров и \[ [**в**](/windows/desktop/Midl/in), **выходные** \] параметры для асинхронной удаленной процедуры остаются выделенными до получения ответа от сервера.

При вызове асинхронной удаленной процедуры клиент должен выбрать метод, который библиотека времени выполнения RPC будет использовать для уведомления о завершении вызова. Клиент может получить это уведомление одним из следующих способов:

-   Событие. Клиент может указать событие, которое должно запускаться по завершении вызова. Дополнительные сведения см. в разделе [объекты событий](/windows/desktop/Sync/event-objects).
-   опрос; Клиент может многократно вызывать [**рпкасинкжеткаллстатус**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus). Если возвращаемое значение отличается \_ \_ от асинхронного вызова RPC S \_ \_ , вызов завершен. Этот метод использует больше времени ЦП, чем другие методы, описанные здесь.
-   APC. Клиент может указать [асинхронный вызов процедуры (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) , который вызывается по завершении вызова. Прототип функции APC см. в разделе [**\_ подпрограммы рпкнотификатион**](/previous-versions/aa375808(v=vs.80)). Метод APC вызывается с параметром Event, имеющим значение Рпккаллкомплете. Чтобы APC можно было отправить, клиентский поток должен находиться в состоянии ожидания с оповещением.

    Если поле **хсреад** в асинхронном обработчике имеет значение 0, APC помещаются в очередь в потоке, который выполнил асинхронный вызов. Если он не равен нулю, APC помещается в очередь в потоке, заданном параметром m.

-   Инфраструктур. Порт завершения ввода-вывода получает уведомление с параметрами, указанными в асинхронном обработчике. Дополнительные сведения см. в разделе [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).
-   Windowsный обработчик. Сообщение отправляется в указанный дескриптор окна (HWND).

В следующем фрагменте кода показаны необходимые шаги для инициализации асинхронного обработчика и его использования для выполнения асинхронного вызова удаленной процедуры.


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



Как показано в этом примере, клиентская программа может выполнять синхронные удаленные вызовы процедур, пока асинхронный вызов процедуры все еще находится в состоянии ожидания. Этот клиент создает объект события для библиотеки времени выполнения RPC, который используется для уведомления о завершении асинхронного вызова.

> [!Note]  
> Уведомление о завершении не будет возвращено из асинхронной подпрограммы RPC, если во время асинхронного вызова возникает исключение RPC.

 

 

 