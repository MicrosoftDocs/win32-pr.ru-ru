---
title: Объединение параметров pipe и неканального
description: Объединение параметров pipe и неканального вызова в удаленном вызове процедур (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890937"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a><span data-ttu-id="66423-103">Объединение параметров pipe и неканального</span><span class="sxs-lookup"><span data-stu-id="66423-103">Combining Pipe and Nonpipe Parameters</span></span>

<span data-ttu-id="66423-104">При объединении типов каналов и других типов при удаленном вызове процедуры данные передаются в соответствии с направлением параметра:</span><span class="sxs-lookup"><span data-stu-id="66423-104">When you combine pipe types and other types in a remote procedure call, the data is transmitted according to the direction of the parameter:</span></span>

-   <span data-ttu-id="66423-105">В направлении сначала передаются данные для всех неканальных аргументов, а затем данные по каналу. **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="66423-105">In the **\[in\]** direction, the data for all nonpipe arguments is transmitted first, followed by pipe data.</span></span>
-   <span data-ttu-id="66423-106">В **\[ обратном \]** направлении сервер сначала отправляет данные канала.</span><span class="sxs-lookup"><span data-stu-id="66423-106">In the **\[out\]** direction, the server sends the pipe data first.</span></span> <span data-ttu-id="66423-107">После того как подпрограммы диспетчера возвращают, сервер передает неканалные данные.</span><span class="sxs-lookup"><span data-stu-id="66423-107">After the manager routine returns, the server transmits the nonpipe data.</span></span>
-   <span data-ttu-id="66423-108">При наличии **\[ входных \]** аргументов канала в сочетании с аргументами **\[ in и \] out** не-pipe входные данные сначала передаются целиком, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="66423-108">When there are **\[in,out\]** pipe arguments combined with **\[in,out\]** non-pipe arguments, first the input data is transmitted in its entirety, as previously described.</span></span> <span data-ttu-id="66423-109">Затем выходные данные передаются, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="66423-109">Then, the output data is transmitted as previously described.</span></span>

<span data-ttu-id="66423-110">Следующее ограничение применяется к этой реализации (MIDL 3,0). Если типы каналов и другие типы объединяются в одном удаленном вызове процедуры, то параметры, не относящиеся к каналу, должны иметь четко определенный размер, чтобы компилятор MIDL мог вычислить необходимый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="66423-110">The following restriction applies to this (MIDL 3.0) implementation of pipes: When you combine pipe types and other types in a single remote procedure call, the nonpipe parameters must have a well-defined size in order to allow the MIDL compiler to calculate the buffer size needed.</span></span> <span data-ttu-id="66423-111">Например, нельзя объединить параметры канала с \[ [уникальным](/windows/desktop/Midl/unique) \] указателем или соответствующей структурой, так как их размеры нельзя определить во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="66423-111">For example, you cannot combine pipe parameters with a \[ [unique](/windows/desktop/Midl/unique)\] pointer or a conformant structure, since their sizes cannot be determined at compile time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66423-112">См. также</span><span class="sxs-lookup"><span data-stu-id="66423-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66423-113">дать</span><span class="sxs-lookup"><span data-stu-id="66423-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="66423-114">/Oi</span><span class="sxs-lookup"><span data-stu-id="66423-114">/Oi</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 