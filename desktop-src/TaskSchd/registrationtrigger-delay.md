---
title: Регистратионтригжер. Delay, свойство
description: Для сценариев Возвращает или задает промежуток времени между регистрацией задачи и началом задачи.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- планировщик задач свойства Delay
- Свойство Delay планировщик задач, объект Регистратионтригжер
- Планировщик задач объекта Регистратионтригжер, свойство Delay
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534988"
---
# <a name="registrationtriggerdelay-property"></a><span data-ttu-id="0b2dc-106">Регистратионтригжер. Delay, свойство</span><span class="sxs-lookup"><span data-stu-id="0b2dc-106">RegistrationTrigger.Delay property</span></span>

<span data-ttu-id="0b2dc-107">Для сценариев Возвращает или задает промежуток времени между регистрацией задачи и началом задачи.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-107">For scripting, gets or sets the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="0b2dc-108">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="0b2dc-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b2dc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b2dc-109">Syntax</span></span>


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="0b2dc-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0b2dc-110">Property value</span></span>

<span data-ttu-id="0b2dc-111">Промежуток времени между регистрацией системы и временем запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-111">The amount of time between when the system is registered and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b2dc-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b2dc-112">Remarks</span></span>

<span data-ttu-id="0b2dc-113">При чтении или записи XML для задачи задержка загрузки указывается с помощью элемента [**delay**](taskschedulerschema-delay-registrationtriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-113">When reading or writing XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="0b2dc-114">Если регистрируется задача с триггером отложенной регистрации и компьютер, на котором зарегистрирована задача, завершается или перезапускается во время задержки, перед выполнением задачи Выполнение задачи не выполняется и задержка будет потеряна.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-114">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b2dc-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0b2dc-115">Requirements</span></span>



| <span data-ttu-id="0b2dc-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0b2dc-116">Requirement</span></span> | <span data-ttu-id="0b2dc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0b2dc-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b2dc-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b2dc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0b2dc-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b2dc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0b2dc-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b2dc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0b2dc-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b2dc-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0b2dc-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0b2dc-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b2dc-123"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0b2dc-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0b2dc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0b2dc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b2dc-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b2dc-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b2dc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b2dc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b2dc-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="0b2dc-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





