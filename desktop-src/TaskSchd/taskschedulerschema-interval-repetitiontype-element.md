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
ms.openlocfilehash: 9720bc2257d4c0b45116089bfdd4113335fc6b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988420"
---
# <a name="interval-repetitiontype-element"></a><span data-ttu-id="91d9d-104">Элемент Interval (Репетитионтипе)</span><span class="sxs-lookup"><span data-stu-id="91d9d-104">Interval (repetitionType) Element</span></span>

<span data-ttu-id="91d9d-105">Задает интервал времени между перезапусками задачи.</span><span class="sxs-lookup"><span data-stu-id="91d9d-105">Specifies the amount of time between each restart of the task.</span></span> <span data-ttu-id="91d9d-106">Формат этой строки — P <days> DT <hours> H <minutes> <seconds> S (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут).</span><span class="sxs-lookup"><span data-stu-id="91d9d-106">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="91d9d-107">Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.</span><span class="sxs-lookup"><span data-stu-id="91d9d-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

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

<span data-ttu-id="91d9d-108">Элемент определяется сложным типом [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="91d9d-108">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="91d9d-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="91d9d-109">Parent element</span></span>



| <span data-ttu-id="91d9d-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="91d9d-110">Element</span></span>                                                                      | <span data-ttu-id="91d9d-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="91d9d-111">Derived from</span></span>                                                             | <span data-ttu-id="91d9d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="91d9d-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91d9d-113">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="91d9d-113">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="91d9d-114">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="91d9d-114">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="91d9d-115">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="91d9d-115">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="91d9d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91d9d-116">Remarks</span></span>

<span data-ttu-id="91d9d-117">Для разработки сценариев интервал шаблона повторения указывается с помощью свойства [**репетитионпаттерн. Interval**](repetitionpattern-interval.md) .</span><span class="sxs-lookup"><span data-stu-id="91d9d-117">For scripting development, the interval of the repetition pattern is specified using the [**RepetitionPattern.Interval**](repetitionpattern-interval.md) property.</span></span>

<span data-ttu-id="91d9d-118">Для разработки на C++ интервал создания шаблона повторения указывается с помощью свойства [**ирепетитионпаттерн:: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) .</span><span class="sxs-lookup"><span data-stu-id="91d9d-118">For C++ development, the interval of the repetition pattern is specified using the [**IRepetitionPattern::Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="91d9d-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="91d9d-119">Examples</span></span>

<span data-ttu-id="91d9d-120">Полный пример XML-кода для задачи, в которой используется интервал повторения, см. в разделе [Пример ежедневного триггера (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="91d9d-120">For a complete example of the XML for a task that uses a repetition interval, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91d9d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="91d9d-121">Requirements</span></span>



| <span data-ttu-id="91d9d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="91d9d-122">Requirement</span></span> | <span data-ttu-id="91d9d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="91d9d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91d9d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91d9d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="91d9d-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91d9d-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91d9d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91d9d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="91d9d-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="91d9d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91d9d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91d9d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d9d-129">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="91d9d-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="91d9d-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="91d9d-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





