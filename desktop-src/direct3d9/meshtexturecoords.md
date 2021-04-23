---
description: Определяет координаты текстуры сетки.
ms.assetid: c87eb176-b502-49b6-bc73-401cc46e8412
title: мештекстурекурдс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974ec31f4358578277cfac46dc014f34752df46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805303"
---
# <a name="meshtexturecoords"></a><span data-ttu-id="d7be2-103">мештекстурекурдс</span><span class="sxs-lookup"><span data-stu-id="d7be2-103">MeshTextureCoords</span></span>

<span data-ttu-id="d7be2-104">Определяет координаты текстуры сетки.</span><span class="sxs-lookup"><span data-stu-id="d7be2-104">Defines a mesh's texture coordinates.</span></span>

``` syntax
template MeshTextureCoords
{
    < F6F23F40-7686-11cf-8F52-0040333594A3 >
    DWORD nTextureCoords;
    array Coords2d textureCoords[nTextureCoords] ;
} 
```

<span data-ttu-id="d7be2-105">Где:</span><span class="sxs-lookup"><span data-stu-id="d7be2-105">Where:</span></span>

-   <span data-ttu-id="d7be2-106">Нтекстурекурдс — число координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="d7be2-106">nTextureCoords - Number of texture coordinates.</span></span>
-   <span data-ttu-id="d7be2-107">Array Coords2d Текстурекурдс \[ нтекстурекурдс \] — Массив координат двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="d7be2-107">array Coords2d textureCoords\[nTextureCoords\] - Array of 2D texture coordinates.</span></span> <span data-ttu-id="d7be2-108">См. [**Coords2d**](coords2d.md).</span><span class="sxs-lookup"><span data-stu-id="d7be2-108">See [**Coords2d**](coords2d.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d7be2-109">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7be2-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7be2-110">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="d7be2-110">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



