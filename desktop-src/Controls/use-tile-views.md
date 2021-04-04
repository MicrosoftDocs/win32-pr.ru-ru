---
title: Использование мозаичных представлений
description: В этом разделе показано, как задать мозаичное представление для элемента управления "представление списка".
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103987999"
---
# <a name="how-to-use-tile-views"></a><span data-ttu-id="d13fc-103">Использование мозаичных представлений</span><span class="sxs-lookup"><span data-stu-id="d13fc-103">How to Use Tile Views</span></span>

<span data-ttu-id="d13fc-104">В этом разделе показано, как задать мозаичное представление для элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="d13fc-104">This topic demonstrates how to set the tile view for a list-view control.</span></span> <span data-ttu-id="d13fc-105">В мозаичном представлении каждый элемент представлен крупным значком с одной или несколькими строками сопроводительного текста.</span><span class="sxs-lookup"><span data-stu-id="d13fc-105">In tile view, each item is represented by a large icon with one or more lines of accompanying text.</span></span> <span data-ttu-id="d13fc-106">Иллюстрации см. в разделе [About List-View Controls](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d13fc-106">For an illustration, see [About List-View Controls](list-view-controls-overview.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d13fc-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="d13fc-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d13fc-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="d13fc-108">Technologies</span></span>

-   [<span data-ttu-id="d13fc-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="d13fc-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d13fc-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="d13fc-110">Prerequisites</span></span>

-   <span data-ttu-id="d13fc-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d13fc-111">C/C++</span></span>
-   <span data-ttu-id="d13fc-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="d13fc-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d13fc-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="d13fc-113">Instructions</span></span>


<span data-ttu-id="d13fc-114">Задайте общие параметры отображения для мозаичного представления с помощью макроса [**\_ сеттилевиевинфо ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) .</span><span class="sxs-lookup"><span data-stu-id="d13fc-114">Set the general display parameters for tile view by using the [**ListView\_SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) macro.</span></span> <span data-ttu-id="d13fc-115">Используйте структуру [**лвтилевиевинфо**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) , переданную в этот макрос, чтобы указать расположение текста относительно значка, размер каждой плитки (включая сопроводительный текст) и максимальное число строк текста.</span><span class="sxs-lookup"><span data-stu-id="d13fc-115">Use the [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) structure that is passed to this macro to specify the position of the text in relation to the icon, the size of each tile (including accompanying text), and the maximum number of lines of text.</span></span>

<span data-ttu-id="d13fc-116">Если вы не хотите, чтобы размеры плиток автоматически изменялись, необходимо задать **лвтвиф \_ FIXEDSIZE** в элементе **dwFlags** и **лвтвим \_ тилесизе** в **Двмаск лвтилевиевинфо** , [**а**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo)также предоставить измерения в элементе **сизетиле** .</span><span class="sxs-lookup"><span data-stu-id="d13fc-116">If you do not want tiles to be automatically sized, you must set **LVTVIF\_FIXEDSIZE** in the **dwFlags** member and **LVTVIM\_TILESIZE** in the **dwMask** member of [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), as well as providing the dimensions in the **sizeTile** member.</span></span>

<span data-ttu-id="d13fc-117">Следующий пример кода C++ устанавливает сведения о мозаичном представлении для элемента управления "представление списка", чтобы для каждого элемента отображалось не более двух подэлементов.</span><span class="sxs-lookup"><span data-stu-id="d13fc-117">The following C++ code example sets the tile view info for a list-view control so that a maximum of two subitems are displayed for each item.</span></span> <span data-ttu-id="d13fc-118">Он также задает размер каждой плитки.</span><span class="sxs-lookup"><span data-stu-id="d13fc-118">It also sets the size of each tile.</span></span>


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



<span data-ttu-id="d13fc-119">Для каждого элемента в списке можно задать дополнительные параметры при вставке элемента в список или позже.</span><span class="sxs-lookup"><span data-stu-id="d13fc-119">For each item in the list, you can set further parameters when the item is inserted in the list, or later.</span></span> <span data-ttu-id="d13fc-120">Структура [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , используемая с [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) , содержит члены, указывающие, какие столбцы данных должны отображаться под элементом, и их выравнивание.</span><span class="sxs-lookup"><span data-stu-id="d13fc-120">The [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that is used with [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contains members that specify which columns of data to display below the item, and their alignment.</span></span> <span data-ttu-id="d13fc-121">Эти же параметры вывода также находятся в структуре [**лвтилеинфо**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) , используемой с [**ListView \_ сеттилеинфо**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span><span class="sxs-lookup"><span data-stu-id="d13fc-121">These same display parameters are also found in the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure used with [**ListView\_SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span></span>

> [!Note]  
> <span data-ttu-id="d13fc-122">Здесь "Columns" означает не отображать столбцы в мозаичном представлении, а не подэлементы, отображаемые в столбцах в представлении сведений.</span><span class="sxs-lookup"><span data-stu-id="d13fc-122">"Columns" here refers not to display columns in tile view but rather to subitems, which are displayed in columns in details view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d13fc-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d13fc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d13fc-124">Справочник по элементу управления представления списка</span><span class="sxs-lookup"><span data-stu-id="d13fc-124">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d13fc-125">Сведения об элементах управления List-View</span><span class="sxs-lookup"><span data-stu-id="d13fc-125">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="d13fc-126">Использование элементов управления List-View</span><span class="sxs-lookup"><span data-stu-id="d13fc-126">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




