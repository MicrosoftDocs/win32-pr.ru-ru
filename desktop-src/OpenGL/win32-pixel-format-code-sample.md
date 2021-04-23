---
title: Пример кода формата пикселей Windows
description: В следующем примере кода показана функция, которая задает формат пикселей с помощью функций Windows.
ms.assetid: fa863999-72f1-4280-b278-d9336f62108d
keywords:
- пикселы OpenGL, образец Windows
- перенос в OpenGL, ПКС
- Перенос с OpenGL, Пиксели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4328976a3622d19c3482aa2845c2094975dd7f74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330299"
---
# <a name="windows-pixel-format-code-sample"></a><span data-ttu-id="027d0-106">Пример кода формата пикселей Windows</span><span class="sxs-lookup"><span data-stu-id="027d0-106">Windows Pixel Format Code Sample</span></span>

<span data-ttu-id="027d0-107">В следующем примере кода показана функция, которая задает формат пикселей с помощью функций Windows.</span><span class="sxs-lookup"><span data-stu-id="027d0-107">The following code sample shows a function that sets the pixel format using Windows functions:</span></span>


```C++
BOOL bSetupPixelFormat(HDC hdc) 
{ 
    PIXELFORMATDESCRIPTOR pfd, *ppfd; 
    int pixelformat; 
 
    ppfd = &pfd; 
 
    ppfd->nSize = sizeof(PIXELFORMATDESCRIPTOR); 
    ppfd->nVersion = 1; 
    ppfd->dwFlags = PFD_DRAW_TO_WINDOW | PFD_SUPPORT_OPENGL |  
                        PFD_DOUBLEBUFFER; 
    ppfd->dwLayerMask = PFD_MAIN_PLANE; 
    ppfd->iPixelType = PFD_TYPE_COLORINDEX; 
    ppfd->cColorBits = 8; 
    ppfd->cDepthBits = 16; 
    ppfd->cAccumBits = 0; 
    ppfd->cStencilBits = 0; 
 
    pixelformat = ChoosePixelFormat(hdc, ppfd); 
 
    if ( (pixelformat = ChoosePixelFormat(hdc, ppfd)) == 0 ) 
    { 
        MessageBox(NULL, "ChoosePixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    if (SetPixelFormat(hdc, pixelformat, ppfd) == FALSE) 
    { 
        MessageBox(NULL, "SetPixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    return TRUE; 
}
```



 

 




