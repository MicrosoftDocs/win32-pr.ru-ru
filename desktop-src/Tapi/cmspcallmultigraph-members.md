---
description: Элементы Кмспкаллмултиграф
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Элементы Кмспкаллмултиграф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673852"
---
# <a name="cmspcallmultigraph-members"></a><span data-ttu-id="6f2bc-103">Элементы Кмспкаллмултиграф</span><span class="sxs-lookup"><span data-stu-id="6f2bc-103">CMSPCallMultiGraph Members</span></span>

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

<span data-ttu-id="6f2bc-104">Блоки ожидания хранят сведения о времени ожидания, зарегистрированном в пуле потоков.</span><span class="sxs-lookup"><span data-stu-id="6f2bc-104">The wait blocks store the information about the wait registered to the thread pool.</span></span> <span data-ttu-id="6f2bc-105">Он включает дескрипторы ожидания, возвращаемые вызовом [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) , и указатель на структуру контекста.</span><span class="sxs-lookup"><span data-stu-id="6f2bc-105">It includes the wait handles returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) call and a pointer to the context structure.</span></span> <span data-ttu-id="6f2bc-106">Каждый блок в массиве предназначен для графа в одном из объектов потока.</span><span class="sxs-lookup"><span data-stu-id="6f2bc-106">Each block in the array is for a graph in one of the stream objects.</span></span> <span data-ttu-id="6f2bc-107">Смещение блока в этом массиве совпадает со смещением потока, владеющего графом.</span><span class="sxs-lookup"><span data-stu-id="6f2bc-107">The offset of a block in this array is the same as the offset of the stream that owns the graph.</span></span>

 

 
