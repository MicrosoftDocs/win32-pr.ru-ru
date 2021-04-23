---
title: Пример кода контекста визуализации Windows
description: В следующем примере кода показано, как код контекста отрисовки ГЛКС в предыдущем разделе будет выглядеть, когда он был перенесен в Windows.
ms.assetid: 12992faa-eb64-4a21-8015-3c73c2914189
keywords:
- Контексты отрисовки
- Перенос на OpenGL, контексты отрисовки
- Перенос содержимого OpenGL, контексты отрисовки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0423f7458538f903a339f2f82dbff1c86c0626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661508"
---
# <a name="windows-rendering-context-code-sample"></a><span data-ttu-id="6e4ac-106">Пример кода контекста визуализации Windows</span><span class="sxs-lookup"><span data-stu-id="6e4ac-106">Windows Rendering Context Code Sample</span></span>

<span data-ttu-id="6e4ac-107">В следующем примере кода показано, как код контекста отрисовки ГЛКС в предыдущем разделе будет выглядеть, когда он был перенесен в Windows.</span><span class="sxs-lookup"><span data-stu-id="6e4ac-107">The following code sample shows how the GLX rendering context code in the previous section looks when it has been ported to Windows.</span></span>


```C++
HGLRC hRC;           // rendering context variable  
 
/* Create and initialize a window */ 
        
/* Window message switch in a window procedure */ 
case WM_CREATE:      // Message when window is created  
{ 
    HDC hDC, hDCTemp;    // device context handles   
 
    /* Get the handle of the windows device context. */ 
    hDC = GetDC(hWnd); 
 
    /* Create a rendering context and make it the current context */  
    hRC = wglCreateContext(hDC); 
    if (!hRC)  
    { 
        MessageBox(NULL, "Cannot create context.", "Error", MB_OK); 
        return FALSE; 
    }  
    wglMakeCurrent(hDC, hRC); 
} 
break; 
        
        .    
case WM_DESTROYED:   // Message when window is destroyed  
{ 
    HGLRC hRC        // rendering context handle  
    HDC   hDC;       // device context handle  
 
    /* Release and free the device context and rendering context. */ 
    hDC = wglGetCurrentDC; 
    hRC = wglGetCurrentContext; 
 
    wglMakeCurrent(NULL, NULL); 
 
    if (hRC) 
        wglDeleteContext(hRC); 
 
    if (hDC) 
        ReleaseDC(hWnd, hDC); 
 
    PostQuitMessage (0); 
} 
break;
```



 

 




