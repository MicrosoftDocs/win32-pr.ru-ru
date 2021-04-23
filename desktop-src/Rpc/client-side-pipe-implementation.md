---
title: Реализация Client-Sideного канала
description: Реализация конвейера на стороне клиента в удаленном вызове процедур (RPC).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888920"
---
# <a name="client-side-pipe-implementation"></a><span data-ttu-id="22c57-103">Реализация Client-Sideного канала</span><span class="sxs-lookup"><span data-stu-id="22c57-103">Client-Side Pipe Implementation</span></span>

<span data-ttu-id="22c57-104">Клиентское приложение должно реализовать следующие процедуры, которые клиентская заглушка будет вызывать во время пересылки данных:</span><span class="sxs-lookup"><span data-stu-id="22c57-104">The client application must implement the following procedures, which the client stub will call during data transfer:</span></span>

-   <span data-ttu-id="22c57-105">Процедура извлечения (для входного канала)</span><span class="sxs-lookup"><span data-stu-id="22c57-105">A pull procedure (for an input pipe)</span></span>
-   <span data-ttu-id="22c57-106">Процедура Push (для выходного канала)</span><span class="sxs-lookup"><span data-stu-id="22c57-106">A push procedure (for an output pipe)</span></span>
-   <span data-ttu-id="22c57-107">Процедура выделения, которая выделяет буфер для данных для перемещения</span><span class="sxs-lookup"><span data-stu-id="22c57-107">An alloc procedure to allocate a buffer for the transfer data</span></span>

<span data-ttu-id="22c57-108">Все эти процедуры должны использовать аргументы, указанные в файле заголовка, созданном с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="22c57-108">All of these procedures must use the arguments specified by the MIDL-generated header file.</span></span> <span data-ttu-id="22c57-109">Кроме того, клиентское приложение должно иметь переменную состояния для указания места расположения или размещения данных.</span><span class="sxs-lookup"><span data-stu-id="22c57-109">In addition, the client application must have a state variable to identify where to locate or place data.</span></span>

<span data-ttu-id="22c57-110">Процедура выделения может также быть простой или сложной по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="22c57-110">The alloc procedure can also be as simple or as complex as needed.</span></span> <span data-ttu-id="22c57-111">Например, он может вернуть указатель на один и тот же буфер каждый раз, когда заглушка вызывает функцию, или может выделить отдельный объем памяти каждый раз.</span><span class="sxs-lookup"><span data-stu-id="22c57-111">For example, it can return a pointer to the same buffer every time the stub calls the function, or it can allocate a different amount of memory each time.</span></span> <span data-ttu-id="22c57-112">Если данные уже находятся в соответствующей форме (например, массив элементов канала), можно координировать процедуру выделения с помощью процедуры Pull, чтобы выделить буфер, который уже содержит данные.</span><span class="sxs-lookup"><span data-stu-id="22c57-112">If your data is already in the proper form (an array of pipe elements, for example) you can coordinate the alloc procedure with the pull procedure to allocate a buffer that already contains the data.</span></span> <span data-ttu-id="22c57-113">В этом случае процедура Pull может быть пустой процедурой.</span><span class="sxs-lookup"><span data-stu-id="22c57-113">In that case, your pull procedure could be an empty routine.</span></span>

<span data-ttu-id="22c57-114">Выделение буфера должно быть в байтах.</span><span class="sxs-lookup"><span data-stu-id="22c57-114">The buffer allocation must be in bytes.</span></span> <span data-ttu-id="22c57-115">Процедуры push и Pull, с другой стороны, управляют элементами, размер которых в байтах зависит от того, как они были определены.</span><span class="sxs-lookup"><span data-stu-id="22c57-115">The push and pull procedures, on the other hand, manipulate elements, whose size in bytes depends on how they were defined.</span></span>

<span data-ttu-id="22c57-116">В этом разделе обсуждается реализация клиента входных и выходных каналов в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="22c57-116">This section discusses the client implementation of input and output pipes in the following sections:</span></span>

-   [<span data-ttu-id="22c57-117">Реализация входных каналов на клиенте</span><span class="sxs-lookup"><span data-stu-id="22c57-117">Implementing Input Pipes on the Client</span></span>](implementing-input-pipes-on-the-client.md)
-   [<span data-ttu-id="22c57-118">Реализация выходных каналов на клиенте</span><span class="sxs-lookup"><span data-stu-id="22c57-118">Implementing Output Pipes on the Client</span></span>](implementing-output-pipes-on-the-client.md)

 

 




