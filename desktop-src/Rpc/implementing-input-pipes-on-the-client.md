---
title: Реализация входных каналов на клиенте
description: При использовании входного канала для передачи данных с клиента на сервер необходимо реализовать процедуру извлечения.
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810caa31c4932294797a5ed502c6f93d8613ea0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890900"
---
# <a name="implementing-input-pipes-on-the-client"></a><span data-ttu-id="a6a7d-103">Реализация входных каналов на клиенте</span><span class="sxs-lookup"><span data-stu-id="a6a7d-103">Implementing Input Pipes on the Client</span></span>

<span data-ttu-id="a6a7d-104">При использовании входного канала для передачи данных с клиента на сервер необходимо реализовать процедуру извлечения.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-104">When using an input pipe to transfer data from the client to the server, you must implement a pull procedure.</span></span> <span data-ttu-id="a6a7d-105">Процедура извлечения должна находить данные для передачи, считывать данные в буфер и задавать количество элементов для отправки.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-105">The pull procedure must find the data to be transferred, read the data into the buffer, and set the number of elements to send.</span></span> <span data-ttu-id="a6a7d-106">Не все данные должны находиться в буфере, когда сервер начинает извлекать данные в себя.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-106">Not all of the data has to be in the buffer when the server begins to pull data to itself.</span></span> <span data-ttu-id="a6a7d-107">Процедура Pull может выполнить добавочную заливку буфера.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-107">The pull procedure can fill the buffer incrementally.</span></span>

<span data-ttu-id="a6a7d-108">Если больше нет данных для отправки, процедура задает для последнего аргумента значение 0.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-108">When there is no more data to send, the procedure sets its last argument to zero.</span></span> <span data-ttu-id="a6a7d-109">При отправке всех данных процедура извлечения должна выполнить необходимую очистку перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-109">When all the data is sent, the pull procedure should do any needed cleanup before returning.</span></span> <span data-ttu-id="a6a7d-110">Для параметра, который является \[ выходным \] каналом, процедура извлечения должна сбрасывать переменную состояния клиента после передачи всех данных, чтобы процедура Push могла использовать ее для получения данных.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-110">For a parameter that is an \[in, out\] pipe, the pull procedure must reset the client's state variable after all the data has been transmitted, so that the push procedure can use it to receive data.</span></span>

<span data-ttu-id="a6a7d-111">Следующий пример извлекается из программы Пипедемо, входящей в комплект SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-111">The following example is extracted from the Pipedemo program included with the Platform Software Development Kit (SDK).</span></span>


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void SendLongs()
{
    LONG_PIPE inPipe;
    int i;
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
 
    for (i=0; i<PIPE_SIZE; i++)
        globalPipeData[i] = IN_VALUE;
 
    pipeDataIndex = 0;
    inPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    inPipe.pull  = PipePull;
    inPipe.alloc = PipeAlloc;
 
    InPipe( inPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );

}//end SendLongs
 
void PipeAlloc( rpc_ss_pipe_state_t stateInfo,
                ulong requestedSize,
                long **allocatedBuffer,
                ulong *allocatedSize )
{ 
    ulong *state = (ulong *)stateInfo;
    if ( requestedSize > (BUF_SIZE*sizeof(long)) )
    {
       *allocatedSize = BUF_SIZE * sizeof(long);
    }
    else
    {
       *allocatedSize = requestedSize;
    }
    *allocatedBuffer = globalBuffer; 
} //end PipeAlloc
 
