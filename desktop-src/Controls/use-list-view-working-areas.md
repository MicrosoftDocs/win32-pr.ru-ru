---
title: Использование List-View рабочих областей
description: В этом разделе показано, как работать с рабочими областями в представлении списка. Рабочие области представляют собой прямоугольные виртуальные области, которые можно использовать для упорядочения элементов в элементе управления List-представление.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067806"
---
# <a name="how-to-use-list-view-working-areas"></a><span data-ttu-id="7c8b2-104">Использование List-View рабочих областей</span><span class="sxs-lookup"><span data-stu-id="7c8b2-104">How to Use List-View Working Areas</span></span>

<span data-ttu-id="7c8b2-105">В этом разделе показано, как работать с рабочими областями в представлении списка.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-105">This topic demonstrates how to work with list-view working areas.</span></span> <span data-ttu-id="7c8b2-106">Рабочие области представляют собой прямоугольные виртуальные области, которые можно использовать для упорядочения элементов в элементе управления List-представление.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-106">Working areas are rectangular virtual areas that can be used to arrange items in a list-vew control.</span></span> <span data-ttu-id="7c8b2-107">Рабочая область не является окном и не может иметь видимую границу.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-107">A working area is not a window and cannot have a visible border.</span></span> <span data-ttu-id="7c8b2-108">По умолчанию элемент управления "представление списка" не имеет рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-108">By default, the list-view control has no working areas.</span></span> <span data-ttu-id="7c8b2-109">Создавая рабочую область, можно создать пустую границу слева, сверху или справа от элементов или вызвать горизонтальную полосу прокрутки, если обычно это не будет.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-109">By creating a working area, you can create an empty border on the left, top, or right of the items or cause a horizontal scroll bar to be displayed when there normally would not be one.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7c8b2-110">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="7c8b2-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7c8b2-111">Технологии</span><span class="sxs-lookup"><span data-stu-id="7c8b2-111">Technologies</span></span>

-   [<span data-ttu-id="7c8b2-112">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="7c8b2-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7c8b2-113">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7c8b2-113">Prerequisites</span></span>

-   <span data-ttu-id="7c8b2-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="7c8b2-114">C/C++</span></span>
-   <span data-ttu-id="7c8b2-115">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="7c8b2-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7c8b2-116">Инструкции</span><span class="sxs-lookup"><span data-stu-id="7c8b2-116">Instructions</span></span>

### <a name="create-a-working-area"></a><span data-ttu-id="7c8b2-117">Создание рабочей области</span><span class="sxs-lookup"><span data-stu-id="7c8b2-117">Create a Working Area</span></span>

<span data-ttu-id="7c8b2-118">В следующем примере кода C++ показано, как создать рабочую область с пустой границей размером 25 пикселей в верхней, левой и правой частях.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-118">The following C++ code example demonstrates how to create a working area with a 25-pixel empty border on its top, left, and right sides.</span></span>


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a><span data-ttu-id="7c8b2-119">Создание нескольких рабочих областей</span><span class="sxs-lookup"><span data-stu-id="7c8b2-119">Create Multiple Working Areas</span></span>

<span data-ttu-id="7c8b2-120">В следующем примере кода C++ показано, как создать две рабочие области в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-120">The following C++ code example demonstrates how to create two working areas in a control.</span></span> <span data-ttu-id="7c8b2-121">Каждая Рабочая область использует около половины клиентской области и окружена пустой границей размером в 25 пикселей.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-121">Each working area uses about half of the client area, and is surrounded by a 25-pixel empty border.</span></span>


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a><span data-ttu-id="7c8b2-122">Определение рабочей области, к которой принадлежит элемент</span><span class="sxs-lookup"><span data-stu-id="7c8b2-122">Determine the Working Area to Which an Item Belongs</span></span>

<span data-ttu-id="7c8b2-123">Одним из способов определения рабочей области, к которой принадлежит элемент, является выполнение следующих действий.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-123">One way to determine which working area an item belongs is to do the following:</span></span>

-   <span data-ttu-id="7c8b2-124">Получение списка координат всех рабочих областей в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="7c8b2-124">Retrieve the list of coordinates of all of the working areas in the list-view control.</span></span>
-   <span data-ttu-id="7c8b2-125">Получение координат элемента.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-125">Retrieve the coordinates of the item.</span></span>
-   <span data-ttu-id="7c8b2-126">Определите, находятся ли координаты элемента в координатах одной из рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-126">Determine whether the item coordinates lie within the coordinates of one of the working areas.</span></span>

<span data-ttu-id="7c8b2-127">Определяемая приложением функция в следующем примере кода C++ возвращает индекс рабочей области, к которой принадлежит элемент.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-127">The application-defined function in the following C++ code example returns the index of the working area to which the item belongs.</span></span> <span data-ttu-id="7c8b2-128">Если функция завершается с ошибкой, возвращается значение – 1.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-128">If the function fails, it returns –1.</span></span> <span data-ttu-id="7c8b2-129">Если функция завершается с ошибкой, но элемент не входит в рабочие области, функция возвращает 0, так как все элементы, которые находятся вне рабочей области, автоматически становятся членами нулевой области.</span><span class="sxs-lookup"><span data-stu-id="7c8b2-129">If the function succeeds, but the item is not inside any of the working areas, the function returns 0, because all items that are not inside a working area automatically become a member of working area zero.</span></span>


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a><span data-ttu-id="7c8b2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="7c8b2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c8b2-131">Справочник по элементу управления представления списка</span><span class="sxs-lookup"><span data-stu-id="7c8b2-131">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7c8b2-132">Сведения об элементах управления List-View</span><span class="sxs-lookup"><span data-stu-id="7c8b2-132">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="7c8b2-133">Использование элементов управления List-View</span><span class="sxs-lookup"><span data-stu-id="7c8b2-133">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




