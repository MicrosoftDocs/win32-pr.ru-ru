---
description: После возврата результата из запроса можно получить доступ к нескольким свойствам набора строк.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Свойства набора строк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701382"
---
# <a name="rowset-properties"></a><span data-ttu-id="397a6-103">Свойства набора строк</span><span class="sxs-lookup"><span data-stu-id="397a6-103">Rowset Properties</span></span>

<span data-ttu-id="397a6-104">После возврата результата из запроса можно получить доступ к нескольким свойствам набора строк.</span><span class="sxs-lookup"><span data-stu-id="397a6-104">After a result is returned from a query, you can access several properties for the rowset.</span></span>

<span data-ttu-id="397a6-105">Помимо стандартных свойств набора строк OLE-DB, SQL Search предоставляет следующие четыре пользовательских свойства.</span><span class="sxs-lookup"><span data-stu-id="397a6-105">In addition to the standard OLE-DB rowset properties, Windows Search SQL offers the following four custom properties.</span></span> <span data-ttu-id="397a6-106">Для этого свойства задано значение GUID {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span><span class="sxs-lookup"><span data-stu-id="397a6-106">The GUID for this property set is {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span></span>

<span data-ttu-id="397a6-107">Поиск Windows поддерживает стандартное свойство OLE-DB DBPROP \_ COMMANDTIMEOUT набора свойств [ \_ набора строк DBPROPSET](/previous-versions//ms691738(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="397a6-107">Windows Search supports the standard OLE-DB property DBPROP\_COMMANDTIMEOUT of the [DBPROPSET\_ROWSET](/previous-versions//ms691738(v=vs.85)) property set.</span></span>



| <span data-ttu-id="397a6-108">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="397a6-108">Property name</span></span>                  | <span data-ttu-id="397a6-109">PROPID/тип</span><span class="sxs-lookup"><span data-stu-id="397a6-109">PROPID/type</span></span> | <span data-ttu-id="397a6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="397a6-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="397a6-111">доноткомпутикспенсивепропс</span><span class="sxs-lookup"><span data-stu-id="397a6-111">DONOTCOMPUTEEXPENSIVEPROPS</span></span>     | <span data-ttu-id="397a6-112">15 или VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="397a6-112">15/VT\_BOOL</span></span> | <span data-ttu-id="397a6-113">Установка значения true позволяет запретить вычисление ресурсоемких свойств, таких как найденные результаты, и максимального ранга, который требует оценки всего запроса при доступе к любому свойству набора строк.</span><span class="sxs-lookup"><span data-stu-id="397a6-113">Setting this to true prevents computing expensive properties like Results Found and Max Rank that require evaluating the whole query when any rowset property is accessed.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="397a6-114">Максимальный ранг (Макс. \_ ранг)</span><span class="sxs-lookup"><span data-stu-id="397a6-114">Maximum Rank (MAX\_RANK)</span></span>       | <span data-ttu-id="397a6-115">6 или VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="397a6-115">6/VT\_I4</span></span>    | <span data-ttu-id="397a6-116">Наивысший ранг, вычисленный для любого результата.</span><span class="sxs-lookup"><span data-stu-id="397a6-116">The highest rank computed for any result.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="397a6-117">Найдены результаты (результаты \_ найдены)</span><span class="sxs-lookup"><span data-stu-id="397a6-117">Results Found (RESULTS\_FOUND)</span></span> | <span data-ttu-id="397a6-118">7 или VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="397a6-118">7/VT\_I4</span></span>    | <span data-ttu-id="397a6-119">Общее число уникальных элементов для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="397a6-119">The total number of unique items for this query.</span></span> <span data-ttu-id="397a6-120">Для запроса SELECT это число элементов в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="397a6-120">For a SELECT query, this is the number of items in the rowset.</span></span> <span data-ttu-id="397a6-121">Для группы по запросу это число уникальных конечных элементов.</span><span class="sxs-lookup"><span data-stu-id="397a6-121">For a GROUP ON query, this is the number of unique leaf items.</span></span> <span data-ttu-id="397a6-122">Это свойство не определяет количество строк в наборе строк верхнего уровня (число групп верхнего уровня).</span><span class="sxs-lookup"><span data-stu-id="397a6-122">This property does not identify the number of rows in the top-level rowset (the number of top-level groups).</span></span>                                                        |
| <span data-ttu-id="397a6-123">WHERE ID (ВХЕРЕИД)</span><span class="sxs-lookup"><span data-stu-id="397a6-123">Where ID (WHEREID)</span></span>             | <span data-ttu-id="397a6-124">8 или VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="397a6-124">8/VT\_I4</span></span>    | <span data-ttu-id="397a6-125">Идентификатор для ограничений, используемых для запроса.</span><span class="sxs-lookup"><span data-stu-id="397a6-125">The identifier for the restrictions used for a query.</span></span> <span data-ttu-id="397a6-126">Если набор строк открыт при выполнении нового запроса, новый запрос может повторно использовать ограничения из старого запроса, тем самым используя преимущества уже выполненной работы.</span><span class="sxs-lookup"><span data-stu-id="397a6-126">If a rowset is open when a new query is executed, the new query can reuse the restrictions from the older query, thereby taking advantage of the work already completed.</span></span> <span data-ttu-id="397a6-127">Дополнительные сведения о повторном использовании с ограничениями см. в [функции реусевхере](-search-sql-reusewhere.md).</span><span class="sxs-lookup"><span data-stu-id="397a6-127">For more information on reusing WHERE restrictions, refer to the [ReuseWhere function](-search-sql-reusewhere.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="397a6-128">См. также</span><span class="sxs-lookup"><span data-stu-id="397a6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="397a6-129">Определение приоритетов индексирования и событий набора строк в Windows 7</span><span class="sxs-lookup"><span data-stu-id="397a6-129">Indexing Prioritization and Rowset Events in Windows 7</span></span>](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
