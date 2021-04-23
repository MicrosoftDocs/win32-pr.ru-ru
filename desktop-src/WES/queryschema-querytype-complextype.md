---
title: Сложный тип QueryType
description: Определяет набор запросов Selector и суппрессор, которые используются для включения или исключения событий из результирующего набора.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- Журнал событий сложных типов QueryType
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135810"
---
# <a name="querytype-complex-type"></a><span data-ttu-id="019db-104">Сложный тип QueryType</span><span class="sxs-lookup"><span data-stu-id="019db-104">QueryType Complex Type</span></span>

<span data-ttu-id="019db-105">Определяет набор запросов Selector и суппрессор, которые используются для включения или исключения событий из результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="019db-105">Defines a set of selector and suppressor queries that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="019db-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="019db-106">Child elements</span></span>



| <span data-ttu-id="019db-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="019db-107">Element</span></span>                                                    | <span data-ttu-id="019db-108">Тип</span><span class="sxs-lookup"><span data-stu-id="019db-108">Type</span></span> | <span data-ttu-id="019db-109">Описание</span><span class="sxs-lookup"><span data-stu-id="019db-109">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="019db-110">**Метьте**</span><span class="sxs-lookup"><span data-stu-id="019db-110">**Select**</span></span>](queryschema-select-querytype-element.md)     |      | <span data-ttu-id="019db-111">Запрос XPath, определяющий события, включаемые в результирующий набор запроса.</span><span class="sxs-lookup"><span data-stu-id="019db-111">An XPath query that identifies the events to include in the query result set.</span></span> <span data-ttu-id="019db-112">Укажите XPath в текстовом тексте этого элемента.</span><span class="sxs-lookup"><span data-stu-id="019db-112">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="019db-113">Выражение XPath ограничено 32 выражениями.</span><span class="sxs-lookup"><span data-stu-id="019db-113">The XPath is limited to 32 expressions.</span></span><br/>   |
| [<span data-ttu-id="019db-114">**Подавление**</span><span class="sxs-lookup"><span data-stu-id="019db-114">**Suppress**</span></span>](queryschema-suppress-querytype-element.md) |      | <span data-ttu-id="019db-115">Запрос XPath, определяющий события, исключаемые из результирующего набора запроса.</span><span class="sxs-lookup"><span data-stu-id="019db-115">An XPath query that identifies the events to exclude from the query result set.</span></span> <span data-ttu-id="019db-116">Укажите XPath в текстовом тексте этого элемента.</span><span class="sxs-lookup"><span data-stu-id="019db-116">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="019db-117">Выражение XPath ограничено 32 выражениями.</span><span class="sxs-lookup"><span data-stu-id="019db-117">The XPath is limited to 32 expressions.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="019db-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="019db-118">Attributes</span></span>



| <span data-ttu-id="019db-119">Имя</span><span class="sxs-lookup"><span data-stu-id="019db-119">Name</span></span> | <span data-ttu-id="019db-120">Тип</span><span class="sxs-lookup"><span data-stu-id="019db-120">Type</span></span>   | <span data-ttu-id="019db-121">Описание</span><span class="sxs-lookup"><span data-stu-id="019db-121">Description</span></span>                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="019db-122">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="019db-122">Id</span></span>   | <span data-ttu-id="019db-123">long</span><span class="sxs-lookup"><span data-stu-id="019db-123">long</span></span>   | <span data-ttu-id="019db-124">Идентификатор, однозначно определяющий этот запрос в списке запросов.</span><span class="sxs-lookup"><span data-stu-id="019db-124">An identifier that uniquely identifies this query in your list of queries.</span></span> <span data-ttu-id="019db-125">Идентификатор отсчитывается от нуля.</span><span class="sxs-lookup"><span data-stu-id="019db-125">The identifier is zero-based.</span></span> <span data-ttu-id="019db-126">Если список запросов содержит более одного запроса, необходимо указать идентификатор.</span><span class="sxs-lookup"><span data-stu-id="019db-126">You must specify an identifier if your query list contains more than one query.</span></span><br/> |
| <span data-ttu-id="019db-127">Путь</span><span class="sxs-lookup"><span data-stu-id="019db-127">Path</span></span> | <span data-ttu-id="019db-128">anyURI</span><span class="sxs-lookup"><span data-stu-id="019db-128">anyURI</span></span> | <span data-ttu-id="019db-129">Имя канала или путь к файлу журнала, содержащему события.</span><span class="sxs-lookup"><span data-stu-id="019db-129">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="019db-130">Путь</span><span class="sxs-lookup"><span data-stu-id="019db-130">Path</span></span> | <span data-ttu-id="019db-131">anyURI</span><span class="sxs-lookup"><span data-stu-id="019db-131">anyURI</span></span> | <span data-ttu-id="019db-132">Имя канала или путь к файлу журнала, содержащему события.</span><span class="sxs-lookup"><span data-stu-id="019db-132">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="019db-133">Путь</span><span class="sxs-lookup"><span data-stu-id="019db-133">Path</span></span> | <span data-ttu-id="019db-134">anyURI</span><span class="sxs-lookup"><span data-stu-id="019db-134">anyURI</span></span> | <span data-ttu-id="019db-135">Не используется.</span><span class="sxs-lookup"><span data-stu-id="019db-135">Not used.</span></span><br/>                                                                                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="019db-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="019db-136">Remarks</span></span>

