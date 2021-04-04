---
title: Базовая операция OpenGL
description: Базовая операция OpenGL
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, основные операции
- OpenGL, обработка данных
- OpenGL, этапы обработки
- OpenGL, списки вывода
- Отображение списков OpenGL
- OpenGL, оценщики
- Оценщики OpenGL
- Использование OpenGL, операций на вершину
- операции на вершину OpenGL
- OpenGL, примитивная сборка
- Примитивная сборка OpenGL
- OpenGL, растрирование
- Растрирование (OpenGL)
- Операции OpenGL, для отдельных фрагментов
- операции с каждым фрагментом OpenGL
- фрамебуфферс, основные операции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "103999832"
---
# <a name="basic-opengl-operation"></a><span data-ttu-id="ffc24-119">Базовая операция OpenGL</span><span class="sxs-lookup"><span data-stu-id="ffc24-119">Basic OpenGL Operation</span></span>

<span data-ttu-id="ffc24-120">На следующей схеме показано, как OpenGL обрабатывает данные.</span><span class="sxs-lookup"><span data-stu-id="ffc24-120">The following diagram illustrates how OpenGL processes data.</span></span> <span data-ttu-id="ffc24-121">Как показано выше, команды вводят их слева и проходят по конвейеру обработки.</span><span class="sxs-lookup"><span data-stu-id="ffc24-121">As shown, commands enter from the left and proceed through a processing pipeline.</span></span> <span data-ttu-id="ffc24-122">Некоторые команды задают геометрические объекты для рисования, а другие управляют обработкой объектов на различных стадиях обработки.</span><span class="sxs-lookup"><span data-stu-id="ffc24-122">Some commands specify geometric objects to be drawn, and others control how the objects are handled during various processing stages.</span></span>

![Диаграмма, на которой показаны этапы конвейера обработки данных OpenGL.](images/basic01.png)

<span data-ttu-id="ffc24-124">Ниже приведены этапы обработки в базовой операции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ffc24-124">The processing stages in basic OpenGL operation are as follows:</span></span>

-   <span data-ttu-id="ffc24-125">**Список отображаемых** Вместо того, чтобы выполнять все команды немедленно через конвейер, можно накапливать некоторые из них в списке вывода для дальнейшей обработки.</span><span class="sxs-lookup"><span data-stu-id="ffc24-125">**Display list** Rather than having all commands proceed immediately through the pipeline, you can choose to accumulate some of them in a display list for processing later.</span></span>
-   <span data-ttu-id="ffc24-126">**Оценщик** Этап оценки обеспечивает эффективный способ приблизительного приближения кривой и геометрической поверхности, оценивая однонаправленные команды входных значений.</span><span class="sxs-lookup"><span data-stu-id="ffc24-126">**Evaluator** The evaluator stage of processing provides an efficient way to approximate curve and surface geometry by evaluating polynomial commands of input values.</span></span>
-   <span data-ttu-id="ffc24-127">**Операции на вершину и примитивную сборку** OpenGL обрабатывает геометрические примитивеспоинтс, сегменты линий и полигонсалл, которые описаны вершинами.</span><span class="sxs-lookup"><span data-stu-id="ffc24-127">**Per-vertex operations and primitive assembly** OpenGL processes geometric primitivespoints, line segments, and polygonsall of which are described by vertices.</span></span> <span data-ttu-id="ffc24-128">Вершины преобразуются и освещены, а примитивы обрезаются в окне просмотра при подготовке к растеризации.</span><span class="sxs-lookup"><span data-stu-id="ffc24-128">Vertices are transformed and lit, and primitives are clipped to the viewport in preparation for rasterization.</span></span>
-   <span data-ttu-id="ffc24-129">**Растрирование** Этап растрирования создает ряд адресов буферов кадров и связанных значений с помощью двумерного описания точки, сегмента линии или многоугольника.</span><span class="sxs-lookup"><span data-stu-id="ffc24-129">**Rasterization** The rasterization stage produces a series of frame-buffer addresses and associated values using a two-dimensional description of a point, line segment, or polygon.</span></span> <span data-ttu-id="ffc24-130">Каждый фрагмент, созданный таким образом, передается на последний этап, операции по каждому фрагменту.</span><span class="sxs-lookup"><span data-stu-id="ffc24-130">Each fragment so produced is fed into the last stage, per-fragment operations.</span></span>
-   <span data-ttu-id="ffc24-131">**Операции на фрагменты** Это окончательные операции с данными до их сохранения в виде пикселей в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="ffc24-131">**Per-fragment operations** These are the final operations performed on the data before it is stored as pixels in the framebuffer.</span></span>

    <span data-ttu-id="ffc24-132">Операции для каждого фрагмента включают в себя условные обновления для буфера кадров на основе входящих и ранее сохраненных значений z (для z-буферизации) и объединения входящих цветов пикселя с сохраненными цветами, а также маскировки и других логических операций с значениями пикселей.</span><span class="sxs-lookup"><span data-stu-id="ffc24-132">Per-fragment operations include conditional updates to the framebuffer based on incoming and previously stored z values (for z buffering) and blending of incoming pixel colors with stored colors, as well as masking and other logical operations on pixel values.</span></span>

<span data-ttu-id="ffc24-133">Данные могут быть введены в виде пикселей, а не вершин.</span><span class="sxs-lookup"><span data-stu-id="ffc24-133">Data can be input in the form of pixels rather than vertices.</span></span> <span data-ttu-id="ffc24-134">Данные в виде пикселов, например, могут описывать изображение для использования в сопоставлении текстур, пропускают первый этап обработки, описанный выше, а обрабатываются как Пиксели на этапе операций пикселей.</span><span class="sxs-lookup"><span data-stu-id="ffc24-134">Data in the form of pixels, such as might describe an image for use in texture mapping, skips the first stage of processing described above and instead is processed as pixels, in the pixel operations stage.</span></span> <span data-ttu-id="ffc24-135">Следующие операции с пикселями представляют собой одно из следующих данных:</span><span class="sxs-lookup"><span data-stu-id="ffc24-135">Following pixel operations, the pixel data is either:</span></span>

-   <span data-ttu-id="ffc24-136">Хранится как Текстурная память для использования на этапе растрирования.</span><span class="sxs-lookup"><span data-stu-id="ffc24-136">Stored as texture memory, for use in the rasterization stage.</span></span>
-   <span data-ttu-id="ffc24-137">Растрирование, с полученными фрагментами, объединенными в буфера кадров, так же, как если бы они были созданы из геометрических данных.</span><span class="sxs-lookup"><span data-stu-id="ffc24-137">Rasterized, with the resulting fragments merged into the framebuffer just as if they were generated from geometric data.</span></span>

 

 




