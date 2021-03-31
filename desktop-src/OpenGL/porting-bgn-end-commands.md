---
title: Перенос команд бгн/End
description: IRI GL использует парадигму Begin/End, но имеет различные функции для каждого графического примитива.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Перенос GL в ГК, команды бгн/End
- Перенос из команд IRI GL, бгн/End
- перенос в OpenGL из команд IRI GL, бгн/End
- Перенос по стандарту OpenGL из команд IRI GL, бгн/End
- функции рисования, команды бгн/End
- команды бгн/End
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411272"
---
# <a name="porting-bgnend-commands"></a><span data-ttu-id="b0a0f-109">Перенос команд бгн/End</span><span class="sxs-lookup"><span data-stu-id="b0a0f-109">Porting bgn/end Commands</span></span>

<span data-ttu-id="b0a0f-110">IRI GL использует парадигму Begin/End, но имеет различные функции для каждого графического примитива.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-110">IRIS GL uses the begin/end paradigm but has a different function for each graphics primitive.</span></span> <span data-ttu-id="b0a0f-111">Например, вы, вероятно, используете **бгнполигон** и **ендполигон** для рисования многоугольников, а также **бгнлине** и **endLine** для рисования линий.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-111">For example, you probably use **bgnpolygon** and **endpolygon** to draw polygons, and **bgnline** and **endline** to draw lines.</span></span> <span data-ttu-id="b0a0f-112">В OpenGL [](glbegin.md)  /  для обоих типов используется структура [**гленд**](glend.md) глбегин.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-112">In OpenGL, you use the [**glBegin**](glbegin.md) / [**glEnd**](glend.md) structure for both.</span></span> <span data-ttu-id="b0a0f-113">В OpenGL Рисование наиболее геометрических объектов осуществляется путем включения ряда функций, определяющих вершины, нормали, текстуры и цвета между парами вызовов **глбегин** и **гленд** .</span><span class="sxs-lookup"><span data-stu-id="b0a0f-113">In OpenGL you draw most geometric objects by enclosing a series of functions that specify vertices, normals, textures, and colors between pairs of **glBegin** and **glEnd** calls.</span></span> <span data-ttu-id="b0a0f-114">Пример:</span><span class="sxs-lookup"><span data-stu-id="b0a0f-114">For example:</span></span>

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

<span data-ttu-id="b0a0f-115">Функция **глбегин** принимает один параметр, который задает режим рисования, и, таким же, примитив.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-115">The **glBegin** function takes a single parameter that specifies the drawing mode, and thus the primitive.</span></span> <span data-ttu-id="b0a0f-116">Вот пример кода OpenGL, который рисует многоугольник, а затем строку:</span><span class="sxs-lookup"><span data-stu-id="b0a0f-116">Here's an OpenGL code sample that draws a polygon and then a line:</span></span>

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

