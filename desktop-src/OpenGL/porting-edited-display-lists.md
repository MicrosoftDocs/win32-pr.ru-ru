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
ms.openlocfilehash: 13f1630b0560091482d47f85e038d908dcfab202ae772c4d35dc388324b46075
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485584"
---
# <a name="porting-edited-display-lists"></a>Перенос измененных списков вывода

Хотя вы не можете изменять списки дисплеев OpenGL, вы можете получить аналогичные результаты, добавив вложенные списки, а затем удалив и создав новые версии подсписков. Пример:

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

 

 




