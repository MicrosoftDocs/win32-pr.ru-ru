---
title: Точки переноса
description: OpenGL не имеет команды для рисования одной точки. В противном случае функции точек переноса просты. В следующей таблице перечислены функции IRI GL для точек рисования и их эквивалентные функции OpenGL.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Перенос GL по IRI, точки
- Перенос из IRI GL, баллы
- перенос в OpenGL из IRI GL, баллы
- Перенос по стандарту OpenGL из IRI GL, баллы
- функции рисования, точки
- точки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661596"
---
# <a name="porting-points"></a><span data-ttu-id="9442c-111">Точки переноса</span><span class="sxs-lookup"><span data-stu-id="9442c-111">Porting Points</span></span>

<span data-ttu-id="9442c-112">OpenGL не имеет команды для рисования одной точки.</span><span class="sxs-lookup"><span data-stu-id="9442c-112">OpenGL has no command to draw a single point.</span></span> <span data-ttu-id="9442c-113">В противном случае функции точек переноса просты.</span><span class="sxs-lookup"><span data-stu-id="9442c-113">Otherwise, porting point functions is straightforward.</span></span> <span data-ttu-id="9442c-114">В следующей таблице перечислены функции IRI GL для точек рисования и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9442c-114">The following table lists IRIS GL functions for drawing points and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="9442c-115">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="9442c-115">IRIS GL function</span></span>           | <span data-ttu-id="9442c-116">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="9442c-116">OpenGL function</span></span>                                                   | <span data-ttu-id="9442c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9442c-117">Meaning</span></span>                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9442c-118">**дочерней PNT**</span><span class="sxs-lookup"><span data-stu-id="9442c-118">**pnt**</span></span>                    |                                                                   | <span data-ttu-id="9442c-119">Рисует одну точку.</span><span class="sxs-lookup"><span data-stu-id="9442c-119">Draws a single point.</span></span>                                                                                                                                |
| <span data-ttu-id="9442c-120">**бгнпоинт**, **Конечная точка**</span><span class="sxs-lookup"><span data-stu-id="9442c-120">**bgnpoint**, **endpoint**</span></span> | <span data-ttu-id="9442c-121">[**глбегин**](glbegin.md) ( \_ пункты GL), [ **гленд**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="9442c-121">[**glBegin**](glbegin.md) ( GL\_POINTS ), [**glEnd**](glend.md)</span></span> | <span data-ttu-id="9442c-122">Интерпретирует вершины как точки.</span><span class="sxs-lookup"><span data-stu-id="9442c-122">Interprets vertices as points.</span></span>                                                                                                                       |
| <span data-ttu-id="9442c-123">**пнтсизе**</span><span class="sxs-lookup"><span data-stu-id="9442c-123">**pntsize**</span></span>                | [<span data-ttu-id="9442c-124">**глпоинтсизе**</span><span class="sxs-lookup"><span data-stu-id="9442c-124">**glPointSize**</span></span>](glpointsize.md)                                | <span data-ttu-id="9442c-125">Задает размер точки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="9442c-125">Sets point size in pixels.</span></span>                                                                                                                           |
| <span data-ttu-id="9442c-126">**пнтсмус**</span><span class="sxs-lookup"><span data-stu-id="9442c-126">**pntsmooth**</span></span>              | <span data-ttu-id="9442c-127">[**гленабле**](glenable.md) ( \_ Smooth для точки GL \_ )</span><span class="sxs-lookup"><span data-stu-id="9442c-127">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>                | <span data-ttu-id="9442c-128">Включает сглаживание точек.</span><span class="sxs-lookup"><span data-stu-id="9442c-128">Turns on point antialiasing.</span></span> <span data-ttu-id="9442c-129">(Дополнительные сведения о сглаживание точек см. в разделе [Перенос функций сглаживания](porting-antialiasing-functions.md).)</span><span class="sxs-lookup"><span data-stu-id="9442c-129">(For more information on point antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="9442c-130">Дополнительные сведения о связанных функциях Get см. в разделе [**глпоинтсизе**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="9442c-130">For information about related get functions, see [**glPointSize**](glpointsize.md).</span></span>

<span data-ttu-id="9442c-131">??</span><span class="sxs-lookup"><span data-stu-id="9442c-131">??</span></span>

 

 




