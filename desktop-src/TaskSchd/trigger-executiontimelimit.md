---
title: Trigger.Exe, свойство Кутионтимелимит
description: Для создания скриптов Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- планировщик задач свойства Ексекутионтимелимит
- Планировщик задач свойства Ексекутионтимелимит, объект Trigger
- Планировщик задач объекта триггера, свойство Ексекутионтимелимит
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988414"
---
# <a name="triggerexecutiontimelimit-property"></a><span data-ttu-id="7c1e7-106">Trigger.Exe, свойство Кутионтимелимит</span><span class="sxs-lookup"><span data-stu-id="7c1e7-106">Trigger.ExecutionTimeLimit property</span></span>

<span data-ttu-id="7c1e7-107">Для создания скриптов Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.</span><span class="sxs-lookup"><span data-stu-id="7c1e7-107">For scripting, gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c1e7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c1e7-108">Syntax</span></span>


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="7c1e7-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7c1e7-109">Property value</span></span>

<span data-ttu-id="7c1e7-110">Максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.</span><span class="sxs-lookup"><span data-stu-id="7c1e7-110">The maximum amount of time that the task launched by the trigger is allowed to run.</span></span> <span data-ttu-id="7c1e7-111">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="7c1e7-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c1e7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c1e7-112">Remarks</span></span>

<span data-ttu-id="7c1e7-113">При чтении или записи XML для задачи предельное время выполнения указывается в элементе [**ексекутионтимелимит**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="7c1e7-113">When reading or writing XML for a task, the execution time limit is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c1e7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7c1e7-114">Requirements</span></span>



| <span data-ttu-id="7c1e7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7c1e7-115">Requirement</span></span> | <span data-ttu-id="7c1e7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7c1e7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1e7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c1e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7c1e7-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c1e7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7c1e7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c1e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7c1e7-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7c1e7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c1e7-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7c1e7-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c1e7-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7c1e7-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7c1e7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7c1e7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c1e7-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c1e7-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c1e7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c1e7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c1e7-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="7c1e7-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





