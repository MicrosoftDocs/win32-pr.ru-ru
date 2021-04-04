---
title: Обработка уведомления DTN_DATETIMECHANGE
description: В этом разделе показано, как обрабатывать уведомления об изменениях, внесенных пользователем, к элементу выбора даты и времени (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988030"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>Обработка \_ уведомления ДТН датетимечанже

В этом разделе показано, как обрабатывать уведомления об изменениях, внесенных пользователем, к элементу выбора даты и времени (DTP).

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления "Выбор даты и времени"](using-date-and-time-picker.md)
</dt> <dt>

[Справочник по элементу выбора даты и времени](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Выбор даты и времени](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




