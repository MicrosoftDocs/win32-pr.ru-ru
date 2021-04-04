---
title: Обработка сообщений с уведомлениями
description: Страница свойств отправляет сообщения WM \_ Notify для получения сведений со страниц и для уведомления страниц действий пользователя.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789355"
---
# <a name="how-to-process-notification-messages"></a>Обработка сообщений с уведомлениями

Страница свойств отправляет сообщения [**WM \_ Notify**](wm-notify.md) для получения сведений со страниц и для уведомления страниц действий пользователя.

Параметр *lParam* сообщения является адресом структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , которая содержит маркер диалогового окна страницы свойств, обработчика для диалогового окна страница и код уведомления. Страница должна отвечать на некоторые сообщения уведомления, присвоив параметру DWL \_ мсгресулт страницы значение **true** или **false**.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="process-notification-messages"></a>Обработка сообщений уведомления

Следующий пример является фрагментом кода из процедуры диалогового окна для страницы. В нем показано, как обработать код уведомления [ \_ справки PSN](psn-help.md) .


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование страниц свойств](using-property-sheets.md)
</dt> <dt>

[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




