---
title: Использование функций сглаживания
description: В следующей таблице перечислены функции сглаживания в ГК, а также их эквивалентные функции OpenGL.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Перенос GL в ГК, сглаживание
- Перенос из ДИАФРАГМы в ГК, сглаживание
- перенос в OpenGL из IRI GL, сглаживание
- Перенос по стандарту OpenGL из IRI GL, сглаживание
- сглаживание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253076"
---
# <a name="using-antialiasing-functions"></a><span data-ttu-id="d3144-108">Использование функций сглаживания</span><span class="sxs-lookup"><span data-stu-id="d3144-108">Using Antialiasing Functions</span></span>

<span data-ttu-id="d3144-109">В следующей таблице перечислены функции сглаживания в ГК, а также их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d3144-109">The following table lists IRIS GL antialiasing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="d3144-110">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="d3144-110">IRIS GL function</span></span> | <span data-ttu-id="d3144-111">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="d3144-111">OpenGL function</span></span>                                      | <span data-ttu-id="d3144-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d3144-112">Meaning</span></span>                           |
|------------------|------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="d3144-113">**пнтсмус**</span><span class="sxs-lookup"><span data-stu-id="d3144-113">**pntsmooth**</span></span>    | <span data-ttu-id="d3144-114">[**гленабле**](glenable.md) ( \_ Smooth для точки GL \_ )</span><span class="sxs-lookup"><span data-stu-id="d3144-114">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>   | <span data-ttu-id="d3144-115">Включает сглаживание точек.</span><span class="sxs-lookup"><span data-stu-id="d3144-115">Enables antialiasing of points.</span></span>   |
| <span data-ttu-id="d3144-116">**линесмус**</span><span class="sxs-lookup"><span data-stu-id="d3144-116">**linesmooth**</span></span>   | <span data-ttu-id="d3144-117">**гленабле**( \_ \_ гладкая линия GL)</span><span class="sxs-lookup"><span data-stu-id="d3144-117">**glEnable**( GL\_LINE\_SMOOTH )</span></span>                     | <span data-ttu-id="d3144-118">Включает сглаживание линий.</span><span class="sxs-lookup"><span data-stu-id="d3144-118">Enables antialiasing of lines.</span></span>    |
| <span data-ttu-id="d3144-119">**Smooth**</span><span class="sxs-lookup"><span data-stu-id="d3144-119">**polysmooth**</span></span>   | <span data-ttu-id="d3144-120">[**гленабле**](glenable.md) ( \_ \_ несглаженный многоугольник GL)</span><span class="sxs-lookup"><span data-stu-id="d3144-120">[**glEnable**](glenable.md) ( GL\_POLYGON\_SMOOTH )</span></span> | <span data-ttu-id="d3144-121">Включает сглаживание многоугольников.</span><span class="sxs-lookup"><span data-stu-id="d3144-121">Enables antialiasing of polygons.</span></span> |



 

<span data-ttu-id="d3144-122">Используйте эквивалентные вызовы [**глдисабле**](gldisable.md) для отключения сглаживания.</span><span class="sxs-lookup"><span data-stu-id="d3144-122">Use the equivalent [**glDisable**](gldisable.md) calls to turn off antialiasing.</span></span>

<span data-ttu-id="d3144-123">В IRI GL можно управлять качеством сглаживания, вызывая:</span><span class="sxs-lookup"><span data-stu-id="d3144-123">In IRIS GL, you can control the quality of the antialiasing by calling:</span></span>


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



<span data-ttu-id="d3144-124">OpenGL предоставляет аналогичные контролусе [**глхинт**](glhint.md):</span><span class="sxs-lookup"><span data-stu-id="d3144-124">OpenGL provides similar controluse [**glHint**](glhint.md):</span></span>


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



<span data-ttu-id="d3144-125">где *хинтмоде* является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="d3144-125">where *hintMode* is one of the following:</span></span>

-   <span data-ttu-id="d3144-126">\_НИЦЕСТ GL (используйте наилучшее качество сглаживания.)</span><span class="sxs-lookup"><span data-stu-id="d3144-126">GL\_NICEST (Use the highest quality smoothing.)</span></span>
-   <span data-ttu-id="d3144-127">\_Самая быстрая (используйте наиболее эффективное сглаживание).</span><span class="sxs-lookup"><span data-stu-id="d3144-127">GL\_FASTEST (Use the most efficient smoothing.)</span></span>
-   <span data-ttu-id="d3144-128">\_Неа \_ GL</span><span class="sxs-lookup"><span data-stu-id="d3144-128">GL\_DONT\_CARE</span></span>

<span data-ttu-id="d3144-129">IRI GL также разрешает конечное исправление путем вызова:</span><span class="sxs-lookup"><span data-stu-id="d3144-129">IRIS GL also permits end-correction by calling:</span></span>


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



<span data-ttu-id="d3144-130">OpenGL не имеет эквивалента для этой функции.</span><span class="sxs-lookup"><span data-stu-id="d3144-130">OpenGL has no equivalent for this function.</span></span>

 

 




