---
title: Перенос функций v
description: В IRI GL для указания вершин используются варианты в функции v. Эквивалентная функция OpenGL Глвертекс ниже — примеры Глвертекс.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- Перенос GL в ГК, вершины
- Перенос из IRI GL, вершин
- перенос в OpenGL из IRI GL, вершин
- Перенос по стандарту OpenGL из IRI GL, вершин
- функции рисования, вершины
- вершины, перенос из IRI GL
- Перенос GL в ГК, функции v
- Перенос из функций IRI GL, v
- перенос в OpenGL из функций IRI GL, v
- Перенос по стандарту OpenGL из функций IRI GL, v
- функции рисования, функции v
- функции v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329419"
---
# <a name="porting-v-functions"></a><span data-ttu-id="897d7-116">Перенос функций v</span><span class="sxs-lookup"><span data-stu-id="897d7-116">Porting v Functions</span></span>

<span data-ttu-id="897d7-117">В IRI GL для указания вершин используются варианты в функции **v** .</span><span class="sxs-lookup"><span data-stu-id="897d7-117">In IRIS GL, you use variations on the **v** function to specify vertices.</span></span> <span data-ttu-id="897d7-118">Эквивалентная функция OpenGL — [глвертекс](glvertex-functions.md): ниже приведены примеры **глвертекс**.</span><span class="sxs-lookup"><span data-stu-id="897d7-118">The equivalent OpenGL function is [glVertex](glvertex-functions.md): Below are examples of **glVertex**.</span></span>

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

<span data-ttu-id="897d7-119">Функция **глвертекс** использует суффиксы так же, как и другие вызовы OpenGL.</span><span class="sxs-lookup"><span data-stu-id="897d7-119">The **glVertex** function takes suffixes the same way other OpenGL calls do.</span></span> <span data-ttu-id="897d7-120">Векторные версии вызова принимают массивы соответствующего размера в качестве аргументов.</span><span class="sxs-lookup"><span data-stu-id="897d7-120">The vector versions of the call take arrays of the proper size as arguments.</span></span> <span data-ttu-id="897d7-121">В двумерной версии z = 0 и w = 1.</span><span class="sxs-lookup"><span data-stu-id="897d7-121">In the 2-D version, z=0 and w=1.</span></span> <span data-ttu-id="897d7-122">В трехмерной версии w = 1.</span><span class="sxs-lookup"><span data-stu-id="897d7-122">In the 3-D version, w=1.</span></span>

 

 




