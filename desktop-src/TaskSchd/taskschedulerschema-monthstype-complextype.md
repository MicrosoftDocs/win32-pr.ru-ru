---
title: Сложный тип Монсстипе
description: Определяет дочерние элементы и сведения о последовательности для элементов month (Монслидайофвиксчедулетипе) и months (Монслисчедулетипе).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- планировщик задач сложного типа Монсстипе
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801480"
---
# <a name="monthstype-complex-type"></a><span data-ttu-id="99747-104">Сложный тип Монсстипе</span><span class="sxs-lookup"><span data-stu-id="99747-104">monthsType Complex Type</span></span>

<span data-ttu-id="99747-105">Определяет дочерние элементы и сведения о последовательности для элементов [**Month (монслидайофвиксчедулетипе)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) и [**months (монслисчедулетипе)**](taskschedulerschema-months-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="99747-105">Defines the child elements and sequencing information for the [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) and [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="99747-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="99747-106">Child elements</span></span>



| <span data-ttu-id="99747-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="99747-107">Element</span></span>                                                               | <span data-ttu-id="99747-108">Тип</span><span class="sxs-lookup"><span data-stu-id="99747-108">Type</span></span> | <span data-ttu-id="99747-109">Описание</span><span class="sxs-lookup"><span data-stu-id="99747-109">Description</span></span>                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [<span data-ttu-id="99747-110">**Апрель**</span><span class="sxs-lookup"><span data-stu-id="99747-110">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         | <span data-ttu-id="99747-111">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-111">N/A</span></span>  | <span data-ttu-id="99747-112">Указывает, что задача выполняется в апреле.</span><span class="sxs-lookup"><span data-stu-id="99747-112">Specifies that the task runs in April.</span></span> <br/>     |
| [<span data-ttu-id="99747-113">**Августа**</span><span class="sxs-lookup"><span data-stu-id="99747-113">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       | <span data-ttu-id="99747-114">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-114">N/A</span></span>  | <span data-ttu-id="99747-115">Указывает, что задача выполняется в августе.</span><span class="sxs-lookup"><span data-stu-id="99747-115">Specifies that the task runs in August.</span></span> <br/>    |
| [<span data-ttu-id="99747-116">**Декабрь**</span><span class="sxs-lookup"><span data-stu-id="99747-116">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   | <span data-ttu-id="99747-117">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-117">N/A</span></span>  | <span data-ttu-id="99747-118">Указывает, что задача выполняется в декабре.</span><span class="sxs-lookup"><span data-stu-id="99747-118">Specifies that the task runs in December.</span></span> <br/>  |
| [<span data-ttu-id="99747-119">**Февраль**</span><span class="sxs-lookup"><span data-stu-id="99747-119">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   | <span data-ttu-id="99747-120">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-120">N/A</span></span>  | <span data-ttu-id="99747-121">Указывает, что задача выполняется в феврале.</span><span class="sxs-lookup"><span data-stu-id="99747-121">Specifies that the task runs in February.</span></span> <br/>  |
| [<span data-ttu-id="99747-122">**Января**</span><span class="sxs-lookup"><span data-stu-id="99747-122">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     | <span data-ttu-id="99747-123">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-123">N/A</span></span>  | <span data-ttu-id="99747-124">Указывает, что задача выполняется в январе.</span><span class="sxs-lookup"><span data-stu-id="99747-124">Specifies that the task runs in January.</span></span> <br/>   |
| [<span data-ttu-id="99747-125">**Июле**</span><span class="sxs-lookup"><span data-stu-id="99747-125">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           | <span data-ttu-id="99747-126">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-126">N/A</span></span>  | <span data-ttu-id="99747-127">Указывает, что задача выполняется в июле.</span><span class="sxs-lookup"><span data-stu-id="99747-127">Specifies that the task runs in July.</span></span> <br/>      |
| [<span data-ttu-id="99747-128">**Июнь**</span><span class="sxs-lookup"><span data-stu-id="99747-128">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           | <span data-ttu-id="99747-129">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-129">N/A</span></span>  | <span data-ttu-id="99747-130">Указывает, что задача выполняется в июне.</span><span class="sxs-lookup"><span data-stu-id="99747-130">Specifies that the task runs in June.</span></span> <br/>      |
| [<span data-ttu-id="99747-131">**Март**</span><span class="sxs-lookup"><span data-stu-id="99747-131">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         | <span data-ttu-id="99747-132">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-132">N/A</span></span>  | <span data-ttu-id="99747-133">Указывает, что задача выполняется в марте.</span><span class="sxs-lookup"><span data-stu-id="99747-133">Specifies that the task runs in March.</span></span> <br/>     |
| [<span data-ttu-id="99747-134">**Мая**</span><span class="sxs-lookup"><span data-stu-id="99747-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             | <span data-ttu-id="99747-135">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-135">N/A</span></span>  | <span data-ttu-id="99747-136">Указывает, что задача выполняется в Май.</span><span class="sxs-lookup"><span data-stu-id="99747-136">Specifies that the task runs in May.</span></span> <br/>       |
| [<span data-ttu-id="99747-137">**Ноября**</span><span class="sxs-lookup"><span data-stu-id="99747-137">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   | <span data-ttu-id="99747-138">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-138">N/A</span></span>  | <span data-ttu-id="99747-139">Указывает, что задача выполняется в ноябре.</span><span class="sxs-lookup"><span data-stu-id="99747-139">Specifies that the task runs in November.</span></span> <br/>  |
| [<span data-ttu-id="99747-140">**Октябре**</span><span class="sxs-lookup"><span data-stu-id="99747-140">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     | <span data-ttu-id="99747-141">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-141">N/A</span></span>  | <span data-ttu-id="99747-142">Указывает, что задача выполняется в октябре.</span><span class="sxs-lookup"><span data-stu-id="99747-142">Specifies that the task runs in October.</span></span> <br/>   |
| [<span data-ttu-id="99747-143">**Сентябрь**</span><span class="sxs-lookup"><span data-stu-id="99747-143">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) | <span data-ttu-id="99747-144">Н/Д</span><span class="sxs-lookup"><span data-stu-id="99747-144">N/A</span></span>  | <span data-ttu-id="99747-145">Указывает, что задача выполняется в сентябре.</span><span class="sxs-lookup"><span data-stu-id="99747-145">Specifies that the task runs in September.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="99747-146">Требования</span><span class="sxs-lookup"><span data-stu-id="99747-146">Requirements</span></span>



| <span data-ttu-id="99747-147">Требование</span><span class="sxs-lookup"><span data-stu-id="99747-147">Requirement</span></span> | <span data-ttu-id="99747-148">Значение</span><span class="sxs-lookup"><span data-stu-id="99747-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99747-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99747-149">Minimum supported client</span></span><br/> | <span data-ttu-id="99747-150">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99747-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="99747-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99747-151">Minimum supported server</span></span><br/> | <span data-ttu-id="99747-152">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99747-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99747-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99747-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99747-154">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="99747-154">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="99747-155">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="99747-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





