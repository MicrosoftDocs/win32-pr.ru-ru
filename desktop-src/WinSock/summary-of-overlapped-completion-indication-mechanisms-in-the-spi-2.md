---
description: Сводка по механизмам индикации завершения перекрытия в сокетах Windows (Winsock).
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Сводка по механизмам индикации завершения перекрытия в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144950"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a><span data-ttu-id="dec07-103">Сводка по механизмам индикации завершения перекрытия в SPI</span><span class="sxs-lookup"><span data-stu-id="dec07-103">Summary of Overlapped Completion Indication Mechanisms in the SPI</span></span>

<span data-ttu-id="dec07-104">В следующей таблице перечислены семантики завершения для перекрывающихся сокетов, в которых показаны различные сочетания *лповерлаппед*, **Хевент** и *лпкомплетионраутине*.</span><span class="sxs-lookup"><span data-stu-id="dec07-104">The following table summarizes the completion semantics for an overlapped socket, showing the various combination of *lpOverlapped*, **hEvent**, and *lpCompletionRoutine*.</span></span>



| <span data-ttu-id="dec07-105">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="dec07-105">*lpOverlapped*</span></span> | <span data-ttu-id="dec07-106">**хевент**</span><span class="sxs-lookup"><span data-stu-id="dec07-106">**hEvent**</span></span>     | <span data-ttu-id="dec07-107">*лпкомплетионраутине*</span><span class="sxs-lookup"><span data-stu-id="dec07-107">*lpCompletionRoutine*</span></span> | <span data-ttu-id="dec07-108">Индикатор завершения</span><span class="sxs-lookup"><span data-stu-id="dec07-108">Completion indication</span></span>                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec07-109">NULL</span><span class="sxs-lookup"><span data-stu-id="dec07-109">NULL</span></span>           | <span data-ttu-id="dec07-110">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="dec07-110">Not applicable</span></span> | <span data-ttu-id="dec07-111">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="dec07-111">Ignored</span></span>               | <span data-ttu-id="dec07-112">Операция завершается синхронно, то есть она ведет себя так, как если бы она была ноноверлаппед сокетом.</span><span class="sxs-lookup"><span data-stu-id="dec07-112">Operation completes synchronously, that is, it behaves as if it were a nonoverlapped socket.</span></span>                                                                                                                                 |
| <span data-ttu-id="dec07-113">не NULL</span><span class="sxs-lookup"><span data-stu-id="dec07-113">not NULL</span></span>       | <span data-ttu-id="dec07-114">NULL</span><span class="sxs-lookup"><span data-stu-id="dec07-114">NULL</span></span>           | <span data-ttu-id="dec07-115">NULL</span><span class="sxs-lookup"><span data-stu-id="dec07-115">NULL</span></span>                  | <span data-ttu-id="dec07-116">Операция завершается перекрытием, но механизм завершения, поддерживаемый Windows Sockets 2, отсутствует.</span><span class="sxs-lookup"><span data-stu-id="dec07-116">Operation completes overlapped, but there is no Windows Sockets 2-supported completion mechanism.</span></span> <span data-ttu-id="dec07-117">Механизм порта завершения (если поддерживается) может использоваться в этом случае, в противном случае уведомление о завершении не будет.</span><span class="sxs-lookup"><span data-stu-id="dec07-117">The completion port mechanism (if supported) may be used in this case, otherwise there will be no completion notification.</span></span> |
| <span data-ttu-id="dec07-118">не NULL</span><span class="sxs-lookup"><span data-stu-id="dec07-118">not NULL</span></span>       | <span data-ttu-id="dec07-119">не NULL</span><span class="sxs-lookup"><span data-stu-id="dec07-119">not NULL</span></span>       | <span data-ttu-id="dec07-120">NULL</span><span class="sxs-lookup"><span data-stu-id="dec07-120">NULL</span></span>                  | <span data-ttu-id="dec07-121">Операция завершает перекрытие, уведомление по сигнальному объекту события.</span><span class="sxs-lookup"><span data-stu-id="dec07-121">Operation completes overlapped, notification by signaling event object.</span></span>                                                                                                                                                      |
| <span data-ttu-id="dec07-122">не NULL</span><span class="sxs-lookup"><span data-stu-id="dec07-122">not NULL</span></span>       | <span data-ttu-id="dec07-123">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="dec07-123">Ignored</span></span>        | <span data-ttu-id="dec07-124">не NULL</span><span class="sxs-lookup"><span data-stu-id="dec07-124">not NULL</span></span>              | <span data-ttu-id="dec07-125">Операция завершает перекрытие, уведомление по плану завершения.</span><span class="sxs-lookup"><span data-stu-id="dec07-125">Operation completes overlapped, notification by scheduling completion routine.</span></span>                                                                                                                                               |



 

 

 



