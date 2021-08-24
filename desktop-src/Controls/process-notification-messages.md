---
title: Обработка сообщений с уведомлениями
description: Страница свойств отправляет сообщения WM \_ Notify для получения сведений со страниц и для уведомления страниц действий пользователя.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9baf0c58fdbcbe5378dd46e828a2d29a7c91832174c9564660a82c5ab70997a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575484"
---
# <a name="how-to-process-notification-messages"></a>Обработка сообщений с уведомлениями

Страница свойств отправляет сообщения [**WM \_ Notify**](wm-notify.md) для получения сведений со страниц и для уведомления страниц действий пользователя.

Параметр *lParam* сообщения является адресом структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , которая содержит маркер диалогового окна страницы свойств, обработчика для диалогового окна страница и код уведомления. Страница должна отвечать на некоторые сообщения уведомления, присвоив параметру DWL \_ мсгресулт страницы значение **true** или **false**.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование страниц свойств](using-property-sheets.md)
</dt> <dt>

[демонстрация Windows стандартных элементов управления (кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




