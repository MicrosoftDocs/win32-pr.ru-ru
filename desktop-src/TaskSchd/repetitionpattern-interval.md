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
ms.openlocfilehash: 1d62bb821f4c5e61d344e21fafa4ba1265c73470
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534601"
---
# <a name="repetitionpatterninterval-property"></a><span data-ttu-id="20f75-106">Репетитионпаттерн. Interval, свойство</span><span class="sxs-lookup"><span data-stu-id="20f75-106">RepetitionPattern.Interval property</span></span>

<span data-ttu-id="20f75-107">Для создания скриптов Возвращает или задает интервал времени между перезапусками задачи.</span><span class="sxs-lookup"><span data-stu-id="20f75-107">For scripting, gets or sets the amount of time between each restart of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="20f75-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20f75-108">Syntax</span></span>


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a><span data-ttu-id="20f75-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="20f75-109">Property value</span></span>

<span data-ttu-id="20f75-110">Промежуток времени между перезапусками задачи.</span><span class="sxs-lookup"><span data-stu-id="20f75-110">The amount of time between each restart of the task.</span></span> <span data-ttu-id="20f75-111">Формат этой строки — P <days> DT <hours> H <minutes> <seconds> S (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут).</span><span class="sxs-lookup"><span data-stu-id="20f75-111">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="20f75-112">Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.</span><span class="sxs-lookup"><span data-stu-id="20f75-112">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="20f75-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20f75-113">Remarks</span></span>

<span data-ttu-id="20f75-114">Если для задачи задана длительность повторения, необходимо также указать интервал повторения.</span><span class="sxs-lookup"><span data-stu-id="20f75-114">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="20f75-115">При чтении или записи XML для задачи интервал повтора указывается в элементе [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="20f75-115">When reading or writing XML for a task, the repetition interval is specified in the [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="20f75-116">Требования</span><span class="sxs-lookup"><span data-stu-id="20f75-116">Requirements</span></span>



| <span data-ttu-id="20f75-117">Требование</span><span class="sxs-lookup"><span data-stu-id="20f75-117">Requirement</span></span> | <span data-ttu-id="20f75-118">Значение</span><span class="sxs-lookup"><span data-stu-id="20f75-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20f75-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20f75-119">Minimum supported client</span></span><br/> | <span data-ttu-id="20f75-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20f75-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="20f75-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20f75-121">Minimum supported server</span></span><br/> | <span data-ttu-id="20f75-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20f75-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20f75-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="20f75-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="20f75-124"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="20f75-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="20f75-125">DLL</span><span class="sxs-lookup"><span data-stu-id="20f75-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20f75-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20f75-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f75-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20f75-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f75-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="20f75-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





