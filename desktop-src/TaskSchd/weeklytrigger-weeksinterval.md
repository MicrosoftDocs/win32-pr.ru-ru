---
title: Виклитригжер. Виксинтервал, свойство
description: Для создания скриптов Возвращает или задает интервал между неделями в расписании.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- планировщик задач свойства Виксинтервал
- Планировщик задач свойства Виксинтервал, объект Виклитригжер
- Планировщик задач объекта Виклитригжер, свойство Виксинтервал
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681782"
---
# <a name="weeklytriggerweeksinterval-property"></a><span data-ttu-id="3f96e-106">Виклитригжер. Виксинтервал, свойство</span><span class="sxs-lookup"><span data-stu-id="3f96e-106">WeeklyTrigger.WeeksInterval property</span></span>

<span data-ttu-id="3f96e-107">Для создания скриптов Возвращает или задает интервал между неделями в расписании.</span><span class="sxs-lookup"><span data-stu-id="3f96e-107">For scripting, gets or sets the interval between the weeks in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f96e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f96e-108">Syntax</span></span>


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a><span data-ttu-id="3f96e-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3f96e-109">Property value</span></span>

<span data-ttu-id="3f96e-110">Интервал между неделями в расписании.</span><span class="sxs-lookup"><span data-stu-id="3f96e-110">The interval between the weeks in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f96e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f96e-111">Remarks</span></span>

<span data-ttu-id="3f96e-112">Чтобы запускать задание раз в неделю, укажите 1.</span><span class="sxs-lookup"><span data-stu-id="3f96e-112">An interval of 1 produces a weekly schedule.</span></span> <span data-ttu-id="3f96e-113">Чтобы запускать задание раз в две недели, укажите 2.</span><span class="sxs-lookup"><span data-stu-id="3f96e-113">An interval of 2 produces an every-other week schedule.</span></span>

<span data-ttu-id="3f96e-114">При чтении или записи собственного XML-кода для задачи интервал для еженедельного расписания указывается с помощью элемента [**виксинтервал**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="3f96e-114">When reading or writing your own XML for a task, the interval for a weekly schedule is specified using the [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f96e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3f96e-115">Requirements</span></span>



| <span data-ttu-id="3f96e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3f96e-116">Requirement</span></span> | <span data-ttu-id="3f96e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3f96e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f96e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f96e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3f96e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f96e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3f96e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f96e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3f96e-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f96e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f96e-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3f96e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f96e-123"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3f96e-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3f96e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3f96e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f96e-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f96e-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f96e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f96e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f96e-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="3f96e-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





