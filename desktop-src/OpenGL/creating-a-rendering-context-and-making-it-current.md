---
title: Создание контекста отрисовки и его обеспечение текущим
description: В следующем примере кода показано, как создать контекст визуализации OpenGL в ответ на \_ сообщение о создании WM.
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- OpenGL на Windows, контексты отрисовки
- Контексты отрисовки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1768506eba506506a7198fbccc7dfefc0491adc96dd1e7bd03d2ec2aa5df8eb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868794"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a>Создание контекста отрисовки и его обеспечение текущим

В следующем примере кода показано, как создать контекст визуализации OpenGL в ответ на \_ сообщение о создании WM. Обратите внимание, что перед созданием контекста отрисовки настраивается формат пикселей. Также обратите внимание, что в этом сценарии контекст устройства не запускается локально. Вы освобождаете его при закрытии окна, после того как контекст визуализации не является текущим. Дополнительные сведения см. [в разделе Удаление контекста отрисовки](deleting-a-rendering-context.md). Наконец, обратите внимание, что можно использовать локальные переменные для контекста устройства и дескрипторов контекста отрисовки, так как с помощью функций [**вглжеткуррентконтекст**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) и [**вглжеткуррентдк**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) можно получить дескрипторы этих контекстов по мере необходимости.

``` syntax
// a window has been created, but is not yet visible  
case WM_CREATE: 
    { 
    // local variables  
    HDC      hdc ; 
    HGLRC    hglrc ; 
 
    // obtain a device context for the window  
    hdc = GetDC(hWnd); 
     
    // set an appropriate pixel format   
    myPixelFormatSetupFunction(hdc); 
 
    // if we can create a rendering context ...   
    if (hglrc = wglCreateContext( hdc ) ) { 
 
        // try to make it the thread's current rendering context  
        bHaveCurrentRC = wglMakeCurrent(hdc, hglrc) ; 
 
        } 
 
    // perform miscellaneous other WM_CREATE chores ...  
 
    }  
    break;
```

 

 




