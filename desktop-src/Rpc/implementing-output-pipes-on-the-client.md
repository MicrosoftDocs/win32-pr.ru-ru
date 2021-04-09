---
title: Реализация выходных каналов на клиенте
description: При использовании выходного канала для передачи данных с сервера клиенту необходимо реализовать процедуру принудительной отправки в клиенте.
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff274491e2b665d86b550853d07c3ff6a4b2a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791994"
---
# <a name="implementing-output-pipes-on-the-client"></a><span data-ttu-id="2a65b-103">Реализация выходных каналов на клиенте</span><span class="sxs-lookup"><span data-stu-id="2a65b-103">Implementing Output Pipes on the Client</span></span>

<span data-ttu-id="2a65b-104">При использовании выходного канала для передачи данных с сервера клиенту необходимо реализовать процедуру принудительной отправки в клиенте.</span><span class="sxs-lookup"><span data-stu-id="2a65b-104">When using an output pipe to transfer data from the server to the client, you must implement a push procedure in your client.</span></span> <span data-ttu-id="2a65b-105">Процедура Push принимает указатель на буфер и число элементов из клиентской заглушки и, если число элементов больше 0, обрабатывает данные.</span><span class="sxs-lookup"><span data-stu-id="2a65b-105">The push procedure takes a pointer to a buffer and an element count from the client stub and, if the element count is greater than 0, processes the data.</span></span> <span data-ttu-id="2a65b-106">Например, он может скопировать данные из буфера заглушки в собственную память.</span><span class="sxs-lookup"><span data-stu-id="2a65b-106">For example, it could copy the data from the stub's buffer to its own memory.</span></span> <span data-ttu-id="2a65b-107">Кроме того, он может обработать данные в буфере заглушки и сохранить их в файл.</span><span class="sxs-lookup"><span data-stu-id="2a65b-107">Alternately, it could process the data in the stub's buffer and save it to a file.</span></span> <span data-ttu-id="2a65b-108">Если число элементов равно нулю, процедура Push завершает все необходимые задачи очистки перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="2a65b-108">When the element count equals zero, the push procedure completes any needed cleanup tasks before returning.</span></span>

<span data-ttu-id="2a65b-109">В следующем примере клиентская функция Рецеивелонгс выделяет структуру канала и глобальный буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="2a65b-109">In the following example, the client function ReceiveLongs allocates a pipe structure and a global memory buffer.</span></span> <span data-ttu-id="2a65b-110">Он инициализирует структуру, выполняет удаленный вызов процедур, а затем освобождает память.</span><span class="sxs-lookup"><span data-stu-id="2a65b-110">It initializes the structure, makes the remote procedure call, and then frees the memory.</span></span>

## <a name="example"></a><span data-ttu-id="2a65b-111">Пример</span><span class="sxs-lookup"><span data-stu-id="2a65b-111">Example</span></span>


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *  globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void ReceiveLongs()
{
    LONG_PIPE *outputPipe;
    idl_long_int i;
 
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    pipeDataIndex = 0;
    outputPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    outputPipe.push  = PipePush;
    outputPipe.alloc = PipeAlloc;
 
    OutPipe( &outputPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );
 
}//end ReceiveLongs()

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
 
