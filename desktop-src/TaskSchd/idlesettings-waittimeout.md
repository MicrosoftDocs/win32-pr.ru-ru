---
title: Идлесеттингс. Ваиттимеаут, свойство
description: Для создания скриптов Возвращает или задает значение, указывающее время, в течение которого планировщик задач будет ожидать наступления условия простоя.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- планировщик задач свойства Ваиттимеаут
- Планировщик задач свойства Ваиттимеаут, объект Идлесеттингс
- Планировщик задач объекта Идлесеттингс, свойство Ваиттимеаут
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071726"
---
# <a name="idlesettingswaittimeout-property"></a><span data-ttu-id="a73f6-106">Идлесеттингс. Ваиттимеаут, свойство</span><span class="sxs-lookup"><span data-stu-id="a73f6-106">IdleSettings.WaitTimeout property</span></span>

<span data-ttu-id="a73f6-107">Для создания скриптов Возвращает или задает значение, указывающее время, в течение которого планировщик задач будет ожидать наступления условия простоя.</span><span class="sxs-lookup"><span data-stu-id="a73f6-107">For scripting, gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="a73f6-108">Если для этого свойства не указано значение, то служба планировщик задач будет ожидать возникновения условия простоя в течение неограниченного времени.</span><span class="sxs-lookup"><span data-stu-id="a73f6-108">If no value is specified for this property, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73f6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a73f6-109">Syntax</span></span>


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a><span data-ttu-id="a73f6-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a73f6-110">Property value</span></span>

<span data-ttu-id="a73f6-111">Значение, указывающее период времени, в течение которого планировщик задач будет ожидать наступления условия простоя.</span><span class="sxs-lookup"><span data-stu-id="a73f6-111">A value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="a73f6-112">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="a73f6-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="a73f6-113">Минимальное допустимое время — 1 минута.</span><span class="sxs-lookup"><span data-stu-id="a73f6-113">The minimum time allowed is 1 minute.</span></span> <span data-ttu-id="a73f6-114">Если это значение равно **null**, то для задержки будет задано значение по умолчанию, равное 1 часу.</span><span class="sxs-lookup"><span data-stu-id="a73f6-114">If this value is **NULL**, then the delay will be set to the default of 1 hour.</span></span>

## <a name="remarks"></a><span data-ttu-id="a73f6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a73f6-115">Remarks</span></span>

<span data-ttu-id="a73f6-116">При чтении или записи XML для задачи этот параметр указывается в элементе [**ваиттимеаут**](taskschedulerschema-waittimeout-idlesettingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="a73f6-116">When reading or writing XML for a task, this setting is specified in the [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="a73f6-117">Если задача запускается триггером Idle, свойство **идлесеттингс. ваиттимеаут** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="a73f6-117">If a task is triggered by an idle trigger, then the **IdleSettings.WaitTimeout** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73f6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a73f6-118">Requirements</span></span>



| <span data-ttu-id="a73f6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a73f6-119">Requirement</span></span> | <span data-ttu-id="a73f6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a73f6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a73f6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a73f6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a73f6-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a73f6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a73f6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a73f6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a73f6-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a73f6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a73f6-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a73f6-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="a73f6-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a73f6-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a73f6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a73f6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a73f6-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a73f6-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a73f6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a73f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73f6-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a73f6-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="a73f6-131">**идлесеттингс**</span><span class="sxs-lookup"><span data-stu-id="a73f6-131">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





