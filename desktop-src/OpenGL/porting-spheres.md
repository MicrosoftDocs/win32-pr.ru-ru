---
title: Перенос шарик
description: При переносе шарик на OpenGL учитывайте следующие моменты.
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Перенос GL в ГК, шарик
- Перенос из IRI GL, шарик
- перенос в OpenGL из IRI GL, шарик
- Перенос по стандарту OpenGL из IRI GL, шарик
- функции рисования, шарик
- шарик
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411121"
---
# <a name="porting-spheres"></a><span data-ttu-id="8fab0-109">Перенос шарик</span><span class="sxs-lookup"><span data-stu-id="8fab0-109">Porting Spheres</span></span>

<span data-ttu-id="8fab0-110">При переносе шарик в OpenGL учитывайте следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="8fab0-110">When porting spheres to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="8fab0-111">Нельзя управлять типами примитивов, используемых для рисования сферы.</span><span class="sxs-lookup"><span data-stu-id="8fab0-111">You cannot control the type of primitives used to draw the sphere.</span></span> <span data-ttu-id="8fab0-112">Можно управлять точностью рисования другим способом: используйте параметры срезы и стеки.</span><span class="sxs-lookup"><span data-stu-id="8fab0-112">You can control drawing precision in another way: use the slices and stacks parameters.</span></span> <span data-ttu-id="8fab0-113">Срезы — это долготу; стеки — широту.</span><span class="sxs-lookup"><span data-stu-id="8fab0-113">Slices are longitudinal; stacks are latitudinal.</span></span>
-   <span data-ttu-id="8fab0-114">Шарик рисуются по центру источника.</span><span class="sxs-lookup"><span data-stu-id="8fab0-114">Spheres are drawn centered at the origin.</span></span> <span data-ttu-id="8fab0-115">Вместо указания местоположения, как это делается с помощью функции IRI GL **сфдрав** , перед вызовом функции [**глусфере**](glusphere.md) Glu с переводом.</span><span class="sxs-lookup"><span data-stu-id="8fab0-115">Instead of specifying the location, as you do with the IRIS GL **sphdraw** function, precede a call to the GLU [**gluSphere**](glusphere.md) function with a translation.</span></span>
-   <span data-ttu-id="8fab0-116">Библиотека сфер пока недоступна для OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8fab0-116">The sphere library is not yet available for OpenGL.</span></span>

<span data-ttu-id="8fab0-117">В следующей таблице перечислены функции IRI GL для рисования шарик и их эквивалентные функции GLU, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="8fab0-117">The following table lists the IRIS GL functions for drawing spheres and their equivalent GLU functions where available.</span></span>



| <span data-ttu-id="8fab0-118">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="8fab0-118">IRIS GL function</span></span> | <span data-ttu-id="8fab0-119">Функция GLU</span><span class="sxs-lookup"><span data-stu-id="8fab0-119">GLU function</span></span>                                 | <span data-ttu-id="8fab0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8fab0-120">Meaning</span></span>                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="8fab0-121">**сфобж**</span><span class="sxs-lookup"><span data-stu-id="8fab0-121">**sphobj**</span></span>       | [<span data-ttu-id="8fab0-122">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="8fab0-122">**gluNewQuadric**</span></span>](glunewquadric.md)       | <span data-ttu-id="8fab0-123">Создает новый объект sphere.</span><span class="sxs-lookup"><span data-stu-id="8fab0-123">Creates a new sphere object.</span></span>                  |
| <span data-ttu-id="8fab0-124">**сффри**</span><span class="sxs-lookup"><span data-stu-id="8fab0-124">**sphfree**</span></span>      | [<span data-ttu-id="8fab0-125">**глуделетекуадрик**</span><span class="sxs-lookup"><span data-stu-id="8fab0-125">**gluDeleteQuadric**</span></span>](gludeletequadric.md) | <span data-ttu-id="8fab0-126">Удаляет объект Sphere и используемую свободную память.</span><span class="sxs-lookup"><span data-stu-id="8fab0-126">Deletes sphere object and free memory used.</span></span>   |
| <span data-ttu-id="8fab0-127">**сфдрав**</span><span class="sxs-lookup"><span data-stu-id="8fab0-127">**sphdraw**</span></span>      | [<span data-ttu-id="8fab0-128">**глусфере**</span><span class="sxs-lookup"><span data-stu-id="8fab0-128">**gluSphere**</span></span>](glusphere.md)               | <span data-ttu-id="8fab0-129">Рисует сферу.</span><span class="sxs-lookup"><span data-stu-id="8fab0-129">Draws a sphere.</span></span>                               |
| <span data-ttu-id="8fab0-130">**сфмоде**</span><span class="sxs-lookup"><span data-stu-id="8fab0-130">**sphmode**</span></span>      |                                              | <span data-ttu-id="8fab0-131">Задает атрибуты сферы.</span><span class="sxs-lookup"><span data-stu-id="8fab0-131">Sets sphere attributes.</span></span>                       |
| <span data-ttu-id="8fab0-132">**сфротматрикс**</span><span class="sxs-lookup"><span data-stu-id="8fab0-132">**sphrotmatrix**</span></span> |                                              | <span data-ttu-id="8fab0-133">Управляет ориентацией на сферу.</span><span class="sxs-lookup"><span data-stu-id="8fab0-133">Controls sphere orientation.</span></span>                  |
| <span data-ttu-id="8fab0-134">**сфгнполис**</span><span class="sxs-lookup"><span data-stu-id="8fab0-134">**sphgnpolys**</span></span>   |                                              | <span data-ttu-id="8fab0-135">Возвращает число многоугольников в текущей сфере.</span><span class="sxs-lookup"><span data-stu-id="8fab0-135">Returns number of polygons in current sphere.</span></span> |



 

<span data-ttu-id="8fab0-136">??</span><span class="sxs-lookup"><span data-stu-id="8fab0-136">??</span></span>

 

 




