---
title: Рисование изображения
description: В этом разделе показано, как использовать \_ функцию рисования ImageList для рисования изображения.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac13eef2eb5bc55866ac2fd930db5494f2683dd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988019"
---
# <a name="how-to-draw-an-image"></a>Рисование изображения

В этом разделе показано, как использовать [**функцию \_ рисования ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) для рисования изображения.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Чтобы нарисовать изображение, используйте функцию [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) или [**ImageList \_ дравекс**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) . Вы указываете маркер для списка изображений, индекс изображения для рисования, маркер для контекста устройства назначения, расположение в контексте устройства и один или несколько стилей рисования.

Определяемая пользователем функция в следующем примере кода C++ использует функцию [**\_ рисования ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) для рисования изображения и сохраняет клиентские координаты ограничивающего прямоугольника изображения. Последующая функция использует ограничивающий прямоугольник для определения того, щелкнул пользователь изображение.



```C++
// DrawTheImage - draws an image transparently and saves 
// the bounding rectangle of the drawn image.
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which to draw the image. 
// himl - handle to the image list that contains the image. 
// cx and cy - client coordinates for the upper-left corner of the image. 
// 
// Global variables and constants 
//     g_nImage - index of the image to draw. 
//     g_rcImage - bounding rectangle of the image. 
//     CX_IMAGE and CY_IMAGE - width and height of the image. 
extern int g_nImage; 
extern RECT g_rcImage; 
 
#define CX_IMAGE 32 
#define CY_IMAGE 32 
 
BOOL DrawTheImage(HWND hwnd, HIMAGELIST himl, int cx, int cy) 
{ 
    HDC hdc; 
 
    if ((hdc = GetDC(hwnd)) == NULL) 
        return FALSE; 
    if (!ImageList_Draw(himl, g_nImage, hdc, cx, cy, ILD_TRANSPARENT)) 
        return FALSE; 
    ReleaseDC(hwnd, hdc); 
 
    SetRect(&g_rcImage, cx, cy, CX_IMAGE + cx, CY_IMAGE + cy); 
 
    return TRUE; 
} 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по спискам изображений](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[О списках изображений](image-lists.md)
</dt> <dt>

[Использование списков изображений](using-image-lists.md)
</dt> </dl>

 

 




