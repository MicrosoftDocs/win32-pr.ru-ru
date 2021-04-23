---
title: Идлесеттингс. Идледуратион, свойство
description: Для создания скриптов Возвращает или задает значение, указывающее период времени, в течение которого компьютер должен находиться в состоянии простоя перед выполнением задачи.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- планировщик задач свойства Идледуратион
- Планировщик задач свойства Идледуратион, объект Идлесеттингс
- Планировщик задач объекта Идлесеттингс, свойство Идледуратион
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802992"
---
# <a name="idlesettingsidleduration-property"></a><span data-ttu-id="6a92b-106">Идлесеттингс. Идледуратион, свойство</span><span class="sxs-lookup"><span data-stu-id="6a92b-106">IdleSettings.IdleDuration property</span></span>

<span data-ttu-id="6a92b-107">Для создания скриптов Возвращает или задает значение, указывающее период времени, в течение которого компьютер должен находиться в состоянии простоя перед выполнением задачи.</span><span class="sxs-lookup"><span data-stu-id="6a92b-107">For scripting, gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a92b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a92b-108">Syntax</span></span>


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a><span data-ttu-id="6a92b-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6a92b-109">Property value</span></span>

<span data-ttu-id="6a92b-110">Значение, указывающее период времени, в течение которого компьютер должен находиться в состоянии простоя перед выполнением задачи.</span><span class="sxs-lookup"><span data-stu-id="6a92b-110">A value that indicates the amount of time that the computer must be in an idle state before the task is run).</span></span> <span data-ttu-id="6a92b-111">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="6a92b-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="6a92b-112">Минимальное значение — одна минута.</span><span class="sxs-lookup"><span data-stu-id="6a92b-112">The minimum value is one minute.</span></span> <span data-ttu-id="6a92b-113">Если это значение равно **null**, то для задержки будет задано значение по умолчанию, равное 10 минутам.</span><span class="sxs-lookup"><span data-stu-id="6a92b-113">If this value is **NULL**, then the delay will be set to the default of 10 minutes.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a92b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a92b-114">Remarks</span></span>

<span data-ttu-id="6a92b-115">При чтении или записи XML для задачи этот параметр указывается в элементе [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="6a92b-115">When reading or writing XML for a task, this setting is specified in the [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a92b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6a92b-116">Requirements</span></span>



| <span data-ttu-id="6a92b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6a92b-117">Requirement</span></span> | <span data-ttu-id="6a92b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6a92b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a92b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a92b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6a92b-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a92b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6a92b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a92b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6a92b-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a92b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a92b-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6a92b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a92b-124"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6a92b-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6a92b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6a92b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a92b-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a92b-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a92b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a92b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a92b-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="6a92b-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="6a92b-129">**идлесеттингс**</span><span class="sxs-lookup"><span data-stu-id="6a92b-129">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





