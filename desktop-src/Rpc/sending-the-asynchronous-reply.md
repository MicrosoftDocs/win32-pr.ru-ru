---
title: Отправка асинхронного ответа
description: По завершении асинхронного вызова сервер отправляет клиенту ответ, вызывая функцию Рпкасинккомплетекалл и передавая ей асинхронный обработчик.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdcaf4db4a27a49a8025596668893518c6b6c577a0d81d91189a44ec81df4de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925582"
---
# <a name="sending-the-asynchronous-reply"></a>Отправка асинхронного ответа

По завершении асинхронного вызова сервер отправляет клиенту ответ, вызывая функцию [**рпкасинккомплетекалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) и передавая ей асинхронный обработчик. Этот вызов необходим, даже если асинхронный вызов имеет возвращаемое значение void и не \[ имеет \] параметров out. Если функция имеет возвращаемое значение, она передается по ссылке на **рпкасинккомплетекалл**.

Когда сервер вызывает [**рпкасинккомплетекалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) или **рпкасинкаборткалл** или вызов завершается, поскольку в подпрограммы диспетчера сервера возникло исключение, Библиотека времени выполнения RPC автоматически уничтожает асинхронный обработчик сервера.

> [!Note]  
> \[ \] \[ \] Перед вызовом **рпкасинккомплетекалл** сервер должен завершить обновление параметров In, out и out. Невозможно внести изменения в эти параметры или асинхронный обработчик после вызова **рпкасинккомплетекалл**. Если вызов функции **рпкасинккомплетекалл** завершается ошибкой, среда выполнения RPC освобождает параметры.

 

В следующем примере демонстрируется простой асинхронный вызов процедуры.


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



Для простоты эта асинхронная Серверная процедура не обрабатывает фактические данные. Он просто помещает себя в спящий режим в течение некоторого времени.

> [!Note]  
> Функцию **рпкасинккомплетекалл** можно вызывать либо в потоке, который получил вызов, либо в любом другом потоке в процессе. Если все данные, необходимые для завершения вызова, доступны, сервер может заполнить их в одном потоке и вызвать **рпкасинккомплетекалл** в том же потоке. Этот подход позволяет сохранить некоторые контекстные переключения и повысить производительность. Такие вызовы называются рационально асинхронными.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**\_асинхронное \_ Состояние RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[**рпкасинккомплетекалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[**рпкасинкаборткалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[**рпксервертестканцел**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




