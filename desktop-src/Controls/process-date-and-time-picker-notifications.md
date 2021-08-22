---
title: Обработка уведомлений средства выбора даты и времени
description: В этом разделе показано, как обрабатывать уведомления средства выбора даты и времени.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81846d22f3c946d1bfdf661823429fd092b78647cf0ebcb0d683d2600ddcaf17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540483"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a>Обработка уведомлений средства выбора даты и времени

В этом разделе показано, как обрабатывать уведомления средства выбора даты и времени.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Элемент управления "Выбор даты и времени" (DTP) отправляет сообщения уведомления родительскому окну, когда события, обычно активируемые вводом от пользователя, происходят в элементе управления. Приложение должно включать код для определения типа сообщения уведомления и ответа соответствующим образом.

Если вы планируете использовать поля обратного вызова с элементами управления DTP в приложении, необходимо подготовиться к обработке кодов уведомлений [ДТН \_ форматкуери](dtn-formatquery.md), [ДТН \_ ](dtn-format.md)и [ДТН \_ вмкэйдовн](dtn-wmkeydown.md) . Дополнительные сведения о полях обратного вызова см. в разделе [поля обратного вызова](date-and-time-picker-controls.md).

В следующем примере кода C++ определяется сообщение уведомления, отправленное элементом управления DTP, и вызывается соответствующая определяемая приложением функция. В следующих разделах приведены примеры кода, иллюстрирующие процесс обработки уведомлений, которые отображаются в этом примере.

|   Разделы                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [Обработка \_ уведомления ДТН датетимечанже](process-the-dtn-datetimechange-notification.md) |
| [Обработка \_ уведомления ДТН форматкуери](process-the-dtn-formatquery-notification.md)       |
| [Обработка \_ уведомления формата ДТН](process-the-dtn-format-notfication.md)                  |
| [Обработка \_ уведомления ДТН вмкэйдовн](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Уведомления средства выбора даты и времени](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[Справочник по элементу выбора даты и времени](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Использование элементов управления "Выбор даты и времени"](using-date-and-time-picker.md)
</dt> <dt>

[Выбор даты и времени](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




