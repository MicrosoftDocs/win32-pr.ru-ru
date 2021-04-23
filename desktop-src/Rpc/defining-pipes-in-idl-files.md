---
title: Определение каналов в IDL-файлах
description: Если в IDL-файле определен канал, компилятор MIDL создает структуру управления канала, члены которой являются указателями на процедуры Push, Pull и Alloc, а также переменную состояния, которая координирует эти процедуры.
ms.assetid: f6c282e4-3056-48c4-bd12-dfcae6d238d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115be7fc5d00458d13df102afebe9ba5b55de070
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413331"
---
# <a name="defining-pipes-in-idl-files"></a><span data-ttu-id="a84f5-103">Определение каналов в IDL-файлах</span><span class="sxs-lookup"><span data-stu-id="a84f5-103">Defining Pipes in IDL Files</span></span>

<span data-ttu-id="a84f5-104">Если в IDL-файле определен канал, компилятор MIDL создает структуру управления канала, члены которой являются указателями на процедуры Push, Pull и Alloc, а также переменную состояния, которая координирует эти процедуры.</span><span class="sxs-lookup"><span data-stu-id="a84f5-104">When a pipe is defined in an IDL file, the MIDL compiler generates a pipe control structure whose members are pointers to push, pull, and alloc procedures as well as a state variable that coordinates these procedures.</span></span> <span data-ttu-id="a84f5-105">Клиентское приложение инициализирует поля в структуре управления каналом, сохраняет свою переменную состояния и управляет передачей данных с помощью собственных функций Push, Pull и Alloc.</span><span class="sxs-lookup"><span data-stu-id="a84f5-105">The client application initializes the fields in the pipe control structure, maintains its state variable, and manages the data transfer with its own push, pull, and alloc functions.</span></span> <span data-ttu-id="a84f5-106">Код клиентской заглушки вызывает эти функции приложения в циклах во время перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="a84f5-106">The client stub code calls these application functions in loops during data transfer.</span></span> <span data-ttu-id="a84f5-107">Для входного канала заглушка клиента маршалирует данные передачи и передает их в заглушку сервера.</span><span class="sxs-lookup"><span data-stu-id="a84f5-107">For an input pipe, the client stub marshals the transfer data and transmits it to the server stub.</span></span> <span data-ttu-id="a84f5-108">Для выходного канала заглушка клиента распаковать данные в буфер и передает указатель на этот буфер обратно клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="a84f5-108">For an output pipe, the client stub unmarshals the data into a buffer and passes a pointer to that buffer back to the client application.</span></span>

<span data-ttu-id="a84f5-109">Серверный код заглушки инициализирует поля структуры управления каналом переменной состояния, а также указателями на подпрограммы push и Pull.</span><span class="sxs-lookup"><span data-stu-id="a84f5-109">The server stub code initializes the fields of the pipe control structure to a state variable, as well as pointers to push and pull routines.</span></span> <span data-ttu-id="a84f5-110">Заглушка сервера поддерживает состояние и управляет своим частным хранилищем для передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="a84f5-110">The server stub maintains the state and manages its private storage for the transfer data.</span></span> <span data-ttu-id="a84f5-111">Серверное приложение вызывает процедуры Pull и Push в циклах во время вызова удаленной процедуры при получении и распаковке данных из клиентской заглушки, а также для маршалирования и передачи данных в клиентскую заглушку.</span><span class="sxs-lookup"><span data-stu-id="a84f5-111">The server application calls the pull and push routines in loops during the remote procedure call as it receives and unmarshals data from the client stub, or marshals and transmits data to the client stub.</span></span>

<span data-ttu-id="a84f5-112">В следующем примере IDL-файла определяется длинный канал типа канала \_ , размер элемента которого определяется как **Long**.</span><span class="sxs-lookup"><span data-stu-id="a84f5-112">The following example IDL file defines a pipe type LONG\_PIPE, whose element size is defined as **long**.</span></span> <span data-ttu-id="a84f5-113">В нем также объявляются прототипы функций для удаленной процедуры, которые вызывают конвейер и pipe для отправки и получения данных соответственно.</span><span class="sxs-lookup"><span data-stu-id="a84f5-113">It also declares function prototypes for the remote procedure calls InPipe and OutPipe, to send and receive data, respectively.</span></span> <span data-ttu-id="a84f5-114">Когда компилятор MIDL обрабатывает IDL-файл, он создает файл заголовка, показанный в примере.</span><span class="sxs-lookup"><span data-stu-id="a84f5-114">When the MIDL compiler processes the IDL file, it generates the header file shown in the example.</span></span>

## <a name="example"></a><span data-ttu-id="a84f5-115">Пример</span><span class="sxs-lookup"><span data-stu-id="a84f5-115">Example</span></span>

``` syntax
// File: pipedemo.idl
typedef pipe long LONG_PIPE;
void InPipe( [in] LONG_PIPE pipe_data );
void OutPipe( [out] LONG_PIPE *pipe_data ); 
//end pipedemo.idl
 
// File: pipedemo.h (fragment)
// Generated by the MIDL compiler from pipedemo.idl
typedef struct pipe_LONG_PIPE
{
    void (__RPC_FAR * pull) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long esize,
        unsigned long __RPC_FAR * ecount );
    void (__RPC_FAR * push) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long ecount );
    void (__RPC_FAR * alloc) (
        char __RPC_FAR * state,
        unsigned long bsize,
        long __RPC_FAR * __RPC_FAR * buf,
        unsigned long __RPC_FAR * bcount );
    char __RPC_FAR * state;
} LONG_PIPE;
 
void InPipe( 
    /* [in] */ LONG_PIPE pipe_data);
void OutPipe( 
    /* [out] */ LONG_PIPE __RPC_FAR *pipe_data);
//end pipedemo.h
```

## <a name="related-topics"></a><span data-ttu-id="a84f5-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a84f5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a84f5-117">дать</span><span class="sxs-lookup"><span data-stu-id="a84f5-117">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="a84f5-118">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="a84f5-118">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 