---
title: Использование дружественной Windows
description: Настроив другие элементы управления как дружественные окна для TrackBar, можно автоматически размещать эти элементы управления на концах TrackBar в виде меток.
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6819e0f37f07a90ae08a623f14c6c26d1d67f55ea81143834dfd10816f74396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829063"
---
# <a name="how-to-use-buddy-windows"></a>Использование дружественной Windows

Настроив другие элементы управления как дружественные окна для TrackBar, можно автоматически размещать эти элементы управления на концах TrackBar в виде меток.

На следующем рисунке показана горизонтальная и вертикальная линейка, как со статическими элементами управления в качестве дружественных окон.

![снимок экрана, показывающий диалоговое окно с горизонтальной и вертикальной TrackBar](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Обязательные условия

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="use-buddy-windows"></a>Использовать приятель Windows

В следующем примере кода создаются дружественные окна, показанные на рисунке.


```
void LabelTrackbarsWithBuddies(HWND hDlg)
{
    HWND hwndTrackbar;
    HWND hwndBuddy;
    
    const int staticWidth   = 50;
    const int staticHeight  = 20;

//======================================================
// For horizontal Trackbar.

    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Left", SS_RIGHT | WS_CHILD | WS_VISIBLE, 
                                    0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                    
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);
    
    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Right", SS_LEFT | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
    
//======================================================    
// For vertical Trackbar.
    
    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER2);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Top", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);

    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Bottom", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
}
```



## <a name="remarks"></a>Remarks

**IDC \_ SLIDER1** и **IDC \_ SLIDER2** — это ползунки, созданные в редакторе ресурсов.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




