---
title: Обработка уведомления DTN_DATETIMECHANGE
description: В этом разделе показано, как обрабатывать уведомления об изменениях, внесенных пользователем, к элементу выбора даты и времени (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9490059a202eff69a05b34a086e74d6df52758713fd5b66d899d1ab114a31040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829925"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>Обработка \_ уведомления ДТН датетимечанже

В этом разделе показано, как обрабатывать уведомления об изменениях, внесенных пользователем, к элементу выбора даты и времени (DTP).

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Обязательные условия

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Элемент управления DTP отправляет код [уведомления \_ датетимечанже ДТН](dtn-datetimechange.md) каждый раз, когда происходит изменение. Например, это уведомление будет создано при изменении пользователем одного из полей в элементе управления или в случае, если элемент управления установлен в стиль [**\_ шовноне DTS**](date-and-time-picker-control-styles.md) , когда пользователь изменяет состояние флажка элемента управления.

Приложение должно содержать код для обработки сообщений ДТН \_ датетимечанже, которые отправляются элементом управления DTP.

Следующий пример кода C++ представляет собой определяемую приложением функцию, предназначенную для указания состояния элемента управления DTP, для которого задан стиль **\_ Шовноне служб DTS** .



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления "Выбор даты и времени"](using-date-and-time-picker.md)
</dt> <dt>

[Справочник по элементу выбора даты и времени](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Выбор даты и времени](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




