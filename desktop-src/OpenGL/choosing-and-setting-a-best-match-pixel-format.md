---
title: Выбор и настройка формата пикселей Best-Match
description: В этом разделе описывается процедура сопоставления контекста устройства с форматом пикселей.
ms.assetid: 7b974fb5-e34d-4781-858c-572c4e7754bc
keywords:
- OpenGL в Windows, ПКС
- наиболее подходящий формат пикселей OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143800a9c43d8c8a7779bb5e6cd119c6737f8129
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681442"
---
# <a name="choosing-and-setting-a-best-match-pixel-format"></a><span data-ttu-id="f54df-105">Выбор и настройка формата пикселей Best-Match</span><span class="sxs-lookup"><span data-stu-id="f54df-105">Choosing and Setting a Best-Match Pixel Format</span></span>

<span data-ttu-id="f54df-106">В этом разделе описывается процедура сопоставления контекста устройства с форматом пикселей.</span><span class="sxs-lookup"><span data-stu-id="f54df-106">This topic explains the procedure for matching a device context to a pixel format.</span></span>

<span data-ttu-id="f54df-107">**Получение лучшего соответствия контекста устройства формату пикселей**</span><span class="sxs-lookup"><span data-stu-id="f54df-107">**To obtain a device context's best match to a pixel format**</span></span>

1.  <span data-ttu-id="f54df-108">Укажите требуемый формат пикселей в структуре [**пикселформатдескриптор**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="f54df-108">Specify the desired pixel format in a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) structure.</span></span>
2.  <span data-ttu-id="f54df-109">Вызовите [**чусепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="f54df-109">Call [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span>

    <span data-ttu-id="f54df-110">Функция **чусепикселформат** возвращает индекс формата пикселей, который затем можно передать в [**сетпикселформат**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) , чтобы задать наилучшее соответствие формата пикселей в качестве текущего формата пикселей контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="f54df-110">The **ChoosePixelFormat** function returns a pixel format index, which you can then pass to [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) to set the best pixel format match as the device context's current pixel format.</span></span>

<span data-ttu-id="f54df-111">В следующем примере кода показано, как выполнить описанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="f54df-111">The following code sample shows how to carry out the above steps.</span></span>


```C++
PIXELFORMATDESCRIPTOR pfd = { 
    sizeof(PIXELFORMATDESCRIPTOR),    // size of this pfd  
    1,                                // version number  
    PFD_DRAW_TO_WINDOW |              // support window  
    PFD_SUPPORT_OPENGL |              // support OpenGL  
    PFD_DOUBLEBUFFER,                 // double buffered  
    PFD_TYPE_RGBA,                    // RGBA type  
    24,                               // 24-bit color depth  
    0, 0, 0, 0, 0, 0,                 // color bits ignored  
    0,                                // no alpha buffer  
    0,                                // shift bit ignored  
    0,                                // no accumulation buffer  
    0, 0, 0, 0,                       // accum bits ignored  
    32,                               // 32-bit z-buffer      
    0,                                // no stencil buffer  
    0,                                // no auxiliary buffer  
    PFD_MAIN_PLANE,                   // main layer  
    0,                                // reserved  
    0, 0, 0                           // layer masks ignored  
}; 
HDC  hdc; 
int  iPixelFormat; 
 
// get the device context's best, available pixel format match  
iPixelFormat = ChoosePixelFormat(hdc, &pfd); 
 
// make that match the device context's current pixel format  
SetPixelFormat(hdc, iPixelFormat, &pfd);
```



 

 




