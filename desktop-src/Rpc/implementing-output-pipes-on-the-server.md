---
title: Реализация выходных каналов на сервере
description: Чтобы начать получать данные с сервера, клиент вызывает одну из удаленных процедур сервера.
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3eb1362736207f9cc79d82ab6c981431d0bfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070506"
---
# <a name="implementing-output-pipes-on-the-server"></a><span data-ttu-id="b53eb-103">Реализация выходных каналов на сервере</span><span class="sxs-lookup"><span data-stu-id="b53eb-103">Implementing Output Pipes on the Server</span></span>

<span data-ttu-id="b53eb-104">Чтобы начать получать данные с сервера, клиент вызывает одну из удаленных процедур сервера.</span><span class="sxs-lookup"><span data-stu-id="b53eb-104">To begin receiving data from a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="b53eb-105">Эта процедура должна многократно вызывать процедуру принудительной отправки в заглушке сервера.</span><span class="sxs-lookup"><span data-stu-id="b53eb-105">This procedure must repeatedly call the push procedure in the server's stub.</span></span> <span data-ttu-id="b53eb-106">Компилятор MIDL использует IDL-файл приложения для автоматического создания принудительной процедуры сервера.</span><span class="sxs-lookup"><span data-stu-id="b53eb-106">The MIDL compiler uses the application's IDL file to automatically generate the server's push procedure.</span></span>

<span data-ttu-id="b53eb-107">Процедура удаленного сервера должна заполнить буфер выходного конвейера данными перед вызовом процедуры Push.</span><span class="sxs-lookup"><span data-stu-id="b53eb-107">The remote server routine must fill the output pipe's buffer with data before it calls the push procedure.</span></span> <span data-ttu-id="b53eb-108">Каждый раз, когда серверная программа вызывает процедуру Push в своей заглушке, процедура Push маршалирует данные и передает их клиенту.</span><span class="sxs-lookup"><span data-stu-id="b53eb-108">Each time the server program invokes the push procedure in its stub, the push procedure marshals the data and transmits it to the client.</span></span> <span data-ttu-id="b53eb-109">Цикл продолжится до тех пор, пока сервер не отправит буфер нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="b53eb-109">The loop continues until the server sends a buffer of zero length.</span></span>

<span data-ttu-id="b53eb-110">Следующий пример взят из программы Пипедемо, содержащейся в примерах, которые входят в состав Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b53eb-110">The following example is from the Pipedemo program contained in the samples that come with the Windows SDK.</span></span> <span data-ttu-id="b53eb-111">В нем показана процедура удаленного сервера, использующая канал для отправки данных с сервера клиенту.</span><span class="sxs-lookup"><span data-stu-id="b53eb-111">It illustrates a remote server procedure that uses a pipe to push data from the server to the client.</span></span>


```C++
void OutPipe(LONG_PIPE *outputPipe )
{
    long *outputPipeData;
    ulong index = 0;
    ulong elementsToSend = PIPE_TRANSFER_SIZE;
 
    /* Allocate memory for the data to be passed back in the pipe */
    outputPipeData = (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    while(elementsToSend >0) /* Loop to send pipe data elements */
    {
        if (index >= PIPE_SIZE)
            elementsToSend = 0;
        else
        {
            if ( (index + PIPE_TRANSFER_SIZE) > PIPE_SIZE )
                elementsToSend = PIPE_SIZE - index;
            else
                elementsToSend = PIPE_TRANSFER_SIZE;
        }
                    
        outputPipe->push( outputPipe->state,
                          &(outputPipeData[index]),
                          elementsToSend ); 
        index += elementsToSend;
 
    } //end while
 
    free((void *)outputPipeData);
 
}
```



## <a name="related-topics"></a><span data-ttu-id="b53eb-112">См. также</span><span class="sxs-lookup"><span data-stu-id="b53eb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b53eb-113">дать</span><span class="sxs-lookup"><span data-stu-id="b53eb-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="b53eb-114">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="b53eb-114">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 