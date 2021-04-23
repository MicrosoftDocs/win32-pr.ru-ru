---
title: Отрисовка простых поверхностей
description: Библиотека GLU включает набор функций для рисования различных простых поверхностей (шарик, цилиндров, дисков и частей дисков) в различных стилях и ориентациях. Эти функции подробно описаны в справочном руководстве по OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Служебная программа OpenGL (GLU), простые поверхности
- GLU (служебная программа OpenGL), простые поверхности
- простые поверхности OpenGL
- Служебная программа OpenGL (GLU), шарик
- GLU (служебная программа OpenGL), шарик
- шарик OpenGL
- Служебная программа OpenGL (GLU), цилиндры
- GLU (служебная программа OpenGL), цилиндры
- Цилиндры OpenGL
- Служебная программа OpenGL (GLU), диски
- GLU (служебная программа OpenGL), диски
- диски OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411425"
---
# <a name="rendering-simple-surfaces"></a><span data-ttu-id="2920d-116">Отрисовка простых поверхностей</span><span class="sxs-lookup"><span data-stu-id="2920d-116">Rendering Simple Surfaces</span></span>

<span data-ttu-id="2920d-117">Библиотека GLU включает набор функций для рисования различных простых поверхностей (шарик, цилиндров, дисков и частей дисков) в различных стилях и ориентациях.</span><span class="sxs-lookup"><span data-stu-id="2920d-117">The GLU library includes a set of functions for drawing various simple surfaces (spheres, cylinders, disks, and parts of disks) in a variety of styles and orientations.</span></span> <span data-ttu-id="2920d-118">Эти функции подробно описаны в *справочном руководстве по OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="2920d-118">These functions are described in detail in the *OpenGL Reference Manual*.</span></span>

<span data-ttu-id="2920d-119">**Отрисовка простых поверхностей**</span><span class="sxs-lookup"><span data-stu-id="2920d-119">**To render simple surfaces**</span></span>

1.  <span data-ttu-id="2920d-120">Создайте объект куадрик с помощью [**глуневкуадрик**](glunewquadric.md).</span><span class="sxs-lookup"><span data-stu-id="2920d-120">Create a quadric object with [**gluNewQuadric**](glunewquadric.md).</span></span>

    <span data-ttu-id="2920d-121">Чтобы уничтожить этот объект по завершении работы с ним, используйте [**глуделетекуадрик**](gludeletequadric.md).</span><span class="sxs-lookup"><span data-stu-id="2920d-121">To destroy this object when you're finished with it, use [**gluDeleteQuadric**](gludeletequadric.md).</span></span>

2.  <span data-ttu-id="2920d-122">Укажите требуемый стиль подготовки к просмотру, как указано ниже, с соответствующей функцией (если вы не удовлетворены значениями по умолчанию):</span><span class="sxs-lookup"><span data-stu-id="2920d-122">Specify the desired rendering style, as listed below, with the appropriate function (unless you're satisfied with the default values):</span></span>
    -   <span data-ttu-id="2920d-123">Следует ли создавать нормали Surface, и если да, то должно ли одно нормальное на каждую вершину или один нормальный для каждого лица: [ **глукуадрикнормалс**](gluquadricnormals.md)</span><span class="sxs-lookup"><span data-stu-id="2920d-123">Whether surface normals should be generated, and if so, whether there should be one normal per vertex or one normal per face: [**gluQuadricNormals**](gluquadricnormals.md)</span></span>
    -   <span data-ttu-id="2920d-124">Следует ли создавать координаты текстуры: [ **глукуадриктекстуре**](gluquadrictexture.md)</span><span class="sxs-lookup"><span data-stu-id="2920d-124">Whether texture coordinates should be generated: [**gluQuadricTexture**](gluquadrictexture.md)</span></span>
    -   <span data-ttu-id="2920d-125">Какая сторона куадрик должна считаться внешней и внутренней: [ **глукуадрикориентатион**](gluquadricorientation.md)</span><span class="sxs-lookup"><span data-stu-id="2920d-125">Which side of the quadric should be considered the outside and which the inside: [**gluQuadricOrientation**](gluquadricorientation.md)</span></span>
    -   <span data-ttu-id="2920d-126">Следует ли рисовать куадрик как набор многоугольников, линий или точек: [ **глукуадрикдравстиле**](gluquadricdrawstyle.md)</span><span class="sxs-lookup"><span data-stu-id="2920d-126">Whether the quadric should be drawn as a set of polygons, lines, or points: [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span></span>
3.  <span data-ttu-id="2920d-127">После указания стиля подготовки к просмотру вызовите функцию отрисовки для требуемого типа объекта куадрик: [**глусфере**](glusphere.md), [**глуцилиндер**](glucylinder.md), [**глудиск**](gludisk.md)или [**глупартиалдиск**](glupartialdisk.md).</span><span class="sxs-lookup"><span data-stu-id="2920d-127">After specifying the rendering style, invoke the rendering function for the desired type of quadric object: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md), or [**gluPartialDisk**](glupartialdisk.md).</span></span>

    <span data-ttu-id="2920d-128">При возникновении ошибки во время подготовки к просмотру вызывается функция обработки ошибок, указанная с помощью [*глукуадриккаллбакк*](gluquadric.md) .</span><span class="sxs-lookup"><span data-stu-id="2920d-128">If an error occurs during rendering, the error-handling function you've specified with [*gluQuadricCallBack*](gluquadric.md) is invoked.</span></span>

<span data-ttu-id="2920d-129">Используйте *\* радиус*, *высоту* и аналогичные аргументы, а не функцию [**глскале**](glscale.md) , чтобы масштабировать куадрикс, чтобы не нужно было выполнять денормализацию всех создаваемых нормализованных символов.</span><span class="sxs-lookup"><span data-stu-id="2920d-129">Use the *\*Radius*, *height*, and similar arguments, rather than the [**glScale**](glscale.md) function, to scale the quadrics, so that you don't have to renormalize any unit-length normals that are generated.</span></span> <span data-ttu-id="2920d-130">Чтобы принудительно выполнять вычисления освещения с большей степенью детализации, особенно если значение отражения материала велико, задайте для аргументов *Loops* и *Stack* значения, отличные от 1.</span><span class="sxs-lookup"><span data-stu-id="2920d-130">To force lighting calculations at a finer granularity, especially if the material specularity is high, set the *loops* and *stacks* arguments to values other than 1.</span></span>

 

 




