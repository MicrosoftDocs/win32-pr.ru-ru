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
# <a name="implementing-output-pipes-on-the-server"></a>Реализация выходных каналов на сервере

Чтобы начать получать данные с сервера, клиент вызывает одну из удаленных процедур сервера. Эта процедура должна многократно вызывать процедуру принудительной отправки в заглушке сервера. Компилятор MIDL использует IDL-файл приложения для автоматического создания принудительной процедуры сервера.

Процедура удаленного сервера должна заполнить буфер выходного конвейера данными перед вызовом процедуры Push. Каждый раз, когда серверная программа вызывает процедуру Push в своей заглушке, процедура Push маршалирует данные и передает их клиенту. Цикл продолжится до тех пор, пока сервер не отправит буфер нулевой длины.

Следующий пример взят из программы Пипедемо, содержащейся в примерах, которые входят в состав Windows SDK. В нем показана процедура удаленного сервера, использующая канал для отправки данных с сервера клиенту.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[дать](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 