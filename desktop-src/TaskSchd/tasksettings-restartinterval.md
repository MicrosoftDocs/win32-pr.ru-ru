---
title: Тасксеттингс. Рестартинтервал, свойство
description: Для создания скриптов Возвращает или задает значение, указывающее, как долго планировщик задач будет пытаться перезапустить задачу.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- планировщик задач свойства Рестартинтервал
- Планировщик задач свойства Рестартинтервал, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Рестартинтервал
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f511e43ebb1d61fd80f2fcab34aba092704b8338
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801468"
---
# <a name="tasksettingsrestartinterval-property"></a><span data-ttu-id="5804b-106">Тасксеттингс. Рестартинтервал, свойство</span><span class="sxs-lookup"><span data-stu-id="5804b-106">TaskSettings.RestartInterval property</span></span>

<span data-ttu-id="5804b-107">Для создания скриптов Возвращает или задает значение, указывающее, как долго планировщик задач будет пытаться перезапустить задачу.</span><span class="sxs-lookup"><span data-stu-id="5804b-107">For scripting, gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="5804b-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5804b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5804b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5804b-109">Syntax</span></span>


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a><span data-ttu-id="5804b-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5804b-110">Property value</span></span>

<span data-ttu-id="5804b-111">Значение, указывающее, как долго планировщик задач будет пытаться перезапустить задачу.</span><span class="sxs-lookup"><span data-stu-id="5804b-111">A value that specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="5804b-112">Если это свойство задано, также должно быть задано свойство [**рестарткаунт**](tasksettings-restartcount.md) .</span><span class="sxs-lookup"><span data-stu-id="5804b-112">If this property is set, the [**RestartCount**](tasksettings-restartcount.md) property must also be set.</span></span> <span data-ttu-id="5804b-113">Формат этой строки — P <days> DT <hours> H <minutes> <seconds> S (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут).</span><span class="sxs-lookup"><span data-stu-id="5804b-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="5804b-114">Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.</span><span class="sxs-lookup"><span data-stu-id="5804b-114">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="5804b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5804b-115">Remarks</span></span>

<span data-ttu-id="5804b-116">При чтении или записи XML для задачи этот параметр указывается в элементе [**Interval**](taskschedulerschema-interval-restarttype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="5804b-116">When reading or writing XML for a task, this setting is specified in the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5804b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5804b-117">Requirements</span></span>



| <span data-ttu-id="5804b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5804b-118">Requirement</span></span> | <span data-ttu-id="5804b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5804b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5804b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5804b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5804b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5804b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5804b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5804b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5804b-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5804b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5804b-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5804b-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="5804b-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5804b-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5804b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5804b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5804b-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5804b-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5804b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5804b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5804b-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="5804b-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





