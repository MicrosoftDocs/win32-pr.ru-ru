---
title: Перенос команд на экран и очистку буфера
description: OpenGL заменяет различные функции очистки IRI GL (например, зклеар, аклеар, склеар и т. д.) с помощью одной функции Глклеар. Укажите, что именно нужно очистить, передав маски в Глклеар.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Перенос GL в ГК, очистка функций
- Перенос из IRI GL, очистка функций
- перенос в OpenGL из IRI GL, очистка функций
- Перенос по стандарту OpenGL из IRI GL, очистка функций
- очистить функции
- Перенос GL в ГК, команды очистки экрана
- Перенос из IRI GL, команды очистки экрана
- Перенос на OpenGL из IRI GL, команды очистки экрана
- Перенос по стандарту OpenGL из IRI GL, команды очистки экрана
- команды очистки экрана
- Перенос GL в ГК, команды очистки буфера
- Перенос из ДИАФРАГМы в ГК, команды очистки буфера
- перенос в OpenGL из IRI GL, команды очистки буфера
- Перенос по стандарту OpenGL из IRI GL, команды очистки буфера
- команды очистки буфера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661595"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a><span data-ttu-id="592a6-119">Перенос команд на экран и очистку буфера</span><span class="sxs-lookup"><span data-stu-id="592a6-119">Porting Screen and Buffer Clearing Commands</span></span>

<span data-ttu-id="592a6-120">OpenGL заменяет различные функции **очистки** IRI GL (например, **зклеар**, **аклеар**, **склеар** и т. д.) с помощью одной функции [**глклеар**](glclear.md).</span><span class="sxs-lookup"><span data-stu-id="592a6-120">OpenGL replaces a variety of IRIS GL **clear** functions (such as **zclear**, **aclear**, **sclear**, and so on) with a single function, [**glClear**](glclear.md).</span></span> <span data-ttu-id="592a6-121">Укажите, что именно нужно очистить, передав маски в **глклеар**.</span><span class="sxs-lookup"><span data-stu-id="592a6-121">Specify exactly what you want to clear by passing masks to **glClear**.</span></span>

<span data-ttu-id="592a6-122">При переносе команд Screen и buffer учитывайте следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="592a6-122">Keep the following points in mind when porting screen and buffer commands:</span></span>

-   <span data-ttu-id="592a6-123">OpenGL поддерживает очистку цветов отдельно от цветов рисования с помощью вызовов, таких как [**глклеарколор**](glclearcolor.md) и [**глклеариндекс**](glclearindex.md).</span><span class="sxs-lookup"><span data-stu-id="592a6-123">OpenGL maintains clearing colors separately from drawing colors, with calls like [**glClearColor**](glclearcolor.md) and [**glClearIndex**](glclearindex.md).</span></span> <span data-ttu-id="592a6-124">Не забудьте установить флажок очистить цвет для каждого буфера перед очисткой.</span><span class="sxs-lookup"><span data-stu-id="592a6-124">Be sure to set the clear color for each buffer before clearing.</span></span>
-   <span data-ttu-id="592a6-125">Вместо использования одного из нескольких методов очистки с разными именами теперь можно удалить несколько буферов с одним вызовом, [**Глклеар**](glclear.md) **или** объединить буферные маски.</span><span class="sxs-lookup"><span data-stu-id="592a6-125">Instead of using one of several differently named clear calls, you now clear several buffers with one call, [**glClear**](glclear.md), by **OR** ing together buffer masks.</span></span> <span data-ttu-id="592a6-126">Например, **кзклеар** заменяется на:</span><span class="sxs-lookup"><span data-stu-id="592a6-126">For example, **czclear** is replaced by:</span></span>

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   <span data-ttu-id="592a6-127">IRI GL ссылается на многоугольник стиппле и цвет вритемаск.</span><span class="sxs-lookup"><span data-stu-id="592a6-127">IRIS GL references the polygon stipple and the color writemask.</span></span> <span data-ttu-id="592a6-128">OpenGL игнорирует стиппле многоугольника, но ссылается на вритемаск Color.</span><span class="sxs-lookup"><span data-stu-id="592a6-128">OpenGL ignores the polygon stipple but references the color writemask.</span></span> <span data-ttu-id="592a6-129">(Функция **кзклеар** игнорирует как многоугольник стиппле, так и вритемаск Color.)</span><span class="sxs-lookup"><span data-stu-id="592a6-129">(The **czclear** function ignores both the polygon stipple and the color writemask.)</span></span>

