---
title: Добавление List-View элементов и подэлементов
description: В этом разделе показано, как добавлять элементы и подэлементы в элемент управления "представление списка".
ms.assetid: B7E204DC-FD08-4639-985D-1459A1AC0ED6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b3d20008edc10fda810261427507c77e9cfe34
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104134799"
---
# <a name="how-to-add-list-view-items-and-subitems"></a><span data-ttu-id="4aeb4-103">Добавление List-View элементов и подэлементов</span><span class="sxs-lookup"><span data-stu-id="4aeb4-103">How to Add List-View Items and Subitems</span></span>

<span data-ttu-id="4aeb4-104">В этом разделе показано, как добавлять элементы и подэлементы в элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="4aeb4-104">This topic demonstrates how to add items and subitems to a list-view control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4aeb4-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="4aeb4-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4aeb4-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="4aeb4-106">Technologies</span></span>

-   [<span data-ttu-id="4aeb4-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="4aeb4-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4aeb4-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="4aeb4-108">Prerequisites</span></span>

-   <span data-ttu-id="4aeb4-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="4aeb4-109">C/C++</span></span>
-   <span data-ttu-id="4aeb4-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="4aeb4-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4aeb4-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="4aeb4-111">Instructions</span></span>


<span data-ttu-id="4aeb4-112">Чтобы добавить элемент в элемент управления "представление списка", приложение должно сначала определить структуру [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , а затем отправить сообщение [**\_ INSERTITEM LVM**](lvm-insertitem.md) , указав адрес структуры **лвитем** .</span><span class="sxs-lookup"><span data-stu-id="4aeb4-112">To add an item to a list-view control, an application must first define an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure and then send an [**LVM\_INSERTITEM**](lvm-insertitem.md) message, specifying the address of the **LVITEM** structure.</span></span> <span data-ttu-id="4aeb4-113">Если приложение использует представление отчетов, необходимо указать текст подэлемента.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-113">If an application uses report view, subitem text must be provided.</span></span>

<span data-ttu-id="4aeb4-114">Следующий пример кода C++ заполняет структуру [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) и добавляет элементы представления списка с помощью сообщения [**LVM \_ INSERTITEM**](lvm-insertitem.md) или соответствующего макроса [**\_ INSERTITEM ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem).</span><span class="sxs-lookup"><span data-stu-id="4aeb4-114">The following C++ code example fills an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure and adds the list-view items by using the [**LVM\_INSERTITEM**](lvm-insertitem.md) message or the corresponding macro [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem).</span></span> <span data-ttu-id="4aeb4-115">Так как приложение сохраняет собственный текст, оно указывает \_ значение LPSTR тексткаллбакк для элемента **Псзтекст** структуры **лвитем** .</span><span class="sxs-lookup"><span data-stu-id="4aeb4-115">Because the application saves its own text, it specifies the LPSTR\_TEXTCALLBACK value for the **pszText** member of the **LVITEM** structure.</span></span> <span data-ttu-id="4aeb4-116">Указание \_ значения ТЕКСТКАЛЛБАКК LPSTR приводит к тому, что элемент управления отправляет код уведомления [**\_ жетдиспинфо ЛВН**](lvn-getdispinfo.md) в окно своего владельца каждый раз, когда ему требуется отобразить элемент.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-116">Specifying the LPSTR\_TEXTCALLBACK value causes the control to send an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code to its owner window whenever it needs to display an item.</span></span>


```C++
// InsertListViewItems: Inserts items into a list view. 
// hWndListView:        Handle to the list-view control.
// cItems:              Number of items to insert.
// Returns TRUE if successful, and FALSE otherwise.
BOOL InsertListViewItems(HWND hWndListView, int cItems)
{
    LVITEM lvI;

    // Initialize LVITEM members that are common to all items.
    lvI.pszText   = LPSTR_TEXTCALLBACK; // Sends an LVN_GETDISPINFO message.
    lvI.mask      = LVIF_TEXT | LVIF_IMAGE |LVIF_STATE;
    lvI.stateMask = 0;
    lvI.iSubItem  = 0;
    lvI.state     = 0;

    // Initialize LVITEM members that are different for each item.
    for (int index = 0; index < cItems; index++)
    {
        lvI.iItem  = index;
        lvI.iImage = index;
    
        // Insert items into the list.
        if (ListView_InsertItem(hWndListView, &lvI) == -1)
            return FALSE;
    }

    return TRUE;
}

// HandleWM_NOTIFY - Handles the LVN_GETDISPINFO notification code that is 
//         sent in a WM_NOTIFY to the list view parent window. The function 
//        provides display strings for list view items and subitems.
//
// lParam - The LPARAM parameter passed with the WM_NOTIFY message.
// rgPetInfo - A global array of structures, defined as follows:
//         struct PETINFO
//        {
//            TCHAR szKind[10];
//            TCHAR szBreed[50];
//            TCHAR szPrice[20];
//        };
//
//        PETINFO rgPetInfo[ ] = 
//        {
//            {TEXT("Dog"),  TEXT("Poodle"),     TEXT("$300.00")},
//            {TEXT("Cat"),  TEXT("Siamese"),    TEXT("$100.00")},
//            {TEXT("Fish"), TEXT("Angel Fish"), TEXT("$10.00")},
//            {TEXT("Bird"), TEXT("Parakeet"),   TEXT("$5.00")},
//            {TEXT("Toad"), TEXT("Woodhouse"),  TEXT("$0.25")},
//        };
//
void HandleWM_NOTIFY(LPARAM lParam)
{
    NMLVDISPINFO* plvdi;

    switch (((LPNMHDR) lParam)->code)
    {
        case LVN_GETDISPINFO:

            plvdi = (NMLVDISPINFO*)lParam;

            switch (plvdi->item.iSubItem)
            {
                case 0:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szKind;
                    break;
                      
                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;
                
                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;
                
                default:
                    break;
            }

        break;

    }
    // NOTE: In addition to setting pszText to point to the item text, you could 
    // copy the item text into pszText using StringCchCopy. For example:
    //
    // StringCchCopy(plvdi->item.pszText, 
    //                         plvdi->item.cchTextMax, 
    //                         rgPetInfo[plvdi->item.iItem].szKind);

    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="4aeb4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="4aeb4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aeb4-118">Справочник по элементу управления представления списка</span><span class="sxs-lookup"><span data-stu-id="4aeb4-118">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="4aeb4-119">Сведения об элементах управления List-View</span><span class="sxs-lookup"><span data-stu-id="4aeb4-119">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="4aeb4-120">Использование элементов управления List-View</span><span class="sxs-lookup"><span data-stu-id="4aeb4-120">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




