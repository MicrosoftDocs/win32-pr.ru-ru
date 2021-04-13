---
title: Сложный тип Дайсофвиктипе
description: Определяет дочерние элементы и сведения о последовательности для элементов DaysOfWeek (Виклисчедулетипе) и DaysOfWeek (Монслидайофвиксчедулетипе).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- планировщик задач сложного типа Дайсофвиктипе
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341335"
---
# <a name="daysofweektype-complex-type"></a><span data-ttu-id="370aa-104">Сложный тип Дайсофвиктипе</span><span class="sxs-lookup"><span data-stu-id="370aa-104">daysOfWeekType Complex Type</span></span>

<span data-ttu-id="370aa-105">Определяет дочерние элементы и сведения о последовательности для элементов [**DaysOfWeek (виклисчедулетипе)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) и [**DaysOfWeek (монслидайофвиксчедулетипе)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="370aa-105">Defines the child elements and sequencing information for the [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) and [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="370aa-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="370aa-106">Child elements</span></span>



| <span data-ttu-id="370aa-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="370aa-107">Element</span></span>                                                                   | <span data-ttu-id="370aa-108">Тип</span><span class="sxs-lookup"><span data-stu-id="370aa-108">Type</span></span> | <span data-ttu-id="370aa-109">Описание</span><span class="sxs-lookup"><span data-stu-id="370aa-109">Description</span></span>                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [<span data-ttu-id="370aa-110">**Пятница**</span><span class="sxs-lookup"><span data-stu-id="370aa-110">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       | <span data-ttu-id="370aa-111">Н/Д</span><span class="sxs-lookup"><span data-stu-id="370aa-111">N/A</span></span>  | <span data-ttu-id="370aa-112">Задача выполняется в пятницу.</span><span class="sxs-lookup"><span data-stu-id="370aa-112">Task runs on Friday.</span></span> <br/>    |
| [<span data-ttu-id="370aa-113">**Понедельник**</span><span class="sxs-lookup"><span data-stu-id="370aa-113">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       | <span data-ttu-id="370aa-114">Н/Д</span><span class="sxs-lookup"><span data-stu-id="370aa-114">N/A</span></span>  | <span data-ttu-id="370aa-115">Задача выполняется в понедельник.</span><span class="sxs-lookup"><span data-stu-id="370aa-115">Task runs on Monday.</span></span><br/>     |
| [<span data-ttu-id="370aa-116">**Суббота**</span><span class="sxs-lookup"><span data-stu-id="370aa-116">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   | <span data-ttu-id="370aa-117">Н/Д</span><span class="sxs-lookup"><span data-stu-id="370aa-117">N/A</span></span>  | <span data-ttu-id="370aa-118">Задача выполняется в субботу.</span><span class="sxs-lookup"><span data-stu-id="370aa-118">Task runs on Saturday.</span></span> <br/>  |
| [<span data-ttu-id="370aa-119">**Воскресенье**</span><span class="sxs-lookup"><span data-stu-id="370aa-119">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       | <span data-ttu-id="370aa-120">Н/Д</span><span class="sxs-lookup"><span data-stu-id="370aa-120">N/A</span></span>  | <span data-ttu-id="370aa-121">Задача выполняется в воскресенье.</span><span class="sxs-lookup"><span data-stu-id="370aa-121">Task runs on Sunday.</span></span> <br/>    |
| [<span data-ttu-id="370aa-122">**Четверг**</span><span class="sxs-lookup"><span data-stu-id="370aa-122">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   | <span data-ttu-id="370aa-123">Н/Д</span><span class="sxs-lookup"><span data-stu-id="370aa-123">N/A</span></span>  | <span data-ttu-id="370aa-124">Задача выполняется в четверг</span><span class="sxs-lookup"><span data-stu-id="370aa-124">Task runs on Thursday</span></span> <br/>   |
| [<span data-ttu-id="370aa-125">**Вторник**</span><span class="sxs-lookup"><span data-stu-id="370aa-125">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     | <span data-ttu-id="370aa-126">Н/Д</span><span class="sxs-lookup"><span data-stu-id="370aa-126">N/A</span></span>  | <span data-ttu-id="370aa-127">Задача выполняется во вторник.</span><span class="sxs-lookup"><span data-stu-id="370aa-127">Task runs on Tuesday.</span></span> <br/>   |
| [<span data-ttu-id="370aa-128">**Среда**</span><span class="sxs-lookup"><span data-stu-id="370aa-128">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) | <span data-ttu-id="370aa-129">Н/Д</span><span class="sxs-lookup"><span data-stu-id="370aa-129">N/A</span></span>  | <span data-ttu-id="370aa-130">Задача выполняется в среду.</span><span class="sxs-lookup"><span data-stu-id="370aa-130">Task runs on Wednesday.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="370aa-131">Требования</span><span class="sxs-lookup"><span data-stu-id="370aa-131">Requirements</span></span>



| <span data-ttu-id="370aa-132">Требование</span><span class="sxs-lookup"><span data-stu-id="370aa-132">Requirement</span></span> | <span data-ttu-id="370aa-133">Значение</span><span class="sxs-lookup"><span data-stu-id="370aa-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="370aa-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="370aa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="370aa-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="370aa-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="370aa-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="370aa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="370aa-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="370aa-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="370aa-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="370aa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="370aa-139">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="370aa-139">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="370aa-140">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="370aa-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





