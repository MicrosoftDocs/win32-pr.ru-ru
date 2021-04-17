---
title: Использование элементов управления Virtual List-View
description: В этом разделе показано, как работать с виртуальными элементами управления "представление списка".
ms.assetid: DA32D7B3-5FDB-4D73-9A72-0D4EEB2A0C4F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3baf5e37d0d4f6da0cdf596dd8ba3c71e852a99
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "105656747"
---
# <a name="how-to-use-virtual-list-view-controls"></a><span data-ttu-id="63d68-103">Использование элементов управления Virtual List-View</span><span class="sxs-lookup"><span data-stu-id="63d68-103">How to Use Virtual List-View Controls</span></span>

<span data-ttu-id="63d68-104">В этом разделе показано, как работать с виртуальными элементами управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="63d68-104">This topic demonstrates how to work with virtual list-view controls.</span></span> <span data-ttu-id="63d68-105">В прилагаемых примерах кода C++ показано, как обрабатывать сообщения уведомления элементов управления виртуального списка, как оптимизировать кэш и как получить элемент из кэша.</span><span class="sxs-lookup"><span data-stu-id="63d68-105">The accompanying C++ code examples show how to process virtual list-view control notification messages, how to optimize the cache, and how to retrieve an item from the cache.</span></span>

