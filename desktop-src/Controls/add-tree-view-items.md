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
# <a name="how-to-add-tree-view-items"></a><span data-ttu-id="825af-103">Добавление Tree-View элементов</span><span class="sxs-lookup"><span data-stu-id="825af-103">How to Add Tree-View Items</span></span>

<span data-ttu-id="825af-104">Вы добавляете элемент в элемент управления "дерево", отправляя сообщение [**TVM \_ INSERTITEM**](tvm-insertitem.md) в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="825af-104">You add an item to a tree-view control by sending the [**TVM\_INSERTITEM**](tvm-insertitem.md) message to the control.</span></span> <span data-ttu-id="825af-105">Сообщение включает адрес структуры [**твинсертструкт**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , задавая родительский элемент, элемент, после которого вставляется новый элемент, и структуру [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , определяющую атрибуты элемента.</span><span class="sxs-lookup"><span data-stu-id="825af-105">The message includes the address of a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure, specifying the parent item, the item after which the new item is inserted, and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that defines the attributes of the item.</span></span> <span data-ttu-id="825af-106">Атрибуты включают метку элемента, его выбранные и невыбранные изображения, а также 32-разрядное значение, определяемое приложением.</span><span class="sxs-lookup"><span data-stu-id="825af-106">The attributes include the item's label, its selected and nonselected images, and a 32-bit application-defined value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="825af-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="825af-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="825af-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="825af-108">Technologies</span></span>

-   [<span data-ttu-id="825af-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="825af-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="825af-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="825af-110">Prerequisites</span></span>

-   <span data-ttu-id="825af-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="825af-111">C/C++</span></span>
-   <span data-ttu-id="825af-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="825af-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="825af-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="825af-113">Instructions</span></span>

### <a name="add-items-to-the-tree-view"></a><span data-ttu-id="825af-114">Добавление элементов в Tree-View</span><span class="sxs-lookup"><span data-stu-id="825af-114">Add Items to the Tree-View</span></span>

<span data-ttu-id="825af-115">В примере в этом разделе показано, как создать оглавление на основе сведений о заголовке документа, предоставленных в определяемом приложением массиве.</span><span class="sxs-lookup"><span data-stu-id="825af-115">The example in this section demonstrates how to create a table of contents based on document heading information that is provided in an application-defined array.</span></span> <span data-ttu-id="825af-116">Каждый элемент массива состоит из строки заголовка и целого числа, указывающего на уровень заголовка.</span><span class="sxs-lookup"><span data-stu-id="825af-116">Each array element consists of a heading string and an integer that indicates the heading level.</span></span> <span data-ttu-id="825af-117">Пример поддерживает три уровня заголовков (1, 2 и 3).</span><span class="sxs-lookup"><span data-stu-id="825af-117">The example supports three heading levels (1, 2, and 3).</span></span>

<span data-ttu-id="825af-118">Пример включает две функции.</span><span class="sxs-lookup"><span data-stu-id="825af-118">The example includes two functions.</span></span> <span data-ttu-id="825af-119">Первая функция извлекает каждый заголовок и сопутствующий уровень заголовка, а затем передает их второй функции.</span><span class="sxs-lookup"><span data-stu-id="825af-119">The first function extracts each heading and accompanying heading level and then passes them to the second function.</span></span>

<span data-ttu-id="825af-120">Вторая функция добавляет элемент в элемент управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="825af-120">The second function adds an item to a tree-view control.</span></span> <span data-ttu-id="825af-121">Он использует текст заголовка в качестве метки элемента и использует уровень заголовка для определения родительского элемента для нового элемента.</span><span class="sxs-lookup"><span data-stu-id="825af-121">It uses the heading text as the item's label, and it uses the heading level to determine the parent item for the new item.</span></span> <span data-ttu-id="825af-122">Заголовок первого уровня добавляется к корню элемента управления "дерево-представление", а заголовок уровня "два" добавляется в качестве дочернего элемента предыдущего уровня для одного элемента и т. д.</span><span class="sxs-lookup"><span data-stu-id="825af-122">A level one heading is added to the root of the tree-view control, a level two heading is added as a child item of the previous level one item, and so on.</span></span> <span data-ttu-id="825af-123">Функция назначает изображение элементу в зависимости от того, содержит ли он дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="825af-123">The function assigns an image to an item based on whether it has child items.</span></span> <span data-ttu-id="825af-124">Если элемент имеет дочерние элементы, он получает изображение, представляющее закрытую папку.</span><span class="sxs-lookup"><span data-stu-id="825af-124">If an item has child items, it gets an image that represents a closed folder.</span></span> <span data-ttu-id="825af-125">В противном случае он получает изображение, представляющее документ.</span><span class="sxs-lookup"><span data-stu-id="825af-125">Otherwise, it gets an image that represents a document.</span></span> <span data-ttu-id="825af-126">Элемент использует то же изображение для выбранных и невыбранных состояний.</span><span class="sxs-lookup"><span data-stu-id="825af-126">An item uses the same image for both the selected and nonselected states.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="825af-127">См. также</span><span class="sxs-lookup"><span data-stu-id="825af-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="825af-128">Использование элементов управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="825af-128">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="825af-129">Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="825af-129">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




