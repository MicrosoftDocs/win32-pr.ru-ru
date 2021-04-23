---
title: Библиотека сферы IRI GL
description: OpenGL не поддерживает библиотеку "Сфера" (IRI). Вызовы библиотеки сферы можно заменить на подпрограммы куадрикс из библиотеки GLU. Дополнительные сведения о библиотеке GLU см. в разделе Open GL Guide и библиотека служебных программ OpenGL.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- Перенос GL по IRI, Библиотека Sphere
- Перенос из ДИАФРАГМы в ГК, Библиотека Sphere
- перенос в OpenGL из IRI GL, Библиотека Sphere
- Перенос по стандарту OpenGL из IRI GL, Библиотека Sphere
- функции рисования, Библиотека Sphere
- Библиотека Sphere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330640"
---
# <a name="the-iris-gl-sphere-library"></a><span data-ttu-id="abc2e-111">Библиотека сферы IRI GL</span><span class="sxs-lookup"><span data-stu-id="abc2e-111">The IRIS GL Sphere Library</span></span>

<span data-ttu-id="abc2e-112">OpenGL не поддерживает библиотеку "Сфера" (IRI).</span><span class="sxs-lookup"><span data-stu-id="abc2e-112">OpenGL does not support the IRIS GL sphere library.</span></span> <span data-ttu-id="abc2e-113">Вызовы библиотеки сферы можно заменить на подпрограммы куадрикс из библиотеки GLU.</span><span class="sxs-lookup"><span data-stu-id="abc2e-113">You can replace your sphere library calls with quadrics routines from the GLU library.</span></span> <span data-ttu-id="abc2e-114">Дополнительные сведения о библиотеке GLU см. в разделе *Open GL Guide* и [Библиотека служебных программ OpenGL](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="abc2e-114">For more information about the GLU library, see the *Open GL Programming Guide* and [OpenGL Utility Library](opengl-utility-library.md).</span></span>

<span data-ttu-id="abc2e-115">В следующей таблице перечислены функции куадрикс OpenGL.</span><span class="sxs-lookup"><span data-stu-id="abc2e-115">The following table lists the OpenGL quadrics functions.</span></span>



| <span data-ttu-id="abc2e-116">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="abc2e-116">OpenGL function</span></span>                                        | <span data-ttu-id="abc2e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="abc2e-117">Meaning</span></span>                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="abc2e-118">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="abc2e-118">**gluNewQuadric**</span></span>](glunewquadric.md)                 | <span data-ttu-id="abc2e-119">Создает новый объект куадрик.</span><span class="sxs-lookup"><span data-stu-id="abc2e-119">Creates a new quadric object.</span></span>                                    |
| [<span data-ttu-id="abc2e-120">**глуделетекуадрик**</span><span class="sxs-lookup"><span data-stu-id="abc2e-120">**gluDeleteQuadric**</span></span>](gludeletequadric.md)           | <span data-ttu-id="abc2e-121">Удаляет объект куадрик.</span><span class="sxs-lookup"><span data-stu-id="abc2e-121">Deletes a quadric object.</span></span>                                        |
| [<span data-ttu-id="abc2e-122">*глукуадриккаллбакк*</span><span class="sxs-lookup"><span data-stu-id="abc2e-122">*gluQuadricCallback*</span></span>](gluquadric.md)                 | <span data-ttu-id="abc2e-123">Связывает обратный вызов с объектом куадрик для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="abc2e-123">Associates a callback with a quadric object, for error handling.</span></span> |
| [<span data-ttu-id="abc2e-124">**глукуадрикнормалс**</span><span class="sxs-lookup"><span data-stu-id="abc2e-124">**gluQuadricNormals**</span></span>](gluquadricnormals.md)         | <span data-ttu-id="abc2e-125">Задает нормали: нет обычных, по одному на каждый из них или по одному на вершину.</span><span class="sxs-lookup"><span data-stu-id="abc2e-125">Specifies normals: no normals, one per face, or one per vertex.</span></span>  |
| [<span data-ttu-id="abc2e-126">**глукуадрикориентатион**</span><span class="sxs-lookup"><span data-stu-id="abc2e-126">**gluQuadricOrientation**</span></span>](gluquadricorientation.md) | <span data-ttu-id="abc2e-127">Задает направление нормалей: по внешнему или внутрь.</span><span class="sxs-lookup"><span data-stu-id="abc2e-127">Specifies direction of normals: outward or inward.</span></span>               |
| [<span data-ttu-id="abc2e-128">**глукуадриктекстуре**</span><span class="sxs-lookup"><span data-stu-id="abc2e-128">**gluQuadricTexture**</span></span>](gluquadrictexture.md)         | <span data-ttu-id="abc2e-129">Включает или выключает создание координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="abc2e-129">Turns texture-coordinate generation on or off.</span></span>                   |
| [<span data-ttu-id="abc2e-130">**глукуадрикдравстиле**</span><span class="sxs-lookup"><span data-stu-id="abc2e-130">**gluQuadricDrawstyle**</span></span>](gluquadricdrawstyle.md)     | <span data-ttu-id="abc2e-131">Задает стиль отображения: многоугольники, линии, точки и т. д.</span><span class="sxs-lookup"><span data-stu-id="abc2e-131">Specifies drawing style: polygons, lines, points, and so on.</span></span>     |
| [<span data-ttu-id="abc2e-132">**глусфере**</span><span class="sxs-lookup"><span data-stu-id="abc2e-132">**gluSphere**</span></span>](glusphere.md)                         | <span data-ttu-id="abc2e-133">Рисует сферу.</span><span class="sxs-lookup"><span data-stu-id="abc2e-133">Draws a sphere.</span></span>                                                  |
| [<span data-ttu-id="abc2e-134">**глуцилиндер**</span><span class="sxs-lookup"><span data-stu-id="abc2e-134">**gluCylinder**</span></span>](glucylinder.md)                     | <span data-ttu-id="abc2e-135">Рисование цилиндра или конуса.</span><span class="sxs-lookup"><span data-stu-id="abc2e-135">Draws a cylinder or cone.</span></span>                                        |
| [<span data-ttu-id="abc2e-136">**глупартиалдиск**</span><span class="sxs-lookup"><span data-stu-id="abc2e-136">**gluPartialDisk**</span></span>](glupartialdisk.md)               | <span data-ttu-id="abc2e-137">Рисование дуги.</span><span class="sxs-lookup"><span data-stu-id="abc2e-137">Draws an arc.</span></span>                                                    |
| [<span data-ttu-id="abc2e-138">**глудиск**</span><span class="sxs-lookup"><span data-stu-id="abc2e-138">**gluDisk**</span></span>](gludisk.md)                             | <span data-ttu-id="abc2e-139">Рисует круг или диск.</span><span class="sxs-lookup"><span data-stu-id="abc2e-139">Draws a circle or disk.</span></span>                                          |



 

<span data-ttu-id="abc2e-140">Можно использовать один объект куадрик для всех куадрикс, которые требуется визуализировать подобным образом.</span><span class="sxs-lookup"><span data-stu-id="abc2e-140">You can use one quadric object for all quadrics you want to render in similar ways.</span></span> <span data-ttu-id="abc2e-141">В следующем примере кода используются два объекта куадрик для рисования четырех куадрикс, два из которых текстурированы.</span><span class="sxs-lookup"><span data-stu-id="abc2e-141">The following code sample uses two quadric objects to draw four quadrics, two of them textured.</span></span>


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




