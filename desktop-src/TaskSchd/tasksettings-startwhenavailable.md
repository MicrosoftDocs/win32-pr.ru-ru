---
title: Тасксеттингс. Стартвхенаваилабле, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- планировщик задач свойства Стартвхенаваилабле
- Планировщик задач свойства Стартвхенаваилабле, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Стартвхенаваилабле
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492255"
---
# <a name="tasksettingsstartwhenavailable-property"></a><span data-ttu-id="66611-106">Тасксеттингс. Стартвхенаваилабле, свойство</span><span class="sxs-lookup"><span data-stu-id="66611-106">TaskSettings.StartWhenAvailable property</span></span>

<span data-ttu-id="66611-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.</span><span class="sxs-lookup"><span data-stu-id="66611-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

<span data-ttu-id="66611-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="66611-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="66611-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66611-109">Syntax</span></span>


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="66611-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="66611-110">Property value</span></span>

<span data-ttu-id="66611-111">Если значение — true, свойство указывает, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.</span><span class="sxs-lookup"><span data-stu-id="66611-111">If True, the property indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span> <span data-ttu-id="66611-112">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="66611-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="66611-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66611-113">Remarks</span></span>

<span data-ttu-id="66611-114">Это свойство применяется только к задачам, основанным на времени, с конечной границей и задачами на основе времени, которые настроены для повтора бесконечности.</span><span class="sxs-lookup"><span data-stu-id="66611-114">This property applies only to time-based tasks with an end boundary or time-based tasks that are set to repeat infinitely.</span></span>

<span data-ttu-id="66611-115">Задачи, запускаемые после истечения запланированного времени (из-за того, что свойство [**стартвхенаваилабле**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) имеет значение true), помещаются в очередь задач Планировщик задач службы и запускаются после некоторой задержки.</span><span class="sxs-lookup"><span data-stu-id="66611-115">Tasks that are started after the scheduled time has passed (because of the [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) property being set to True) are queued in the Task Scheduler service's queue of tasks and they are started after a delay.</span></span> <span data-ttu-id="66611-116">Задержка по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="66611-116">The default delay is 10 minutes.</span></span>

<span data-ttu-id="66611-117">При чтении или записи XML для задачи этот параметр указывается в элементе [**стартвхенаваилабле**](taskschedulerschema-startwhenavailable-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="66611-117">When reading or writing XML for a task, this setting is specified in the [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="66611-118">Требования</span><span class="sxs-lookup"><span data-stu-id="66611-118">Requirements</span></span>



| <span data-ttu-id="66611-119">Требование</span><span class="sxs-lookup"><span data-stu-id="66611-119">Requirement</span></span> | <span data-ttu-id="66611-120">Значение</span><span class="sxs-lookup"><span data-stu-id="66611-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66611-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66611-121">Minimum supported client</span></span><br/> | <span data-ttu-id="66611-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66611-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="66611-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66611-123">Minimum supported server</span></span><br/> | <span data-ttu-id="66611-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66611-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66611-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="66611-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="66611-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="66611-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="66611-127">DLL</span><span class="sxs-lookup"><span data-stu-id="66611-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66611-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66611-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66611-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66611-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66611-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="66611-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