void PipePush( rpc_ss_pipe_state_t stateInfo,
               long *buffer,
               ulong numberOfElements )
{
    ulong elementsToCopy, i;
    ulong *state = (ulong *)stateInfo;

    if (numberOfElements == 0)/* end of data */
    {
        *state = 0; /* Reset the state = global index */
    }
    else
    {
        if (*state + numberOfElements > PIPE_SIZE)
            elementsToCopy = PIPE_SIZE - *state;
        else
            elementsToCopy = numberOfElements;
 
        for (i=0; i <elementsToCopy; i++)
        { 
            /*client receives data */
            globalPipeData[*state] = buffer[i];
            (*state)++;
        }
    }
}//end PipePush
```



<span data-ttu-id="2a65b-112">Этот пример включает файл заголовка, созданный компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="2a65b-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="2a65b-113">Дополнительные сведения см. [в разделе Определение каналов в IDL-файле](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="2a65b-113">For details see [Defining Pipes in IDL File](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="2a65b-114">Он также объявляет переменную Глобалпипедата, которая используется в качестве приемника данных.</span><span class="sxs-lookup"><span data-stu-id="2a65b-114">It also declares a variable, globalPipeData, that it uses as the data sink.</span></span> <span data-ttu-id="2a65b-115">Переменная Глобалбуффер — это буфер, используемый процедурой Push для получения блоков данных, которые он хранит в Глобалпипедата.</span><span class="sxs-lookup"><span data-stu-id="2a65b-115">The variable globalBuffer is a buffer that the push procedure uses to receive blocks of data it stores in globalPipeData.</span></span>

<span data-ttu-id="2a65b-116">Функция Рецеивелонгс объявляет канал и выделяет пространство памяти для переменной приемника глобальных данных.</span><span class="sxs-lookup"><span data-stu-id="2a65b-116">The ReceiveLongs function declares a pipe and allocates memory space for the global data sink variable.</span></span> <span data-ttu-id="2a65b-117">В программе Client/Server приемник данных может представлять собой файл или структуру данных, создаваемую клиентом.</span><span class="sxs-lookup"><span data-stu-id="2a65b-117">In your client/server program, the data sink can be a file or data structure the client creates.</span></span> <span data-ttu-id="2a65b-118">В этом простом примере источником данных является динамически выделяемый буфер длинных целых чисел.</span><span class="sxs-lookup"><span data-stu-id="2a65b-118">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="2a65b-119">Перед началом передачи данных клиентская программа должна инициализировать структуру выходного канала.</span><span class="sxs-lookup"><span data-stu-id="2a65b-119">Before the data transfer can begin, your client program must initialize the output pipe structure.</span></span> <span data-ttu-id="2a65b-120">Он должен устанавливать указатели на переменную состояния, процедуру push и процедуру выделения.</span><span class="sxs-lookup"><span data-stu-id="2a65b-120">It must set pointers to the state variable, the push procedure, and the alloc procedure.</span></span> <span data-ttu-id="2a65b-121">В этом примере переменная конвейера вывода называется Аутпутпипе.</span><span class="sxs-lookup"><span data-stu-id="2a65b-121">In this example, the output pipe variable is called outputPipe.</span></span>

<span data-ttu-id="2a65b-122">Клиенты предупреждают серверы о том, что они готовы принимать данные, путем вызова удаленной процедуры на сервере.</span><span class="sxs-lookup"><span data-stu-id="2a65b-122">Clients signal servers that they are ready to receive data by invoking a remote procedure on the server.</span></span> <span data-ttu-id="2a65b-123">В этом примере Удаленная процедура называется «внешним каналом».</span><span class="sxs-lookup"><span data-stu-id="2a65b-123">In this example, the remote procedure is called OutPipe.</span></span> <span data-ttu-id="2a65b-124">Когда клиент вызывает удаленную процедуру, сервер начинает передавать данные.</span><span class="sxs-lookup"><span data-stu-id="2a65b-124">When the client calls the remote procedure, the server begins the data transfer.</span></span> <span data-ttu-id="2a65b-125">Каждый раз при поступлении данных заглушка клиента вызывает процедуры распределения и принудительного выполнения клиента по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="2a65b-125">Each time data arrives, the client stub calls the client's alloc and push procedures as needed.</span></span>

<span data-ttu-id="2a65b-126">Вместо выделения памяти каждый раз, когда необходим буфер, процедура выделения в этом примере просто устанавливает указатель на переменную Глобалбуффер.</span><span class="sxs-lookup"><span data-stu-id="2a65b-126">Rather than allocate memory each time a buffer is needed, the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="2a65b-127">Затем процедура по запросу повторно использует этот буфер при каждой передаче данных.</span><span class="sxs-lookup"><span data-stu-id="2a65b-127">The pull procedure then reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="2a65b-128">Более сложным клиентским программам может потребоваться выделить новый буфер каждый раз, когда сервер извлекает данные от клиента.</span><span class="sxs-lookup"><span data-stu-id="2a65b-128">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="2a65b-129">Процедура Push в этом примере использует переменную состояния для отслеживания следующего места, где данные будут храниться в глобальном буфере приемника данных.</span><span class="sxs-lookup"><span data-stu-id="2a65b-129">The push procedure in this example uses the state variable to track the next position where it will store data in the global data sink buffer.</span></span> <span data-ttu-id="2a65b-130">Он записывает данные из буфера канала в буфер приемника.</span><span class="sxs-lookup"><span data-stu-id="2a65b-130">It writes data from the pipe buffer into sink buffer.</span></span> <span data-ttu-id="2a65b-131">Клиентская заглушка затем получает следующий блок данных с сервера и сохраняет их в буфере канала.</span><span class="sxs-lookup"><span data-stu-id="2a65b-131">The client stub then receives the next block of data from the server and stores it in the pipe buffer.</span></span> <span data-ttu-id="2a65b-132">После отправки всех данных сервер передает буфер нулевого размера.</span><span class="sxs-lookup"><span data-stu-id="2a65b-132">When all the data has been sent, the server transmits a zero-sized buffer.</span></span> <span data-ttu-id="2a65b-133">В этом случае процедура Push-уведомлений перестает получать данные.</span><span class="sxs-lookup"><span data-stu-id="2a65b-133">This cues the push procedure to stop receiving data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a65b-134">См. также</span><span class="sxs-lookup"><span data-stu-id="2a65b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a65b-135">дать</span><span class="sxs-lookup"><span data-stu-id="2a65b-135">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="2a65b-136">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="2a65b-136">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 