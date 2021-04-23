---
title: Перенос Дефс, привязок и наборов
description: Перенос Дефс, привязок и наборов
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- Перенос в ГК IRI, определения
- Перенос из IRI GL, определения
- перенос в OpenGL из IRI GL, определения
- Перенос по стандарту OpenGL из IRI GL, определения
- Перенос GL в ГК, привязки
- Перенос из IRI GL, привязки
- перенос в OpenGL из IRI GL, привязки
- Перенос по стандарту OpenGL из IRI GL, привязки
- Перенос GL в ГК, наборы
- Перенос из IRI GL, наборы
- перенос в OpenGL из IRI GL, наборы
- Перенос по стандарту OpenGL из IRI GL, наборы
- definitions
- Привязывает
- наборы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f9a88253390ee99f5b5870fd7a09e272f1c549
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661512"
---
# <a name="porting-defs-binds-and-sets"></a><span data-ttu-id="a89a9-118">Перенос Дефс, привязок и наборов</span><span class="sxs-lookup"><span data-stu-id="a89a9-118">Porting Defs, Binds, and Sets</span></span>

<span data-ttu-id="a89a9-119">OpenGL не содержит таблиц хранимых определений. Вы не можете определить модели освещения, материал, текстуры, стили линий или закономерности как отдельные объекты, как в IRI GL.</span><span class="sxs-lookup"><span data-stu-id="a89a9-119">OpenGL doesn't have tables of stored definitions; you can't define lighting models, material, textures, line styles, or patterns as separate objects as you can in IRIS GL.</span></span> <span data-ttu-id="a89a9-120">Таким образом, OpenGL не имеет прямых эквивалентов для следующих функций IRI GL:</span><span class="sxs-lookup"><span data-stu-id="a89a9-120">Thus OpenGL has no direct equivalents to the following IRIS GL functions:</span></span>

-   <span data-ttu-id="a89a9-121">**Имдеф** и **Unbind**</span><span class="sxs-lookup"><span data-stu-id="a89a9-121">**Imdef** and **Imbind**</span></span>
-   <span data-ttu-id="a89a9-122">**тевдеф** и **тевбинд**</span><span class="sxs-lookup"><span data-stu-id="a89a9-122">**tevdef** and **tevbind**</span></span>
-   <span data-ttu-id="a89a9-123">**текстдеф** и **текстбинд**</span><span class="sxs-lookup"><span data-stu-id="a89a9-123">**textdef** and **textbind**</span></span>
-   <span data-ttu-id="a89a9-124">**дефинестиле** и **SetStyle**</span><span class="sxs-lookup"><span data-stu-id="a89a9-124">**definestyle** and **setstyle**</span></span>
-   <span data-ttu-id="a89a9-125">**дефпаттерн** и **сетпаттерн**</span><span class="sxs-lookup"><span data-stu-id="a89a9-125">**defpattern** and **setpattern**</span></span>

<span data-ttu-id="a89a9-126">Списки отображаемых списков OpenGL можно использовать для имитации механизма по использованию DEF и привязки IRI GL.</span><span class="sxs-lookup"><span data-stu-id="a89a9-126">You can use OpenGL display lists to mimic the IRIS GL def/bind mechanism.</span></span> <span data-ttu-id="a89a9-127">Например, ниже приведено определение материала в IRI GL:</span><span class="sxs-lookup"><span data-stu-id="a89a9-127">For example, here is a material definition in IRIS GL:</span></span>


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



<span data-ttu-id="a89a9-128">Следующий образец кода OpenGL определяет тот же материал в списке просмотра, на который ссылается номер списка, определенный параметром **миматериал**.</span><span class="sxs-lookup"><span data-stu-id="a89a9-128">The following OpenGL code sample defines the same material in a display list that is referred to by the list number defined by **MYMATERIAL**.</span></span>


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




