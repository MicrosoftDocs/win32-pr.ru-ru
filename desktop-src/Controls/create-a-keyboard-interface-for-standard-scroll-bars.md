---
title: Создание интерфейса клавиатуры для стандартных полос прокрутки
description: Хотя элемент управления "полоса прокрутки" предоставляет встроенный интерфейс клавиатуры, стандартная полоса прокрутки не предусмотрена.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25994639a40a6380bbf2f9cc0075e8a78b9e15787dbdf1babf0e6a15550faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698744"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>Создание интерфейса клавиатуры для стандартных полос прокрутки

Хотя элемент управления "полоса прокрутки" предоставляет встроенный интерфейс клавиатуры, стандартная полоса прокрутки не предусмотрена. Чтобы реализовать интерфейс клавиатуры для стандартной полосы прокрутки, процедура окна должна обработать сообщение [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) и изучить код виртуального ключа, указанный параметром *wParam* . Если код виртуального ключа соответствует клавише со стрелкой, то процедура окна отправляет сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) с младшим словом параметра *wParam* , установленным в соответствующий код запроса полосы прокрутки.

Например, когда пользователь нажимает клавишу со стрелкой вверх, процедура окна получает сообщение [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) с параметром *wParam* , равным VK \_ up. В ответ процедура окна отправляет сообщение [**WM \_ VSCROLL**](wm-vscroll.md) с неупорядоченным словом *wParam* , установленным в \_ код запроса SB.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a>Создание интерфейса клавиатуры для стандартной полосы прокрутки

В следующем примере кода показано, как включить интерфейс клавиатуры для стандартной полосы прокрутки.


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование полос прокрутки](using-scroll-bars.md)
</dt> <dt>

[демонстрация Windows стандартных элементов управления (кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 