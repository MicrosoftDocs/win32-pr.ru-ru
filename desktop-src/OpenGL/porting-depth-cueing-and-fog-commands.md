---
title: Перенос команд cueing и туман глубины
description: Перенос команд cueing и туман глубины
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Перенос GL по IRI, глубина cueing
- Перенос из IRI GL, Depth cueing
- перенос в OpenGL из IRI GL, Depth cueing
- Перенос по стандарту OpenGL из IRI GL, Depth cueing
- Перенос GL в ГК, туман
- Перенос из IRI GL, туман
- Перенос на OpenGL из IRI GL, туман
- Перенос по стандарту OpenGL из IRI GL, тумана
- cueing глубины
- туман
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258809"
---
# <a name="porting-depth-cueing-and-fog-commands"></a>Перенос команд cueing и туман глубины

При переносе команд Depth-cueing и тумана учитывайте следующие моменты:

-   Вызов IRI GL, **фогвертекс**, задает режим и параметры, влияющие на этот режим. В OpenGL вы вызываете [**глфог**](glfog.md) один раз, чтобы установить режим, а затем снова дважды или больше, чтобы задать различные параметры.
-   В OpenGL глубина cueing не является отдельной функцией. Используйте линейную туман, а не глубину cueing. (В этом разделе приводится пример того, как это сделать.) В следующих функциях IRI GL нет прямого эквивалента OpenGL:

    **депскуе**

    **лргбранже**

    **лшадеранже**

    **жетдкм**

-   Чтобы настроить качество тумана, используйте [**глхинт**](glhint.md)( \_ Указание тумана GL \_ ).

В следующей таблице перечислены функции IRI GL по управлению туманом и их эквивалентные функции OpenGL.



| Функция IRI GL         | Функция OpenGL                                     | Значение                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| **фогвертекс**            | [**глфог**](glfog.md)                              | Задает различные параметры тумана.      |
| **фогвертекс**(FG \_ On)  | [**гленабле**](glenable.md) ( \_ туман GL)            | Включает туман.                     |
| **фогвертекс**(FG \_ Off) | [**глдисабле**](gldisable.md) ( \_ туман GL)          | Отключает туман.                    |
| **депскуе**             | [**глфог**](glfog.md) (GL- \_ туман \_ Mod, \_ линейная, GL) | Использует линейный туман для глубины cueing. |



 

В следующей таблице перечислены параметры, которые можно передать в **глфог**.



| Параметр тумана    | Значение                       | Значение по умолчанию                  |
|------------------|-------------------------------|--------------------------|
| \_плотность тумана GL \_ | Плотность тумана.                  | 1.0                      |
| Начало работы с \_ туманом GL \_   | Близкое расстояние для линейного тумана. | 0,0                      |
| Окончание GL в главной \_ \_ части     | Дальнее расстояние линейного тумана.  | 1.0                      |
| \_индекс тумана GL \_   | Цветовой индекс тумана.              | 0,0                      |
| \_Цвет тумана GL \_   | Цвет RGBA тумана.               | (0, 0, 0, 0)             |
| \_режим тумана GL \_    | Режим тумана.                     | См. следующую таблицу. |



 

Параметр плотности тумана OpenGL отличается от стандарта в IRI GL. Они связаны следующим образом:

-   Если *фогмоде* = EXP2
     

    *опенглфогденсити* = (*ирисглфогденсити* ) ( **sqrt** ( **Журнал** (1/255)))
-   Если *фогмоде* = exp
     

    *опенглфогденсити* = (*ирисглфогденсити* ) ( **Журнал** (1/255))

где **sqrt** — это квадратный корень, **log** — это натуральный логарифм, *ирисглфогденсити* — плотность тумана в форме IRI, а *опенглфогденсити* — плотность тумана OpenGL.

Для переключения между вычислением тумана в режиме "на пиксель" и режимом вершины используйте [**глхинт**](glhint.md)( \_ Указание тумана в ГК \_ , *хинтмоде*). Доступны два режима подсказок:

-   \_Вычисление тумана НИЦЕСТ GL на пиксельном уровне
-   \_Самый быстрый расчет тумана на вершину в ГК

В следующей таблице перечислены режимы и эквиваленты типов тумана IRI GL.



| Режим тумана IRI GL                       | Режим тумана OpenGL | Режим подсказки                         | Значение                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| FG \_ вткс \_ exp, FG \_ PIX \_ exp<br/>   | \_exp ГК         | \_самая быстрая, GL, \_ ницест<br/> | Интенсивный режим тумана (по умолчанию).                |
| FG \_ вткс \_ EXP2, FG \_ PIX \_ EXP2<br/> | \_EXP2 GL        | \_самая быстрая, GL, \_ ницест<br/> | Режим ХАЗе.                               |
| FG \_ вткс \_ ссыл, FG \_ PIX \_<br/>   | Линейная (GL) \_      | \_самая быстрая, GL, \_ ницест<br/> | Линейный режим тумана. (Используйте для глубины cueing.) |



 

В следующем примере кода показано cueing глубины в OpenGL:


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





