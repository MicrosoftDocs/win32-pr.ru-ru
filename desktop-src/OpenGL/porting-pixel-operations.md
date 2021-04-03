---
title: Перенос операций с пикселами
description: Перенос операций с пикселами
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Перенос GL в ГК, Пиксели
- Перенос из IRI GL, ПКС
- перенос в OpenGL из IRI GL, пикселей
- Перенос по стандарту OpenGL из IRI GL, пикселей
- Пиксели, перенос из IRI GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778044"
---
# <a name="porting-pixel-operations"></a><span data-ttu-id="b3442-108">Перенос операций с пикселами</span><span class="sxs-lookup"><span data-stu-id="b3442-108">Porting Pixel Operations</span></span>

<span data-ttu-id="b3442-109">При переносе кода, включающего операции с пикселями, учитывайте следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="b3442-109">When porting code that involves pixel operations, keep the following points in mind:</span></span>

-   <span data-ttu-id="b3442-110">Операции логического пикселя не применяются к буферам цветов RGBA.</span><span class="sxs-lookup"><span data-stu-id="b3442-110">Logical pixel operations are not applied to RGBA color buffers.</span></span> <span data-ttu-id="b3442-111">Дополнительные сведения см. в разделе [**гллогикоп**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="b3442-111">For more information, see [**glLogicOp**](gllogicop.md).</span></span>
-   <span data-ttu-id="b3442-112">В целом, функция IRI GL использует формат АБГР для пикселей, тогда как OpenGL использует RGBA.</span><span class="sxs-lookup"><span data-stu-id="b3442-112">In general, IRIS GL uses the format ABGR for pixels, whereas OpenGL uses RGBA.</span></span> <span data-ttu-id="b3442-113">Формат можно изменить на [**глпикселсторе**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b3442-113">You can change the format with [**glPixelStore**](glpixelstore-functions.md).</span></span>
-   <span data-ttu-id="b3442-114">При переносе функций **лректврите** следует обратить внимание на место записи **лректврите** (например, можно записать в буфер глубины).</span><span class="sxs-lookup"><span data-stu-id="b3442-114">When porting **lrectwrite** functions, be careful to note where **lrectwrite** is writing (for example, it could be writing to the depth buffer).</span></span>

<span data-ttu-id="b3442-115">OpenGL предоставляет дополнительную гибкость в операциях с пикселами.</span><span class="sxs-lookup"><span data-stu-id="b3442-115">OpenGL gives you some additional flexibility in pixel operations.</span></span> <span data-ttu-id="b3442-116">В следующей таблице перечислены функции IRI GL для операций с пикселями и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="b3442-116">The following table lists IRIS GL functions for pixel operations and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="b3442-117">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="b3442-117">IRIS GL function</span></span>                                   | <span data-ttu-id="b3442-118">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="b3442-118">OpenGL function</span></span>                                                                           | <span data-ttu-id="b3442-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b3442-119">Meaning</span></span>                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b3442-120">**лректреад**, **ректреад**,**реадргб**</span><span class="sxs-lookup"><span data-stu-id="b3442-120">**lrectread**, **rectread**,**readRGB**</span></span><br/> | [<span data-ttu-id="b3442-121">**глреадпикселс**</span><span class="sxs-lookup"><span data-stu-id="b3442-121">**glReadPixels**</span></span>](glreadpixels.md)                                                      | <span data-ttu-id="b3442-122">Считывает блок пикселей из буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="b3442-122">Reads a block of pixels from the framebuffer.</span></span>                           |
| <span data-ttu-id="b3442-123">**лректврите**, **ректврите**</span><span class="sxs-lookup"><span data-stu-id="b3442-123">**lrectwrite**, **rectwrite**</span></span>                      | [<span data-ttu-id="b3442-124">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="b3442-124">**glDrawPixels**</span></span>](gldrawpixels.md)                                                      | <span data-ttu-id="b3442-125">Записывает блок пикселей в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="b3442-125">Writes a block of pixels to the framebuffer.</span></span>                            |
| <span data-ttu-id="b3442-126">**ректкопи**</span><span class="sxs-lookup"><span data-stu-id="b3442-126">**rectcopy**</span></span>                                       | [<span data-ttu-id="b3442-127">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="b3442-127">**glCopyPixels**</span></span>](glcopypixels.md)                                                      | <span data-ttu-id="b3442-128">Копирует Пиксели в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="b3442-128">Copies pixels in the framebuffer.</span></span>                                       |
| <span data-ttu-id="b3442-129">**ректзум**</span><span class="sxs-lookup"><span data-stu-id="b3442-129">**rectzoom**</span></span>                                       | [<span data-ttu-id="b3442-130">**глпикселзум**</span><span class="sxs-lookup"><span data-stu-id="b3442-130">**glPixelZoom**</span></span>](glpixelzoom.md)                                                        | <span data-ttu-id="b3442-131">Задает коэффициенты масштабирования пикселей для **глдравпикселс** и **глкопипикселс**.</span><span class="sxs-lookup"><span data-stu-id="b3442-131">Specifies pixel zoom factors for **glDrawPixels** and **glCopyPixels**.</span></span> |
| <span data-ttu-id="b3442-132">**кмов**</span><span class="sxs-lookup"><span data-stu-id="b3442-132">**cmov**</span></span>                                           | [<span data-ttu-id="b3442-133">глрастерпос</span><span class="sxs-lookup"><span data-stu-id="b3442-133">glRasterPos</span></span>](glrasterpos-functions.md)                                                  | <span data-ttu-id="b3442-134">Задает растровое расположение для операций с пикселями.</span><span class="sxs-lookup"><span data-stu-id="b3442-134">Specifies raster position for pixel operations.</span></span>                         |
| <span data-ttu-id="b3442-135">**реадсаурце**</span><span class="sxs-lookup"><span data-stu-id="b3442-135">**readsource**</span></span>                                     | [<span data-ttu-id="b3442-136">**глреадбуффер**</span><span class="sxs-lookup"><span data-stu-id="b3442-136">**glReadBuffer**</span></span>](glreadbuffer.md)                                                      | <span data-ttu-id="b3442-137">Выбирает источник цветового буфера для пикселей.</span><span class="sxs-lookup"><span data-stu-id="b3442-137">Selects a color buffer source for pixels.</span></span>                               |
| <span data-ttu-id="b3442-138">**пиксмоде**</span><span class="sxs-lookup"><span data-stu-id="b3442-138">**pixmode**</span></span>                                        | <span data-ttu-id="b3442-139">[**глпикселсторе**](glpixelstore-functions.md),[**глпикселтрансфер**](glpixeltransfer.md)</span><span class="sxs-lookup"><span data-stu-id="b3442-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span></span> | <span data-ttu-id="b3442-140">Задает режимы хранения в пикселях. Задайте режимы обмена пикселами.</span><span class="sxs-lookup"><span data-stu-id="b3442-140">Sets pixel storage modes.Set pixel transfer modes.</span></span>                      |
| <span data-ttu-id="b3442-141">**логикоп**</span><span class="sxs-lookup"><span data-stu-id="b3442-141">**logicop**</span></span>                                        | [<span data-ttu-id="b3442-142">**гллогикоп**</span><span class="sxs-lookup"><span data-stu-id="b3442-142">**glLogicOp**</span></span>](gllogicop.md)                                                            | <span data-ttu-id="b3442-143">Задает логическую операцию для операций записи в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b3442-143">Specifies a logical operation for pixel writes.</span></span>                         |
|                                                    | <span data-ttu-id="b3442-144">[**гленабле**](glenable.md) ( \_ логическая \_ Операция ГК)</span><span class="sxs-lookup"><span data-stu-id="b3442-144">[**glEnable**](glenable.md) ( GL\_LOGIC\_OP )</span></span>                                            | <span data-ttu-id="b3442-145">Включает логические операции с пиксельными пикселями.</span><span class="sxs-lookup"><span data-stu-id="b3442-145">Turns on pixel logic operations.</span></span>                                        |



 

<span data-ttu-id="b3442-146">Полный список возможных логических операций см. в разделе [**гллогикоп**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="b3442-146">For a complete list of possible logical operations, see [**glLogicOp**](gllogicop.md).</span></span>

<span data-ttu-id="b3442-147">В этом образце кода IRI GL показана типичная запись в пикселях:</span><span class="sxs-lookup"><span data-stu-id="b3442-147">This IRIS GL code sample shows a typical pixel write:</span></span>

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

<span data-ttu-id="b3442-148">Приведенный выше код выглядит следующим образом при переводе в OpenGL:</span><span class="sxs-lookup"><span data-stu-id="b3442-148">The preceding code looks like this when translated to OpenGL:</span></span>

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





