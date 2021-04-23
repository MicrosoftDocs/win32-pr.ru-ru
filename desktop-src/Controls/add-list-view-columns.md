---
title: Добавление List-View столбцов
description: В этом разделе показано, как добавить столбцы в элемент управления "представление списка".
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e478c57a31fdd7ad91e0089106e93c24c47d5c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070873"
---
# <a name="how-to-add-list-view-columns"></a><span data-ttu-id="e40bd-103">Добавление List-View столбцов</span><span class="sxs-lookup"><span data-stu-id="e40bd-103">How to Add List-View Columns</span></span>

<span data-ttu-id="e40bd-104">В этом разделе показано, как добавить столбцы в элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="e40bd-104">This topic demonstrates how to add columns to a list-view control.</span></span> <span data-ttu-id="e40bd-105">Столбцы используются для отображения элементов и подэлементов, если элемент управления "представление списка" находится в представлении "отчет (сведения)".</span><span class="sxs-lookup"><span data-stu-id="e40bd-105">Columns are used to display the items and subitems when a list-view control is in report (details) view.</span></span> <span data-ttu-id="e40bd-106">Текст из выбранных столбцов также может отображаться в мозаичном представлении.</span><span class="sxs-lookup"><span data-stu-id="e40bd-106">Text from selected columns can also be displayed in tile view.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e40bd-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="e40bd-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e40bd-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="e40bd-108">Technologies</span></span>

-   [<span data-ttu-id="e40bd-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="e40bd-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e40bd-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e40bd-110">Prerequisites</span></span>

-   <span data-ttu-id="e40bd-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="e40bd-111">C/C++</span></span>
-   <span data-ttu-id="e40bd-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="e40bd-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e40bd-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="e40bd-113">Instructions</span></span>


<span data-ttu-id="e40bd-114">Чтобы добавить столбец в элемент управления "представление списка", отправьте сообщение [**LVM \_ инсертколумн**](lvm-insertcolumn.md) или используйте макрос [**\_ инсертколумн ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .</span><span class="sxs-lookup"><span data-stu-id="e40bd-114">To add a column to a list-view control, send the [**LVM\_INSERTCOLUMN**](lvm-insertcolumn.md) message or use the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span> <span data-ttu-id="e40bd-115">Чтобы удалить столбец, используйте сообщение [**LVM \_ делетеколумн**](lvm-deletecolumn.md) .</span><span class="sxs-lookup"><span data-stu-id="e40bd-115">To delete a column, use the [**LVM\_DELETECOLUMN**](lvm-deletecolumn.md) message.</span></span>

<span data-ttu-id="e40bd-116">Следующий пример кода C++ вызывает макрос [**ListView \_ инсертколумн**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) для добавления столбцов в элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="e40bd-116">The following C++ code example calls the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro to add columns to a list-view control.</span></span> <span data-ttu-id="e40bd-117">Заголовки столбцов определяются в файле заголовка приложения как строковые ресурсы, которые нумеруются последовательно, начиная с ИДЕНТИФИКАТОРов \_ фирстколумн.</span><span class="sxs-lookup"><span data-stu-id="e40bd-117">The column headings are defined in the application's header file as string resources, which are numbered consecutively starting with IDS\_FIRSTCOLUMN.</span></span> <span data-ttu-id="e40bd-118">Число столбцов определяется в файле заголовка как **\_ столбцы C**.</span><span class="sxs-lookup"><span data-stu-id="e40bd-118">The number of columns is defined in the header file as **C\_COLUMNS**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e40bd-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e40bd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e40bd-120">Справочник по элементу управления представления списка</span><span class="sxs-lookup"><span data-stu-id="e40bd-120">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e40bd-121">Сведения об элементах управления List-View</span><span class="sxs-lookup"><span data-stu-id="e40bd-121">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="e40bd-122">Использование элементов управления List-View</span><span class="sxs-lookup"><span data-stu-id="e40bd-122">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




