---
title: Пример порта списка дисплеев
description: В этом разделе приводится пример кода с кодом IRI GL, который определяет три списка отображаемых списков. один из списков вывода ссылается на другие в его определении. Ниже приведен пример кода, который будет выглядеть при переносе на OpenGL.
ms.assetid: 03283b00-fb5b-4e89-9384-171b38f141ee
keywords:
- Перенос GL по IRI, списки вывода
- Перенос из IRI GL, списки вывода
- перенос в OpenGL из IRI GL, списки вывода
- Перенос по стандарту OpenGL из IRI GL, списки вывода
- списки для показа, перенос из IRI GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbb696673da7f4dc83abd625bb616b67449de64a40df1cfc99bd429a2a980e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962434"
---
# <a name="a-sample-port-of-a-display-list"></a>Пример порта списка дисплеев

В этом разделе приводится пример кода с кодом IRI GL, который определяет три списка отображаемых списков. один из списков вывода ссылается на другие в его определении. Ниже приведен пример кода, который будет выглядеть при переносе на OpenGL.

## <a name="iris-gl-sample-display-list-code"></a>Пример кода вывода списка для примера IRI GL


```C++
makeobj(10);  // 10 object  
    cpack(0x0000FF); 
    recti(164, 33, 364, 600);   // Hollow rectangle  
closeobj(); 
 
makeobj(20);  // 20 object  
    cpack(0xFFFF00); 
    circle(0, 0, 25);           // Unfilled circle  
    recti(100, 100, 200, 200);  // Filled rectangle  
closeobj(); 
 
makeobj(30);  // 30 object  
    callobj(10); 
    cpack(0xFFFFFF); 
    recti(400, 100, 500, 300);  // Draw filled rectangle  
    callobj(20); 
closeobj(); 
 
// Now draw by calling the lists  
call(30);
```



## <a name="opengl-sample-display-list-code"></a>Пример кода для списка дисплеев OpenGL

Приведенный выше код IRI GL переведен в OpenGL:


```C++
glNewList(10, GL_COMPILE);            // List #10  
    glColor3f(1, 0, 0); 
    glRecti(164, 33, 364, 600); 
glEndList(); 
 
glNewList(20, GL_COMPILE);            //List #20  
    glColor3f(1, 1, 0);               // Set color to YELLOW  
    glPolygonMode(GL_BOTH, GL_LINE);  // Unfilled mode  
    glBegin(GL_POLYGON);  // Use polygon to approximate a circle  
        for(i=0; i<100; i++) { 
            cosine = 25 * cos(i * 2 * PI/100.0); 
            sine =   25 * sin(i * 2 * PI/100.0); 
            glVertex2f(cosine, sine); 
        } 
    glEnd(); 
    glBegin(GL_QUADS); 
        glColorf(0, 1, 1);            // Set color to CYAN  
        glVertex2i(100, 100); 
        glVertex2i(100, 200); 
        glVertex2i(200, 200); 
        glVertex2i(100, 200); 
    glEnd(); 
glEndList(); 
 
glNewList(30, GL_COMPILE);            // List #30  
    glCallList(10); 
        glColorf(1, 1, 1);            // Set color to WHITE  
        glRecti(400, 100, 500, 300); 
    glCallList(20); 
glEndList(); 
 
// Execute the display lists  
glCallList(30);
```



 

 




