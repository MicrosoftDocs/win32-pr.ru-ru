---
title: Функция type_free_xmit
description: Заглушки вызывают \_ \_ функцию Free xmit типа, чтобы освободить память, связанную с переданными данными.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33d5cb8079d50923de2161b0384550829a5f22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253351"
---
# <a name="the-type_free_xmit-function"></a><span data-ttu-id="db9c6-104">Функция типа \_ Free \_ xmit</span><span class="sxs-lookup"><span data-stu-id="db9c6-104">The type\_free\_xmit Function</span></span>

<span data-ttu-id="db9c6-105">Заглушки вызывают функцию **\_ Free \_ xmit типа** , чтобы освободить память, связанную с переданными данными.</span><span class="sxs-lookup"><span data-stu-id="db9c6-105">The stubs call the **type\_free\_xmit** function to free memory associated with the transmitted data.</span></span> <span data-ttu-id="db9c6-106">После того как [тип \_ из функции \_ xmit](the-type-from-xmit-function.md) преобразует передаваемые данные в представленный тип, память больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="db9c6-106">After the [type\_from\_xmit](the-type-from-xmit-function.md) function converts the transmitted data to its presented type, the memory is no longer needed.</span></span> <span data-ttu-id="db9c6-107">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="db9c6-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

<span data-ttu-id="db9c6-108">Параметр является указателем на память, содержащую переданный тип.</span><span class="sxs-lookup"><span data-stu-id="db9c6-108">The parameter is a pointer to the memory that contains the transmitted type.</span></span>

<span data-ttu-id="db9c6-109">В этом примере память содержит массив, который находится в одной структуре.</span><span class="sxs-lookup"><span data-stu-id="db9c6-109">In this example, the memory contains an array that is in a single structure.</span></span> <span data-ttu-id="db9c6-110">Функция двойной \_ связи \_ типа Double \_ \_ xmit использует предоставляемую пользователем функцию MIDL \_ \_ Free для освобождения памяти:</span><span class="sxs-lookup"><span data-stu-id="db9c6-110">The function DOUBLE\_LINK\_TYPE\_free\_xmit uses the user-supplied function midl\_user\_free to free the memory:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




