---
title: Функция named_type_free_inst
description: Заглушки вызывают функцию с именованным \_ типом \_ Free \_ inst для освобождения памяти, связанной с передаваемым типом.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774627"
---
# <a name="the-named_type_free_inst-function"></a><span data-ttu-id="410e4-104">Функция с именованным \_ типом \_ Free \_ inst</span><span class="sxs-lookup"><span data-stu-id="410e4-104">The named\_type\_free\_inst Function</span></span>

<span data-ttu-id="410e4-105">Заглушки вызывают функцию **с именованным \_ типом \_ Free \_ inst** для освобождения памяти, связанной с передаваемым типом.</span><span class="sxs-lookup"><span data-stu-id="410e4-105">The stubs call the **named\_type\_free\_inst** function to free memory associated with the transmitted type.</span></span> <span data-ttu-id="410e4-106">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="410e4-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="410e4-107">Параметр указывает на экземпляр переданного типа.</span><span class="sxs-lookup"><span data-stu-id="410e4-107">The parameter points to the instance of the transmitted type.</span></span> <span data-ttu-id="410e4-108">Этот объект не должен освобождаться.</span><span class="sxs-lookup"><span data-stu-id="410e4-108">This object should not be freed.</span></span> <span data-ttu-id="410e4-109">Обсуждение того, когда следует вызывать функцию, см. [в разделе \_ атрибут представления как](the-represent-as-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="410e4-109">For a discussion on when to call the function, see [The represent\_as Attribute](the-represent-as-attribute.md).</span></span>

 

 




