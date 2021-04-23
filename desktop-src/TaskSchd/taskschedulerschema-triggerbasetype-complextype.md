---
title: Сложный тип Тригжербасетипе
description: Определяет атрибут, базовые дочерние элементы и сведения о последовательности для всех сложных типов триггеров.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- планировщик задач сложного типа Тригжербасетипе
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56602e4a7e6599b7b756ff6bc109376dddc63ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341295"
---
# <a name="triggerbasetype-complex-type"></a><span data-ttu-id="1e98f-104">Сложный тип Тригжербасетипе</span><span class="sxs-lookup"><span data-stu-id="1e98f-104">triggerBaseType Complex Type</span></span>

<span data-ttu-id="1e98f-105">Определяет атрибут, базовые дочерние элементы и сведения о последовательности для всех сложных типов триггеров.</span><span class="sxs-lookup"><span data-stu-id="1e98f-105">Defines the attribute, base child elements, and sequencing information for all trigger complex types.</span></span>

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1e98f-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1e98f-106">Child elements</span></span>



| <span data-ttu-id="1e98f-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="1e98f-107">Element</span></span>                                                                                      | <span data-ttu-id="1e98f-108">Тип</span><span class="sxs-lookup"><span data-stu-id="1e98f-108">Type</span></span>                                                                     | <span data-ttu-id="1e98f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1e98f-109">Description</span></span>                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e98f-110">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="1e98f-110">**Enabled**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="1e98f-111">Логическое</span><span class="sxs-lookup"><span data-stu-id="1e98f-111">boolean</span></span>                                                                  | <span data-ttu-id="1e98f-112">Указывает, что триггер включен.</span><span class="sxs-lookup"><span data-stu-id="1e98f-112">Specifies that the trigger is enabled.</span></span><br/>                                                                      |
| [<span data-ttu-id="1e98f-113">**ендбаундари**</span><span class="sxs-lookup"><span data-stu-id="1e98f-113">**EndBoundary**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="1e98f-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="1e98f-114">dateTime</span></span>                                                                 | <span data-ttu-id="1e98f-115">Дата и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="1e98f-115">The date and time when the trigger is deactivated.</span></span><br/>                                                          |
| [<span data-ttu-id="1e98f-116">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="1e98f-116">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="1e98f-117">длительность</span><span class="sxs-lookup"><span data-stu-id="1e98f-117">duration</span></span>                                                                 | <span data-ttu-id="1e98f-118">Указывает интервал, в течение которого триггер может запустить задачу.</span><span class="sxs-lookup"><span data-stu-id="1e98f-118">Specifies the interval when the trigger can start the task.</span></span><br/>                                                 |
| [<span data-ttu-id="1e98f-119">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="1e98f-119">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="1e98f-120">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="1e98f-120">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="1e98f-121">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после срабатывания триггера.</span><span class="sxs-lookup"><span data-stu-id="1e98f-121">Specifies how often the task is run and how long the repetition pattern is repeated once the trigger fires.</span></span><br/> |
| [<span data-ttu-id="1e98f-122">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="1e98f-122">**StartBoundary**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="1e98f-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="1e98f-123">dateTime</span></span>                                                                 | <span data-ttu-id="1e98f-124">Дата и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="1e98f-124">The date and time when the trigger is activated.</span></span><br/>                                                            |



## <a name="attributes"></a><span data-ttu-id="1e98f-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1e98f-125">Attributes</span></span>



| <span data-ttu-id="1e98f-126">Имя</span><span class="sxs-lookup"><span data-stu-id="1e98f-126">Name</span></span> | <span data-ttu-id="1e98f-127">Тип</span><span class="sxs-lookup"><span data-stu-id="1e98f-127">Type</span></span> | <span data-ttu-id="1e98f-128">Описание</span><span class="sxs-lookup"><span data-stu-id="1e98f-128">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="1e98f-129">идентификатор</span><span class="sxs-lookup"><span data-stu-id="1e98f-129">id</span></span>   | <span data-ttu-id="1e98f-130">ID</span><span class="sxs-lookup"><span data-stu-id="1e98f-130">ID</span></span>   | <span data-ttu-id="1e98f-131">Идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="1e98f-131">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1e98f-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e98f-132">Remarks</span></span>

<span data-ttu-id="1e98f-133">К сложным типам триггеров относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="1e98f-133">Trigger complex types include the following.</span></span>

-   [<span data-ttu-id="1e98f-134">**буттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="1e98f-134">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)
-   [<span data-ttu-id="1e98f-135">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="1e98f-135">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)
-   [<span data-ttu-id="1e98f-136">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="1e98f-136">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)
-   [<span data-ttu-id="1e98f-137">**идлетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="1e98f-137">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)
-   [<span data-ttu-id="1e98f-138">**логонтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="1e98f-138">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)
-   [<span data-ttu-id="1e98f-139">**регистратионтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="1e98f-139">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)
-   [<span data-ttu-id="1e98f-140">**тиметригжертипе**</span><span class="sxs-lookup"><span data-stu-id="1e98f-140">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a><span data-ttu-id="1e98f-141">Требования</span><span class="sxs-lookup"><span data-stu-id="1e98f-141">Requirements</span></span>



| <span data-ttu-id="1e98f-142">Требование</span><span class="sxs-lookup"><span data-stu-id="1e98f-142">Requirement</span></span> | <span data-ttu-id="1e98f-143">Значение</span><span class="sxs-lookup"><span data-stu-id="1e98f-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1e98f-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e98f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1e98f-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e98f-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1e98f-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e98f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1e98f-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1e98f-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e98f-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e98f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e98f-149">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="1e98f-149">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="1e98f-150">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="1e98f-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





