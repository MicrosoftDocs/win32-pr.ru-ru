---
title: Перенос измененных списков вывода
description: Хотя вы не можете изменять списки дисплеев OpenGL, вы можете получить аналогичные результаты, добавив вложенные списки, а затем удалив и создав новые версии подсписков.
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- Перенос GL по IRI, списки вывода
- Перенос из IRI GL, списки вывода
- перенос в OpenGL из IRI GL, списки вывода
- Перенос по стандарту OpenGL из IRI GL, списки вывода
- списки для показа, перенос из IRI GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5555c850d4695ba3732b61c0a41b7aedd8af0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661605"
---
# <a name="porting-edited-display-lists"></a><span data-ttu-id="a0f9c-108">Перенос измененных списков вывода</span><span class="sxs-lookup"><span data-stu-id="a0f9c-108">Porting Edited Display Lists</span></span>

<span data-ttu-id="a0f9c-109">Хотя вы не можете изменять списки дисплеев OpenGL, вы можете получить аналогичные результаты, добавив вложенные списки, а затем удалив и создав новые версии подсписков.</span><span class="sxs-lookup"><span data-stu-id="a0f9c-109">Although you can't edit OpenGL display lists, you can get similar results by nesting display lists and then destroying and creating new versions of the sublists.</span></span> <span data-ttu-id="a0f9c-110">Пример:</span><span class="sxs-lookup"><span data-stu-id="a0f9c-110">For example:</span></span>

``` syntax
glNewList (1, GL_COMPILE); 
    glIndexi(MY_RED); 
glEndlist(); 
 
glNewList(2, GL_COMPILE); 
    glScalef(1.2, 1.2, 1.0); 
glEndList(); 
 
glNewList(3, GL_COMPILE); 
    glCallList(1); 
    glCallList(2); 
glEndList(); 
 
glDeleteLists(1, 2); 
glNewList(1, GL_COMPILE); 
    glIndexi(MY_CYAN); 
glEndList(); 
glNewList(2, GL_COPILE); 
    glScalef(0.5, 0.5, 1.0); 
glEndList;
```

 

 




