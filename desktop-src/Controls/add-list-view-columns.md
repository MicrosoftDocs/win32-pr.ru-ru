---
title: Добавление List-View столбцов
description: В этом разделе показано, как добавить столбцы в элемент управления "представление списка".
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee71065729502410d189493527af0e3e37663a4a2aaf541852454af7fa4a5aac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922084"
---
# <a name="how-to-add-list-view-columns"></a>Добавление List-View столбцов

В этом разделе показано, как добавить столбцы в элемент управления "представление списка". Столбцы используются для отображения элементов и подэлементов, если элемент управления "представление списка" находится в представлении "отчет (сведения)". Текст из выбранных столбцов также может отображаться в мозаичном представлении.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Чтобы добавить столбец в элемент управления "представление списка", отправьте сообщение [**LVM \_ инсертколумн**](lvm-insertcolumn.md) или используйте макрос [**\_ инсертколумн ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) . Чтобы удалить столбец, используйте сообщение [**LVM \_ делетеколумн**](lvm-deletecolumn.md) .

Следующий пример кода C++ вызывает макрос [**ListView \_ инсертколумн**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) для добавления столбцов в элемент управления "представление списка". Заголовки столбцов определяются в файле заголовка приложения как строковые ресурсы, которые нумеруются последовательно, начиная с ИДЕНТИФИКАТОРов \_ фирстколумн. Число столбцов определяется в файле заголовка как **\_ столбцы C**.


```C++
// InitListViewColumns: Adds columns to a list-view control.
// hWndListView:        Handle to the list-view control. 
// Returns TRUE if successful, and FALSE otherwise. 
BOOL InitListViewColumns(HWND hWndListView) 
{ 
    WCHAR szText[256];     // Temporary buffer.
    LVCOLUMN lvc;
    int iCol;

    // Initialize the LVCOLUMN structure.
    // The mask specifies that the format, width, text,
    // and subitem members of the structure are valid.
    lvc.mask = LVCF_FMT | LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM;

    // Add the columns.
    for (iCol = 0; iCol < C_COLUMNS; iCol++)
    {
        lvc.iSubItem = iCol;
        lvc.pszText = szText;
        lvc.cx = 100;               // Width of column in pixels.

        if ( iCol < 2 )
            lvc.fmt = LVCFMT_LEFT;  // Left-aligned column.
        else
            lvc.fmt = LVCFMT_RIGHT; // Right-aligned column.

        // Load the names of the column headings from the string resources.
        LoadString(g_hInst,
                   IDS_FIRSTCOLUMN + iCol,
                   szText,
                   sizeof(szText)/sizeof(szText[0]));

        // Insert the columns into the list view.
        if (ListView_InsertColumn(hWndListView, iCol, &lvc) == -1)
            return FALSE;
    }
    
    return TRUE;
} 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по элементу управления представления списка](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Сведения об элементах управления List-View](list-view-controls-overview.md)
</dt> <dt>

[Использование элементов управления List-View](using-list-view-controls.md)
</dt> </dl>

 

 




