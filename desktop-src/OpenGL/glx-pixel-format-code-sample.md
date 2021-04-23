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
ms.openlocfilehash: 9f0ab6464d54e696c136a6c987b94124f52b0ee2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773352"
---
# <a name="glx-pixel-format-code-sample"></a><span data-ttu-id="015cb-108">Пример кода формата пикселей ГЛКС</span><span class="sxs-lookup"><span data-stu-id="015cb-108">GLX Pixel Format Code Sample</span></span>

<span data-ttu-id="015cb-109">В примере кода ниже показано, как программа X Window System (OpenGL) использует функции форматирования ГЛКС или пикселей.</span><span class="sxs-lookup"><span data-stu-id="015cb-109">The code sample below shows how an X Window System OpenGL program uses GLX visual/pixel formatting functions.</span></span>


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



<span data-ttu-id="015cb-110">Визуальный элемент можно использовать для создания окна и контекста отрисовки.</span><span class="sxs-lookup"><span data-stu-id="015cb-110">The Visual can be used to create a window and a rendering context.</span></span>

 

 




