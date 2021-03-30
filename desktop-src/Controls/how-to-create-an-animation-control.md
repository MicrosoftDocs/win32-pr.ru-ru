---
title: Создание элемента управления "анимация"
description: В этом разделе показано, как создать элемент управления анимации.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067596"
---
# <a name="how-to-create-an-animation-control"></a>Создание элемента управления "анимация"

В этом разделе показано, как создать элемент управления анимации. В соответствующем примере кода C++ в диалоговом окне создается элемент управления "анимация". Он позиционирует элемент управления анимации под заданным элементом управления и устанавливает размеры элемента управления анимации на основе размеров кадра в Audio-Videoном ролике AVI.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows
-   Файлы AVI

## <a name="instructions"></a>Инструкции

### <a name="step-1-create-an-instance-of-the-animation-control"></a>Шаг 1. Создание экземпляра элемента управления "анимация".

Используйте макрос [**анимации \_ CREATE**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) , чтобы создать экземпляр элемента управления анимации.


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>Шаг 2. размещение элемента управления анимации.

Получение координат экрана указанной кнопки управления.


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



Преобразование координат левого нижнего угла в клиентские координаты.


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



Размещение элемента управления "анимация" под указанной кнопкой элемента управления.


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a>Шаг 3. Откройте ролик AVI.

Вызовите макрос [**анимировать \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) , чтобы открыть ролик AVI и отобразить первый кадр в элементе управления анимации. Вызовите функцию **ShowWindow** , чтобы сделать элемент управления анимацией видимым.


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a>Полный пример


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Об элементах управления анимацией](animation-control-overview.md)
</dt> <dt>

[Справочник по элементу управления анимацией](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Использование элементов управления анимацией](using-animation-control.md)
</dt> <dt>

[Анимация](animation-control-reference.md)
</dt> </dl>

 

 




