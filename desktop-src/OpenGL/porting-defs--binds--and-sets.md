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
# <a name="porting-defs-binds-and-sets"></a>Перенос Дефс, привязок и наборов

OpenGL не содержит таблиц хранимых определений. Вы не можете определить модели освещения, материал, текстуры, стили линий или закономерности как отдельные объекты, как в IRI GL. Таким образом, OpenGL не имеет прямых эквивалентов для следующих функций IRI GL:

-   **Имдеф** и **Unbind**
-   **тевдеф** и **тевбинд**
-   **текстдеф** и **текстбинд**
-   **дефинестиле** и **SetStyle**
-   **дефпаттерн** и **сетпаттерн**

Списки отображаемых списков OpenGL можно использовать для имитации механизма по использованию DEF и привязки IRI GL. Например, ниже приведено определение материала в IRI GL:


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



Следующий образец кода OpenGL определяет тот же материал в списке просмотра, на который ссылается номер списка, определенный параметром **миматериал**.


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



 

 




