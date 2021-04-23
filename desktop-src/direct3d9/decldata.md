---
description: Описывает объявление вершины.
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: деклдата
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a26d667f853db3044db3155c55eb4a6d941c6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494589"
---
# <a name="decldata"></a><span data-ttu-id="d899f-103">деклдата</span><span class="sxs-lookup"><span data-stu-id="d899f-103">DeclData</span></span>

<span data-ttu-id="d899f-104">Описывает объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="d899f-104">Describes a vertex declaration.</span></span>

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="d899f-105">Где:</span><span class="sxs-lookup"><span data-stu-id="d899f-105">Where:</span></span>

-   <span data-ttu-id="d899f-106">Нелементс — число элементов объявления вершины.</span><span class="sxs-lookup"><span data-stu-id="d899f-106">nElements - Number of vertex declaration elements.</span></span>
-   <span data-ttu-id="d899f-107">Elements \[ нелементс \] -Array элементов объявления вершины.</span><span class="sxs-lookup"><span data-stu-id="d899f-107">Elements\[nElements\] - Array of vertex declaration elements.</span></span>
-   <span data-ttu-id="d899f-108">Ндвордс — число DWORD.</span><span class="sxs-lookup"><span data-stu-id="d899f-108">nDWords - Number of DWORDS.</span></span>
-   <span data-ttu-id="d899f-109">\[ндвордс данных \] — массив DWORD, который содержит данные в каждом элементе вершины.</span><span class="sxs-lookup"><span data-stu-id="d899f-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="d899f-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d899f-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d899f-111">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="d899f-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



