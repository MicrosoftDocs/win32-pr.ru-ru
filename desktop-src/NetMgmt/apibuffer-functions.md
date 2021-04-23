---
title: Функции Апибуффер
description: Функции Апибуффер управления сетью используются для управления выделением памяти, используемым приложением с функциями управления сетью.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105661754"
---
# <a name="apibuffer-functions"></a><span data-ttu-id="0ac8c-103">Функции Апибуффер</span><span class="sxs-lookup"><span data-stu-id="0ac8c-103">ApiBuffer Functions</span></span>

<span data-ttu-id="0ac8c-104">Функции Апибуффер управления сетью используются для управления выделением памяти, используемым приложением с функциями управления сетью.</span><span class="sxs-lookup"><span data-stu-id="0ac8c-104">The network management ApiBuffer functions are used to manage memory allocation used by an application with network management functions.</span></span> <span data-ttu-id="0ac8c-105">Однако в общем случае для другой памяти, используемой приложением, вместо этих функций Апибуффер следует использовать [функции управления памятью](/windows/desktop/Memory/memory-management-functions) .</span><span class="sxs-lookup"><span data-stu-id="0ac8c-105">However, in general, for other memory used by an application you should use the [memory management functions](/windows/desktop/Memory/memory-management-functions) instead of these ApiBuffer functions.</span></span>

<span data-ttu-id="0ac8c-106">Ниже перечислены функции Апибуффер.</span><span class="sxs-lookup"><span data-stu-id="0ac8c-106">The ApiBuffer functions are listed following.</span></span>



| <span data-ttu-id="0ac8c-107">Функция</span><span class="sxs-lookup"><span data-stu-id="0ac8c-107">Function</span></span>                                                 | <span data-ttu-id="0ac8c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0ac8c-108">Description</span></span>                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ac8c-109">**нетапибуффераллокате**</span><span class="sxs-lookup"><span data-stu-id="0ac8c-109">**NetApiBufferAllocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | <span data-ttu-id="0ac8c-110">Выделяет память из кучи.</span><span class="sxs-lookup"><span data-stu-id="0ac8c-110">Allocates memory from the heap.</span></span> <span data-ttu-id="0ac8c-111">Вызывайте эту функцию, если требуется совместимость с функцией **нетапибуфферфри** .</span><span class="sxs-lookup"><span data-stu-id="0ac8c-111">Call this function when you require compatibility with the **NetApiBufferFree** function.</span></span> |
| [<span data-ttu-id="0ac8c-112">**нетапибуфферфри**</span><span class="sxs-lookup"><span data-stu-id="0ac8c-112">**NetApiBufferFree**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | <span data-ttu-id="0ac8c-113">Освобождает память, выделенную функцией **нетапибуффераллокате** и другими функциями управления сетью.</span><span class="sxs-lookup"><span data-stu-id="0ac8c-113">Frees memory allocated by the **NetApiBufferAllocate** function and other network management functions.</span></span>                   |
| [<span data-ttu-id="0ac8c-114">**нетапибуфферреаллокате**</span><span class="sxs-lookup"><span data-stu-id="0ac8c-114">**NetApiBufferReallocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | <span data-ttu-id="0ac8c-115">Изменяет размер буфера, выделенного вызовом функции **нетапибуффераллокате** .</span><span class="sxs-lookup"><span data-stu-id="0ac8c-115">Changes the size of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                                |
| [<span data-ttu-id="0ac8c-116">**нетапибуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="0ac8c-116">**NetApiBufferSize**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | <span data-ttu-id="0ac8c-117">Возвращает размер (в байтах) буфера, выделенного путем вызова функции **нетапибуффераллокате** .</span><span class="sxs-lookup"><span data-stu-id="0ac8c-117">Returns the size, in bytes, of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                     |



 

<span data-ttu-id="0ac8c-118">Для удаленных функций, возвращающих сведения вызывающему объекту, Библиотека времени выполнения RPC выделяет буфер, содержащий возвращаемые сведения.</span><span class="sxs-lookup"><span data-stu-id="0ac8c-118">For remotable functions that return information to the caller, the RPC run-time library allocates the buffer containing the return information.</span></span> <span data-ttu-id="0ac8c-119">Когда вызывающий объект заканчивает обработку информации, он должен вызвать функцию [**нетапибуфферфри**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) , чтобы освободить выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="0ac8c-119">When the caller has finished processing the information, it must call the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function to free the allocated buffer.</span></span>

 

 