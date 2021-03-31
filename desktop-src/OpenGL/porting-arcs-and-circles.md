---
title: Перенос дуг и кругов
description: При использовании OpenGL заполненные дуги и окружности рисуются с помощью тех же вызовов, что и незаполненные дуги и круги. В следующей таблице перечислены функции дуги и кружка IRI GL, а также их эквивалентные функции OpenGL (GLU).
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- Перенос GL по IRI, дуги
- Перенос из ДИАФРАГМы в ГК, дуги
- перенос в OpenGL из IRI GL, Дуг
- Перенос по стандарту OpenGL из IRI GL, Дуг
- функции рисования, дуги
- Перенос GL по IRI, круги
- Перенос из IRI GL, кругов
- Перенос на OpenGL из IRI GL, круги
- Перенос по стандарту OpenGL из IRI GL, кругов
- функции рисования, круги
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411375"
---
# <a name="porting-arcs-and-circles"></a><span data-ttu-id="f1e6c-114">Перенос дуг и кругов</span><span class="sxs-lookup"><span data-stu-id="f1e6c-114">Porting Arcs and Circles</span></span>

<span data-ttu-id="f1e6c-115">При использовании OpenGL заполненные дуги и окружности рисуются с помощью тех же вызовов, что и незаполненные дуги и круги.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-115">With OpenGL, filled arcs and circles are drawn with the same calls as unfilled arcs and circles.</span></span> <span data-ttu-id="f1e6c-116">В следующей таблице перечислены функции дуги и кружка IRI GL, а также их эквивалентные функции OpenGL (GLU).</span><span class="sxs-lookup"><span data-stu-id="f1e6c-116">The following table lists the IRIS GL arc and circle functions and their equivalent OpenGL (GLU) functions.</span></span>



| <span data-ttu-id="f1e6c-117">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="f1e6c-117">IRIS GL function</span></span> | <span data-ttu-id="f1e6c-118">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="f1e6c-118">OpenGL function</span></span>                          | <span data-ttu-id="f1e6c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f1e6c-119">Meaning</span></span>                 |
|------------------|------------------------------------------|-------------------------|
| <span data-ttu-id="f1e6c-120">**аркаркф**</span><span class="sxs-lookup"><span data-stu-id="f1e6c-120">**arcarcf**</span></span>      | [<span data-ttu-id="f1e6c-121">**глупартиалдиск**</span><span class="sxs-lookup"><span data-stu-id="f1e6c-121">**gluPartialDisk**</span></span>](glupartialdisk.md) | <span data-ttu-id="f1e6c-122">Рисование дуги.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-122">Draws an arc.</span></span>           |
| <span data-ttu-id="f1e6c-123">**ЦиркЦиркф**</span><span class="sxs-lookup"><span data-stu-id="f1e6c-123">**circcircf**</span></span>    | [<span data-ttu-id="f1e6c-124">**глудиск**</span><span class="sxs-lookup"><span data-stu-id="f1e6c-124">**gluDisk**</span></span>](gludisk.md)               | <span data-ttu-id="f1e6c-125">Рисует круг или диск.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-125">Draws a circle or disk.</span></span> |



 

<span data-ttu-id="f1e6c-126">Вы можете выполнять некоторые действия с помощью дуг и кругов OpenGL, которые невозможно выполнить с помощью IRI GL.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-126">You can do some things with OpenGL arcs and circles that you can't do with IRIS GL.</span></span> <span data-ttu-id="f1e6c-127">OpenGL вызывает дуги и окружности, диски и частичные диски соответственно.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-127">OpenGL calls arcs and circles, disks and partial disks respectively.</span></span>

<span data-ttu-id="f1e6c-128">При переносе дуг и кругов учитывайте следующие моменты, связанные с OpenGL:</span><span class="sxs-lookup"><span data-stu-id="f1e6c-128">When porting arcs and circles, keep the following points about OpenGL in mind:</span></span>

-   <span data-ttu-id="f1e6c-129">Углы измеряются в градусах, а не в десятых градусах.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-129">Angles are measured in degrees, and not in tenths of degrees.</span></span>
-   <span data-ttu-id="f1e6c-130">Начальный угол измеряется от положительной оси y, а не от оси x.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-130">The start angle is measured from the positive y-axis, and not from the x-axis.</span></span>
-   <span data-ttu-id="f1e6c-131">Угол поворота теперь не отличается против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-131">The sweep angle is now clockwise instead of counterclockwise.</span></span>

<span data-ttu-id="f1e6c-132">??</span><span class="sxs-lookup"><span data-stu-id="f1e6c-132">??</span></span>

 

 




