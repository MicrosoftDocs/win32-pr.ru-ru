---
title: Включенный (Тригжербасетипе) элемент
description: Указывает, что триггер включен.
ms.assetid: 14c98f40-0ec5-4dc1-978e-b02c08ee2384
keywords:
- Включенный элемент планировщик задач
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42b495ba1af5f3b9b99034b0d6ca9d02040460c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072017"
---
# <a name="enabled-triggerbasetype-element"></a><span data-ttu-id="f40ae-104">Включенный (Тригжербасетипе) элемент</span><span class="sxs-lookup"><span data-stu-id="f40ae-104">Enabled (triggerBaseType) Element</span></span>

<span data-ttu-id="f40ae-105">Указывает, что триггер включен.</span><span class="sxs-lookup"><span data-stu-id="f40ae-105">Specifies that the trigger is enabled.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
 />
```

<span data-ttu-id="f40ae-106">Элемент **Enabled** определяется сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f40ae-106">The **Enabled** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f40ae-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="f40ae-107">Parent element</span></span>



| <span data-ttu-id="f40ae-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="f40ae-108">Element</span></span>                                                                                     | <span data-ttu-id="f40ae-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="f40ae-109">Derived from</span></span>                                                                               | <span data-ttu-id="f40ae-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f40ae-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f40ae-111">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="f40ae-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="f40ae-112">**буттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="f40ae-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="f40ae-113">Указывает триггер, который запускает задачу при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="f40ae-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="f40ae-114">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="f40ae-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="f40ae-115">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="f40ae-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="f40ae-116">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="f40ae-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="f40ae-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="f40ae-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="f40ae-118">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="f40ae-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="f40ae-119">Указывает триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="f40ae-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="f40ae-120">**идлетригжер**</span><span class="sxs-lookup"><span data-stu-id="f40ae-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="f40ae-121">**идлетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="f40ae-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="f40ae-122">Указывает триггер, который запускает задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="f40ae-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="f40ae-123">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="f40ae-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="f40ae-124">**логонтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="f40ae-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="f40ae-125">Указывает триггер, который запускает задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="f40ae-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="f40ae-126">**регистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="f40ae-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="f40ae-127">**регистратионтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="f40ae-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="f40ae-128">Указывает триггер, который запускает задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="f40ae-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="f40ae-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="f40ae-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="f40ae-130">**тиметригжертипе**</span><span class="sxs-lookup"><span data-stu-id="f40ae-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="f40ae-131">Указывает триггер, который запускает задачу при активации триггера.</span><span class="sxs-lookup"><span data-stu-id="f40ae-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="f40ae-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f40ae-132">Remarks</span></span>

<span data-ttu-id="f40ae-133">Для разработки сценариев эта информация доступна через свойство [**Trigger. Enabled**](trigger-enabled.md) , которое наследуется всеми объектами триггера.</span><span class="sxs-lookup"><span data-stu-id="f40ae-133">For scripting development, this information is accessed through the [**Trigger.Enabled**](trigger-enabled.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="f40ae-134">Для разработки на C++ эта информация доступна через свойство [**итригжер:: Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) , унаследованное интерфейсами триггера ALL.</span><span class="sxs-lookup"><span data-stu-id="f40ae-134">For C++ development, this information is accessed through the [**ITrigger::Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="f40ae-135">Требования</span><span class="sxs-lookup"><span data-stu-id="f40ae-135">Requirements</span></span>



| <span data-ttu-id="f40ae-136">Требование</span><span class="sxs-lookup"><span data-stu-id="f40ae-136">Requirement</span></span> | <span data-ttu-id="f40ae-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f40ae-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f40ae-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f40ae-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f40ae-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f40ae-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f40ae-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f40ae-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f40ae-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f40ae-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f40ae-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f40ae-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f40ae-143">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="f40ae-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f40ae-144">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="f40ae-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





