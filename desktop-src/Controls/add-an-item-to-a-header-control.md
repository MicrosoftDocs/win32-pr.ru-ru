---
title: Добавление элемента в элемент управления "заголовок"
description: В этом разделе показано, как добавить элемент в элемент управления "заголовок".
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988012"
---
# <a name="how-to-add-an-item-to-a-header-control"></a>Добавление элемента в элемент управления "заголовок"

В этом разделе показано, как добавить элемент в элемент управления "заголовок". Элемент управления "заголовок" обычно имеет несколько элементов заголовка, определяющих столбцы элемента управления. Вы можете добавить элемент в элемент управления "заголовок", отправив сообщение [**\_ INSERTITEM HDM**](hdm-insertitem.md) в элемент управления.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Используйте сообщение [**HDM \_ INSERTITEM**](hdm-insertitem.md) , чтобы добавить элемент в элемент управления "заголовок". Сообщение должно включать адрес структуры [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Эта структура определяет свойства элемента заголовка, которые могут включать строку, Растровое изображение, начальный размер и определяемое приложением 32-разрядное значение.

В следующем примере показано, как использовать сообщение [**\_ INSERTITEM HDM**](hdm-insertitem.md) и структуру [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) для добавления элемента в элемент управления заголовка. Новый элемент состоит из строки, выровненной по левому краю внутри прямоугольника элемента.



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Сведения об элементах управления "заголовок"](header-controls.md)
</dt> <dt>

[Справочник по элементу Header](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Использование элементов управления "заголовок"](using-header-controls.md)
</dt> </dl>

 

 




