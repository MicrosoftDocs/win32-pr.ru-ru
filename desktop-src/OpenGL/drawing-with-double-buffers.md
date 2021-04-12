---
title: Рисование с помощью двойных буферов
description: Двойные буферы плавно переходят между одним изображением и другим на экране.
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- OpenGL в Windows, двойные буферы
- Двойная буферизация OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe52d427467b2a6e460ea56a9e72e580ea6f97d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332067"
---
# <a name="drawing-with-double-buffers"></a><span data-ttu-id="0b058-105">Рисование с помощью двойных буферов</span><span class="sxs-lookup"><span data-stu-id="0b058-105">Drawing with Double Buffers</span></span>

<span data-ttu-id="0b058-106">Двойные буферы плавно переходят между одним изображением и другим на экране.</span><span class="sxs-lookup"><span data-stu-id="0b058-106">Double buffers smooth the transition between one image and another on the screen.</span></span> <span data-ttu-id="0b058-107">Переключение буферов обычно происходит в конце последовательности команд рисования.</span><span class="sxs-lookup"><span data-stu-id="0b058-107">Swapping buffers typically comes at the end of a sequence of drawing commands.</span></span> <span data-ttu-id="0b058-108">По умолчанию реализация центра OpenGL в Windows на экран выводится из буфера экрана. После завершения рисования вызовите функцию [**свапбуфферс**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) , чтобы скопировать буфер из буфера экрана в буфер экрана.</span><span class="sxs-lookup"><span data-stu-id="0b058-108">By default, the Microsoft implementation of OpenGL in Windows draws to the off-screen buffer; when drawing is complete, you call the [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) function to copy the off-screen buffer to the on-screen buffer.</span></span> <span data-ttu-id="0b058-109">Следующий пример кода готовится к рисованию, вызывает функцию рисования, а затем копирует готовое изображение на экран, если доступна двойная буферизация.</span><span class="sxs-lookup"><span data-stu-id="0b058-109">The following code sample prepares to draw, calls a drawing function, and then copies the completed image on to the screen if double buffering is available.</span></span>


```C++
void myRedraw(void) 
{ 
    // set up for drawing commands  
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective(45, 1.0, 0.1, 100.0); 
 
    // draw our objects  
    myDrawAllObjects(GL_FALSE); 
 
    // if we're double-buffering ...  
    if (bDoubleBuffering)  
 
        // ...draw the copied image to the screen  
        SwapBuffers(hdc); 
}
```



<span data-ttu-id="0b058-110">Следующий пример кода получает контекст устройства окна, отображает сцену, копирует изображение на экран (для отображения отрисовки), а затем освобождает контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="0b058-110">The following code sample obtains a window device context, renders a scene, copies the image to the screen (to show the rendering), and then releases the device context.</span></span>


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




