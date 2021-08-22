---
title: Обработка сообщений с уведомлениями TrackBar
description: Значения TrackBar уведомляют свое родительское окно действий пользователя, отправляя родительское \_ сообщение WM HSCROLL или WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211a468c5c107a96fc6b28d12feed219799450828db07be87cd8887b5816bd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540324"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Обработка сообщений с уведомлениями TrackBar

Значения TrackBar уведомляют свое родительское окно действий пользователя, отправляя родительское сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

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



## <a name="remarks"></a>Remarks

В диалоговом окне, содержащем линейку с [**\_ вертикальным**](trackbar-control-styles.md) стилем TBS, эта функция может использоваться при получении сообщения [**\_ VSCROLL WM**](wm-vscroll.md) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




