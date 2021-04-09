---
description: Задает данные сетки за вычетом данных о положении.
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: фвфдата
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52af6096357c4855d2dc34442c6cd4814b6713b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139555"
---
# <a name="fvfdata"></a><span data-ttu-id="ea94b-103">фвфдата</span><span class="sxs-lookup"><span data-stu-id="ea94b-103">FVFData</span></span>

<span data-ttu-id="ea94b-104">Задает данные сетки за вычетом данных о положении.</span><span class="sxs-lookup"><span data-stu-id="ea94b-104">Specifies the mesh data minus the position data.</span></span>

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="ea94b-105">Где:</span><span class="sxs-lookup"><span data-stu-id="ea94b-105">Where:</span></span>

-   <span data-ttu-id="ea94b-106">Двфвф — код ФВФ.</span><span class="sxs-lookup"><span data-stu-id="ea94b-106">dwFVF - A FVF code.</span></span>
-   <span data-ttu-id="ea94b-107">Ндвордс — двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="ea94b-107">nDWords - Binary data.</span></span> <span data-ttu-id="ea94b-108">Число DWORD.</span><span class="sxs-lookup"><span data-stu-id="ea94b-108">The number of DWORDS.</span></span>
-   <span data-ttu-id="ea94b-109">\[ндвордс данных \] — массив DWORD, который содержит данные в каждом элементе вершины.</span><span class="sxs-lookup"><span data-stu-id="ea94b-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea94b-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea94b-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea94b-111">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="ea94b-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