<span data-ttu-id="019db-137">Запрос должен содержать по крайней мере одну инструкцию SELECT.</span><span class="sxs-lookup"><span data-stu-id="019db-137">The query must have at least one select statement.</span></span> <span data-ttu-id="019db-138">Для каждой инструкции "подавлять" должна существовать хотя бы одна инструкция SELECT, указывающая тот же путь.</span><span class="sxs-lookup"><span data-stu-id="019db-138">For each suppress statement, there must be at least one select statement that specifies the same path.</span></span> <span data-ttu-id="019db-139">Если запрос SELECT и подавлять возвращает одинаковые события, то приоритет имеет оператор подавлять.</span><span class="sxs-lookup"><span data-stu-id="019db-139">If the select and suppress query return the same events, the suppress statement takes precedence.</span></span> <span data-ttu-id="019db-140">При выборе события из нескольких источников события возвращаются в порядке отметок времени.</span><span class="sxs-lookup"><span data-stu-id="019db-140">If you select events from multiple sources, the events are returned in time stamp order.</span></span> <span data-ttu-id="019db-141">Если используется метка системного времени и интенсивность событий высока, возможно, что несколько событий будут иметь одну и ту же отметку времени.</span><span class="sxs-lookup"><span data-stu-id="019db-141">If you use the system time stamp and the rate of events is high, it is possible that more than one event will have the same time stamp.</span></span> <span data-ttu-id="019db-142">В этом случае порядок событий станет неоднозначным и события могут отображаться неупорядоченно.</span><span class="sxs-lookup"><span data-stu-id="019db-142">When this occurs, the ordering of events becomes ambiguous and the events may appear out of order.</span></span>

<span data-ttu-id="019db-143">Если указать путь для одного из запросов в списке запросов, то все запросы должны указывать путь.</span><span class="sxs-lookup"><span data-stu-id="019db-143">If you specify a path for one of the queries in the list of queries, all of the queries must specify a path.</span></span> <span data-ttu-id="019db-144">Если не указать путь для всех запросов, необходимо указать путь при вызове функции [**евткуери**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) или [**евтсубскрибе**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .</span><span class="sxs-lookup"><span data-stu-id="019db-144">If you do not specify a path for all of the queries, you must specify the path when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="019db-145">Требования</span><span class="sxs-lookup"><span data-stu-id="019db-145">Requirements</span></span>



| <span data-ttu-id="019db-146">Требование</span><span class="sxs-lookup"><span data-stu-id="019db-146">Requirement</span></span> | <span data-ttu-id="019db-147">Значение</span><span class="sxs-lookup"><span data-stu-id="019db-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="019db-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="019db-148">Minimum supported client</span></span><br/> | <span data-ttu-id="019db-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="019db-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="019db-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="019db-150">Minimum supported server</span></span><br/> | <span data-ttu-id="019db-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="019db-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





