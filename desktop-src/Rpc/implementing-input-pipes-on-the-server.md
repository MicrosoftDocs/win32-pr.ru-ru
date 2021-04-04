---
title: Реализация входных каналов на сервере
description: Чтобы начать отправку данных на сервер, клиент вызывает одну из удаленных процедур сервера.
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d60c2436129b59619f5a9954c70823631d72ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888567"
---
# <a name="implementing-input-pipes-on-the-server"></a>Реализация входных каналов на сервере

Чтобы начать отправку данных на сервер, клиент вызывает одну из удаленных процедур сервера. Эта процедура должна многократно вызывать процедуру Pull в заглушке сервера. Компилятор MIDL использует IDL-файл приложения для автоматического создания процедуры по запросу сервера.

Каждый раз, когда серверная программа вызывает процедуру извлечения в своей заглушке, процедура извлечения получает блоки данных от клиента. Отменяет упаковку данных в буфер сервера. После этого Удаленная процедура сервера может обрабатывать эти данные любым необходимым образом. Цикл будет продолжен до тех пор, пока сервер не получит буфер нулевой длины.

Следующий пример взят из программы Пипедемо, содержащейся в примерах, поступающих с пакетом SDK для платформы (Software Development Kit). В нем показана процедура удаленного сервера, использующая канал для извлечения данных с клиента на сервер.

``` syntax
//file: server.c (fragment)
#include uc_server.c
#define PIPE_TRANSFER_SIZE 100 /* Transfer 100 pipe elements at one time */
 
void InPipe(LONG_PIPE     long_pipe )
{
    long local_pipe_buf[PIPE_TRANSFER_SIZE];
    ulong actual_transfer_count = PIPE_TRANSFER_SIZE;
 
    while(actual_transfer_count > 0) /* Loop to get all 
                                        the pipe data elements */
    {
        long_pipe.pull( long_pipe.state,
                        local_pipe_buf,
                        PIPE_TRANSFER_SIZE,
                        &actual_transfer_count);
        /* process the elements */
    } // end while
} //end InPipe
```

 

 




