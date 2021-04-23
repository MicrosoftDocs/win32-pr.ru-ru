---
title: Логонтригжер. Delay, свойство
description: Для создания скриптов Возвращает или задает значение, указывающее промежуток времени между входом пользователя в систему и запуском задачи.
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- планировщик задач свойства Delay
- Свойство Delay планировщик задач, объект Логонтригжер
- Планировщик задач объекта Логонтригжер, свойство Delay
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414984"
---
# <a name="logontriggerdelay-property"></a><span data-ttu-id="a8c8e-106">Логонтригжер. Delay, свойство</span><span class="sxs-lookup"><span data-stu-id="a8c8e-106">LogonTrigger.Delay property</span></span>

<span data-ttu-id="a8c8e-107">Для создания скриптов Возвращает или задает значение, указывающее промежуток времени между входом пользователя в систему и запуском задачи.</span><span class="sxs-lookup"><span data-stu-id="a8c8e-107">For scripting, gets or sets a value that indicates the amount of time between when the user logs on and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c8e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8c8e-108">Syntax</span></span>


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="a8c8e-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a8c8e-109">Property value</span></span>

<span data-ttu-id="a8c8e-110">Значение, указывающее промежуток времени между входом пользователя в систему и запуском задачи.</span><span class="sxs-lookup"><span data-stu-id="a8c8e-110">A value that indicates the amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="a8c8e-111">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="a8c8e-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8c8e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8c8e-112">Remarks</span></span>

<span data-ttu-id="a8c8e-113">При чтении или записи XML для задачи задержка триггера входа задается с помощью элемента [**delay**](taskschedulerschema-delay-logontriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="a8c8e-113">When reading or writing XML for a task, the logon trigger delay is specified using the [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c8e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a8c8e-114">Requirements</span></span>



| <span data-ttu-id="a8c8e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a8c8e-115">Requirement</span></span> | <span data-ttu-id="a8c8e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a8c8e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c8e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8c8e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c8e-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8c8e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a8c8e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8c8e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c8e-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8c8e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a8c8e-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a8c8e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8c8e-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a8c8e-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a8c8e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a8c8e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8c8e-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8c8e-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8c8e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8c8e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c8e-126">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="a8c8e-126">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="a8c8e-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a8c8e-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





