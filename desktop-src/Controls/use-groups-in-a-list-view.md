---
title: Использование групп в List-View
description: В этом разделе описывается создание экземпляра группы и его добавление в элемент управления "представление списка".
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec47d73c3e8b808eaf1909bdafb015c7eebc37de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103891249"
---
# <a name="how-to-use-groups-in-a-list-view"></a><span data-ttu-id="c0d50-103">Использование групп в List-View</span><span class="sxs-lookup"><span data-stu-id="c0d50-103">How to Use Groups in a List-View</span></span>

<span data-ttu-id="c0d50-104">В этом разделе описывается создание экземпляра группы и его добавление в элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="c0d50-104">This topic describes how to create an instance of a group and add it to a list-view control.</span></span> <span data-ttu-id="c0d50-105">Группирование позволяет пользователю упорядочивать списки по группам элементов, которые визуально разделены на странице, с помощью горизонтального разделителя и заголовка группы.</span><span class="sxs-lookup"><span data-stu-id="c0d50-105">Grouping allows a user to arrange lists into groups of items that are visually divided on the page, using a horizontal divider and a group title.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c0d50-106">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="c0d50-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c0d50-107">Технологии</span><span class="sxs-lookup"><span data-stu-id="c0d50-107">Technologies</span></span>

-   [<span data-ttu-id="c0d50-108">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="c0d50-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c0d50-109">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="c0d50-109">Prerequisites</span></span>

-   <span data-ttu-id="c0d50-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="c0d50-110">C/C++</span></span>
-   <span data-ttu-id="c0d50-111">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="c0d50-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c0d50-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="c0d50-112">Instructions</span></span>


<span data-ttu-id="c0d50-113">Чтобы использовать группы в элементе управления "представление списка", убедитесь, что элемент управления содержит стиль окна [**LVS \_ алигнтоп**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c0d50-113">To use groups in a list-view control, ensure that the control includes the [**LVS\_ALIGNTOP**](list-view-window-styles.md) window style.</span></span>

<span data-ttu-id="c0d50-114">При добавлении элемента в список его необходимо назначить группе, задав элемент **играупид** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) элемента в качестве значения элемента **играупид** структуры [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) в группах.</span><span class="sxs-lookup"><span data-stu-id="c0d50-114">When you add an item to the list, you assign it to a group by setting the **iGroupId** member of the item's [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the value of the **iGroupId** member of the groups's [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure.</span></span> <span data-ttu-id="c0d50-115">Элемент, не назначенный группе, не отображается в списке, если включено представление группы.</span><span class="sxs-lookup"><span data-stu-id="c0d50-115">An item that is not assigned to a group does not appear in the list when group view is enabled.</span></span> <span data-ttu-id="c0d50-116">Чтобы включить или отключить представление группы, используйте макрос [**\_ енаблеграупвиев ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) .</span><span class="sxs-lookup"><span data-stu-id="c0d50-116">To enable or disable group view, use the [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) macro.</span></span>

<span data-ttu-id="c0d50-117">В следующем примере показано, как создать группу с заголовком и добавить ее в элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="c0d50-117">The following example shows how to create a group with a header and add it to a list-view control.</span></span>


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a><span data-ttu-id="c0d50-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c0d50-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0d50-119">Справочник по элементу управления представления списка</span><span class="sxs-lookup"><span data-stu-id="c0d50-119">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="c0d50-120">Сведения об элементах управления List-View</span><span class="sxs-lookup"><span data-stu-id="c0d50-120">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="c0d50-121">Использование элементов управления List-View</span><span class="sxs-lookup"><span data-stu-id="c0d50-121">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




