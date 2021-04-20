---
title: Элемент Interval (Репетитионтипе)
description: Задает интервал времени между перезапусками задачи.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Элемент Interval планировщик задач
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfb87884438f1a39a5bd6f08eb9bb855311eb5d3
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734199"
---
# <a name="interval-repetitiontype-element"></a><span data-ttu-id="40206-104">Элемент Interval (Репетитионтипе)</span><span class="sxs-lookup"><span data-stu-id="40206-104">Interval (repetitionType) Element</span></span>

<span data-ttu-id="40206-105">Задает интервал времени между перезапусками задачи.</span><span class="sxs-lookup"><span data-stu-id="40206-105">Specifies the amount of time between each restart of the task.</span></span> <span data-ttu-id="40206-106">Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут).</span><span class="sxs-lookup"><span data-stu-id="40206-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="40206-107">Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.</span><span class="sxs-lookup"><span data-stu-id="40206-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="40206-108">Элемент определяется сложным типом [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="40206-108">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="40206-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="40206-109">Parent element</span></span>



| <span data-ttu-id="40206-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="40206-110">Element</span></span>                                                                      | <span data-ttu-id="40206-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="40206-111">Derived from</span></span>                                                             | <span data-ttu-id="40206-112">Описание</span><span class="sxs-lookup"><span data-stu-id="40206-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40206-113">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="40206-113">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="40206-114">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="40206-114">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="40206-115">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="40206-115">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="40206-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="40206-116">Remarks</span></span>

<span data-ttu-id="40206-117">Для разработки сценариев интервал шаблона повторения указывается с помощью свойства [**репетитионпаттерн. Interval**](repetitionpattern-interval.md) .</span><span class="sxs-lookup"><span data-stu-id="40206-117">For scripting development, the interval of the repetition pattern is specified using the [**RepetitionPattern.Interval**](repetitionpattern-interval.md) property.</span></span>

<span data-ttu-id="40206-118">Для разработки на C++ интервал создания шаблона повторения указывается с помощью свойства [**ирепетитионпаттерн:: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) .</span><span class="sxs-lookup"><span data-stu-id="40206-118">For C++ development, the interval of the repetition pattern is specified using the [**IRepetitionPattern::Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="40206-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="40206-119">Examples</span></span>

<span data-ttu-id="40206-120">Полный пример XML-кода для задачи, в которой используется интервал повторения, см. в разделе [Пример ежедневного триггера (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="40206-120">For a complete example of the XML for a task that uses a repetition interval, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40206-121">Требования</span><span class="sxs-lookup"><span data-stu-id="40206-121">Requirements</span></span>



| <span data-ttu-id="40206-122">Требование</span><span class="sxs-lookup"><span data-stu-id="40206-122">Requirement</span></span> | <span data-ttu-id="40206-123">Значение</span><span class="sxs-lookup"><span data-stu-id="40206-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="40206-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40206-124">Minimum supported client</span></span><br/> | <span data-ttu-id="40206-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="40206-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="40206-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40206-126">Minimum supported server</span></span><br/> | <span data-ttu-id="40206-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="40206-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40206-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40206-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40206-129">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="40206-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="40206-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="40206-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





