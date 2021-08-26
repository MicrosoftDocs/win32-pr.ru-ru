---
title: Пример кода формата пикселей ГЛКС
description: В примере кода ниже показано, как программа X Window System (OpenGL) использует функции форматирования ГЛКС или пикселей.
ms.assetid: f01193a9-c0ff-4399-a86e-06bb4603b3f1
keywords:
- перенос в OpenGL, ПКС
- Перенос с OpenGL, Пиксели
- Система X Window, ПКС
- Функции ГЛКС, Пиксели
- Пиксели, пример ГЛКС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312b95fb2ff4719c9ecda863b67ac926905b09d0e4b8aecbcc673a03c18c307a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035393"
---
# <a name="glx-pixel-format-code-sample"></a>Пример кода формата пикселей ГЛКС

В примере кода ниже показано, как программа X Window System (OpenGL) использует функции форматирования ГЛКС или пикселей.


```C++
/* X globals, defines, and prototypes */ 
Display *dpy; 
Window glwin; 
static int attributes[] = {GLX_DEPTH_SIZE, 16, GLX_DOUBLEBUFFER, None}; 
        
    /* find an OpenGL-capable Color Index visual with depth buffer */ 
    vi = glXChooseVisual(dpy, DefaultScreen(dpy), attributes); 
    if (vi == NULL) { 
        fprintf(stderr, "could not get visual\n"); 
        exit(1); 
    }
```



Визуальный элемент можно использовать для создания окна и контекста отрисовки.

 

 




