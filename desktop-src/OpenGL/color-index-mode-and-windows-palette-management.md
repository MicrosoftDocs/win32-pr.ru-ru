---
title: Режим Color-Index и управление палитрой Windows
description: Режим цветового индекса задает цвета в логической палитре с индексом для определенной записи логической палитры.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL в Windows, управление палитрами
- OpenGL в Windows, режим индексирования цветов
- режим индексирования цветов OpenGL
- Управление палитрами OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873308c4ac64d496e344b1c71d440d4dc8321418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068252"
---
# <a name="color-index-mode-and-windows-palette-management"></a>Режим Color-Index и управление палитрой Windows

Режим цветового индекса задает цвета в логической палитре с индексом для определенной записи логической палитры. Большинство программ GDI используют палитры цветового индекса, но режим RGBA для OpenGL лучше подходит для нескольких эффектов, таких как заливка, освещение, туман и сопоставление текстур. Если цвет труест не является критически важным для приложения OpenGL, можно выбрать режим индексирования цвета (например, для схемы топографик, которая использует "false Color", чтобы подчеркнуть градиент повышения прав).

## <a name="color-index-mode-palette-sample"></a>Образец палитры Color-Index Mode

Следующий код настраивает структуру [**пикселформатдескриптор**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) , которая устанавливает флаг элемента **ипикселтипе** в ПФД \_ типа \_ колориндекс. Это означает, что приложение использует палитру цветового индекса.


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
 
    /* Set to color-index mode and use the default color palette. */ 
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



 

 