void PipePull( rpc_ss_pipe_state_t stateInfo,
               long *inputBuffer,
               ulong maxBufSize,
               ulong *sizeToSend )
{
    ulong currentIndex;
    ulong i;
    ulong elementsToRead;
    ulong *state = (ulong *)stateInfo;

    currentIndex = *state;
    if (*state >=  PIPE_SIZE )
    {
        *sizeToSend = 0; /* end of pipe data */
        *state = 0; /* Reset the state = global index */
    }
    else 
    {
        if ( currentIndex + maxBufSize > PIPE_SIZE )
            elementsToRead = PIPE_SIZE - currentIndex;
        else
            elementsToRead = maxBufSize;
 
        for (i=0; i < elementsToRead; i++)
        {
            /*client sends data */
            inputBuffer[i] = globalPipeData[i + currentIndex];
        }
 
        *state +=   elementsToRead;
        *sizeToSend = elementsToRead;
    } 
}//end PipePull
```



<span data-ttu-id="a6a7d-112">Этот пример включает файл заголовка, созданный компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="a6a7d-113">Дополнительные сведения см. [в разделе Определение каналов в IDL-файлах](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="a6a7d-113">For details see [Defining Pipes in IDL Files](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="a6a7d-114">Он также объявляет переменную, которая используется в качестве источника данных с именем Глобалпипедата.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-114">It also declares a variable it uses as the data source called globalPipeData.</span></span> <span data-ttu-id="a6a7d-115">Переменная Глобалбуффер — это буфер, который используется процедурой извлечения для отправки блоков данных, получаемых из Глобалпипедата.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-115">The variable globalBuffer is a buffer that the pull procedure uses to send the blocks of data it obtains from globalPipeData.</span></span>

<span data-ttu-id="a6a7d-116">Функция Сендлонгс объявляет входной канал и выделяет память для переменной источника данных Глобалпипедата.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-116">The SendLongs function declares the input pipe, and allocates memory for the data source variable globalPipeData.</span></span> <span data-ttu-id="a6a7d-117">В программе Client/Server источником данных может быть файл или структура, создаваемая клиентом.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-117">In your client/server program, the data source can be a file or structure that the client creates.</span></span> <span data-ttu-id="a6a7d-118">Кроме того, клиентская программа может получать данные с сервера, обрабатывать их и возвращать на сервер, используя входной канал.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-118">You can also have your client program obtain data from the server, process it, and return it to the server using an input pipe.</span></span> <span data-ttu-id="a6a7d-119">В этом простом примере источником данных является динамически выделяемый буфер длинных целых чисел.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-119">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="a6a7d-120">Перед началом перемещения клиент должен установить указатели на переменную состояния, процедуру Pull и процедуру выделения.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-120">Before the transfer can begin, the client must set pointers to the state variable, the pull procedure, and the alloc procedure.</span></span> <span data-ttu-id="a6a7d-121">Эти указатели хранятся в переменной канала, объявляемой клиентом.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-121">These pointers are kept in the pipe variable the client declares.</span></span> <span data-ttu-id="a6a7d-122">В этом случае Сендлонгс объявляет неконвейерный.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-122">In this case, SendLongs declares inPipe.</span></span> <span data-ttu-id="a6a7d-123">Для переменной состояния можно использовать любой подходящий тип данных.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-123">You can use any appropriate data type for your state variable.</span></span>

<span data-ttu-id="a6a7d-124">Клиенты инициируют передачу данных по каналу, вызывая удаленную процедуру на сервере.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-124">Clients initiate data transfers across a pipe by invoking a remote procedure on the server.</span></span> <span data-ttu-id="a6a7d-125">Вызов удаленной процедуры сообщает серверной программе о том, что клиент готов к передаче.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-125">Calling the remote procedure tells the server program that the client is ready to transmit.</span></span> <span data-ttu-id="a6a7d-126">Затем сервер может извлечь данные в себя.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-126">The server can then pull the data to itself.</span></span> <span data-ttu-id="a6a7d-127">В этом примере вызывается Удаленная процедура с именем onpipe.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-127">This example invokes a remote procedure called InPipe.</span></span> <span data-ttu-id="a6a7d-128">После передачи данных на сервер функция Сендлонгс освобождает динамически выделяемый буфер.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-128">After the data is transferred to the server, the SendLongs function frees the dynamically allocated buffer.</span></span>

<span data-ttu-id="a6a7d-129">Вместо выделения памяти каждый раз, когда требуется буфер.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-129">Rather than allocate memory each time a buffer is needed.</span></span> <span data-ttu-id="a6a7d-130">процедура выделения в этом примере просто устанавливает указатель на переменную Глобалбуффер.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-130">the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="a6a7d-131">Процедура извлечения повторно использует этот буфер каждый раз при передаче данных.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-131">The pull procedure reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="a6a7d-132">Более сложным клиентским программам может потребоваться выделить новый буфер каждый раз, когда сервер извлекает данные от клиента.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-132">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="a6a7d-133">Заглушка клиента вызывает процедуру извлечения.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-133">The client stub calls the pull procedure.</span></span> <span data-ttu-id="a6a7d-134">Процедура извлечения в этом примере использует переменную состояния для отслеживания следующей позицией в глобальном буфере источника данных для чтения из.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-134">The pull procedure in this example uses the state variable to track the next position in the global data source buffer to read from.</span></span> <span data-ttu-id="a6a7d-135">Он считывает данные из исходного буфера в буфер канала.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-135">It reads data from the source buffer into the pipe buffer.</span></span> <span data-ttu-id="a6a7d-136">Заглушка клиента передает данные на сервер.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-136">The client stub transmits the data to the server.</span></span> <span data-ttu-id="a6a7d-137">Когда все данные отправлены, процедура Pull устанавливает размер буфера равным нулю.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-137">When all the data has been sent, the pull procedure sets the buffer size to zero.</span></span> <span data-ttu-id="a6a7d-138">Это указывает серверу на необходимость перестают извлекать данные.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-138">This tells the server to stop pulling data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6a7d-139">См. также</span><span class="sxs-lookup"><span data-stu-id="a6a7d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6a7d-140">дать</span><span class="sxs-lookup"><span data-stu-id="a6a7d-140">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="a6a7d-141">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="a6a7d-141">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 