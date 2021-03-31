---
title: Ограничение перемещения ползунка
description: Как описано в разделе о элементах управления TrackBar, можно отключить часть диапазона TrackBar в качестве диапазона выбора. Одной из целей диапазона выбора может быть ограничение перемещения ползунка, что делает некоторые части ограничений полного диапазона.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887943"
---
# <a name="how-to-limit-slider-movement"></a>Ограничение перемещения ползунка

Как описано в разделе [о элементах управления TrackBar](trackbar-controls.md), можно отключить часть диапазона TrackBar в качестве диапазона выбора. Одной из целей диапазона выбора может быть ограничение перемещения ползунка, что делает некоторые части ограничений полного диапазона.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="limit-slider-movement"></a>Ограничение перемещения ползунка

В следующем примере кода ограничивается перемещение ползунка путем сброса положения ползунка при перемещении за пределы диапазона выбора.


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a>Комментарии

Этот фрагмент кода был бы частью процедуры окна диалогового окна.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




