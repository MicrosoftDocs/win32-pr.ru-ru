---
title: Ошибки выделения буфера RPC
description: Так как библиотека времени выполнения RPC выделяет память для буферов отправки и получения, функция должна ждать ошибки выделения памяти RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe48c113d644447b5ff7b69988f2534d7de3a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329851"
---
# <a name="rpc-buffer-allocation-errors"></a><span data-ttu-id="06409-103">Ошибки выделения буфера RPC</span><span class="sxs-lookup"><span data-stu-id="06409-103">RPC Buffer Allocation Errors</span></span>

<span data-ttu-id="06409-104">Так как библиотека времени выполнения RPC выделяет память для буферов отправки и получения, функция должна ждать ошибки выделения памяти RPC.</span><span class="sxs-lookup"><span data-stu-id="06409-104">Because the RPC run-time library allocates memory for send and receive buffers, the function should expect RPC allocation errors.</span></span> <span data-ttu-id="06409-105">В случае ошибки выделения RPC, возобновляемый обработчик становится недействительным.</span><span class="sxs-lookup"><span data-stu-id="06409-105">In the event of an RPC allocation error, a resumable handle is invalidated.</span></span> <span data-ttu-id="06409-106">Это требование обусловлено тем, что возобновляемые функции не могут перематываться.</span><span class="sxs-lookup"><span data-stu-id="06409-106">This is a requirement because resumable functions are not rewindable.</span></span>

 

 




