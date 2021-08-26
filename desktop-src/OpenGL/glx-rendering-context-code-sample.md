---
title: Пример кода контекста подготовки к просмотру ГЛКС
description: В следующем образце кода показано, как программа X Window System OpenGL использует функции контекста отрисовки ГЛКС.
ms.assetid: 6cee5e5f-ee2f-4fe4-a988-402802e4a1b8
keywords:
- Контексты отрисовки
- Перенос на OpenGL, контексты отрисовки
- Перенос содержимого OpenGL, контексты отрисовки
- Система Window X, контексты отрисовки
- Функции ГЛКС, контексты отрисовки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c15ef1c1e1eddba86da56f8036adfa0724d8c997ba5f4c262f3d14446e86441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035274"
---
# <a name="glx-rendering-context-code-sample"></a>Пример кода контекста подготовки к просмотру ГЛКС

В следующем образце кода показано, как программа X Window System OpenGL использует функции контекста отрисовки ГЛКС.


```C++
Display *dpy;             /* display variable */ 
XVisualInfo *vi;          /* visual variable */ 
Window win;               /* window variable */ 
GLXDrawable drawable;     /* drawable variable */ 
GLXContext cx, cxTemp;    /* rendering context variables */ 
 
/* Code to open a display and get a visual. */ 
        
/* Create a GLX context. */ 
cx = glXCreateContext(dpy, vi, 0, GL_FALSE); 
if (!cx) { 
    fprintf(stderr, "Cannot create context.\n"); 
    exit(-1); 
} 
        
        .    
/* Connect the context to the window. */ 
glXMakeCurrent(dpy, win, cx); 
        
        .    
/* When it's time to destroy the rendering context. . . */ 
cx = glXGetCurrentContext; 
glXDestroyContext(dpy, cx);
```



 

 




