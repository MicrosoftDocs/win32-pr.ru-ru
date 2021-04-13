---
title: Duration (Репетитионтипе), элемент
description: Указывает, как долго шаблон повторяется.
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Элемент Duration планировщик задач
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341325"
---
# <a name="duration-repetitiontype-element"></a><span data-ttu-id="7f60e-104">Duration (Репетитионтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="7f60e-104">Duration (repetitionType) Element</span></span>

<span data-ttu-id="7f60e-105">Указывает, как долго шаблон повторяется.</span><span class="sxs-lookup"><span data-stu-id="7f60e-105">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="7f60e-106">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="7f60e-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="7f60e-107">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="7f60e-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="7f60e-108">Если для длительности не указано значение, шаблон повторяется бесконечно.</span><span class="sxs-lookup"><span data-stu-id="7f60e-108">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span> <span data-ttu-id="7f60e-109">Минимальное значение — одна минута.</span><span class="sxs-lookup"><span data-stu-id="7f60e-109">The minimum value is one minute.</span></span>

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="7f60e-110">Элемент определяется сложным типом [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7f60e-110">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7f60e-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="7f60e-111">Parent element</span></span>



| <span data-ttu-id="7f60e-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="7f60e-112">Element</span></span>                                                                      | <span data-ttu-id="7f60e-113">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="7f60e-113">Derived from</span></span>                                                             | <span data-ttu-id="7f60e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="7f60e-114">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f60e-115">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="7f60e-115">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="7f60e-116">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="7f60e-116">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="7f60e-117">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="7f60e-117">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7f60e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f60e-118">Remarks</span></span>

<span data-ttu-id="7f60e-119">Для приложений со скриптами длительность шаблона указывается с помощью свойства [**репетитионпаттерн. Duration**](repetitionpattern-duration.md) .</span><span class="sxs-lookup"><span data-stu-id="7f60e-119">For scripting applications, the duration of the pattern is specified using the [**RepetitionPattern.Duration**](repetitionpattern-duration.md) property.</span></span>

<span data-ttu-id="7f60e-120">Для приложений C++ длительность шаблона указывается с помощью свойства [**ирепетитионпаттерн::D фигурации**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) .</span><span class="sxs-lookup"><span data-stu-id="7f60e-120">For C++ applications, the duration of the pattern is specified using the [**IRepetitionPattern::Duration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="7f60e-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="7f60e-121">Examples</span></span>

<span data-ttu-id="7f60e-122">Следующий XML-код определяет шаблон повторения для триггера.</span><span class="sxs-lookup"><span data-stu-id="7f60e-122">The following XML defines a repetition pattern for a trigger.</span></span>


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
```



## <a name="requirements"></a><span data-ttu-id="7f60e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7f60e-123">Requirements</span></span>



| <span data-ttu-id="7f60e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7f60e-124">Requirement</span></span> | <span data-ttu-id="7f60e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7f60e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7f60e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f60e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7f60e-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f60e-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7f60e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f60e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7f60e-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f60e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f60e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f60e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f60e-131">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="7f60e-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="7f60e-132">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="7f60e-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





