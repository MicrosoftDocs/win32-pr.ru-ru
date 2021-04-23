---
title: EventTrigger. Delay, свойство
description: Для создания скриптов Возвращает или задает значение, указывающее промежуток времени между возникновением события и моментом запуска задачи.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- планировщик задач свойства Delay
- Свойство Delay планировщик задач, объект EventTrigger
- Объект EventTrigger планировщик задач, свойство Delay
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb67ca7ef12ca023bcb6c0d9d83880d4abb94af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672685"
---
# <a name="eventtriggerdelay-property"></a><span data-ttu-id="35ab3-106">EventTrigger. Delay, свойство</span><span class="sxs-lookup"><span data-stu-id="35ab3-106">EventTrigger.Delay property</span></span>

<span data-ttu-id="35ab3-107">Для создания скриптов Возвращает или задает значение, указывающее промежуток времени между возникновением события и моментом запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="35ab3-107">For scripting, gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span> <span data-ttu-id="35ab3-108">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="35ab3-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="35ab3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35ab3-109">Syntax</span></span>


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="35ab3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="35ab3-110">Property value</span></span>

<span data-ttu-id="35ab3-111">Значение, указывающее промежуток времени между возникновением события и моментом запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="35ab3-111">A value that indicates the amount of time between when the event occurs and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ab3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35ab3-112">Remarks</span></span>

<span data-ttu-id="35ab3-113">При чтении или записи собственного XML-кода для задачи задержка события указывается с помощью элемента [**delay**](taskschedulerschema-delay-eventtriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="35ab3-113">When reading or writing your own XML for a task, the event delay is specified using the [**Delay**](taskschedulerschema-delay-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ab3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="35ab3-114">Requirements</span></span>



| <span data-ttu-id="35ab3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="35ab3-115">Requirement</span></span> | <span data-ttu-id="35ab3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="35ab3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35ab3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35ab3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35ab3-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35ab3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35ab3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35ab3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35ab3-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35ab3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35ab3-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="35ab3-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="35ab3-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35ab3-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35ab3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="35ab3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35ab3-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35ab3-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ab3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35ab3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ab3-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="35ab3-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="35ab3-127">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="35ab3-127">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

 





