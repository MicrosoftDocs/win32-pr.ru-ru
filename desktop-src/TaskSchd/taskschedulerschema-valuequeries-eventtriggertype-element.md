---
title: Валуекуериес (Евенттригжертипе), элемент
description: Содержит последовательность элементов, каждая из которых содержит имя и значение запроса XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- планировщик задач элемента Валуекуериес
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988347"
---
# <a name="valuequeries-eventtriggertype-element"></a><span data-ttu-id="a4946-104">Валуекуериес (Евенттригжертипе), элемент</span><span class="sxs-lookup"><span data-stu-id="a4946-104">ValueQueries (eventTriggerType) Element</span></span>

<span data-ttu-id="a4946-105">Содержит последовательность элементов, каждая из которых содержит имя и значение запроса XPath.</span><span class="sxs-lookup"><span data-stu-id="a4946-105">Contains a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="a4946-106">Запросы применяются к событию, возвращенному из подписки на события, указанной в элементе [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a4946-106">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="a4946-107">Имя для значения запроса XPath можно использовать в качестве переменной в разделе Action задачи.</span><span class="sxs-lookup"><span data-stu-id="a4946-107">The name for the XPath query value can be used as a variable in the action section of a task.</span></span>

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

<span data-ttu-id="a4946-108">Элемент **валуекуериес** определяется сложным типом [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a4946-108">The **ValueQueries** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a4946-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a4946-109">Parent element</span></span>



| <span data-ttu-id="a4946-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="a4946-110">Element</span></span>                                                                                      | <span data-ttu-id="a4946-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="a4946-111">Derived from</span></span>                                                                 | <span data-ttu-id="a4946-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a4946-112">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="a4946-113">**EventTrigger (Тригжерграуп)**</span><span class="sxs-lookup"><span data-stu-id="a4946-113">**EventTrigger (triggerGroup)**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="a4946-114">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="a4946-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="a4946-115">Указывает триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="a4946-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a4946-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4946-116">Remarks</span></span>

<span data-ttu-id="a4946-117">Сведения о разработке на языке C++ см. в разделе [**свойство валуекуериес объекта иевенттригжер**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span><span class="sxs-lookup"><span data-stu-id="a4946-117">For C++ development, see [**ValueQueries Property of IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span></span>

<span data-ttu-id="a4946-118">Сведения о разработке скриптов см. в разделе [**EventTrigger. валуекуериес**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="a4946-118">For script development, see [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a4946-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="a4946-119">Examples</span></span>

<span data-ttu-id="a4946-120">Полный пример XML-кода для задачи, указывающей триггер события с помощью этого элемента, см. в разделе [пример триггера события (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a4946-120">For a complete example of the XML for a task that specifies a an event trigger using this element, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4946-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a4946-121">Requirements</span></span>



| <span data-ttu-id="a4946-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a4946-122">Requirement</span></span> | <span data-ttu-id="a4946-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a4946-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4946-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4946-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a4946-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4946-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4946-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4946-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a4946-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4946-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

