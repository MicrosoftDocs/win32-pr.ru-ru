---
title: TaskSettings.Exe, свойство Кутионтимелимит
description: Для создания скриптов Возвращает или задает период времени, в течение которого может завершиться задача.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- планировщик задач свойства Ексекутионтимелимит
- Планировщик задач свойства Ексекутионтимелимит, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Ексекутионтимелимит
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682028"
---
# <a name="tasksettingsexecutiontimelimit-property"></a><span data-ttu-id="f28cb-106">TaskSettings.Exe, свойство Кутионтимелимит</span><span class="sxs-lookup"><span data-stu-id="f28cb-106">TaskSettings.ExecutionTimeLimit property</span></span>

<span data-ttu-id="f28cb-107">Для создания скриптов Возвращает или задает период времени, в течение которого может завершиться задача.</span><span class="sxs-lookup"><span data-stu-id="f28cb-107">For scripting, gets or sets the amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="f28cb-108">По умолчанию задача будет остановлена 72 часов после начала ее выполнения.</span><span class="sxs-lookup"><span data-stu-id="f28cb-108">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="f28cb-109">Это можно изменить, изменив этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f28cb-109">You can change this by changing this setting.</span></span>

<span data-ttu-id="f28cb-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f28cb-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f28cb-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f28cb-111">Syntax</span></span>


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="f28cb-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f28cb-112">Property value</span></span>

<span data-ttu-id="f28cb-113">Время, в течение которого разрешено выполнение задачи.</span><span class="sxs-lookup"><span data-stu-id="f28cb-113">The amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="f28cb-114">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="f28cb-114">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="f28cb-115">Значение PT0S позволит задаче выполняться неограниченное время.</span><span class="sxs-lookup"><span data-stu-id="f28cb-115">A value of PT0S will enable the task to run indefinitely.</span></span> <span data-ttu-id="f28cb-116">Если для этого параметра задано значение Nothing, то ограничение времени выполнения будет бесконечным.</span><span class="sxs-lookup"><span data-stu-id="f28cb-116">When this parameter is set to Nothing, the execution time limit is infinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="f28cb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f28cb-117">Remarks</span></span>

<span data-ttu-id="f28cb-118">При чтении или записи XML для задачи этот параметр указывается в элементе [**ексекутионтимелимит**](taskschedulerschema-executiontimelimit-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="f28cb-118">When reading or writing XML for a task, this setting is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f28cb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f28cb-119">Requirements</span></span>



| <span data-ttu-id="f28cb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f28cb-120">Requirement</span></span> | <span data-ttu-id="f28cb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f28cb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f28cb-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f28cb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f28cb-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f28cb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f28cb-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f28cb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f28cb-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f28cb-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f28cb-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f28cb-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="f28cb-127"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f28cb-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f28cb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f28cb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f28cb-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f28cb-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f28cb-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f28cb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f28cb-131">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="f28cb-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





