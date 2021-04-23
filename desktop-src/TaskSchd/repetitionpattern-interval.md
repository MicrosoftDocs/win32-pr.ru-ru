---
title: Репетитионпаттерн. Interval, свойство
description: Для создания скриптов Возвращает или задает интервал времени между перезапусками задачи.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Свойство Interval планировщик задач
- Свойство Interval планировщик задач, объект Репетитионпаттерн
- Планировщик задач объекта Репетитионпаттерн, свойство Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734179"
---
# <a name="repetitionpatterninterval-property"></a><span data-ttu-id="8a06a-106">Репетитионпаттерн. Interval, свойство</span><span class="sxs-lookup"><span data-stu-id="8a06a-106">RepetitionPattern.Interval property</span></span>

<span data-ttu-id="8a06a-107">Для создания скриптов Возвращает или задает интервал времени между перезапусками задачи.</span><span class="sxs-lookup"><span data-stu-id="8a06a-107">For scripting, gets or sets the amount of time between each restart of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a06a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a06a-108">Syntax</span></span>


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a><span data-ttu-id="8a06a-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8a06a-109">Property value</span></span>

<span data-ttu-id="8a06a-110">Промежуток времени между перезапусками задачи.</span><span class="sxs-lookup"><span data-stu-id="8a06a-110">The amount of time between each restart of the task.</span></span> <span data-ttu-id="8a06a-111">Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут).</span><span class="sxs-lookup"><span data-stu-id="8a06a-111">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="8a06a-112">Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.</span><span class="sxs-lookup"><span data-stu-id="8a06a-112">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a06a-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="8a06a-113">Remarks</span></span>

<span data-ttu-id="8a06a-114">Если для задачи задана длительность повторения, необходимо также указать интервал повторения.</span><span class="sxs-lookup"><span data-stu-id="8a06a-114">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="8a06a-115">При чтении или записи XML для задачи интервал повтора указывается в элементе [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="8a06a-115">When reading or writing XML for a task, the repetition interval is specified in the [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a06a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8a06a-116">Requirements</span></span>



| <span data-ttu-id="8a06a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8a06a-117">Requirement</span></span> | <span data-ttu-id="8a06a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8a06a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a06a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a06a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8a06a-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a06a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8a06a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a06a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8a06a-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a06a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8a06a-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8a06a-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a06a-124"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a06a-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a06a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8a06a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a06a-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a06a-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a06a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a06a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a06a-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="8a06a-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





