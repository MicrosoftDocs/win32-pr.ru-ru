---
title: Обработка сообщений с уведомлениями TrackBar
description: Значения TrackBar уведомляют свое родительское окно действий пользователя, отправляя родительское \_ сообщение WM HSCROLL или WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774543"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Обработка сообщений с уведомлениями TrackBar

Значения TrackBar уведомляют свое родительское окно действий пользователя, отправляя родительское сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="process-trackbar-notification-messages"></a>Обработка сообщений с уведомлениями линейки

В следующем примере кода показана функция, которая вызывается, когда родительское окно TrackBar получает [**сообщение \_ HSCROLL WM**](wm-hscroll.md) . Значение TrackBar в этом примере имеет стиль [**TBS \_ енаблеселранже**](trackbar-control-styles.md) . Положение ползунка сравнивается с диапазоном выбора, а ползунок перемещается на начальную или конечную точку диапазона выбора при необходимости.


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a>Комментарии

В диалоговом окне, содержащем линейку с [**\_ вертикальным**](trackbar-control-styles.md) стилем TBS, эта функция может использоваться при получении сообщения [**\_ VSCROLL WM**](wm-vscroll.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




