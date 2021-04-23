---
title: Регистередтаск. State, свойство
description: Для сценариев возвращает операционное состояние зарегистрированной задачи.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Свойство State планировщик задач
- Свойство State планировщик задач, объект Регистередтаск
- Планировщик задач объекта Регистередтаск, свойство State
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47af082174bc6927a16760e87566f311ec9f4a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492801"
---
# <a name="registeredtaskstate-property"></a><span data-ttu-id="967e4-106">Регистередтаск. State, свойство</span><span class="sxs-lookup"><span data-stu-id="967e4-106">RegisteredTask.State property</span></span>

<span data-ttu-id="967e4-107">Для сценариев возвращает операционное состояние зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="967e4-107">For scripting, gets the operational state of the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="967e4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="967e4-108">Syntax</span></span>


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a><span data-ttu-id="967e4-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="967e4-109">Property value</span></span>

<span data-ttu-id="967e4-110">Константа [**\_ состояния задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_state) , определяющая операционное состояние задачи.</span><span class="sxs-lookup"><span data-stu-id="967e4-110">A [**TASK\_STATE**](/windows/desktop/api/taskschd/ne-taskschd-task_state) constant that defines the operational state of the task.</span></span>



| <span data-ttu-id="967e4-111">Значение</span><span class="sxs-lookup"><span data-stu-id="967e4-111">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="967e4-112">Значение</span><span class="sxs-lookup"><span data-stu-id="967e4-112">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="967e4-113"><dt>**Задача \_ \_Неизвестное состояние**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="967e4-113"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="967e4-114">Состояние задачи неизвестно.</span><span class="sxs-lookup"><span data-stu-id="967e4-114">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="967e4-115"><dt>**Задача \_ СОСТОЯНИЕ " \_ отключено**</dt> <dt>1</dt> "</span><span class="sxs-lookup"><span data-stu-id="967e4-115"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="967e4-116">Задача зарегистрирована, но отключена и ни одна из экземпляров задачи не поставлена в очередь или запущена.</span><span class="sxs-lookup"><span data-stu-id="967e4-116">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="967e4-117">Задача не может быть выполнена, пока она не будет включена.</span><span class="sxs-lookup"><span data-stu-id="967e4-117">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="967e4-118"><dt>**Задача \_ СОСТОЯНИЕ \_ поставлено в очередь**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="967e4-118"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="967e4-119">Экземпляры задачи поставлены в очередь.</span><span class="sxs-lookup"><span data-stu-id="967e4-119">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="967e4-120"><dt>**Задача \_ СОСТОЯНИЕ \_ готовности**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="967e4-120"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="967e4-121">Задача готова к выполнению, но экземпляры не поставлены в очередь или запущены.</span><span class="sxs-lookup"><span data-stu-id="967e4-121">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="967e4-122"><dt>**Задача \_ СОСТОЯНИЕ \_ выполнения**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="967e4-122"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="967e4-123">Выполняется один или несколько экземпляров задачи.</span><span class="sxs-lookup"><span data-stu-id="967e4-123">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="967e4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="967e4-124">Requirements</span></span>



| <span data-ttu-id="967e4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="967e4-125">Requirement</span></span> | <span data-ttu-id="967e4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="967e4-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="967e4-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="967e4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="967e4-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="967e4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="967e4-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="967e4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="967e4-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="967e4-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="967e4-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="967e4-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="967e4-132"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="967e4-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="967e4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="967e4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="967e4-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="967e4-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="967e4-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="967e4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967e4-136">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="967e4-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="967e4-137">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="967e4-137">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





