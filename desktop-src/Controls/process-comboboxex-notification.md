---
title: Обработка уведомлений ComboBoxEx
description: В этом разделе показано, как обрабатывать сообщения уведомления ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ec73c31020283afe5876567a57fc1fbd8a23cee123e9dc417c14c57a86709a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575494"
---
# <a name="how-to-process-comboboxex-notifications"></a>Обработка уведомлений ComboBoxEx

В этом разделе показано, как обрабатывать сообщения уведомления ComboBoxEx.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения об элементах управления ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Справочник по элементу управления ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Использование элементов управления ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 