<span data-ttu-id="b0a0f-117">С помощью OpenGL вы рисуете различные геометрические объекты, указывая различные параметры для [**глбегин**](glbegin.md).</span><span class="sxs-lookup"><span data-stu-id="b0a0f-117">With OpenGL, you draw different geometric objects by specifying different parameters for [**glBegin**](glbegin.md).</span></span> <span data-ttu-id="b0a0f-118">В следующей таблице перечислены параметры **Глбегин** OpenGL, соответствующие эквивалентным ФУНКЦИЯМ IRI GL.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-118">The following table lists the OpenGL **glBegin** parameters that correspond to equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="b0a0f-119">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="b0a0f-119">IRIS GL function</span></span>  | <span data-ttu-id="b0a0f-120">Значение режима Глбегин</span><span class="sxs-lookup"><span data-stu-id="b0a0f-120">Value of glBegin mode</span></span> | <span data-ttu-id="b0a0f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b0a0f-121">Meaning</span></span>                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a0f-122">**бгнпоинт**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-122">**bgnpoint**</span></span>      | <span data-ttu-id="b0a0f-123">\_точки GL</span><span class="sxs-lookup"><span data-stu-id="b0a0f-123">GL\_POINTS</span></span>            | <span data-ttu-id="b0a0f-124">Отдельные точки.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-124">Individual points.</span></span>                                                                       |
| <span data-ttu-id="b0a0f-125">**бгнлине**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-125">**bgnline**</span></span>       | <span data-ttu-id="b0a0f-126">\_ \_ полоса строк GL</span><span class="sxs-lookup"><span data-stu-id="b0a0f-126">GL\_LINE\_STRIP</span></span>       | <span data-ttu-id="b0a0f-127">Ряд сегментов Соединенных линий.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-127">Series of connected line segments.</span></span>                                                       |
| <span data-ttu-id="b0a0f-128">**бгнклоседлине**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-128">**bgnclosedline**</span></span> | <span data-ttu-id="b0a0f-129">\_линейный \_ цикл GL</span><span class="sxs-lookup"><span data-stu-id="b0a0f-129">GL\_LINE\_LOOP</span></span>        | <span data-ttu-id="b0a0f-130">Ряд Соединенных линейных сегментов с сегментом, добавленным между первой и последней вершинами.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-130">Series of connected line segments, with a segment added between first and last vertices.</span></span> |
|                   | <span data-ttu-id="b0a0f-131">\_строки GL</span><span class="sxs-lookup"><span data-stu-id="b0a0f-131">GL\_LINES</span></span>             | <span data-ttu-id="b0a0f-132">Пары вершин, интерпретируемые как отдельные сегменты линий.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-132">Pairs of vertices interpreted as individual line segments.</span></span>                               |
| <span data-ttu-id="b0a0f-133">**бгнполигон**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-133">**bgnpolygon**</span></span>    | <span data-ttu-id="b0a0f-134">\_МНОГОУГОЛЬНИК GL</span><span class="sxs-lookup"><span data-stu-id="b0a0f-134">GL\_POLYGON</span></span>           | <span data-ttu-id="b0a0f-135">Граница простого выпуклой многоугольника.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-135">Boundary of a simple convex polygon.</span></span>                                                     |
|                   | <span data-ttu-id="b0a0f-136">\_треугольники GL</span><span class="sxs-lookup"><span data-stu-id="b0a0f-136">GL\_TRIANGLES</span></span>         | <span data-ttu-id="b0a0f-137">Тройки вершин, интерпретируемые как треугольники.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-137">Triples of vertices interpreted as triangles.</span></span>                                            |
| <span data-ttu-id="b0a0f-138">**бгнтмеш**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-138">**bgntmesh**</span></span>      | <span data-ttu-id="b0a0f-139">\_полоса треугольников GL \_</span><span class="sxs-lookup"><span data-stu-id="b0a0f-139">GL\_TRIANGLE\_STRIP</span></span>   | <span data-ttu-id="b0a0f-140">Связанные полосы треугольников.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-140">Linked strips of triangles.</span></span>                                                              |
|                   | <span data-ttu-id="b0a0f-141">\_вентилятор с треугольником GL \_</span><span class="sxs-lookup"><span data-stu-id="b0a0f-141">GL\_TRIANGLE\_FAN</span></span>     | <span data-ttu-id="b0a0f-142">Связанные вентиляторы треугольников.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-142">Linked fans of triangles.</span></span>                                                                |
|                   | <span data-ttu-id="b0a0f-143">четыре Нефин. \_</span><span class="sxs-lookup"><span data-stu-id="b0a0f-143">GL\_QUADS</span></span>             | <span data-ttu-id="b0a0f-144">Четверные вершины, интерпретируемые как куадрилатералс.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-144">Quadruples of vertices interpreted as quadrilaterals.</span></span>                                    |
| <span data-ttu-id="b0a0f-145">**бгнкстрип**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-145">**bgnqstrip**</span></span>     | <span data-ttu-id="b0a0f-146">\_четыре \_ ленты GL</span><span class="sxs-lookup"><span data-stu-id="b0a0f-146">GL\_QUAD\_STRIP</span></span>       | <span data-ttu-id="b0a0f-147">Связанные полосы куадрилатералс.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-147">Linked strips of quadrilaterals.</span></span>                                                         |



 

<span data-ttu-id="b0a0f-148">Подробное описание различий между сетками, полосками и вентиляторами треугольников см. в разделе [Перенос треугольников](porting-triangles.md).</span><span class="sxs-lookup"><span data-stu-id="b0a0f-148">For a detailed discussion of the differences between triangle meshes, strips, and fans, see [Porting Triangles](porting-triangles.md).</span></span>

<span data-ttu-id="b0a0f-149">Количество вершин, которые можно указать в паре [**глбегин**](glbegin.md)гленд, не ограничено  /  [](glend.md) .</span><span class="sxs-lookup"><span data-stu-id="b0a0f-149">There is no limit to the number of vertices you can specify between a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair.</span></span>

<span data-ttu-id="b0a0f-150">Помимо указания вершин внутри пары **глбегин**  /  **гленд** , можно указать текущие стандартные координаты текстуры и текущий цвет.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-150">In addition to specifying vertices inside a **glBegin** / **glEnd** pair, you can specify a current normal, current texture coordinates, and a current color.</span></span> <span data-ttu-id="b0a0f-151">В следующей таблице перечислены команды, допустимые в паре **глбегин**  /  **гленд** .</span><span class="sxs-lookup"><span data-stu-id="b0a0f-151">The following table lists the commands valid inside a **glBegin** / **glEnd** pair.</span></span>



