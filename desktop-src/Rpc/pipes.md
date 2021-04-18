---
title: Каналы (RPC)
description: Конструктор типа канала является очень эффективным механизмом передачи больших объемов данных или любого количества данных, которое не доступно в памяти одновременно.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- Удаленный вызов процедур RPC, описание, каналы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488766"
---
# <a name="pipes-rpc"></a><span data-ttu-id="a9be0-104">Каналы (RPC)</span><span class="sxs-lookup"><span data-stu-id="a9be0-104">Pipes (RPC)</span></span>

<span data-ttu-id="a9be0-105">Конструктор типа канала является очень эффективным механизмом передачи больших объемов данных или любого количества данных, которое не доступно в памяти одновременно.</span><span class="sxs-lookup"><span data-stu-id="a9be0-105">The pipe type constructor is a highly efficient mechanism for passing large amounts of data, or any quantity of data that is not all available in memory at one time.</span></span> <span data-ttu-id="a9be0-106">С помощью канала время выполнения RPC обрабатывает фактическую передаваемые данные, устраняя издержки, связанные с повторными вызовами удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="a9be0-106">By using a pipe, RPC run time handles the actual data transfer, eliminating the overhead associated with repeated remote procedure calls.</span></span>

<span data-ttu-id="a9be0-107">После того как клиент вызывает удаленную процедуру с параметром канала, клиент и сервер вводят циклы для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="a9be0-107">After a client invokes a remote procedure that has a pipe parameter, the client and server enter loops to transfer data.</span></span> <span data-ttu-id="a9be0-108">Данные могут быть получены на клиенте или сервере.</span><span class="sxs-lookup"><span data-stu-id="a9be0-108">The data can be produced on the client or the server.</span></span> <span data-ttu-id="a9be0-109">В любом случае объем данных (в байтах) не должен быть известен заранее.</span><span class="sxs-lookup"><span data-stu-id="a9be0-109">Either way, the amount of data (in bytes) does not have to be known in advance.</span></span> <span data-ttu-id="a9be0-110">Данные могут быть сформированы или использованы постепенно.</span><span class="sxs-lookup"><span data-stu-id="a9be0-110">The data can be produced or consumed incrementally.</span></span> <span data-ttu-id="a9be0-111">В цикле передачи данных сервер вызывает подпрограммы-заглушки, которые загружают или выгружают буфер данных.</span><span class="sxs-lookup"><span data-stu-id="a9be0-111">While in the data-transfer loop, the server calls stub routines that load or unload a buffer of data.</span></span> <span data-ttu-id="a9be0-112">Клиент вызывает определяемые программистом процедуры для выделения буферов, загрузки данных в буферы и их выгрузки.</span><span class="sxs-lookup"><span data-stu-id="a9be0-112">The client calls programmer-defined procedures to allocate buffers, load data into and unload data from the buffers.</span></span>

<span data-ttu-id="a9be0-113">В этом разделе приводятся общие сведения об использовании каналов для удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="a9be0-113">This section provides an overview of using pipes for remote procedure calls.</span></span> <span data-ttu-id="a9be0-114">Он представляет общие сведения в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a9be0-114">It presents the overview in the following topics:</span></span>

-   [<span data-ttu-id="a9be0-115">Терминология каналов</span><span class="sxs-lookup"><span data-stu-id="a9be0-115">Essential Pipe Terminology</span></span>](essential-pipe-terminology.md)
-   [<span data-ttu-id="a9be0-116">Состояние канала</span><span class="sxs-lookup"><span data-stu-id="a9be0-116">The Pipe State</span></span>](the-pipe-state.md)
-   [<span data-ttu-id="a9be0-117">Определение каналов в IDL-файлах</span><span class="sxs-lookup"><span data-stu-id="a9be0-117">Defining Pipes in IDL Files</span></span>](defining-pipes-in-idl-files.md)
-   [<span data-ttu-id="a9be0-118">Реализация конвейера на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="a9be0-118">Client-Side Pipe Implementation</span></span>](client-side-pipe-implementation.md)
-   [<span data-ttu-id="a9be0-119">Реализация конвейера на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="a9be0-119">Server-Side Pipe Implementation</span></span>](server-side-pipe-implementation.md)
-   [<span data-ttu-id="a9be0-120">Правила для нескольких каналов</span><span class="sxs-lookup"><span data-stu-id="a9be0-120">Rules for Multiple Pipes</span></span>](rules-for-multiple-pipes.md)
-   [<span data-ttu-id="a9be0-121">Объединение параметров pipe и неканального</span><span class="sxs-lookup"><span data-stu-id="a9be0-121">Combining Pipe and Nonpipe Parameters</span></span>](combining-pipe-and-nonpipe-parameters.md)

<span data-ttu-id="a9be0-122">Дополнительные сведения о синтаксисе и ограничениях канала см. в разделе [канал](/windows/desktop/Midl/pipe) в справочнике по языку MIDL.</span><span class="sxs-lookup"><span data-stu-id="a9be0-122">For more information on pipe syntax and restrictions, see [pipe](/windows/desktop/Midl/pipe) in the MIDL Language Reference.</span></span> <span data-ttu-id="a9be0-123">Пример программы "каналы" в каталоге RPC Samples Software Development Kit (SDK) \\ демонстрирует использование **\[ в, out \]** -каналов для перемещения данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="a9be0-123">The PIPES sample program in the Platform Software Development Kit (SDK) samples\\rpc directory demonstrates how to use **\[in,out\]** pipes to transfer data between a client and a server.</span></span>

 

 
