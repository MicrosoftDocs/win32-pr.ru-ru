---
title: Сложный тип Евенттригжертипе
description: Определяет дочерние элементы и сведения о последовательности для элемента EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- планировщик задач сложного типа Евенттригжертипе
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682006"
---
# <a name="eventtriggertype-complex-type"></a><span data-ttu-id="d8f68-104">Сложный тип Евенттригжертипе</span><span class="sxs-lookup"><span data-stu-id="d8f68-104">eventTriggerType Complex Type</span></span>

<span data-ttu-id="d8f68-105">Определяет дочерние элементы и сведения о последовательности для элемента [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d8f68-105">Defines the child elements and sequencing information for the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d8f68-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d8f68-106">Child elements</span></span>



| <span data-ttu-id="d8f68-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="d8f68-107">Element</span></span>                                                                           | <span data-ttu-id="d8f68-108">Тип</span><span class="sxs-lookup"><span data-stu-id="d8f68-108">Type</span></span>                                                                    | <span data-ttu-id="d8f68-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d8f68-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8f68-110">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="d8f68-110">**Delay**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="d8f68-111">длительность</span><span class="sxs-lookup"><span data-stu-id="d8f68-111">duration</span></span>                                                                | <span data-ttu-id="d8f68-112">Указывает промежуток времени между моментом возникновения события и моментом запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="d8f68-112">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="d8f68-113">**Подписка**</span><span class="sxs-lookup"><span data-stu-id="d8f68-113">**Subscription**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | [<span data-ttu-id="d8f68-114">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="d8f68-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="d8f68-115">Указывает запрос XPath, определяющий событие, вызвавшее срабатывание триггера.</span><span class="sxs-lookup"><span data-stu-id="d8f68-115">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="d8f68-116">**валуекуериес**</span><span class="sxs-lookup"><span data-stu-id="d8f68-116">**ValueQueries**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="d8f68-117">**намедвалуес**</span><span class="sxs-lookup"><span data-stu-id="d8f68-117">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md)      | <span data-ttu-id="d8f68-118">Задает последовательность элементов, каждая из которых содержит имя и значение запроса XPath.</span><span class="sxs-lookup"><span data-stu-id="d8f68-118">Specifies a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="d8f68-119">Запросы применяются к событию, возвращенному из подписки на события, указанной в элементе [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d8f68-119">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="d8f68-120">Имя для значения запроса XPath можно использовать в качестве переменной в элементе [**Body**](taskschedulerschema-body-showmessagetype-element.md) в разделе действия [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) задачи.</span><span class="sxs-lookup"><span data-stu-id="d8f68-120">The name for the XPath query value can be used as a variable in the [**Body**](taskschedulerschema-body-showmessagetype-element.md) element in the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) action section of a task.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="d8f68-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8f68-121">Remarks</span></span>

<span data-ttu-id="d8f68-122">Помимо дочернего элемента, определенного здесь, элемент [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) также использует дочерние элементы, определенные сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d8f68-122">In addition to the child element defined here, the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8f68-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d8f68-123">Requirements</span></span>



| <span data-ttu-id="d8f68-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d8f68-124">Requirement</span></span> | <span data-ttu-id="d8f68-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d8f68-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8f68-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8f68-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d8f68-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8f68-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8f68-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8f68-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d8f68-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d8f68-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8f68-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8f68-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f68-131">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="d8f68-131">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="d8f68-132">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d8f68-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