-   [<span data-ttu-id="63d68-106">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="63d68-106">What you need to know</span></span>](#what-you-need-to-know)
-   [<span data-ttu-id="63d68-107">Обработка кодов уведомлений управления виртуальными List-Viewми</span><span class="sxs-lookup"><span data-stu-id="63d68-107">Process Virtual List-View Control Notification Codes</span></span>](#process-virtual-list-view-control-notification-codes)
-   [<span data-ttu-id="63d68-108">Оптимизация кэша</span><span class="sxs-lookup"><span data-stu-id="63d68-108">Optimize the Cache</span></span>](#optimize-the-cache)
-   [<span data-ttu-id="63d68-109">Получение элемента из кэша</span><span class="sxs-lookup"><span data-stu-id="63d68-109">Retrieve an Item From the Cache</span></span>](#retrieve-an-item-from-the-cache)
-   [<span data-ttu-id="63d68-110">См. также</span><span class="sxs-lookup"><span data-stu-id="63d68-110">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="63d68-111">В примере кода в этом разделе предполагается, что кэш является динамически выделенным массивом определяемых приложением структур.</span><span class="sxs-lookup"><span data-stu-id="63d68-111">The example code in this section assumes that the cache is a dynamically allocated array of application-defined structures.</span></span> <span data-ttu-id="63d68-112">Структура определяется в следующем примере кода C++.</span><span class="sxs-lookup"><span data-stu-id="63d68-112">The structure is defined in the following C++ code example.</span></span>

 


```C++
struct RndItem
{
    int   iIcon;                 // Bitmap assigned to this item.
    UINT  state;                 // Item state value.
    TCHAR Title[BUFFER_SIZE];    // BUFFER_SIZE is a user-defined macro value.
    TCHAR SubText1[BUFFER_SIZE]; // Text for the label of the first sub-item.
    TCHAR SubText2[BUFFER_SIZE]; // Text for the label of the second item.
};

```



## <a name="what-you-need-to-know"></a><span data-ttu-id="63d68-113">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="63d68-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="63d68-114">Технологии</span><span class="sxs-lookup"><span data-stu-id="63d68-114">Technologies</span></span>

-   [<span data-ttu-id="63d68-115">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="63d68-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="63d68-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="63d68-116">Prerequisites</span></span>

-   <span data-ttu-id="63d68-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="63d68-117">C/C++</span></span>
-   <span data-ttu-id="63d68-118">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="63d68-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="63d68-119">Инструкции</span><span class="sxs-lookup"><span data-stu-id="63d68-119">Instructions</span></span>

### <a name="process-virtual-list-view-control-notification-codes"></a><span data-ttu-id="63d68-120">Обработка кодов уведомлений управления виртуальными List-Viewми</span><span class="sxs-lookup"><span data-stu-id="63d68-120">Process Virtual List-View Control Notification Codes</span></span>

<span data-ttu-id="63d68-121">В дополнение к кодам уведомлений, отправленным другими элементами управления "список", элементы управления "представление списка" могут также отправлять коды уведомлений [ЛВН \_ Одкачехинт](lvn-odcachehint.md) и [**ЛВН \_ одфиндитем**](lvn-odfinditem.md) .</span><span class="sxs-lookup"><span data-stu-id="63d68-121">In addition to the notification codes sent by other list-view controls, virtual list-view controls can also send the [LVN\_ODCACHEHINT](lvn-odcachehint.md) and [**LVN\_ODFINDITEM**](lvn-odfinditem.md) notification codes.</span></span>

<span data-ttu-id="63d68-122">Эта определяемая приложением функция обрабатывает сообщения уведомлений, которые обычно отправляются из виртуального элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="63d68-122">This application-defined function handles notification messages that are commonly sent from a virtual list-view control.</span></span>


```C++
LRESULT OnNotify(HWND hwnd, NMHDR* pnmhdr)
{
    HRESULT hr;
    LRESULT lrt = FALSE;

    switch (pnmhdr->code)
    {
    case LVN_GETDISPINFO:
        {
            RndItem rndItem;
            NMLVDISPINFO* plvdi = (NMLVDISPINFO*) pnmhdr;

            if (-1 == plvdi->item.iItem)
            {
                OutputDebugString(TEXT("LVOWNER: Request for -1 item?\n"));
                DebugBreak();
            }

            // Retrieve information for item at index iItem.
            RetrieveItem( &rndItem, plvdi->item.iItem );

            if(plvdi->item.mask & LVIF_STATE)
            {
                // Fill in the state information.
                plvdi->item.state |= rndItem.state;
            }

            if(plvdi->item.mask & LVIF_IMAGE)
            {
                // Fill in the image information.
                plvdi->item.iImage = rndItem.iIcon;
            }

            if(plvdi->item.mask & LVIF_TEXT)
            {
                // Fill in the text information.
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // Copy the main item text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.Title);

                    if(FAILED(hr))
                    { 
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                                
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated.
                    }
                    break;

                case 1:
                    // Copy SubItem1 text.
                    hr = StringCchCopy( plvdi->item.pszText, MAX_COUNT, rndItem.SubText1);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter               
                        // more characters than specified by MAX_COUNT or   
                        // the text will be truncated..
                    }
                    break;

                case 2:
                    // Copy SubItem2 text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.SubText2);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                    
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated..
                    }
                    break;

                default:
                    break;

                }

            }

            lrt = FALSE;
            break;
        }

    case LVN_ODCACHEHINT:
        {
            NMLVCACHEHINT* pcachehint = (NMLVCACHEHINT*) pnmhdr;

            // Load the cache with the recommended range.
            PrepCache( pcachehint->iFrom, pcachehint->iTo );
            break;
        }

    case LVN_ODFINDITEM:
        {
            LPNMLVFINDITEM pnmfi = NULL;
            
            pnmfi = (LPNMLVFINDITEM)pnmhdr;

            // Call a user-defined function that finds the index according to
            // LVFINDINFO (which is embedded in the LPNMLVFINDITEM structure).
            // If nothing is found, then set the return value to -1.

            break;
        }

    default:
        break;

    }       // End Switch block.

    return(lrt);
}
```



### <a name="optimize-the-cache"></a><span data-ttu-id="63d68-123">Оптимизация кэша</span><span class="sxs-lookup"><span data-stu-id="63d68-123">Optimize the Cache</span></span>

<span data-ttu-id="63d68-124">Виртуальный элемент управления "представление списка" отправляет сообщение уведомления [ЛВН \_ одкачехинт](lvn-odcachehint.md) , когда содержимое его области отображения изменилось.</span><span class="sxs-lookup"><span data-stu-id="63d68-124">A virtual list-view control sends a [LVN\_ODCACHEHINT](lvn-odcachehint.md) notification message when the contents of its display area have changed.</span></span> <span data-ttu-id="63d68-125">Сообщение содержит сведения о диапазоне элементов для кэширования.</span><span class="sxs-lookup"><span data-stu-id="63d68-125">The message contains information about the range of items to be cached.</span></span> <span data-ttu-id="63d68-126">После получения сообщения уведомления приложение должно быть готово к загрузке кэша со сведениями об элементе для запрошенного диапазона, чтобы информация была доступна при отправке сообщения уведомления [ЛВН \_ жетдиспинфо](lvn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="63d68-126">Upon receiving the notification message, your application must be prepared to load the cache with item information for the requested range so that the information will be readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification message is sent.</span></span>

<span data-ttu-id="63d68-127">В следующем примере кода C++ определяемая приложением функция принимает диапазон элементов для кэша, который отправляется виртуальным элементом управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="63d68-127">In the following C++ code example, the application-defined function accepts the range of items for the cache that is sent by a virtual list-view control.</span></span> <span data-ttu-id="63d68-128">Он выполняет проверку, чтобы определить, что запрошенный диапазон элементов еще не кэширован, а затем выделяет требуемую глобальную память и заполняет кэш при необходимости.</span><span class="sxs-lookup"><span data-stu-id="63d68-128">It performs a verification to determine that the requested range of items is not already cached, and then it allocates the required global memory and fills the cache if necessary.</span></span>


```C++
void PrepCache(int iFrom, int iTo)
{
    /*  Global Variables

     *  g_priCache[ ]: the main cache.
     *  g_iCache:      the index of the first item in the main cache.
     *  g_cCache:      the count of items in the main cache.
     *
     *  g_priEndCache[ ]: the cache of items at the end of the list.
     *  g_iEndCache:      the index of the first item in the end cache.
     *  g_cEndCache:      the count of items in the end cache.
     */
     
    // Local Variables
    int i;
    BOOL fOLFrom = FALSE;
    BOOL   fOLTo = FALSE;

    // Check to see if this is the end cache.
    if ((iTo == g_cCache - 1) && ((iTo - iFrom) < 30))  // 30 entries wide.
    {
        // Check to see if this is a portion of the current end cache.
        if ((g_cCache) && (iFrom >= g_iEndCache) && (iFrom < g_iEndCache+g_cEndCache))
            return;
            // If it is a part of current end cache, no loading is necessary.

        // This is a new end cache. Free the old memory.
        if ( g_priEndCache )
            GlobalFree( g_priEndCache );
            
        // Set the index and count values for the new end cache,
        // and then retrieve the memory.
        g_iEndCache   = iFrom;
        g_cEndCache   = (iTo - iFrom + 1);
        g_priEndCache = (RndItem *)GlobalAlloc(GPTR, sizeof(RndItem) * g_cEndCache);

        if (! g_priEndCache)
        {
            // TODO: Out of memory. Perform error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cEndCache; i++)
        {
            // TODO: Call a function that accesses item information and
            // fills a cache element.
        }
    }

    else
    {   
        // It is not a member of the current end cache.
        // Try the primary cache instead.

        // Check to see if iFrom is within the primary cache.
        if ((g_cCache) && (iFrom >= g_iCache) && (iFrom < g_iCache+g_cCache))
            fOLFrom = TRUE;

        // Check to see if iTo is within the primary cache.
        if ((g_cCache) && (iTo >= g_iCache) && (iTo <= g_iCache+g_cCache))
            fOLTo = TRUE;

        // do nothing if both iFrom and iTo are within the current cache.

        if (fOLFrom && fOLTo)
            return;

        // Enlarge the cache size rather than make it specific to this hint.
        if (fOLFrom)
            iFrom = g_iCache;

        else if (fOLTo)
            iTo = g_iCache + g_cCache;

        // A new primary cache is needed. Free the old primary cache.
        if ( g_priCache )
            GlobalFree( g_priCache );

        // Set the index and count values for the new primary cache,
        // and then retrieve the memory.
        g_iCache   = iFrom;
        g_cCache   = (iTo - iFrom + 1);
        g_priCache = (RndItem *)GlobalAlloc( GPTR, sizeof( RndItem ) * g_cCache );

        if (!g_priCache)
        {
            // TODO: Out of memory. Do error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cCache; i++)
        {
            // TODO: Call a function that accesses item information
            // and fills a cache element.
        }
    }
}
```



### <a name="retrieve-an-item-from-the-cache"></a><span data-ttu-id="63d68-129">Получение элемента из кэша</span><span class="sxs-lookup"><span data-stu-id="63d68-129">Retrieve an Item From the Cache</span></span>

<span data-ttu-id="63d68-130">Этот пример функции принимает два параметра: адрес структуры, определяемой приложением, и целочисленное значение, представляющее индекс элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="63d68-130">This example function accepts two parameters, the address of the application-defined structure and an integer value representing the index of the item in the list.</span></span> <span data-ttu-id="63d68-131">Он проверяет значение индекса, чтобы определить, кэшируется ли нужный элемент.</span><span class="sxs-lookup"><span data-stu-id="63d68-131">It checks the index value to discover if the desired item is cached.</span></span> <span data-ttu-id="63d68-132">Если это так, то указатель, переданный в функцию, устанавливается в расположение в кэше.</span><span class="sxs-lookup"><span data-stu-id="63d68-132">If it is, the pointer that was passed to the function is set to a location in the cache.</span></span> <span data-ttu-id="63d68-133">Если элемент не находится в основном или конечном кэше, сведения об элементе необходимо найти вручную.</span><span class="sxs-lookup"><span data-stu-id="63d68-133">If the item is not in the main or end cache, the item information must be located manually.</span></span>


```C++
void RetrieveItem( RndItem * prndItem, int index )
{
    // Global Variables

    // g_priCache[ ]: the main cache.
    // g_iCache:      the index of the first item in the main cache.
    // c_cCache:      the count of items in the main cache.
    //
    // g_priEndCache[ ]:  the cache of items at the end of the list.
    // g_iEndCache:       the index of the first item in the end cache.
    // g_cEndCache:       the count of items in the end cache.
    //

    // Check to see if the item is in the main cache.
    if ((index >= g_iCache) && (index < g_iCache + g_cCache))
        *prndItem = g_priCache[index-g_iCache];

    // If it is not in the main cache, then check to see if
    // the item is in the end area cache.
    else if ((index >= g_iEndCache) && (index < g_iEndCache + g_cEndCache))
        *prndItem = g_priEndCache[index-g_iEndCache];

    else
    {
        // The item is not in either cache.
        // Therefore, retrieve the item information manually.
    }
}
```



## <a name="remarks"></a><span data-ttu-id="63d68-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63d68-134">Remarks</span></span>

<span data-ttu-id="63d68-135">Список оконных сообщений, обрабатываемых элементом управления "представление списка", см. в разделе [Обработка сообщений по умолчанию List-View](listview-message-processing.md).</span><span class="sxs-lookup"><span data-stu-id="63d68-135">For a list of the window messages processed by a list-view control, see [Default List-View Message Processing](listview-message-processing.md).</span></span>

## <a name="complete-example"></a><span data-ttu-id="63d68-136">Полный пример</span><span class="sxs-lookup"><span data-stu-id="63d68-136">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="63d68-137">См. также</span><span class="sxs-lookup"><span data-stu-id="63d68-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63d68-138">Справочник по элементу управления представления списка</span><span class="sxs-lookup"><span data-stu-id="63d68-138">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="63d68-139">Сведения об элементах управления List-View</span><span class="sxs-lookup"><span data-stu-id="63d68-139">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="63d68-140">Использование элементов управления List-View</span><span class="sxs-lookup"><span data-stu-id="63d68-140">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




