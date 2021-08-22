---
title: Отображение подсказок для кнопок
description: При указании \_ стиля подсказок тбстиле панель инструментов создает элемент управления ToolTip и управляет им. Элемент управления ToolTip скрыт и появляется, только если пользователь наводит указатель мыши на кнопку панели инструментов и оставляет его примерно на одну секунду.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f169c6cc9324c98ed085b38f14802fcaa3c5cfbc8bd7ee9aa29af62ef41a6adc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320004"
---
# <a name="how-to-display-tooltips-for-buttons"></a>Отображение подсказок для кнопок

При указании стиля [**\_ подсказок тбстиле**](toolbar-control-and-button-styles.md) панель инструментов создает элемент управления ToolTip и управляет им. Элемент управления ToolTip скрыт и появляется, только если пользователь наводит указатель мыши на кнопку панели инструментов и оставляет его примерно на одну секунду.

Приложение может передать текст в элемент управления ToolTip одним из следующих способов:

-   Установите текст подсказки в качестве элемента **истринг** структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) для каждой кнопки. Кроме того, необходимо отправить [**сообщение \_ Сетмакстекстровс в ТБ**](tb-setmaxtextrows.md) и установить максимальное число строк в 0, чтобы текст не отображался как метка кнопки, а не как всплывающая подсказка.
-   Создайте панель инструментов со стилем [**\_ списка тбстиле**](toolbar-control-and-button-styles.md) , а затем задайте расширенный стиль [**тбстиле \_ ex \_ микседбуттонс**](toolbar-extended-styles.md) . Метки отображаются только для кнопок, имеющих стиль [**бтнс \_ SHOWTEXT**](toolbar-control-and-button-styles.md) . Для кнопок, у которых нет этого стиля, отображается подсказка, содержащая текст кнопки.
-   Ответьте на код уведомления [ТТН \_ жетдиспинфо](ttn-getdispinfo.md) .
-   Ответьте на код уведомления [ТБН \_ жетинфотип](tbn-getinfotip.md) .

Приложение, которому требуется отправить сообщения непосредственно в элемент управления ToolTip, может получить этот маркер в элементе управления с помощью сообщения [**TB \_**](tb-gettooltips.md) . Приложение может заменить элемент управления ToolTip панели инструментов другим элементом управления ToolTip с помощью сообщения [**\_ сеттултипс ТБ**](tb-settooltips.md) .

Самый гибкий способ предоставления текста подсказки — ответ на код уведомления [ТТН \_ Жетдиспинфо](ttn-getdispinfo.md) или [ТБН \_ жетинфотип](tbn-getinfotip.md) , отправленный элементом управления ToolBar на родительский элемент в форме сообщения [**WM \_ Notify**](wm-notify.md) . Для [ТТН \_ Жетдиспинфо](ttn-getdispinfo.md)параметр *lParam* включает указатель на структуру [**Нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (также определенную как **лптултиптекст**), которая указывает идентификатор команды для кнопки, для которой требуется текст справки. Этот идентификатор находится в элементе **нмттдиспинфо. HDR. идфром** . Приложение может скопировать текст справки в структуру, указать адрес строки, содержащей текст справки, или указать идентификатор ресурса строкового ресурса.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="display-a-tooltip-for-a-button"></a>Отображение всплывающей подсказки для кнопки

Следующий пример кода обрабатывает код уведомления подсказки [ТТН \_ жетдиспинфо](ttn-getdispinfo.md) , предоставляя текст из идентификаторов ресурсов.


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления ToolBar](using-toolbar-controls.md)
</dt> <dt>

[демонстрация Windows стандартных элементов управления (кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




