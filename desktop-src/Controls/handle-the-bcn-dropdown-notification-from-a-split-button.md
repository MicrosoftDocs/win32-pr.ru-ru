---
title: Обработайте уведомления BCN_DROPDOWN из Сплитбуттонс
description: В этом разделе описывается один из возможных способов реагирования на \_ уведомление в раскрывающемся списке BCN в процедуре диалогового окна.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134678"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a>Как управлять \_ уведомлением из раскрывающегося списка BCN с помощью разворачивающейся кнопки

В этом разделе описывается один из возможных способов реагирования на уведомление в [ \_ раскрывающемся списке BCN](bcn-dropdown.md) в процедуре диалогового окна.

Приложение C++ получает клиентские координаты кнопки из заголовка уведомления и преобразует их в экранные координаты. Затем он создает всплывающее меню и отображает его в нижней части кнопки. Для упрощения примера сочетания клавиш не реализуются в меню.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a>Шаг 1. Дождитесь уведомления в *\_ раскрывающемся списке BCN* .


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a>Шаг 2. получение экранных координат кнопки.

Используйте функцию [**клиенттоскрин**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) для преобразования координат окна нижнего левого края кнопки в экранные координаты.


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a>Шаг 3. Создание меню и добавление элементов.

Для создания меню используйте функцию [**креатепопупмену**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) . Используйте функцию [**аппендмену**](/windows/desktop/menurc/u) для добавления элементов в меню. IDC \_ MENUCOMMAND1 и IDC \_ MENUCOMMAND2 — это определяемые приложением константы для команд меню.


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a>Шаг 4. Отображение меню.

Функция [**метод TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) отображает контекстное меню в указанном расположении и отслеживает выбор элементов в меню.


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a>Полный пример


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[\_Код уведомления для раскрывающегося списка BCN](bcn-dropdown.md)
</dt> <dt>

[О кнопках](about-buttons.md)
</dt> <dt>

[Справочник по элементу управления Button](bumper-button-button-control-reference.md)
</dt> <dt>

[Использование кнопок](using-buttons.md)
</dt> <dt>

[Кнопка](buttons.md)
</dt> </dl>

 

 