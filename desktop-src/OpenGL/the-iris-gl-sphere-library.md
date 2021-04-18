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
# <a name="the-iris-gl-sphere-library"></a>Библиотека сферы IRI GL

OpenGL не поддерживает библиотеку "Сфера" (IRI). Вызовы библиотеки сферы можно заменить на подпрограммы куадрикс из библиотеки GLU. Дополнительные сведения о библиотеке GLU см. в разделе *Open GL Guide* и [Библиотека служебных программ OpenGL](opengl-utility-library.md).

В следующей таблице перечислены функции куадрикс OpenGL.



| Функция OpenGL                                        | Значение                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [**глуневкуадрик**](glunewquadric.md)                 | Создает новый объект куадрик.                                    |
| [**глуделетекуадрик**](gludeletequadric.md)           | Удаляет объект куадрик.                                        |
| [*глукуадриккаллбакк*](gluquadric.md)                 | Связывает обратный вызов с объектом куадрик для обработки ошибок. |
| [**глукуадрикнормалс**](gluquadricnormals.md)         | Задает нормали: нет обычных, по одному на каждый из них или по одному на вершину.  |
| [**глукуадрикориентатион**](gluquadricorientation.md) | Задает направление нормалей: по внешнему или внутрь.               |
| [**глукуадриктекстуре**](gluquadrictexture.md)         | Включает или выключает создание координат текстуры.                   |
| [**глукуадрикдравстиле**](gluquadricdrawstyle.md)     | Задает стиль отображения: многоугольники, линии, точки и т. д.     |
| [**глусфере**](glusphere.md)                         | Рисует сферу.                                                  |
| [**глуцилиндер**](glucylinder.md)                     | Рисование цилиндра или конуса.                                        |
| [**глупартиалдиск**](glupartialdisk.md)               | Рисование дуги.                                                    |
| [**глудиск**](gludisk.md)                             | Рисует круг или диск.                                          |



 

Можно использовать один объект куадрик для всех куадрикс, которые требуется визуализировать подобным образом. В следующем примере кода используются два объекта куадрик для рисования четырех куадрикс, два из которых текстурированы.


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



 

 




