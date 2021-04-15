---
title: Объект Руннингтаск
description: Объект скрипта, предоставляющий методы для получения информации из выполняемой задачи и управления ей.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- планировщик задач объекта Руннингтаск
- Планировщик задач объекта Руннингтаск, описание
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534595"
---
# <a name="runningtask-object"></a><span data-ttu-id="bc45b-105">Объект Руннингтаск</span><span class="sxs-lookup"><span data-stu-id="bc45b-105">RunningTask object</span></span>

<span data-ttu-id="bc45b-106">Объект скрипта, предоставляющий методы для получения информации из выполняемой задачи и управления ей.</span><span class="sxs-lookup"><span data-stu-id="bc45b-106">Scripting object that provides the methods to get information from and control a running task.</span></span>

## <a name="members"></a><span data-ttu-id="bc45b-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="bc45b-107">Members</span></span>

<span data-ttu-id="bc45b-108">Объект **руннингтаск** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bc45b-108">The **RunningTask** object has these types of members:</span></span>

-   [<span data-ttu-id="bc45b-109">Методы</span><span class="sxs-lookup"><span data-stu-id="bc45b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc45b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="bc45b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc45b-111">Методы</span><span class="sxs-lookup"><span data-stu-id="bc45b-111">Methods</span></span>

<span data-ttu-id="bc45b-112">Объект **руннингтаск** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="bc45b-112">The **RunningTask** object has these methods.</span></span>



| <span data-ttu-id="bc45b-113">Метод</span><span class="sxs-lookup"><span data-stu-id="bc45b-113">Method</span></span>                                 | <span data-ttu-id="bc45b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bc45b-114">Description</span></span>                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="bc45b-115">**Обновить**</span><span class="sxs-lookup"><span data-stu-id="bc45b-115">**Refresh**</span></span>](runningtask-refresh.md) | <span data-ttu-id="bc45b-116">Обновляет все локальные переменные экземпляра задачи.</span><span class="sxs-lookup"><span data-stu-id="bc45b-116">Refreshes all of the local instance variables of the task.</span></span><br/> |
| [<span data-ttu-id="bc45b-117">**Stop**</span><span class="sxs-lookup"><span data-stu-id="bc45b-117">**Stop**</span></span>](runningtask-stop.md)       | <span data-ttu-id="bc45b-118">Останавливает этот экземпляр задачи.</span><span class="sxs-lookup"><span data-stu-id="bc45b-118">Stops this instance of the task.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="bc45b-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="bc45b-119">Properties</span></span>

<span data-ttu-id="bc45b-120">Объект **руннингтаск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bc45b-120">The **RunningTask** object has these properties.</span></span>



| <span data-ttu-id="bc45b-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="bc45b-121">Property</span></span>                                                      | <span data-ttu-id="bc45b-122">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="bc45b-122">Access type</span></span>          | <span data-ttu-id="bc45b-123">Описание</span><span class="sxs-lookup"><span data-stu-id="bc45b-123">Description</span></span>                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc45b-124">**куррентактион**</span><span class="sxs-lookup"><span data-stu-id="bc45b-124">**CurrentAction**</span></span>](runningtask-currentaction.md)<br/> | <span data-ttu-id="bc45b-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc45b-125">Read-only</span></span><br/> | <span data-ttu-id="bc45b-126">Возвращает имя текущего действия, выполняемого выполняющейся задачей.</span><span class="sxs-lookup"><span data-stu-id="bc45b-126">Gets the name of the current action that the running task is performing.</span></span><br/> |
| [<span data-ttu-id="bc45b-127">**енгинепид**</span><span class="sxs-lookup"><span data-stu-id="bc45b-127">**EnginePID**</span></span>](runningtask-enginepid.md)<br/>         | <span data-ttu-id="bc45b-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc45b-128">Read-only</span></span><br/> | <span data-ttu-id="bc45b-129">Возвращает идентификатор процесса для подсистемы (процесса), выполняющей задачу.</span><span class="sxs-lookup"><span data-stu-id="bc45b-129">Gets the process ID for the engine (process) which is running the task.</span></span><br/>  |
| [<span data-ttu-id="bc45b-130">**инстанцегуид**</span><span class="sxs-lookup"><span data-stu-id="bc45b-130">**InstanceGuid**</span></span>](runningtask-instanceguid.md)<br/>   | <span data-ttu-id="bc45b-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc45b-131">Read-only</span></span><br/> | <span data-ttu-id="bc45b-132">Возвращает идентификатор GUID для этого экземпляра задачи.</span><span class="sxs-lookup"><span data-stu-id="bc45b-132">Gets the GUID identifier for this instance of the task.</span></span><br/>                  |
| [<span data-ttu-id="bc45b-133">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bc45b-133">**Name**</span></span>](runningtask-name.md)<br/>                   | <span data-ttu-id="bc45b-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc45b-134">Read-only</span></span><br/> | <span data-ttu-id="bc45b-135">Возвращает имя задачи.</span><span class="sxs-lookup"><span data-stu-id="bc45b-135">Gets the name of the task.</span></span><br/>                                               |
| [<span data-ttu-id="bc45b-136">**Путь**</span><span class="sxs-lookup"><span data-stu-id="bc45b-136">**Path**</span></span>](runningtask-path.md)<br/>                   | <span data-ttu-id="bc45b-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc45b-137">Read-only</span></span><br/> | <span data-ttu-id="bc45b-138">Возвращает путь, по которому хранится задача.</span><span class="sxs-lookup"><span data-stu-id="bc45b-138">Gets the path to where the task is stored.</span></span><br/>                               |
| [<span data-ttu-id="bc45b-139">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="bc45b-139">**State**</span></span>](runningtask-state.md)<br/>                 | <span data-ttu-id="bc45b-140">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc45b-140">Read-only</span></span><br/> | <span data-ttu-id="bc45b-141">Возвращает состояние выполняющейся задачи.</span><span class="sxs-lookup"><span data-stu-id="bc45b-141">Gets the state of the running task.</span></span> <br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="bc45b-142">Требования</span><span class="sxs-lookup"><span data-stu-id="bc45b-142">Requirements</span></span>



| <span data-ttu-id="bc45b-143">Требование</span><span class="sxs-lookup"><span data-stu-id="bc45b-143">Requirement</span></span> | <span data-ttu-id="bc45b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="bc45b-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc45b-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc45b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bc45b-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc45b-146">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bc45b-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc45b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bc45b-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc45b-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc45b-149">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bc45b-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc45b-150"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bc45b-150"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bc45b-151">DLL</span><span class="sxs-lookup"><span data-stu-id="bc45b-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc45b-152"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc45b-152"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc45b-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc45b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc45b-154">планировщик задач объекты</span><span class="sxs-lookup"><span data-stu-id="bc45b-154">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="bc45b-155">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="bc45b-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="bc45b-156">**руннингтаскколлектион**</span><span class="sxs-lookup"><span data-stu-id="bc45b-156">**RunningTaskCollection**</span></span>](runningtaskcollection.md)
</dt> <dt>

[<span data-ttu-id="bc45b-157">**Регистередтаск. Run**</span><span class="sxs-lookup"><span data-stu-id="bc45b-157">**RegisteredTask.Run**</span></span>](registeredtask-run.md)
</dt> <dt>

[<span data-ttu-id="bc45b-158">**Регистередтаск. Рунекс**</span><span class="sxs-lookup"><span data-stu-id="bc45b-158">**RegisteredTask.RunEx**</span></span>](registeredtask-runex.md)
</dt> </dl>

 

 





