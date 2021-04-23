---
title: Перенос многоугольников и Куадрилатералс
description: При переносе многоугольников и куадрилатералс учитывайте следующие моменты.
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Перенос GL в ГК, куадрилатералс
- Перенос из IRI GL, куадрилатералс
- перенос в OpenGL из IRI GL, куадрилатералс
- Перенос по стандарту OpenGL из IRI GL, куадрилатералс
- функции рисования, куадрилатералс
- куадрилатералс
- Перенос GL в ГК, многоугольники
- Перенос из ДИАФРАГМы в ГК, многоугольники
- перенос в OpenGL из IRI GL, многоугольников
- Перенос по стандарту OpenGL из IRI GL, многоугольников
- функции рисования, многоугольники
- многоугольники, перенос из IRI GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7900b44051cab9590be11198c8b01af0b7c10244
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908462"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="a4299-115">Перенос многоугольников и Куадрилатералс</span><span class="sxs-lookup"><span data-stu-id="a4299-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="a4299-116">При переносе многоугольников и куадрилатералс учитывайте следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="a4299-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="a4299-117">Прямой эквивалент для **вогнутых участков**(**true**) отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a4299-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="a4299-118">Вместо этого можно использовать подпрограммы тесселяции в GLU, описанные в разделе [тесселяция многоугольников](tessellating-polygons.md).</span><span class="sxs-lookup"><span data-stu-id="a4299-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="a4299-119">Режимы многоугольников задаются по-разному.</span><span class="sxs-lookup"><span data-stu-id="a4299-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="a4299-120">Эти функции рисования многоугольников не имеют прямых эквивалентов в OpenGL: семейства подпрограмм **поли** ; Семейство подпрограмм **полф** ; **ПМВ**, **Народно** и **пклос**; **рпмв** и **рпдр**; **сплф**; и **спклос**.</span><span class="sxs-lookup"><span data-stu-id="a4299-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="a4299-121">Если в коде в IRI используется эти функции, необходимо переписать код с помощью [**глбегин**](glbegin.md)( \_ многоугольник GL).</span><span class="sxs-lookup"><span data-stu-id="a4299-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="a4299-122">В следующей таблице перечислены функции рисования многоугольников IRI GL и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a4299-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="a4299-123">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="a4299-123">IRIS GL function</span></span>         | <span data-ttu-id="a4299-124">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="a4299-124">OpenGL function</span></span>                                                    | <span data-ttu-id="a4299-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a4299-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a4299-126">**бгнполигонендполигон**</span><span class="sxs-lookup"><span data-stu-id="a4299-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="a4299-127">[**глбегин**](glbegin.md) ( \_ многоугольник GL)[**гленд**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="a4299-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="a4299-128">Вершины определяют границу простого многоугольника выпуклой.</span><span class="sxs-lookup"><span data-stu-id="a4299-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="a4299-129">**глбегин**( \_ четыре **неглендных** )</span><span class="sxs-lookup"><span data-stu-id="a4299-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="a4299-130">Интерпретирует четверные вершины как куадрилатералс.</span><span class="sxs-lookup"><span data-stu-id="a4299-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="a4299-131">**бгнкстрипендкстрип**</span><span class="sxs-lookup"><span data-stu-id="a4299-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="a4299-132">[**глбегин**](glbegin.md) ( \_ четыре четырехъядерных \_ ленты)**гленд**</span><span class="sxs-lookup"><span data-stu-id="a4299-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="a4299-133">Интерпретирует вершины как связанные полосы куадрилатералс.</span><span class="sxs-lookup"><span data-stu-id="a4299-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="a4299-134">гледжефлаг</span><span class="sxs-lookup"><span data-stu-id="a4299-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="a4299-135">**в режиме с некотором**</span><span class="sxs-lookup"><span data-stu-id="a4299-135">**polymode**</span></span>             | [<span data-ttu-id="a4299-136">**глполигонмоде**</span><span class="sxs-lookup"><span data-stu-id="a4299-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="a4299-137">Задает режим рисования многоугольника.</span><span class="sxs-lookup"><span data-stu-id="a4299-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="a4299-138">**ректректф**</span><span class="sxs-lookup"><span data-stu-id="a4299-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="a4299-139">глрект</span><span class="sxs-lookup"><span data-stu-id="a4299-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="a4299-140">Рисует прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="a4299-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="a4299-141">**сбокссбоксф**</span><span class="sxs-lookup"><span data-stu-id="a4299-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="a4299-142">Рисует прямоугольник с выставкой по экрану.</span><span class="sxs-lookup"><span data-stu-id="a4299-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="a4299-143">??</span><span class="sxs-lookup"><span data-stu-id="a4299-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="a4299-144">Перенос режимов многоугольников</span><span class="sxs-lookup"><span data-stu-id="a4299-144">Porting Polygon Modes</span></span>

<span data-ttu-id="a4299-145">Функция OpenGL [**глполигонмоде**](glpolygonmode.md) позволяет указать, к какой стороне многоугольника применяется режим (задний или передний).</span><span class="sxs-lookup"><span data-stu-id="a4299-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="a4299-146">Синтаксис:</span><span class="sxs-lookup"><span data-stu-id="a4299-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="a4299-147">где Face является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="a4299-147">where face is one of:</span></span>



|<span data-ttu-id="a4299-148">Значение Гленум</span><span class="sxs-lookup"><span data-stu-id="a4299-148">GLenum value</span></span>                      |  <span data-ttu-id="a4299-149">Значение</span><span class="sxs-lookup"><span data-stu-id="a4299-149">Meaning</span></span>                                                          |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="a4299-150">GL \_ спереди</span><span class="sxs-lookup"><span data-stu-id="a4299-150">GL\_FRONT</span></span>            | <span data-ttu-id="a4299-151">режим, применяемый к внешним многоугольникам</span><span class="sxs-lookup"><span data-stu-id="a4299-151">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="a4299-152">на \_ задний план</span><span class="sxs-lookup"><span data-stu-id="a4299-152">GL\_BACK</span></span>             | <span data-ttu-id="a4299-153">режим, который применяется к фоновым многоугольникам</span><span class="sxs-lookup"><span data-stu-id="a4299-153">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="a4299-154">\_Передняя \_ и \_ задняя части GL</span><span class="sxs-lookup"><span data-stu-id="a4299-154">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="a4299-155">режим, применяемый как к внешнему, так и к фоновому многоугольнику</span><span class="sxs-lookup"><span data-stu-id="a4299-155">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="a4299-156">\_Внешний \_ и \_ задний режимы GL эквивалентны функции в НЕКОТОРОМ **режиме** IRI GL.</span><span class="sxs-lookup"><span data-stu-id="a4299-156">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="a4299-157">В следующей таблице перечислены режимы многоугольников ДИАФРАГМы и их эквивалентные режимы OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a4299-157">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="a4299-158">Режим "IRI GL"</span><span class="sxs-lookup"><span data-stu-id="a4299-158">IRIS GL mode</span></span> | <span data-ttu-id="a4299-159">Режим OpenGL</span><span class="sxs-lookup"><span data-stu-id="a4299-159">OpenGL mode</span></span> | <span data-ttu-id="a4299-160">Значение</span><span class="sxs-lookup"><span data-stu-id="a4299-160">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="a4299-161">\_точка ПИМ</span><span class="sxs-lookup"><span data-stu-id="a4299-161">PYM\_POINT</span></span>   | <span data-ttu-id="a4299-162">\_точка GL</span><span class="sxs-lookup"><span data-stu-id="a4299-162">GL\_POINT</span></span>   | <span data-ttu-id="a4299-163">Рисует вершины в виде точек.</span><span class="sxs-lookup"><span data-stu-id="a4299-163">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="a4299-164">ПИМ \_ строка</span><span class="sxs-lookup"><span data-stu-id="a4299-164">PYM\_LINE</span></span>    | <span data-ttu-id="a4299-165">\_строка GL</span><span class="sxs-lookup"><span data-stu-id="a4299-165">GL\_LINE</span></span>    | <span data-ttu-id="a4299-166">Рисует границы границ в виде сегментов линии.</span><span class="sxs-lookup"><span data-stu-id="a4299-166">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="a4299-167">ПИМ \_ Заливка</span><span class="sxs-lookup"><span data-stu-id="a4299-167">PYM\_FILL</span></span>    | <span data-ttu-id="a4299-168">\_Заливка GL</span><span class="sxs-lookup"><span data-stu-id="a4299-168">GL\_FILL</span></span>    | <span data-ttu-id="a4299-169">Рисуется внутренняя заливка многоугольника.</span><span class="sxs-lookup"><span data-stu-id="a4299-169">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="a4299-170">ПИМ, \_ Заливка</span><span class="sxs-lookup"><span data-stu-id="a4299-170">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="a4299-171">Заполняет только внутренние Пиксели в границах.</span><span class="sxs-lookup"><span data-stu-id="a4299-171">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="a4299-172">Перенос многоугольников Стипплес</span><span class="sxs-lookup"><span data-stu-id="a4299-172">Porting Polygon Stipples</span></span>

<span data-ttu-id="a4299-173">При переносе стипплесного многоугольника IRI GL учитывайте следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="a4299-173">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="a4299-174">OpenGL не использует таблицы для многоугольников стипплес; сохраняется только один шаблон стиппле.</span><span class="sxs-lookup"><span data-stu-id="a4299-174">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="a4299-175">Списки просмотра можно использовать для хранения различных шаблонов стиппле.</span><span class="sxs-lookup"><span data-stu-id="a4299-175">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="a4299-176">Размер растрового изображения OpenGL Polygon стиппле всегда равен 32-разрядному шаблону размером 32x32.</span><span class="sxs-lookup"><span data-stu-id="a4299-176">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="a4299-177">На кодировку стиппле влияет [**глпикселсторе**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a4299-177">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="a4299-178">Дополнительные сведения о переносе многоугольников стипплес см. в разделе [перенос операций пикселей](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="a4299-178">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="a4299-179">В следующей таблице перечислены стиппле функции и их эквивалентные функции OpenGL в компании IRI GL.</span><span class="sxs-lookup"><span data-stu-id="a4299-179">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="a4299-180">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="a4299-180">IRIS GL function</span></span> | <span data-ttu-id="a4299-181">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="a4299-181">OpenGL function</span></span>                                    | <span data-ttu-id="a4299-182">Значение</span><span class="sxs-lookup"><span data-stu-id="a4299-182">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="a4299-183">**дефпаттерн**</span><span class="sxs-lookup"><span data-stu-id="a4299-183">**defpattern**</span></span>   | [<span data-ttu-id="a4299-184">**глполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="a4299-184">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="a4299-185">Задает шаблон стиппле.</span><span class="sxs-lookup"><span data-stu-id="a4299-185">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="a4299-186">**сетпаттерн**</span><span class="sxs-lookup"><span data-stu-id="a4299-186">**setpattern**</span></span>   |                                                    | <span data-ttu-id="a4299-187">OpenGL сохраняет только один шаблон стиппле многоугольника.</span><span class="sxs-lookup"><span data-stu-id="a4299-187">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="a4299-188">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="a4299-188">**getpattern**</span></span>   | [<span data-ttu-id="a4299-189">**глжетполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="a4299-189">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="a4299-190">Возвращает битовую карту стиппле (используемую для возврата индекса).</span><span class="sxs-lookup"><span data-stu-id="a4299-190">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="a4299-191">В OpenGL вы включаете и отключаете стипплинг Polygon, передавая \_ \_ стиппленый многоугольник в качестве параметра для [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="a4299-191">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="a4299-192">Следующий пример кода OpenGL демонстрирует стипплинг Polygon:</span><span class="sxs-lookup"><span data-stu-id="a4299-192">The following OpenGL code sample demonstrates polygon stippling:</span></span>


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="a4299-193">Перенос Тесселяцических многоугольников</span><span class="sxs-lookup"><span data-stu-id="a4299-193">Porting Tessellated Polygons</span></span>

<span data-ttu-id="a4299-194">В IRI GL используется **вогнутых участков**(**true**), а затем **бгнполигон** для рисования вогнутых участков многоугольников.</span><span class="sxs-lookup"><span data-stu-id="a4299-194">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="a4299-195">GLU OpenGL включает функции, которые можно использовать для рисования многоугольников вогнутых участков.</span><span class="sxs-lookup"><span data-stu-id="a4299-195">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="a4299-196">**Рисование многоугольника вогнутых участков с помощью OpenGL**</span><span class="sxs-lookup"><span data-stu-id="a4299-196">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="a4299-197">Создайте объект тесселяции.</span><span class="sxs-lookup"><span data-stu-id="a4299-197">Create a tessellation object.</span></span>
2.  <span data-ttu-id="a4299-198">Определите обратные вызовы, которые будут использоваться для обработки треугольников, созданных тесселяцией.</span><span class="sxs-lookup"><span data-stu-id="a4299-198">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="a4299-199">Укажите многоугольник вогнутых участков для тесселяции.</span><span class="sxs-lookup"><span data-stu-id="a4299-199">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="a4299-200">В следующей таблице перечислены функции OpenGL для рисования тесселяцических многоугольников.</span><span class="sxs-lookup"><span data-stu-id="a4299-200">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="a4299-201">Функция OpenGL GLU</span><span class="sxs-lookup"><span data-stu-id="a4299-201">OpenGL GLU function</span></span>                        | <span data-ttu-id="a4299-202">Значение</span><span class="sxs-lookup"><span data-stu-id="a4299-202">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="a4299-203">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="a4299-203">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="a4299-204">Создает новый объект тесселяции.</span><span class="sxs-lookup"><span data-stu-id="a4299-204">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="a4299-205">**глуделететесс**</span><span class="sxs-lookup"><span data-stu-id="a4299-205">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="a4299-206">Удаляет объект тесселяции.</span><span class="sxs-lookup"><span data-stu-id="a4299-206">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="a4299-207">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="a4299-207">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="a4299-208">**глубегинполигон**</span><span class="sxs-lookup"><span data-stu-id="a4299-208">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="a4299-209">Начинает спецификацию многоугольника.</span><span class="sxs-lookup"><span data-stu-id="a4299-209">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="a4299-210">**глутессвертекс**</span><span class="sxs-lookup"><span data-stu-id="a4299-210">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="a4299-211">Задает вершину многоугольника в контуре.</span><span class="sxs-lookup"><span data-stu-id="a4299-211">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="a4299-212">**глунекстконтаур**</span><span class="sxs-lookup"><span data-stu-id="a4299-212">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="a4299-213">Указывает, что следующий ряд вершин описывает новый профиль.</span><span class="sxs-lookup"><span data-stu-id="a4299-213">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="a4299-214">**глуендполигон**</span><span class="sxs-lookup"><span data-stu-id="a4299-214">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="a4299-215">Завершает спецификацию многоугольника.</span><span class="sxs-lookup"><span data-stu-id="a4299-215">Ends the polygon specification.</span></span>                                    |



 

 

 





