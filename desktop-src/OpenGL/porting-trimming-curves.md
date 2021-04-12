---
title: Перенос кривых обрезки
description: Кривые с обрезкими OpenGL очень похожи на кривые с изгибом в ГК. В следующей таблице перечислены функции IRI GL для определения усеченных кривых и их эквивалентных функций OpenGL.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Перенос GL по IRI, обрезка кривых
- Перенос из ДИАФРАГМы в ГК, обрезка кривых
- перенос в OpenGL из IRI GL, обрезка кривых
- Перенос по стандарту OpenGL из IRI GL, обрезка кривых
- Обрезка кривых
- кривые
- Перенос GL по IRI, кривые
- Перенос из IRI GL, кривых
- перенос в OpenGL из IRI GL, кривых
- Перенос по стандарту OpenGL из IRI GL, кривых
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258804"
---
# <a name="porting-trimming-curves"></a><span data-ttu-id="19320-114">Перенос кривых обрезки</span><span class="sxs-lookup"><span data-stu-id="19320-114">Porting Trimming Curves</span></span>

<span data-ttu-id="19320-115">Кривые с обрезкими OpenGL очень похожи на кривые с изгибом в ГК.</span><span class="sxs-lookup"><span data-stu-id="19320-115">OpenGL trimming curves are very similar to IRIS GL trimming curves.</span></span> <span data-ttu-id="19320-116">В следующей таблице перечислены функции IRI GL для определения усеченных кривых и их эквивалентных функций OpenGL.</span><span class="sxs-lookup"><span data-stu-id="19320-116">The following table lists the IRIS GL functions for defining trimming curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="19320-117">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="19320-117">IRIS GL function</span></span> | <span data-ttu-id="19320-118">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="19320-118">OpenGL function</span></span>                        | <span data-ttu-id="19320-119">Значение</span><span class="sxs-lookup"><span data-stu-id="19320-119">Meaning</span></span>                              |
|------------------|----------------------------------------|--------------------------------------|
| <span data-ttu-id="19320-120">**бгнтрим**</span><span class="sxs-lookup"><span data-stu-id="19320-120">**bgntrim**</span></span>      | [<span data-ttu-id="19320-121">**глубегинтрим**</span><span class="sxs-lookup"><span data-stu-id="19320-121">**gluBeginTrim**</span></span>](glubegintrim.md)   | <span data-ttu-id="19320-122">Начинает усечение определения кривой.</span><span class="sxs-lookup"><span data-stu-id="19320-122">Begins trimming-curve definition.</span></span>    |
| <span data-ttu-id="19320-123">**пвлкурве**</span><span class="sxs-lookup"><span data-stu-id="19320-123">**pwlcurve**</span></span>     | [<span data-ttu-id="19320-124">**глупвлкурве**</span><span class="sxs-lookup"><span data-stu-id="19320-124">**gluPwlCurve**</span></span>](glupwlcurve.md)     | <span data-ttu-id="19320-125">Определяет линейную кривую кусочно-.</span><span class="sxs-lookup"><span data-stu-id="19320-125">Defines a piecewise linear curve.</span></span>    |
| <span data-ttu-id="19320-126">**нурбскурве**</span><span class="sxs-lookup"><span data-stu-id="19320-126">**nurbscurve**</span></span>   | [<span data-ttu-id="19320-127">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="19320-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="19320-128">Задает атрибуты кривой обрезки.</span><span class="sxs-lookup"><span data-stu-id="19320-128">Specifies trimming-curve attributes.</span></span> |
| <span data-ttu-id="19320-129">**ендтрим**</span><span class="sxs-lookup"><span data-stu-id="19320-129">**endtrim**</span></span>      | [<span data-ttu-id="19320-130">**глуендтрим**</span><span class="sxs-lookup"><span data-stu-id="19320-130">**gluEndTrim**</span></span>](gluendtrim.md)       | <span data-ttu-id="19320-131">Завершает определение кривой обрезки.</span><span class="sxs-lookup"><span data-stu-id="19320-131">Ends trimming-curve definition.</span></span>      |



 

<span data-ttu-id="19320-132">??</span><span class="sxs-lookup"><span data-stu-id="19320-132">??</span></span>

 

 




