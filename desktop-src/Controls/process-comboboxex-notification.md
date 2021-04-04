---
title: Обработка уведомлений ComboBoxEx
description: В этом разделе показано, как обрабатывать сообщения уведомления ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988031"
---
# <a name="how-to-process-comboboxex-notifications"></a>Обработка уведомлений ComboBoxEx

В этом разделе показано, как обрабатывать сообщения уведомления ComboBoxEx.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Элемент управления ComboBoxEx уведомляет свое родительское окно о событиях, отправляя сообщения [**WM \_ Notify**](wm-notify.md) . Он также передает сообщения [**\_ командной строки WM**](/windows/desktop/menurc/wm-command) , которые он получает из поля со списком, содержащегося в нем, в родительское окно для обработки. Поэтому приложение должно быть подготовлено к обработке сообщений **WM \_ Notify** из **\_ командных** сообщений ComboBoxEx и WM, пересылаемых из элемента управления дочернего поля ComboBoxEx.

Пример в этом разделе обрабатывает сообщения [**\_ командной строки**](/windows/desktop/menurc/wm-command) [**WM \_ Notify**](wm-notify.md) и WM из элемента управления ComboBoxEx, вызывая соответствующую определяемую приложением функцию для обработки этих сообщений.

## <a name="complete-example"></a>Полный пример


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Сведения об элементах управления ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Справочник по элементу управления ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Использование элементов управления ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 