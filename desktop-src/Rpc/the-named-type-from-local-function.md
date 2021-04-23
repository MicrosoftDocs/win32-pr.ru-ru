---
title: Функция named_type_from_local
description: Заглушки вызывают именованный \_ тип \_ из \_ локальной функции.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329123"
---
# <a name="the-named_type_from_local-function"></a><span data-ttu-id="8fc60-104">Именованный \_ тип \_ из \_ локальной функции</span><span class="sxs-lookup"><span data-stu-id="8fc60-104">The named\_type\_from\_local Function</span></span>

<span data-ttu-id="8fc60-105">Заглушки вызывают именованный \_ тип \_ из \_ локальной функции.</span><span class="sxs-lookup"><span data-stu-id="8fc60-105">The stubs call the named\_type\_from\_local function.</span></span> <span data-ttu-id="8fc60-106">Он преобразует тип, используемый приложением, в тип, который будет передавать суррогаты по сети.</span><span class="sxs-lookup"><span data-stu-id="8fc60-106">It converts the type that the application uses into the type the stubs transmit across the network.</span></span> <span data-ttu-id="8fc60-107">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8fc60-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

<span data-ttu-id="8fc60-108">Первый параметр — это указатель на данные приложения.</span><span class="sxs-lookup"><span data-stu-id="8fc60-108">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="8fc60-109">Второй параметр является указателем на указатель.</span><span class="sxs-lookup"><span data-stu-id="8fc60-109">The second parameter is a pointer to a pointer.</span></span> <span data-ttu-id="8fc60-110">Функция указывает на передаваемые данные.</span><span class="sxs-lookup"><span data-stu-id="8fc60-110">The function points it to the transmitted data.</span></span> <span data-ttu-id="8fc60-111">Функция должна выделить память для переданного типа.</span><span class="sxs-lookup"><span data-stu-id="8fc60-111">The function must allocate memory for the transmitted type.</span></span>

 

 