| <span data-ttu-id="b0a0f-152">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="b0a0f-152">IRIS GL function</span></span>        | <span data-ttu-id="b0a0f-153">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="b0a0f-153">OpenGL function</span></span>                                                      | <span data-ttu-id="b0a0f-154">Значение</span><span class="sxs-lookup"><span data-stu-id="b0a0f-154">Meaning</span></span>                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="b0a0f-155">**v2**, **v3**, **v4**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-155">**v2**, **v3**, **v4**</span></span>  | [<span data-ttu-id="b0a0f-156">глвертекс</span><span class="sxs-lookup"><span data-stu-id="b0a0f-156">glVertex</span></span>](glvertex-functions.md)                                   | <span data-ttu-id="b0a0f-157">Задает координаты вершины.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-157">Sets vertex coordinates.</span></span>                         |
| <span data-ttu-id="b0a0f-158">**RGBcolor**, **кпакк**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-158">**RGBcolor**, **cpack**</span></span> | [<span data-ttu-id="b0a0f-159">глколор</span><span class="sxs-lookup"><span data-stu-id="b0a0f-159">glColor</span></span>](glcolor-functions.md)                                     | <span data-ttu-id="b0a0f-160">Задает текущий цвет.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-160">Sets current color.</span></span>                              |
| <span data-ttu-id="b0a0f-161">**color**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-161">**color**</span></span>               | [<span data-ttu-id="b0a0f-162">глиндекс</span><span class="sxs-lookup"><span data-stu-id="b0a0f-162">glIndex</span></span>](glindex-functions.md)                                     | <span data-ttu-id="b0a0f-163">Задает текущий индекс цвета.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-163">Sets current color index.</span></span>                        |
| <span data-ttu-id="b0a0f-164">**n3f**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-164">**n3f**</span></span>                 | [<span data-ttu-id="b0a0f-165">глнормал</span><span class="sxs-lookup"><span data-stu-id="b0a0f-165">glNormal</span></span>](glnormal-functions.md)                                   | <span data-ttu-id="b0a0f-166">Задает обычные векторные координаты.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-166">Sets normal vector coordinates.</span></span>                  |
|                         | [<span data-ttu-id="b0a0f-167">глевалкурд</span><span class="sxs-lookup"><span data-stu-id="b0a0f-167">glEvalCoord</span></span>](glevalcoord-functions.md)                             | <span data-ttu-id="b0a0f-168">Вычисляет включенные одномерное и двухмерные карты.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-168">Evaluates enabled one- and two-dimensional maps.</span></span> |
| <span data-ttu-id="b0a0f-169">**каллобж**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-169">**callobj**</span></span>             | <span data-ttu-id="b0a0f-170">[**глкалллист**](glcalllist.md), [ **глкалллистс**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="b0a0f-170">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="b0a0f-171">Выполняет список дисплеев.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-171">Executes display list(s).</span></span>                        |
| <span data-ttu-id="b0a0f-172">**T2**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-172">**t2**</span></span>                  | [<span data-ttu-id="b0a0f-173">глтекскурд</span><span class="sxs-lookup"><span data-stu-id="b0a0f-173">glTexCoord</span></span>](gltexcoord-functions.md)                               | <span data-ttu-id="b0a0f-174">Задает координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-174">Sets texture coordinates.</span></span>                        |
|                         | [<span data-ttu-id="b0a0f-175">гледжефлаг</span><span class="sxs-lookup"><span data-stu-id="b0a0f-175">glEdgeFlag</span></span>](gledgeflag-functions.md)                               | <span data-ttu-id="b0a0f-176">Управляет краями.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-176">Controls drawing edges.</span></span>                          |
| <span data-ttu-id="b0a0f-177">**лмбинд**</span><span class="sxs-lookup"><span data-stu-id="b0a0f-177">**lmbind**</span></span>              | [<span data-ttu-id="b0a0f-178">глматериал</span><span class="sxs-lookup"><span data-stu-id="b0a0f-178">glMaterial</span></span>](glmaterial-functions.md)                               | <span data-ttu-id="b0a0f-179">Задает свойства материала.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-179">Sets material properties.</span></span>                        |



 

> [!Note]
>
> <span data-ttu-id="b0a0f-180">Если вы используете любую функцию OpenGL, отличную от перечисленных в предыдущей таблице в паре [**глбегин**](glbegin.md)  /  [**гленд**](glend.md) , вы получите непредсказуемые результаты или, возможно, ошибку.</span><span class="sxs-lookup"><span data-stu-id="b0a0f-180">If you use any OpenGL function other than those listed in the preceding table inside a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair, you'll get unpredictable results, or possibly an error.</span></span>

 

 

 




