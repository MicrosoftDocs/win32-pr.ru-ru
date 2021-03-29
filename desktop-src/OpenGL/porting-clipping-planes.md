---
title: Перенос плоскостей
description: OpenGL реализует отрезкиные плоскости аналогично IRI GL. Кроме того, в OpenGL можно запрашивать обтравочные плоскости. В следующей таблице перечислены функции и эквивалентные функции OpenGL компании IRI GL.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Перенос в ГК по IRI, отсеченные плоскости
- Перенос из ДИАФРАГМы в ГК, обтравочные плоскости
- Перенос на OpenGL из IRI GL, обтравочные плоскости
- Перенос из OpenGL в ДИАФРАГМу, обтравочные плоскости
- обтравочные плоскости
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779118"
---
# <a name="porting-clipping-planes"></a><span data-ttu-id="e12f0-110">Перенос плоскостей</span><span class="sxs-lookup"><span data-stu-id="e12f0-110">Porting Clipping Planes</span></span>

<span data-ttu-id="e12f0-111">OpenGL реализует отрезкиные плоскости аналогично IRI GL.</span><span class="sxs-lookup"><span data-stu-id="e12f0-111">OpenGL implements clipping planes similarly to IRIS GL.</span></span> <span data-ttu-id="e12f0-112">Кроме того, в OpenGL можно запрашивать обтравочные плоскости.</span><span class="sxs-lookup"><span data-stu-id="e12f0-112">In addition, in OpenGL you can query clipping planes.</span></span> <span data-ttu-id="e12f0-113">В следующей таблице перечислены функции и эквивалентные функции OpenGL компании IRI GL.</span><span class="sxs-lookup"><span data-stu-id="e12f0-113">The following table lists IRIS GL clipping plane functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="e12f0-114">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="e12f0-114">IRIS GL function</span></span>                          | <span data-ttu-id="e12f0-115">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="e12f0-115">OpenGL function</span></span>                                                                               | <span data-ttu-id="e12f0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e12f0-116">Meaning</span></span>                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="e12f0-117">**клипплане** (i, **CP \_ вкл**., параметры)</span><span class="sxs-lookup"><span data-stu-id="e12f0-117">**clipplane** (i, **CP\_ON**, params)</span></span>     | <span data-ttu-id="e12f0-118">[**гленабле**](glenable.md) ( \_ клип GL \_ планеи)</span><span class="sxs-lookup"><span data-stu-id="e12f0-118">[**glEnable**](glenable.md) ( GL\_CLIP\_PLANEi )</span></span>                                             | <span data-ttu-id="e12f0-119">Включает обрезку на плоскости i.</span><span class="sxs-lookup"><span data-stu-id="e12f0-119">Enables clipping on plane i.</span></span>             |
| <span data-ttu-id="e12f0-120">**клипплане**(i, **CP- \_ Определение**, плоскость)</span><span class="sxs-lookup"><span data-stu-id="e12f0-120">**clipplane**( i, **CP\_DEFINE**, plane )</span></span> | <span data-ttu-id="e12f0-121">[**глклипплане**](glclipplane.md) ( \_ планеи Clip \_ , плоскость)</span><span class="sxs-lookup"><span data-stu-id="e12f0-121">[**glClipPlane**](glclipplane.md) ( GL\_CLIP\_PLANEi, plane )</span></span>                                | <span data-ttu-id="e12f0-122">Определяет плоскость обрезки.</span><span class="sxs-lookup"><span data-stu-id="e12f0-122">Defines clipping plane.</span></span>                  |
|                                           | [<span data-ttu-id="e12f0-123">**глжетклипплане**</span><span class="sxs-lookup"><span data-stu-id="e12f0-123">**glGetClipPlane**</span></span>](glgetclipplane.md)                                                      | <span data-ttu-id="e12f0-124">Возвращает уравнение обрезанной плоскости.</span><span class="sxs-lookup"><span data-stu-id="e12f0-124">Returns clipping plane equation.</span></span>         |
|                                           | <span data-ttu-id="e12f0-125">[**глисенаблед**](glisenabled.md) ( \_ клип GL \_ планеи)</span><span class="sxs-lookup"><span data-stu-id="e12f0-125">[**glIsEnabled**](glisenabled.md) ( GL\_CLIP\_PLANEi )</span></span>                                       | <span data-ttu-id="e12f0-126">Возвращает значение true, если включена плоскость клипа i.</span><span class="sxs-lookup"><span data-stu-id="e12f0-126">Returns true if clip plane i is enabled.</span></span> |
| <span data-ttu-id="e12f0-127">**скрмаск**</span><span class="sxs-lookup"><span data-stu-id="e12f0-127">**scrmask**</span></span>                               | [<span data-ttu-id="e12f0-128">**глсЦиссор**</span><span class="sxs-lookup"><span data-stu-id="e12f0-128">**glScissor**</span></span>](glscissor.md)                                                                | <span data-ttu-id="e12f0-129">Определяет прямоугольный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="e12f0-129">Defines the scissor box.</span></span>                 |
| <span data-ttu-id="e12f0-130">**жетскрмаск**</span><span class="sxs-lookup"><span data-stu-id="e12f0-130">**getscrmask**</span></span>                            | <span data-ttu-id="e12f0-131">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ распашная \_ раскрывающийся список)</span><span class="sxs-lookup"><span data-stu-id="e12f0-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SCISSOR\_BOX )</span></span> | <span data-ttu-id="e12f0-132">Возвращает текущее прямоугольное поле.</span><span class="sxs-lookup"><span data-stu-id="e12f0-132">Returns the current scissor box.</span></span>         |



 

<span data-ttu-id="e12f0-133">Чтобы включить режим прямоугольного теста, вызовите **гленабле** , \_ используя \_ в качестве параметра прямоугольную ножницу.</span><span class="sxs-lookup"><span data-stu-id="e12f0-133">To turn on the scissor test, call **glEnable** using GL\_SCISSOR\_BOX as the parameter.</span></span>

<span data-ttu-id="e12f0-134">??</span><span class="sxs-lookup"><span data-stu-id="e12f0-134">??</span></span>

 

 




