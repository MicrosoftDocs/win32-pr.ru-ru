---
title: Перенос треугольников
description: Можно нарисовать три типа треугольников в отдельных треугольниках, лентах треугольников и вентиляторах с треугольниками.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Перенос GL по IRI, треугольники
- Перенос из IRI GL, треугольников
- перенос в OpenGL из IRI GL, треугольников
- Перенос по стандарту OpenGL из IRI GL, треугольников
- функции рисования, треугольники
- треугольники
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330987"
---
# <a name="porting-triangles"></a><span data-ttu-id="d6ac3-109">Перенос треугольников</span><span class="sxs-lookup"><span data-stu-id="d6ac3-109">Porting Triangles</span></span>

<span data-ttu-id="d6ac3-110">В OpenGL можно нарисовать три типа треугольников: отдельные треугольники, треугольники и вентиляторы треугольников.</span><span class="sxs-lookup"><span data-stu-id="d6ac3-110">You can draw three types of triangles in OpenGL: separate triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="d6ac3-111">OpenGL не имеет эквивалента функции IRI GL **сваптмеш** .</span><span class="sxs-lookup"><span data-stu-id="d6ac3-111">OpenGL has no equivalent for the IRIS GL **swaptmesh** function.</span></span> <span data-ttu-id="d6ac3-112">Вы можете добиться того же результата, используя сочетание треугольников, треугольников и вентиляторов треугольников.</span><span class="sxs-lookup"><span data-stu-id="d6ac3-112">You can achieve the same effect using a combination of triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="d6ac3-113">В следующей таблице перечислены функции IRI GL для рисования треугольников и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d6ac3-113">The following table lists the IRIS GL functions for drawing triangles and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="d6ac3-114">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="d6ac3-114">IRIS GL function</span></span>           | <span data-ttu-id="d6ac3-115">Эквивалентный параметр Глбегин</span><span class="sxs-lookup"><span data-stu-id="d6ac3-115">Equivalent glBegin parameter</span></span> | <span data-ttu-id="d6ac3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d6ac3-116">Meaning</span></span>                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | <span data-ttu-id="d6ac3-117">\_треугольники GL</span><span class="sxs-lookup"><span data-stu-id="d6ac3-117">GL\_TRIANGLES</span></span>                | <span data-ttu-id="d6ac3-118">Тройки вершин, интерпретируемые как треугольники.</span><span class="sxs-lookup"><span data-stu-id="d6ac3-118">Triples of vertices interpreted as triangles.</span></span> |
| <span data-ttu-id="d6ac3-119">**бгнтмеш**, **ендтмеш**</span><span class="sxs-lookup"><span data-stu-id="d6ac3-119">**bgntmesh**, **endtmesh**</span></span> | <span data-ttu-id="d6ac3-120">\_полоса треугольников GL \_</span><span class="sxs-lookup"><span data-stu-id="d6ac3-120">GL\_TRIANGLE\_STRIP</span></span>          | <span data-ttu-id="d6ac3-121">Связанные полосы треугольников.</span><span class="sxs-lookup"><span data-stu-id="d6ac3-121">Linked strips of triangles.</span></span>                   |
|                            | <span data-ttu-id="d6ac3-122">\_вентилятор с треугольником GL \_</span><span class="sxs-lookup"><span data-stu-id="d6ac3-122">GL\_TRIANGLE\_FAN</span></span>            | <span data-ttu-id="d6ac3-123">Связанные вентиляторы треугольников.</span><span class="sxs-lookup"><span data-stu-id="d6ac3-123">Linked fans of triangles.</span></span>                     |



 

<span data-ttu-id="d6ac3-124">??</span><span class="sxs-lookup"><span data-stu-id="d6ac3-124">??</span></span>

 

 




