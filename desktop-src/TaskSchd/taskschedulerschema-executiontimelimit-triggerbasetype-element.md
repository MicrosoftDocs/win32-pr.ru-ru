---
title: Ексекутионтимелимит (Тригжербасетипе), элемент
description: Указывает максимальное время, в течение которого задача может запускаться триггером.
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- планировщик задач элемента Ексекутионтимелимит
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbe56fb0431ab109b1a19030ae6ba20af55492ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492075"
---
# <a name="executiontimelimit-triggerbasetype-element"></a><span data-ttu-id="b175e-104">Ексекутионтимелимит (Тригжербасетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="b175e-104">ExecutionTimeLimit (triggerBaseType) Element</span></span>

<span data-ttu-id="b175e-105">Указывает максимальное время, в течение которого задача может запускаться триггером.</span><span class="sxs-lookup"><span data-stu-id="b175e-105">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="b175e-106">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="b175e-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="b175e-107">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="b175e-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

<span data-ttu-id="b175e-108">Элемент **ексекутионтимелимит** определяется сложным типом [**тригжербасетипе**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b175e-108">The **ExecutionTimeLimit** element is defined by the [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b175e-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="b175e-109">Parent element</span></span>



| <span data-ttu-id="b175e-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="b175e-110">Element</span></span>                                                                                     | <span data-ttu-id="b175e-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="b175e-111">Derived from</span></span>                                                                               | <span data-ttu-id="b175e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b175e-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b175e-113">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="b175e-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="b175e-114">**буттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="b175e-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="b175e-115">Указывает триггер, который запускает задачу при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="b175e-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="b175e-116">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="b175e-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="b175e-117">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="b175e-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="b175e-118">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="b175e-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="b175e-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="b175e-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="b175e-120">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="b175e-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="b175e-121">Указывает триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="b175e-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="b175e-122">**идлетригжер**</span><span class="sxs-lookup"><span data-stu-id="b175e-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="b175e-123">**идлетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="b175e-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="b175e-124">Указывает триггер, который запускает задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="b175e-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="b175e-125">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="b175e-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="b175e-126">**логонтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="b175e-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="b175e-127">Указывает триггер, который запускает задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="b175e-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="b175e-128">**регистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="b175e-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="b175e-129">**регистратионтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="b175e-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="b175e-130">Указывает триггер, который запускает задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="b175e-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="b175e-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="b175e-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="b175e-132">**тиметригжертипе**</span><span class="sxs-lookup"><span data-stu-id="b175e-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="b175e-133">Указывает триггер, который запускает задачу при активации триггера.</span><span class="sxs-lookup"><span data-stu-id="b175e-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="b175e-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b175e-134">Remarks</span></span>

<span data-ttu-id="b175e-135">Для разработки сценариев ограничение времени выполнения указывается с помощью свойства [**Trigger.Exeкутионтимелимит**](trigger-executiontimelimit.md) , наследуемого всеми объектами триггера.</span><span class="sxs-lookup"><span data-stu-id="b175e-135">For scripting development, the execution time limit is specified using the [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="b175e-136">Для разработки на C++ ограничение времени выполнения задается с помощью свойства [**итригжер:: ексекутионтимелимит**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) , наследуемого всеми интерфейсами триггера.</span><span class="sxs-lookup"><span data-stu-id="b175e-136">For C++ development, the execution time limit is specified using the [**ITrigger::ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="b175e-137">Требования</span><span class="sxs-lookup"><span data-stu-id="b175e-137">Requirements</span></span>



| <span data-ttu-id="b175e-138">Требование</span><span class="sxs-lookup"><span data-stu-id="b175e-138">Requirement</span></span> | <span data-ttu-id="b175e-139">Значение</span><span class="sxs-lookup"><span data-stu-id="b175e-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b175e-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b175e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b175e-141">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b175e-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b175e-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b175e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b175e-143">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b175e-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b175e-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b175e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b175e-145">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="b175e-145">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b175e-146">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="b175e-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





