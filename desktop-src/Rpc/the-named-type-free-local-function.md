---
title: Функция named_type_free_local
description: Заглушки вызывают \_ свободную \_ локальную функцию типа, чтобы освободить память, выделенную вызовом именованного \_ типа, \_ в \_ локальную подпрограммы.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f2796f33e9dc60364b6afda244d8dae47eef0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774624"
---
# <a name="the-named_type_free_local-function"></a><span data-ttu-id="a99fe-104">Локальная функция с именованным \_ типом \_ Free \_</span><span class="sxs-lookup"><span data-stu-id="a99fe-104">The named\_type\_free\_local Function</span></span>

<span data-ttu-id="a99fe-105">Заглушки вызывают **\_ свободную \_ локальную функцию типа** , чтобы освободить память, выделенную вызовом [именованного \_ типа, \_ в \_ локальную](the-named-type-to-local-function.md) подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="a99fe-105">The stubs call the **type\_free\_local** function to free the memory allocated by a call to the [named\_type\_to\_local](the-named-type-to-local-function.md) routine.</span></span> <span data-ttu-id="a99fe-106">Память, выделенная заглушкой, не освобождается.</span><span class="sxs-lookup"><span data-stu-id="a99fe-106">It does not free the memory allocated by the stub.</span></span> <span data-ttu-id="a99fe-107">Прототип функции определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a99fe-107">The function prototype is defined as:</span></span>

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

<span data-ttu-id="a99fe-108">Параметр является указателем на память, выделенную с помощью **именованного \_ типа, \_ в \_ локальную**.</span><span class="sxs-lookup"><span data-stu-id="a99fe-108">The parameter is a pointer to the memory allocated by **named\_type\_to\_local**.</span></span>

 

 




