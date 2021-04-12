---
description: Задает цвета вершин для сетки, а не применяет материал на каждое лицо или на сеть.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: мешвертексколорс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416557"
---
# <a name="meshvertexcolors"></a><span data-ttu-id="7b6ba-103">мешвертексколорс</span><span class="sxs-lookup"><span data-stu-id="7b6ba-103">MeshVertexColors</span></span>

<span data-ttu-id="7b6ba-104">Задает цвета вершин для сетки, а не применяет материал на каждое лицо или на сеть.</span><span class="sxs-lookup"><span data-stu-id="7b6ba-104">Specifies vertex colors for a mesh, instead of applying a material per face or per mesh.</span></span>

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

<span data-ttu-id="7b6ba-105">Где:</span><span class="sxs-lookup"><span data-stu-id="7b6ba-105">Where:</span></span>

-   <span data-ttu-id="7b6ba-106">Нвертексколорс — число цветов.</span><span class="sxs-lookup"><span data-stu-id="7b6ba-106">nVertexColors - Number of colors.</span></span> <span data-ttu-id="7b6ba-107">Это соответствует количеству вершин в сетке.</span><span class="sxs-lookup"><span data-stu-id="7b6ba-107">This matches the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="7b6ba-108">Array Индексколор Вертексколорс \[ нвертексколорс \] -массив индексированных цветов.</span><span class="sxs-lookup"><span data-stu-id="7b6ba-108">array IndexColor vertexColors\[nVertexColors\] - Array of indexed colors.</span></span> <span data-ttu-id="7b6ba-109">См. [**индекседколор**](indexedcolor.md).</span><span class="sxs-lookup"><span data-stu-id="7b6ba-109">See [**IndexedColor**](indexedcolor.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7b6ba-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b6ba-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b6ba-111">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="7b6ba-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



