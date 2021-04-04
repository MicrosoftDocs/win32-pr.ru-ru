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
# <a name="implementing-input-pipes-on-the-server"></a><span data-ttu-id="f5a97-103">Реализация входных каналов на сервере</span><span class="sxs-lookup"><span data-stu-id="f5a97-103">Implementing Input Pipes on the Server</span></span>

<span data-ttu-id="f5a97-104">Чтобы начать отправку данных на сервер, клиент вызывает одну из удаленных процедур сервера.</span><span class="sxs-lookup"><span data-stu-id="f5a97-104">To begin sending data to a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="f5a97-105">Эта процедура должна многократно вызывать процедуру Pull в заглушке сервера.</span><span class="sxs-lookup"><span data-stu-id="f5a97-105">This procedure must repeatedly call the pull procedure in the server's stub.</span></span> <span data-ttu-id="f5a97-106">Компилятор MIDL использует IDL-файл приложения для автоматического создания процедуры по запросу сервера.</span><span class="sxs-lookup"><span data-stu-id="f5a97-106">The MIDL compiler uses the application's IDL file to automatically generate the server's pull procedure.</span></span>

<span data-ttu-id="f5a97-107">Каждый раз, когда серверная программа вызывает процедуру извлечения в своей заглушке, процедура извлечения получает блоки данных от клиента.</span><span class="sxs-lookup"><span data-stu-id="f5a97-107">Each time the server program invokes the pull procedure in its stub, the pull procedure receives blocks of data from the client.</span></span> <span data-ttu-id="f5a97-108">Отменяет упаковку данных в буфер сервера.</span><span class="sxs-lookup"><span data-stu-id="f5a97-108">It unmarshals the data into the server's buffer.</span></span> <span data-ttu-id="f5a97-109">После этого Удаленная процедура сервера может обрабатывать эти данные любым необходимым образом.</span><span class="sxs-lookup"><span data-stu-id="f5a97-109">The server's remote procedure can then process this data in any way required.</span></span> <span data-ttu-id="f5a97-110">Цикл будет продолжен до тех пор, пока сервер не получит буфер нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="f5a97-110">The loop continues until the server receives a buffer of zero length.</span></span>

<span data-ttu-id="f5a97-111">Следующий пример взят из программы Пипедемо, содержащейся в примерах, поступающих с пакетом SDK для платформы (Software Development Kit).</span><span class="sxs-lookup"><span data-stu-id="f5a97-111">The following example is from the Pipedemo program contained in the samples that come with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="f5a97-112">В нем показана процедура удаленного сервера, использующая канал для извлечения данных с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="f5a97-112">It illustrates a remote server procedure that uses a pipe to pull data from the client to the server.</span></span>

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

 

 




