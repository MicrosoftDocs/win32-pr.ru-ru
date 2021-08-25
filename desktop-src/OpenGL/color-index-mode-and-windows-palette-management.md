---
title: Color-Index режим и Windows управление палитрами
description: Режим цветового индекса задает цвета в логической палитре с индексом для определенной записи логической палитры.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL на Windows, управление палитрами
- OpenGL на Windows, режим индексирования цветов
- режим индексирования цветов OpenGL
- Управление палитрами OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e4d7c9db02a80bdffdef93655e88cc5b2ca8197a58c5ffdb488c2b782f10d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889264"
---
# <a name="color-index-mode-and-windows-palette-management"></a>Color-Index режим и Windows управление палитрами

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



 

 




