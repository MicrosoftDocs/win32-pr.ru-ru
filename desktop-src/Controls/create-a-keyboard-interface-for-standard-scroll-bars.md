---
title: Создание интерфейса клавиатуры для стандартных полос прокрутки
description: Хотя элемент управления "полоса прокрутки" предоставляет встроенный интерфейс клавиатуры, стандартная полоса прокрутки не предусмотрена.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891128"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>Создание интерфейса клавиатуры для стандартных полос прокрутки

Хотя элемент управления "полоса прокрутки" предоставляет встроенный интерфейс клавиатуры, стандартная полоса прокрутки не предусмотрена. Чтобы реализовать интерфейс клавиатуры для стандартной полосы прокрутки, процедура окна должна обработать сообщение [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) и изучить код виртуального ключа, указанный параметром *wParam* . Если код виртуального ключа соответствует клавише со стрелкой, то процедура окна отправляет сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) с младшим словом параметра *wParam* , установленным в соответствующий код запроса полосы прокрутки.

Например, когда пользователь нажимает клавишу со стрелкой вверх, процедура окна получает сообщение [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) с параметром *wParam* , равным VK \_ up. В ответ процедура окна отправляет сообщение [**WM \_ VSCROLL**](wm-vscroll.md) с неупорядоченным словом *wParam* , установленным в \_ код запроса SB.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование полос прокрутки](using-scroll-bars.md)
</dt> <dt>

[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 