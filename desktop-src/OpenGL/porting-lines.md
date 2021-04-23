---
title: Перенос строк
description: Перенос кода в ГК, который рисует строки, довольно прост, хотя следует обратить внимание на различия в способах стипплес OpenGL. В следующей таблице перечислены функции IRI GL для рисования линий и их эквивалентных функций OpenGL.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Перенос в ГК по IRI, строки
- Перенос из IRI GL, строки
- перенос в OpenGL из IRI GL, строки
- Перенос по стандарту OpenGL из IRI GL, строк
- функции рисования, линии
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258806"
---
# <a name="porting-lines"></a><span data-ttu-id="da687-110">Перенос строк</span><span class="sxs-lookup"><span data-stu-id="da687-110">Porting Lines</span></span>

<span data-ttu-id="da687-111">Перенос кода в ГК, который рисует строки, довольно прост, хотя следует обратить внимание на различия в способах стипплес OpenGL.</span><span class="sxs-lookup"><span data-stu-id="da687-111">Porting IRIS GL code that draws lines is fairly straightforward, though you should note the differences in the way OpenGL stipples.</span></span> <span data-ttu-id="da687-112">В следующей таблице перечислены функции IRI GL для рисования линий и их эквивалентных функций OpenGL.</span><span class="sxs-lookup"><span data-stu-id="da687-112">The following table lists IRIS GL functions for drawing lines and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="da687-113">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="da687-113">IRIS GL function</span></span>                               | <span data-ttu-id="da687-114">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="da687-114">OpenGL function</span></span>                                                                                         | <span data-ttu-id="da687-115">Значение</span><span class="sxs-lookup"><span data-stu-id="da687-115">Meaning</span></span>                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da687-116">**бгнклоседлине**,**ендклоседлине**</span><span class="sxs-lookup"><span data-stu-id="da687-116">**bgnclosedline**,**endclosedline**</span></span><br/> | <span data-ttu-id="da687-117">[**глбегин**](glbegin.md) ( \_ линейный \_ цикл GL)[**гленд**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="da687-117">[**glBegin**](glbegin.md) ( GL\_LINE\_LOOP )[**glEnd**](glend.md)</span></span><br/>                          | <span data-ttu-id="da687-118">Рисует замкнутую линию.</span><span class="sxs-lookup"><span data-stu-id="da687-118">Draws a closed line.</span></span>                                                                                                                         |
| <span data-ttu-id="da687-119">**бгнлине**</span><span class="sxs-lookup"><span data-stu-id="da687-119">**bgnline**</span></span>                                    | <span data-ttu-id="da687-120">[**глбегин**](glbegin.md) ( \_ \_ полоса строк GL)</span><span class="sxs-lookup"><span data-stu-id="da687-120">[**glBegin**](glbegin.md) ( GL\_LINE\_STRIP )</span></span>                                                          | <span data-ttu-id="da687-121">Рисует сегменты линии.</span><span class="sxs-lookup"><span data-stu-id="da687-121">Draws line segments.</span></span>                                                                                                                         |
| <span data-ttu-id="da687-122">**линевидс**</span><span class="sxs-lookup"><span data-stu-id="da687-122">**linewidth**</span></span>                                  | [<span data-ttu-id="da687-123">**гллиневидс**</span><span class="sxs-lookup"><span data-stu-id="da687-123">**glLineWidth**</span></span>](gllinewidth.md)                                                                      | <span data-ttu-id="da687-124">Задает толщину линии.</span><span class="sxs-lookup"><span data-stu-id="da687-124">Sets line width.</span></span>                                                                                                                             |
| <span data-ttu-id="da687-125">**жетлвидс**</span><span class="sxs-lookup"><span data-stu-id="da687-125">**getlwidth**</span></span>                                  | <span data-ttu-id="da687-126">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ толщина линии GL \_ )</span><span class="sxs-lookup"><span data-stu-id="da687-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_WIDTH )</span></span>            | <span data-ttu-id="da687-127">Возвращает текущую толщину линии.</span><span class="sxs-lookup"><span data-stu-id="da687-127">Returns current line width.</span></span>                                                                                                                  |
| <span data-ttu-id="da687-128">**дефлинестиле**,**сетлинестиле**</span><span class="sxs-lookup"><span data-stu-id="da687-128">**deflinestyle**,**setlinestyle**</span></span><br/>   | [<span data-ttu-id="da687-129">**гллинестиппле**</span><span class="sxs-lookup"><span data-stu-id="da687-129">**glLineStipple**</span></span>](gllinestipple.md)                                                                  | <span data-ttu-id="da687-130">Задает шаблон стиппле линий.</span><span class="sxs-lookup"><span data-stu-id="da687-130">Specifies a line stipple pattern.</span></span>                                                                                                            |
| <span data-ttu-id="da687-131">**лсрепеат**</span><span class="sxs-lookup"><span data-stu-id="da687-131">**lsrepeat**</span></span>                                   | <span data-ttu-id="da687-132">аргумент factor параметра **гллинестиппле**</span><span class="sxs-lookup"><span data-stu-id="da687-132">factor argument of **glLineStipple**</span></span>                                                                    | <span data-ttu-id="da687-133">Задает коэффициент повтора для стиля линии.</span><span class="sxs-lookup"><span data-stu-id="da687-133">Sets a repeat factor for the line style.</span></span>                                                                                                     |
| <span data-ttu-id="da687-134">**жетлстиле**</span><span class="sxs-lookup"><span data-stu-id="da687-134">**getlstyle**</span></span>                                  | <span data-ttu-id="da687-135">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ \_ шаблон стиппле строки GL \_ )</span><span class="sxs-lookup"><span data-stu-id="da687-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_PATTERN )</span></span> | <span data-ttu-id="da687-136">Возвращает шаблон строки стиппле.</span><span class="sxs-lookup"><span data-stu-id="da687-136">Returns line stipple pattern.</span></span>                                                                                                                |
| <span data-ttu-id="da687-137">**жетлсрепеат**</span><span class="sxs-lookup"><span data-stu-id="da687-137">**getlsrepeat**</span></span>                                | <span data-ttu-id="da687-138">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ строка GL \_ стиппле \_ repeat)</span><span class="sxs-lookup"><span data-stu-id="da687-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_REPEAT )</span></span>  | <span data-ttu-id="da687-139">Возвращает коэффициент повтора.</span><span class="sxs-lookup"><span data-stu-id="da687-139">Returns repeat factor.</span></span>                                                                                                                       |
| <span data-ttu-id="da687-140">**линесмус**, **смуслине**</span><span class="sxs-lookup"><span data-stu-id="da687-140">**linesmooth**, **smoothline**</span></span>                 | <span data-ttu-id="da687-141">[**гленабле**](glenable.md) ( \_ \_ гладкая линия GL)</span><span class="sxs-lookup"><span data-stu-id="da687-141">[**glEnable**](glenable.md) ( GL\_LINE\_SMOOTH )</span></span>                                                       | <span data-ttu-id="da687-142">Включает Сглаживание линии (Дополнительные сведения о сглаживание см. в разделе [Перенос функций сглаживания](porting-antialiasing-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="da687-142">Turns on line antialiasing (For more information on antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="da687-143">OpenGL не использует таблицы для строки стипплес; Он поддерживает только один шаблон «Line-стиппле».</span><span class="sxs-lookup"><span data-stu-id="da687-143">OpenGL doesn't use tables for line stipples; it maintains only one line-stipple pattern.</span></span> <span data-ttu-id="da687-144">Для переключения между различными шаблонами стиппле можно использовать [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="da687-144">You can use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to switch between different stipple patterns.</span></span>

<span data-ttu-id="da687-145">Старые функции стилей линий IRI GL (например, **Draw**, **лсбаккуп**, **жетлсбаккуп** и т. д.) не поддерживаются OpenGL.</span><span class="sxs-lookup"><span data-stu-id="da687-145">Older IRIS GL line style functions (such as **draw**, **lsbackup**, **getlsbackup**, and so on) are not supported by OpenGL.</span></span>

<span data-ttu-id="da687-146">Сведения о рисовании линий со сглаженными псевдонимами см. в разделе [Перенос функций сглаживания](porting-antialiasing-functions.md).</span><span class="sxs-lookup"><span data-stu-id="da687-146">For information on drawing antialiased lines, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).</span></span>

<span data-ttu-id="da687-147">??</span><span class="sxs-lookup"><span data-stu-id="da687-147">??</span></span>

 

 