<span data-ttu-id="592a6-130">В следующей таблице перечислены различные функции диафрагмы IRI GL с эквивалентными функциями OpenGL.</span><span class="sxs-lookup"><span data-stu-id="592a6-130">The following table lists the various IRIS GL clear functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="592a6-131">Вызов IRI GL</span><span class="sxs-lookup"><span data-stu-id="592a6-131">IRIS GL call</span></span>         | <span data-ttu-id="592a6-132">Вызов OpenGL</span><span class="sxs-lookup"><span data-stu-id="592a6-132">OpenGL call</span></span>                                                               | <span data-ttu-id="592a6-133">Значение</span><span class="sxs-lookup"><span data-stu-id="592a6-133">Meaning</span></span>                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="592a6-134">**акбуф**(AC \_ clear)</span><span class="sxs-lookup"><span data-stu-id="592a6-134">**acbuf**(AC\_CLEAR)</span></span> | <span data-ttu-id="592a6-135">**глклеар**( \_ бит накопленного \_ буфера GL \_ )</span><span class="sxs-lookup"><span data-stu-id="592a6-135">**glClear**( GL\_ACCUM\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="592a6-136">Очистка буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="592a6-136">Clear the accumulation buffer.</span></span>                    |
|                      | <span data-ttu-id="592a6-137">**глклеарколор**</span><span class="sxs-lookup"><span data-stu-id="592a6-137">**glClearColor**</span></span>                                                          | <span data-ttu-id="592a6-138">Задайте четкий цвет RGBA.</span><span class="sxs-lookup"><span data-stu-id="592a6-138">Set the RGBA clear color.</span></span>                         |
|                      | <span data-ttu-id="592a6-139">**глклеариндекс**</span><span class="sxs-lookup"><span data-stu-id="592a6-139">**glClearIndex**</span></span>                                                          | <span data-ttu-id="592a6-140">Задает индекс Clear-Color.</span><span class="sxs-lookup"><span data-stu-id="592a6-140">Set the clear-color index.</span></span>                        |
| <span data-ttu-id="592a6-141">**пусто**</span><span class="sxs-lookup"><span data-stu-id="592a6-141">**clear**</span></span>            | <span data-ttu-id="592a6-142">**глклеар**( \_ бит цвет \_ буфера GL \_ )</span><span class="sxs-lookup"><span data-stu-id="592a6-142">**glClear**( GL\_COLOR\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="592a6-143">Очистите буфер цвета.</span><span class="sxs-lookup"><span data-stu-id="592a6-143">Clear the color buffer.</span></span>                           |
|                      | <span data-ttu-id="592a6-144">**глклеардепс**</span><span class="sxs-lookup"><span data-stu-id="592a6-144">**glClearDepth**</span></span>                                                          | <span data-ttu-id="592a6-145">Укажите значение Clear для буфера глубины.</span><span class="sxs-lookup"><span data-stu-id="592a6-145">Specify the clear value for the depth buffer.</span></span>     |
| <span data-ttu-id="592a6-146">**зклеар**</span><span class="sxs-lookup"><span data-stu-id="592a6-146">**zclear**</span></span>           | <span data-ttu-id="592a6-147">**глклеар**( \_ \_ бит буфера глубины GL \_ )</span><span class="sxs-lookup"><span data-stu-id="592a6-147">**glClear**( GL\_DEPTH\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="592a6-148">Очистите буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="592a6-148">Clear the depth buffer.</span></span>                           |
| <span data-ttu-id="592a6-149">**кзклеар**</span><span class="sxs-lookup"><span data-stu-id="592a6-149">**czclear**</span></span>          | <span data-ttu-id="592a6-150">**глклеар**(бит цвет буфера главной книги GL — \_ \_ \_ \| \_ \_ бит буфера глубины GL \_ )</span><span class="sxs-lookup"><span data-stu-id="592a6-150">**glClear**( GL\_COLOR\_BUFFER\_BIT \|GL\_DEPTH\_BUFFER\_BIT )</span></span><br/> | <span data-ttu-id="592a6-151">Очистите буфер цвета и буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="592a6-151">Clear the color buffer and the depth buffer.</span></span>      |
|                      | <span data-ttu-id="592a6-152">**глклеараккум**</span><span class="sxs-lookup"><span data-stu-id="592a6-152">**glClearAccum**</span></span>                                                          | <span data-ttu-id="592a6-153">Укажите четкие значения для буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="592a6-153">Specify clear values for the accumulation buffer.</span></span> |
|                      | <span data-ttu-id="592a6-154">**глклеарстенЦил**</span><span class="sxs-lookup"><span data-stu-id="592a6-154">**glClearStencil**</span></span>                                                        | <span data-ttu-id="592a6-155">Укажите значение Clear для буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="592a6-155">Specify the clear value for the stencil buffer.</span></span>   |
| <span data-ttu-id="592a6-156">**склеар**</span><span class="sxs-lookup"><span data-stu-id="592a6-156">**sclear**</span></span>           | <span data-ttu-id="592a6-157">**глклеар**( \_ \_ бит буфера шаблона GL \_ )</span><span class="sxs-lookup"><span data-stu-id="592a6-157">**glClear**( GL\_STENCIL\_BUFFER\_BIT )</span></span>                                   | <span data-ttu-id="592a6-158">Очистите буфер шаблона.</span><span class="sxs-lookup"><span data-stu-id="592a6-158">Clear the stencil buffer.</span></span>                         |



 

<span data-ttu-id="592a6-159">Если в коде IRI используется как **гклеар** , так и **склеар**, их можно объединить в один вызов **глклеар** . может улучшить производительность программы.</span><span class="sxs-lookup"><span data-stu-id="592a6-159">When your IRIS GL code uses both **gclear** and **sclear**, you can combine them into a single **glClear** call; can improve your program's performance.</span></span>

 

 





