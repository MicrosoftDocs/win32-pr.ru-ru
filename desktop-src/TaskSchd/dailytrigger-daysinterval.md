---
title: Даилитригжер. Дайсинтервал, свойство
description: Для создания скриптов Возвращает или задает интервал между днями в расписании.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- планировщик задач свойства Дайсинтервал
- Планировщик задач свойства Дайсинтервал, объект Даилитригжер
- Планировщик задач объекта Даилитригжер, свойство Дайсинтервал
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534301"
---
# <a name="dailytriggerdaysinterval-property"></a><span data-ttu-id="fcee8-106">Даилитригжер. Дайсинтервал, свойство</span><span class="sxs-lookup"><span data-stu-id="fcee8-106">DailyTrigger.DaysInterval property</span></span>

<span data-ttu-id="fcee8-107">Для создания скриптов Возвращает или задает интервал между днями в расписании.</span><span class="sxs-lookup"><span data-stu-id="fcee8-107">For scripting, gets or sets the interval between the days in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcee8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcee8-108">Syntax</span></span>


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a><span data-ttu-id="fcee8-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fcee8-109">Property value</span></span>

<span data-ttu-id="fcee8-110">Интервал между днями в расписании.</span><span class="sxs-lookup"><span data-stu-id="fcee8-110">The interval between the days in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcee8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcee8-111">Remarks</span></span>

<span data-ttu-id="fcee8-112">Интервал 1 создает ежедневное расписание.</span><span class="sxs-lookup"><span data-stu-id="fcee8-112">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="fcee8-113">Интервал 2 создает расписание для каждого дня.</span><span class="sxs-lookup"><span data-stu-id="fcee8-113">An interval of 2 produces an every-other day schedule.</span></span>

<span data-ttu-id="fcee8-114">При чтении или записи собственного XML-кода для задачи интервал ежедневного расписания указывается с помощью элемента [**дайсинтервал**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="fcee8-114">When reading or writing your own XML for a task, the interval for a daily schedule is specified using the [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcee8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fcee8-115">Requirements</span></span>



| <span data-ttu-id="fcee8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fcee8-116">Requirement</span></span> | <span data-ttu-id="fcee8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fcee8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcee8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcee8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fcee8-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcee8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fcee8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcee8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fcee8-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fcee8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fcee8-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fcee8-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="fcee8-123"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fcee8-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fcee8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fcee8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcee8-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcee8-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcee8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcee8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcee8-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="fcee8-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="fcee8-128">**даилитригжер**</span><span class="sxs-lookup"><span data-stu-id="fcee8-128">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> </dl>

 

 





