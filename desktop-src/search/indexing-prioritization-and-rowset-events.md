---
description: Описание появления определения приоритетов индексирования и событий набора строк для Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Определение приоритетов индексирования и событий набора строк в Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6610500a3c2fcd359f346e5239507fb15ad896d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105674523"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a><span data-ttu-id="4d0e5-103">Определение приоритетов индексирования и событий набора строк в Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d0e5-103">Indexing Prioritization and Rowset Events in Windows 7</span></span>

<span data-ttu-id="4d0e5-104">В этом разделе описаны общие сведения о приоритетах индексирования и событиях набора строк для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-104">This topic outlines the introduction of indexing prioritization and rowset events for Windows 7.</span></span>

<span data-ttu-id="4d0e5-105">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4d0e5-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="4d0e5-106">Определение приоритетов индексирования и события набора строк</span><span class="sxs-lookup"><span data-stu-id="4d0e5-106">Indexing Prioritization and Rowset Events</span></span>](#indexing-prioritization-and-rowset-events)
    -   [<span data-ttu-id="4d0e5-107">Примеры Ировсетприоризатион</span><span class="sxs-lookup"><span data-stu-id="4d0e5-107">IRowsetPriorization Examples</span></span>](#irowsetpriorization-examples)
    -   [<span data-ttu-id="4d0e5-108">События Ировсетприоритизатион</span><span class="sxs-lookup"><span data-stu-id="4d0e5-108">IRowsetPrioritization Events</span></span>](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [<span data-ttu-id="4d0e5-109">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4d0e5-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="4d0e5-110">См. также</span><span class="sxs-lookup"><span data-stu-id="4d0e5-110">Related topics</span></span>](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a><span data-ttu-id="4d0e5-111">Определение приоритетов индексирования и события набора строк</span><span class="sxs-lookup"><span data-stu-id="4d0e5-111">Indexing Prioritization and Rowset Events</span></span>

<span data-ttu-id="4d0e5-112">В Windows 7 и более поздних версиях имеется стек приоритетов, в котором контекст любого конкретного запроса, клиент может запросить, чтобы области, используемые в этом запросе, были назначены по приоритету выше, чем обычные элементы.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-112">In Windows 7?and later, there is a priority stack within which the context of any particular query, the client can request that the scopes used in that query be prioritized above that of normal items.</span></span>

<span data-ttu-id="4d0e5-113">Этот стек приоритетов имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-113">This prioritization stack has the following characteristics:</span></span>

-   <span data-ttu-id="4d0e5-114">Элементы в стеке могут иметь передний план, высокий или низкий приоритет:</span><span class="sxs-lookup"><span data-stu-id="4d0e5-114">Items in the stack can have foreground, high, or low priority:</span></span>
    -   <span data-ttu-id="4d0e5-115">**Передний план**: логика отхода пропускается, и индексирование выполняется так же быстро, как это разрешено для компьютера.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-115">**Foreground**: Backoff logic is skipped and indexing proceeds as fast as the machine allows.</span></span>
    -   <span data-ttu-id="4d0e5-116">**Высокий**: приоритет был запрошен с помощью отхода.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-116">**High**: Prioritization has been requested with backoff.</span></span>
    -   <span data-ttu-id="4d0e5-117">**Низкий**: запрошено определение приоритетов, а не затраты на другие области в стеке, но выше индексирование без приоритизации.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-117">**Low**: Prioritization has been requested, not at the expense of other scopes on the stack, but above non-prioritized indexing.</span></span>
-   <span data-ttu-id="4d0e5-118">Любой запрос приоритета High или переднего плана перемещает запрос к верхней части стека автоматически.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-118">Any request for high or foreground priority bumps the requesting query to the top of the stack automatically.</span></span>
-   <span data-ttu-id="4d0e5-119">Приоритет переднего плана может иметь только элемент поверх стека.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-119">Only the item on top of the stack can have foreground priority.</span></span>
-   <span data-ttu-id="4d0e5-120">Запрос с приоритетом переднего плана, который передается по приоритету, получает событие с уведомлением о том, что он потерял приоритет переднего плана и стал высоким приоритетом с отходом.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-120">A query with foreground priority that is bumped down in priority receives an event notifying it that it has lost foreground priority and has become a high priority with backoff.</span></span>

<span data-ttu-id="4d0e5-121">В стеке приоритетов задается общий приоритет элементов, обрабатываемых в индексаторе следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4d0e5-121">The priority stack sets an overall priority of items that are processed in the indexer as follows:</span></span>

-   <span data-ttu-id="4d0e5-122">Уведомления с высоким приоритетом не обрабатываются и обычно отправляются только для небольшого числа элементов.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-122">High Priority notifications have no backoff, and are typically sent only for a small number of items.</span></span> <span data-ttu-id="4d0e5-123">Например, проводник Windows использует этот приоритет для малых операций с подсистемой копирования.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-123">For example, Windows Explorer uses this priority for small copy engine operations.</span></span>
-   <span data-ttu-id="4d0e5-124">Стек приоритетов находится на вершине стека, имеет откладывание и является последним запрошенным запросом приоритета.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-124">Priority Stack is top of the stack, has backoff, and is the last requested priority query.</span></span>
-   <span data-ttu-id="4d0e5-125">Второй запрос в стеке.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-125">Second query in the stack.</span></span>
-   <span data-ttu-id="4d0e5-126">Третий запрос в стеке.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-126">Third query in the stack.</span></span>
-   <span data-ttu-id="4d0e5-127">Четвертый запрос в стеке и т. д.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-127">Fourth query in the stack, and so forth.</span></span>
-   <span data-ttu-id="4d0e5-128">Элементы с нормальным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-128">Normal Priority items.</span></span>
-   <span data-ttu-id="4d0e5-129">Удаленные элементы.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-129">Deleted items.</span></span>
    > [!Note]  
    > <span data-ttu-id="4d0e5-130">Элементы внутри каждой группы задаются внутренне по приоритету с использованием старой семантики для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-130">Items within each group are prioritized internally through the older per-item semantics.</span></span>

     

### <a name="irowsetpriorization-examples"></a><span data-ttu-id="4d0e5-131">Примеры Ировсетприоризатион</span><span class="sxs-lookup"><span data-stu-id="4d0e5-131">IRowsetPriorization Examples</span></span>

<span data-ttu-id="4d0e5-132">Основной API для работы с приоритетами доступен через следующий интерфейс, который можно вызвать, выполнив запрос к возвращенному набору строк:</span><span class="sxs-lookup"><span data-stu-id="4d0e5-132">The primary API for prioritization work is available through the following interface, which can be called by querying the returned rowset:</span></span>


```
typedef [v1_enum] enum
{
    PRIORITY_LEVEL_FOREGROUND           = 0,    // process items in the scope first as quickly as possible
    PRIORITY_LEVEL_HIGH                 = 1,    // process items in the scope first at the normal rate
    PRIORITY_LEVEL_LOW                  = 2,    // process items in this scope before those at the normal rate, but after any other prioritization requests
    PRIORITY_LEVEL_DEFAULT              = 3     // process items at the normal indexer rate
} PRIORITY_LEVEL;


[
    object,
    uuid(IRowsetPrioritization_GUID),
    pointer_default(unique)
]
interface IRowsetPrioritization : IUnknown
{
    // Sets or retrieves the current indexer prioritization level for the scope specified by
    // this query.

    HRESULT SetScopePriority( [in] PRIORITY_LEVEL priority, [in] DWORD scopeStatisticsEventFrequency );
    HRESULT GetScopePriority( [out] PRIORITY_LEVEL * priority, [out] DWORD * scopeStatisticsEventFrequency );

    // Gets information describing the scope specified by this query:
    // indexedDocumentCount     -   The total number of documents currently indexed in the scope
    // oustandingAddCount       -   The total number of documents yet to be indexed in the scope (those not yet included in indexedDocumentCount)
    // oustandingModifyCount    -   The total number of documents indexed in the scope that need to be re-indexed (included in indexedDocumentCount)
    
    HRESULT GetScopeStatistics( [out] DWORD * indexedDocumentCount, [out] DWORD * oustandingAddCount, [out] DWORD * oustandingModifyCount );
};
```



<span data-ttu-id="4d0e5-133">Приоритеты наборов строк работают следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4d0e5-133">Rowset prioritization works as follows:</span></span>

1.  <span data-ttu-id="4d0e5-134">[**Ировсетприоритизатион**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) получен с помощью [метода IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в наборе строк индексатора.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) is acquired with [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an indexer rowset.</span></span> <span data-ttu-id="4d0e5-135">**DBPROP \_ Для ЕНАБЛЕРОВСЕТЕВЕНТС** необходимо задать значение **true** с помощью метода OLE DB [ICommandProperties:: SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) перед выполнением запроса, чтобы использовать определение приоритета набора строк.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-135">**DBPROP\_ENABLEROWSETEVENTS** must be set to **TRUE** with the OLE DB [ICommandProperties::SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) method prior to executing the query in order to use rowset prioritization.</span></span>
2.  <span data-ttu-id="4d0e5-136">[**Ировсетприоритизатион:: сетскопеприорити**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) задает приоритет для областей, принадлежащих запросу, и интервал, который вызывается событием статистики области при наличии необработанных документов для индексирования в областях запроса.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-136">[**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes.</span></span> <span data-ttu-id="4d0e5-137">Это событие возникает, если для уровня приоритета задано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-137">This event is raised if the priority level is set to default.</span></span>
3.  <span data-ttu-id="4d0e5-138">[**Ировсетприоритизатион:: жетскопестатистикс**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) можно использовать для получения количества индексированных элементов в области, количества необработанных документов, которые необходимо добавить в область, и количества документов, которые необходимо повторно индексировать в этой области.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-138">[**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.</span></span>

### <a name="irowsetprioritization-events"></a><span data-ttu-id="4d0e5-139">События Ировсетприоритизатион</span><span class="sxs-lookup"><span data-stu-id="4d0e5-139">IRowsetPrioritization Events</span></span>

<span data-ttu-id="4d0e5-140">Существует три события набора строк в [**ировсетевентс:: онровсетевент**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) в перечислении [**\_ типа ровсетевент**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :</span><span class="sxs-lookup"><span data-stu-id="4d0e5-140">There are three rowset events in [**IRowsetEvents::OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) in the [**ROWSETEVENT\_TYPE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) enumeration:</span></span>


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



<span data-ttu-id="4d0e5-141">Ниже приведены события набора строк.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-141">The rowset events are as follows:</span></span>

-   <span data-ttu-id="4d0e5-142">Событие **ровсетевент \_ типа данных с \_ истекшим сроком действия** указывает на то, что срок действия набора строк истек, и что необходимо запросить новый набор строк.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-142">The **ROWSETEVENT\_TYPE\_DATAEXPIRED** event indicates that data backing the rowset has expired, and that a new rowset should be requested.</span></span>
-   <span data-ttu-id="4d0e5-143">Событие **\_ \_ Фореграундлост типа набора строк** указывает, что элемент, имеющий приоритет переднего плана в стеке приоритизации, был понижен, так как кто-то другой заранее определил приоритеты этого запроса.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-143">The **ROWSET\_TYPE\_FOREGROUNDLOST** event indicates that an item that did have foreground priority in the prioritization stack has been demoted, because someone else prioritized themselves ahead of this query.</span></span>
-   <span data-ttu-id="4d0e5-144">Событие **\_ \_ скопестатистикс типа ровсетевент** предоставляет те же сведения, что и при вызове метода [**ировсетприоритизатион:: жетскопестатистикс**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) , но с помощью Push-механику следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4d0e5-144">The **ROWSETEVENT\_TYPE\_SCOPESTATISTICS** event gives you the same information available from the [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) method call, but through a push mechanic, as follows:</span></span>
    -   <span data-ttu-id="4d0e5-145">Событие возникает, если API приоритизации использовался для запроса уровня приоритетности, отличного от значения по умолчанию, и частоты событий статистики, отличной от нулевой.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-145">The event arises if the prioritization API has been used to request a non-default prioritization level, and a non-zero statistics event frequency.</span></span>
    -   <span data-ttu-id="4d0e5-146">Событие возникает только при фактическом изменении статистики и интервале, указанном в [**ировсетприоритизатион**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) (интервал не гарантирует частоту события).</span><span class="sxs-lookup"><span data-stu-id="4d0e5-146">The event arises only when statistics actually change, and the interval specified in the [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) has elapsed (the interval does not guarantee the frequency of the event).</span></span>
    -   <span data-ttu-id="4d0e5-147">Это событие гарантированно вызовет состояние "возврат к нулю" (для добавления нулевых элементов, оставшиеся нулевые изменения) при условии, что было вызвано ненулевое событие.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-147">This event is guaranteed to raise a "bounce zero" state (zero items remaining to be added, zero modifies remaining), provided that a non-zero event has been raised.</span></span>
    -   <span data-ttu-id="4d0e5-148">Индексатор может обрабатывать элементы без отправки этого события, если очередь очищается до частоты событий статистики.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-148">The indexer may process items without sending this event, if the queue empties before the statistics event frequency.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d0e5-149">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4d0e5-149">Additional Resources</span></span>

<span data-ttu-id="4d0e5-150">См. следующие ресурсы, связанные с определением приоритетов и наборами строк.</span><span class="sxs-lookup"><span data-stu-id="4d0e5-150">See the following resources related to prioritization and rowsets:</span></span>

-   <span data-ttu-id="4d0e5-151">Интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="4d0e5-151">Interfaces:</span></span>
    -   [<span data-ttu-id="4d0e5-152">**ировсетевентс**</span><span class="sxs-lookup"><span data-stu-id="4d0e5-152">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [<span data-ttu-id="4d0e5-153">**ировсетприоритизатион**</span><span class="sxs-lookup"><span data-stu-id="4d0e5-153">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   <span data-ttu-id="4d0e5-154">Перечисления:</span><span class="sxs-lookup"><span data-stu-id="4d0e5-154">Enumerations:</span></span>
    -   [<span data-ttu-id="4d0e5-155">**определение приоритетов \_ флагов**</span><span class="sxs-lookup"><span data-stu-id="4d0e5-155">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [<span data-ttu-id="4d0e5-156">**уровень ПРИОРИТЕТа \_**</span><span class="sxs-lookup"><span data-stu-id="4d0e5-156">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [<span data-ttu-id="4d0e5-157">**РОВСЕТЕВЕНТ \_ ITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="4d0e5-157">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [<span data-ttu-id="4d0e5-158">**\_тип ровсетевент**</span><span class="sxs-lookup"><span data-stu-id="4d0e5-158">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a><span data-ttu-id="4d0e5-159">См. также</span><span class="sxs-lookup"><span data-stu-id="4d0e5-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d0e5-160">Поиск Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d0e5-160">Windows 7 Search</span></span>](./-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="4d0e5-161">Новый для поиска Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d0e5-161">New for Windows 7 Search</span></span>](new-for-windows-7-search.md)
</dt> <dt>

[<span data-ttu-id="4d0e5-162">Библиотеки оболочки Windows в Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d0e5-162">Windows Shell Libraries in Windows 7</span></span>](-search-win7-development-scenarios.md)
</dt> </dl>

 

 