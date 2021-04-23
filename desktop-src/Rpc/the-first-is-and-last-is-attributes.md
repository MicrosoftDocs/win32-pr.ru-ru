---
title: Атрибуты first_is и last_is
description: Можно определить число переданных элементов, указав первый и последний элементы.
ms.assetid: bd4dcf42-64a7-4b05-ac55-be77c381eb2e
keywords:
- first_is
- last_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a2696db8e175f921b797176baaa8f3aa0263c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339049"
---
# <a name="the-first_is-and-last_is-attributes"></a><span data-ttu-id="2ce34-105">\[Атрибуты First \_ — \] и \[ Last \_ — \]</span><span class="sxs-lookup"><span data-stu-id="2ce34-105">The \[first\_is\] and \[last\_is\] Attributes</span></span>

<span data-ttu-id="2ce34-106">Можно определить число переданных элементов, указав первый и последний элементы.</span><span class="sxs-lookup"><span data-stu-id="2ce34-106">You can determine the number of transmitted elements by specifying the first and last elements.</span></span> <span data-ttu-id="2ce34-107">Используйте атрибуты \[ [**First \_ -**](/windows/desktop/Midl/first-is) \] и \[ [**Last \_ —**](/windows/desktop/Midl/last-is) \] как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="2ce34-107">Use the \[[**first\_is**](/windows/desktop/Midl/first-is)\] and \[[**last\_is**](/windows/desktop/Midl/last-is)\] attributes as shown:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(4.0)
]
interface arraytest
{

  void fArray4([in]               short sSize,
               [in]               short sLast,
               [in]               short sFirst,
               [in, 
                out,
                size_is(sSize),
                first_is(sFirst),
                last_is(sLast)]   char achArray[]) ;
}
```

 

 