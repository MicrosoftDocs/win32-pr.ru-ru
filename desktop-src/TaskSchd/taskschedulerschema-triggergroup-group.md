---
title: Группа Тригжерграуп
description: Определяет группу триггеров.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- Тригжерграуп планировщик задач
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137674"
---
# <a name="triggergroup-group"></a><span data-ttu-id="9a7bd-104">Группа Тригжерграуп</span><span class="sxs-lookup"><span data-stu-id="9a7bd-104">triggerGroup Group</span></span>

<span data-ttu-id="9a7bd-105">Определяет группу триггеров.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-105">Defines the trigger group.</span></span>

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="9a7bd-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9a7bd-106">Child elements</span></span>



| <span data-ttu-id="9a7bd-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a7bd-107">Element</span></span>                                                                                                 | <span data-ttu-id="9a7bd-108">Тип</span><span class="sxs-lookup"><span data-stu-id="9a7bd-108">Type</span></span>                                                                                                   | <span data-ttu-id="9a7bd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9a7bd-109">Description</span></span>                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a7bd-110">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-110">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [<span data-ttu-id="9a7bd-111">**буттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-111">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                             | <span data-ttu-id="9a7bd-112">Триггер, запускающий задачу при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-112">A trigger that starts a task when the system is booted.</span></span><br/>                                                |
| [<span data-ttu-id="9a7bd-113">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [<span data-ttu-id="9a7bd-114">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)                     | <span data-ttu-id="9a7bd-115">Триггер, запускающий задачу на основе расписания ежедневного, еженедельного, ежемесячного или месячного дня недели (DOW).</span><span class="sxs-lookup"><span data-stu-id="9a7bd-115">A trigger that starts a task based on a daily, weekly, monthly, or monthly day-of-week (DOW) schedule.</span></span><br/> |
| [<span data-ttu-id="9a7bd-116">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-116">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [<span data-ttu-id="9a7bd-117">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-117">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)                           | <span data-ttu-id="9a7bd-118">Триггер, запускающий задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-118">A trigger that starts a task when a system event occurs.</span></span><br/>                                               |
| [<span data-ttu-id="9a7bd-119">**идлетригжер**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-119">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [<span data-ttu-id="9a7bd-120">**идлетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-120">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                             | <span data-ttu-id="9a7bd-121">Триггер, запускающий задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-121">A trigger that starts a task when the computer goes into an idle state.</span></span><br/>                                |
| [<span data-ttu-id="9a7bd-122">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-122">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [<span data-ttu-id="9a7bd-123">**логонтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-123">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)                           | <span data-ttu-id="9a7bd-124">Триггер, запускающий задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-124">A trigger that starts a task when a user logs on.</span></span><br/>                                                      |
| [<span data-ttu-id="9a7bd-125">**регистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-125">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [<span data-ttu-id="9a7bd-126">**регистратионтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-126">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)             | <span data-ttu-id="9a7bd-127">Триггер, запускающий задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-127">A trigger that starts a task when the task is registered.</span></span><br/>                                              |
| [<span data-ttu-id="9a7bd-128">**сессионстатечанжетригжер**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-128">**SessionStateChangeTrigger**</span></span>](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [<span data-ttu-id="9a7bd-129">**сессионстатечанжетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-129">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="9a7bd-130">Триггер, запускающий задачу при изменении состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-130">A trigger that starts a task when a Terminal Server session changes state.</span></span><br/>                             |
| [<span data-ttu-id="9a7bd-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [<span data-ttu-id="9a7bd-132">**тиметригжертипе**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                             | <span data-ttu-id="9a7bd-133">Триггер, запускающий задачу при активации триггера.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-133">A trigger that starts a task when the trigger is activated.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="9a7bd-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a7bd-134">Remarks</span></span>

<span data-ttu-id="9a7bd-135">При чтении или записи XML элементы, определенные этой группой, являются дочерними элементами элемента [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9a7bd-135">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7bd-136">Требования</span><span class="sxs-lookup"><span data-stu-id="9a7bd-136">Requirements</span></span>



| <span data-ttu-id="9a7bd-137">Требование</span><span class="sxs-lookup"><span data-stu-id="9a7bd-137">Requirement</span></span> | <span data-ttu-id="9a7bd-138">Значение</span><span class="sxs-lookup"><span data-stu-id="9a7bd-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a7bd-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a7bd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7bd-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a7bd-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9a7bd-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a7bd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7bd-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9a7bd-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a7bd-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a7bd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7bd-144">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="9a7bd-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





