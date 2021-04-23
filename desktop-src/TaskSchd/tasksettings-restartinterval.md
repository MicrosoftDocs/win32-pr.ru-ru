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
ms.openlocfilehash: f127c5d434b5cb1e6dec6d8a3c68ee343fa00ffc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734149"
---
# <a name="tasksettingsrestartinterval-property"></a><span data-ttu-id="f8550-106">Тасксеттингс. Рестартинтервал, свойство</span><span class="sxs-lookup"><span data-stu-id="f8550-106">TaskSettings.RestartInterval property</span></span>

<span data-ttu-id="f8550-107">Для создания скриптов Возвращает или задает значение, указывающее, как долго планировщик задач будет пытаться перезапустить задачу.</span><span class="sxs-lookup"><span data-stu-id="f8550-107">For scripting, gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="f8550-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f8550-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8550-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8550-109">Syntax</span></span>


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a><span data-ttu-id="f8550-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f8550-110">Property value</span></span>

<span data-ttu-id="f8550-111">Значение, указывающее, как долго планировщик задач будет пытаться перезапустить задачу.</span><span class="sxs-lookup"><span data-stu-id="f8550-111">A value that specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="f8550-112">Если это свойство задано, также должно быть задано свойство [**рестарткаунт**](tasksettings-restartcount.md) .</span><span class="sxs-lookup"><span data-stu-id="f8550-112">If this property is set, the [**RestartCount**](tasksettings-restartcount.md) property must also be set.</span></span> <span data-ttu-id="f8550-113">Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут).</span><span class="sxs-lookup"><span data-stu-id="f8550-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="f8550-114">Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.</span><span class="sxs-lookup"><span data-stu-id="f8550-114">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8550-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="f8550-115">Remarks</span></span>

<span data-ttu-id="f8550-116">При чтении или записи XML для задачи этот параметр указывается в элементе [**Interval**](taskschedulerschema-interval-restarttype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="f8550-116">When reading or writing XML for a task, this setting is specified in the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8550-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f8550-117">Requirements</span></span>



| <span data-ttu-id="f8550-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f8550-118">Requirement</span></span> | <span data-ttu-id="f8550-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f8550-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8550-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8550-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f8550-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8550-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f8550-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8550-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f8550-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8550-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f8550-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f8550-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="f8550-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f8550-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f8550-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f8550-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8550-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8550-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8550-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8550-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8550-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="f8550-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





