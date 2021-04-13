---
title: Монслидовтригжер. Виксофмонс, свойство
description: Для сценариев Возвращает или задает недели месяца, в течение которых выполняется задача.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- планировщик задач свойства Виксофмонс
- Планировщик задач свойства Виксофмонс, объект Монслидовтригжер
- Планировщик задач объекта Монслидовтригжер, свойство Виксофмонс
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489699"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a><span data-ttu-id="5965c-106">Монслидовтригжер. Виксофмонс, свойство</span><span class="sxs-lookup"><span data-stu-id="5965c-106">MonthlyDOWTrigger.WeeksOfMonth property</span></span>

<span data-ttu-id="5965c-107">Для сценариев Возвращает или задает недели месяца, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="5965c-107">For scripting, gets or sets the weeks of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="5965c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5965c-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a><span data-ttu-id="5965c-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5965c-109">Property value</span></span>

<span data-ttu-id="5965c-110">Битовая маска, указывающая дни недели, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="5965c-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="5965c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5965c-111">Remarks</span></span>

<span data-ttu-id="5965c-112">В следующей таблице показано сопоставление побитовой маски, используемой этим свойством.</span><span class="sxs-lookup"><span data-stu-id="5965c-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="5965c-113">Неделя</span><span class="sxs-lookup"><span data-stu-id="5965c-113">Week</span></span>                     | <span data-ttu-id="5965c-114">Шестнадцатеричное значение</span><span class="sxs-lookup"><span data-stu-id="5965c-114">Hex Value</span></span> | <span data-ttu-id="5965c-115">Десятичное значение</span><span class="sxs-lookup"><span data-stu-id="5965c-115">Decimal Value</span></span> |
|--------------------------|-----------|---------------|
| <span data-ttu-id="5965c-116">Первая неделя месяца</span><span class="sxs-lookup"><span data-stu-id="5965c-116">First week of the month</span></span>  | <span data-ttu-id="5965c-117">0X01</span><span class="sxs-lookup"><span data-stu-id="5965c-117">0X01</span></span>      | <span data-ttu-id="5965c-118">1</span><span class="sxs-lookup"><span data-stu-id="5965c-118">1</span></span>             |
| <span data-ttu-id="5965c-119">Вторая неделя месяца</span><span class="sxs-lookup"><span data-stu-id="5965c-119">Second week of the month</span></span> | <span data-ttu-id="5965c-120">0x02</span><span class="sxs-lookup"><span data-stu-id="5965c-120">0x02</span></span>      | <span data-ttu-id="5965c-121">2</span><span class="sxs-lookup"><span data-stu-id="5965c-121">2</span></span>             |
| <span data-ttu-id="5965c-122">Третья неделя месяца</span><span class="sxs-lookup"><span data-stu-id="5965c-122">Third week of the month</span></span>  | <span data-ttu-id="5965c-123">0X04</span><span class="sxs-lookup"><span data-stu-id="5965c-123">0X04</span></span>      | <span data-ttu-id="5965c-124">4</span><span class="sxs-lookup"><span data-stu-id="5965c-124">4</span></span>             |
| <span data-ttu-id="5965c-125">Четвертая неделя месяца</span><span class="sxs-lookup"><span data-stu-id="5965c-125">Fourth week of the month</span></span> | <span data-ttu-id="5965c-126">0X08</span><span class="sxs-lookup"><span data-stu-id="5965c-126">0X08</span></span>      | <span data-ttu-id="5965c-127">8</span><span class="sxs-lookup"><span data-stu-id="5965c-127">8</span></span>             |



 

<span data-ttu-id="5965c-128">При чтении или записи XML для задачи дни недели месячного дня недели задаются элементом [**weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5965c-128">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**Weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="5965c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5965c-129">Requirements</span></span>



| <span data-ttu-id="5965c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5965c-130">Requirement</span></span> | <span data-ttu-id="5965c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5965c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5965c-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5965c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5965c-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5965c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5965c-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5965c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5965c-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5965c-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5965c-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5965c-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="5965c-137"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5965c-137"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5965c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5965c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5965c-139"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5965c-139"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5965c-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5965c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5965c-141">**монслидовтригжер**</span><span class="sxs-lookup"><span data-stu-id="5965c-141">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="5965c-142">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="5965c-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





