---
title: Добавление Tree-View элементов
description: Вы добавляете элемент в элемент управления "дерево", отправляя \_ сообщение TVM INSERTITEM в элемент управления.
ms.assetid: CD6376F4-8B1A-489D-8538-6C1620E98F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7da0846b57f422de83984b197df0770286882
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412579"
---
# <a name="how-to-add-tree-view-items"></a>Добавление Tree-View элементов

Вы добавляете элемент в элемент управления "дерево", отправляя сообщение [**TVM \_ INSERTITEM**](tvm-insertitem.md) в элемент управления. Сообщение включает адрес структуры [**твинсертструкт**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , задавая родительский элемент, элемент, после которого вставляется новый элемент, и структуру [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , определяющую атрибуты элемента. Атрибуты включают метку элемента, его выбранные и невыбранные изображения, а также 32-разрядное значение, определяемое приложением.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="add-items-to-the-tree-view"></a>Добавление элементов в Tree-View

В примере в этом разделе показано, как создать оглавление на основе сведений о заголовке документа, предоставленных в определяемом приложением массиве. Каждый элемент массива состоит из строки заголовка и целого числа, указывающего на уровень заголовка. Пример поддерживает три уровня заголовков (1, 2 и 3).

Пример включает две функции. Первая функция извлекает каждый заголовок и сопутствующий уровень заголовка, а затем передает их второй функции.

Вторая функция добавляет элемент в элемент управления "дерево-представление". Он использует текст заголовка в качестве метки элемента и использует уровень заголовка для определения родительского элемента для нового элемента. Заголовок первого уровня добавляется к корню элемента управления "дерево-представление", а заголовок уровня "два" добавляется в качестве дочернего элемента предыдущего уровня для одного элемента и т. д. Функция назначает изображение элементу в зависимости от того, содержит ли он дочерние элементы. Если элемент имеет дочерние элементы, он получает изображение, представляющее закрытую папку. В противном случае он получает изображение, представляющее документ. Элемент использует то же изображение для выбранных и невыбранных состояний.


```C++
// Adds items to a tree-view control. 
// Returns the handle to the newly added item. 
// hwndTV - handle to the tree-view control. 
// lpszItem - text of the item to add. 
// nLevel - level at which to add the item. 
//
// g_nClosed, and g_nDocument - global indexes of the images.

HTREEITEM AddItemToTree(HWND hwndTV, LPTSTR lpszItem, int nLevel)
{ 
    TVITEM tvi; 
    TVINSERTSTRUCT tvins; 
    static HTREEITEM hPrev = (HTREEITEM)TVI_FIRST; 
    static HTREEITEM hPrevRootItem = NULL; 
    static HTREEITEM hPrevLev2Item = NULL; 
    HTREEITEM hti; 

    tvi.mask = TVIF_TEXT | TVIF_IMAGE 
               | TVIF_SELECTEDIMAGE | TVIF_PARAM; 

    // Set the text of the item. 
    tvi.pszText = lpszItem; 
    tvi.cchTextMax = sizeof(tvi.pszText)/sizeof(tvi.pszText[0]); 

    // Assume the item is not a parent item, so give it a 
    // document image. 
    tvi.iImage = g_nDocument; 
    tvi.iSelectedImage = g_nDocument; 

    // Save the heading level in the item's application-defined 
    // data area. 
    tvi.lParam = (LPARAM)nLevel; 
    tvins.item = tvi; 
    tvins.hInsertAfter = hPrev; 

    // Set the parent item based on the specified level. 
    if (nLevel == 1) 
        tvins.hParent = TVI_ROOT; 
    else if (nLevel == 2) 
        tvins.hParent = hPrevRootItem; 
    else 
        tvins.hParent = hPrevLev2Item; 

    // Add the item to the tree-view control. 
    hPrev = (HTREEITEM)SendMessage(hwndTV, TVM_INSERTITEM, 
        0, (LPARAM)(LPTVINSERTSTRUCT)&tvins); 

    if (hPrev == NULL)
        return NULL;

    // Save the handle to the item. 
    if (nLevel == 1) 
        hPrevRootItem = hPrev; 
    else if (nLevel == 2) 
        hPrevLev2Item = hPrev; 

    // The new item is a child item. Give the parent item a 
    // closed folder bitmap to indicate it now has child items. 
    if (nLevel > 1)
    { 
        hti = TreeView_GetParent(hwndTV, hPrev); 
        tvi.mask = TVIF_IMAGE | TVIF_SELECTEDIMAGE; 
        tvi.hItem = hti; 
        tvi.iImage = g_nClosed; 
        tvi.iSelectedImage = g_nClosed; 
        TreeView_SetItem(hwndTV, &tvi); 
    } 

    return hPrev; 
} 

// Extracts heading text and heading levels from a global 
// array and passes them to a function that adds them as
// parent and child items to a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 

BOOL InitTreeViewItems(HWND hwndTV)
{ 
    HTREEITEM hti;

    // g_rgDocHeadings is an application-defined global array of 
    // the following structures: 
    //     typedef struct 
    //       { 
    //         TCHAR tchHeading[MAX_HEADING_LEN]; 
    //         int tchLevel; 
    //     } Heading; 
    for (int i = 0; i < ARRAYSIZE(g_rgDocHeadings); i++) 
    { 
        // Add the item to the tree-view control. 
        hti = AddItemToTree(hwndTV, g_rgDocHeadings[i].tchHeading, 
            g_rgDocHeadings[i].tchLevel); 

        if (hti == NULL)
            return FALSE;
    } 
           
    return TRUE; 
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления Tree-View](using-treeview.md)
</dt> <dt>

[Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




