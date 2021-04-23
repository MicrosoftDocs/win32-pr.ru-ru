---
title: Буттригжер. Delay, свойство
description: Для создания скриптов Возвращает или задает значение, указывающее промежуток времени между загрузкой системы и временем запуска задачи.
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- планировщик задач свойства Delay
- Свойство Delay планировщик задач, объект Буттригжер
- Планировщик задач объекта Буттригжер, свойство Delay
topic_type:
- apiref
api_name:
- BootTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6be91f00b79f2c2a47235a389b82ffb9255d586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136558"
---
# <a name="boottriggerdelay-property"></a><span data-ttu-id="5c771-106">Буттригжер. Delay, свойство</span><span class="sxs-lookup"><span data-stu-id="5c771-106">BootTrigger.Delay property</span></span>

<span data-ttu-id="5c771-107">Для создания скриптов Возвращает или задает значение, указывающее промежуток времени между загрузкой системы и временем запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="5c771-107">For scripting, gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c771-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c771-108">Syntax</span></span>


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="5c771-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5c771-109">Property value</span></span>

<span data-ttu-id="5c771-110">Значение, указывающее промежуток времени между загрузкой системы и началом задачи.</span><span class="sxs-lookup"><span data-stu-id="5c771-110">A value that indicates the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="5c771-111">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="5c771-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c771-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c771-112">Remarks</span></span>

<span data-ttu-id="5c771-113">При чтении или записи собственного XML-кода для задачи задержка загрузки указывается с помощью элемента [**delay**](taskschedulerschema-delay-boottriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="5c771-113">When reading or writing your own XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c771-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5c771-114">Requirements</span></span>



| <span data-ttu-id="5c771-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5c771-115">Requirement</span></span> | <span data-ttu-id="5c771-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5c771-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c771-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c771-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5c771-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c771-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5c771-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c771-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5c771-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c771-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c771-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5c771-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c771-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c771-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5c771-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5c771-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c771-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c771-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c771-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c771-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c771-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="5c771-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="5c771-127">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="5c771-127">**BootTrigger**</span></span>](boottrigger.md)
</dt> </dl>

 

 





