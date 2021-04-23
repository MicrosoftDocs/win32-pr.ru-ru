---
title: Объект TaskService
description: Для сценариев предоставляет доступ к службе планировщик задач для управления зарегистрированными задачами.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- планировщик задач объекта TaskService
- Планировщик задач объекта TaskService, описание
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492264"
---
# <a name="taskservice-object"></a><span data-ttu-id="e6620-105">Объект TaskService</span><span class="sxs-lookup"><span data-stu-id="e6620-105">TaskService object</span></span>

<span data-ttu-id="e6620-106">Для сценариев предоставляет доступ к службе планировщик задач для управления зарегистрированными задачами.</span><span class="sxs-lookup"><span data-stu-id="e6620-106">For scripting, provides access to the Task Scheduler service for managing registered tasks.</span></span>

<span data-ttu-id="e6620-107">Метод [**TaskService. Connect**](taskservice-connect.md) следует вызывать до вызова любого из других методов **TaskService** .</span><span class="sxs-lookup"><span data-stu-id="e6620-107">The [**TaskService.Connect**](taskservice-connect.md) method should be called before calling any of the other **TaskService** methods.</span></span>

## <a name="members"></a><span data-ttu-id="e6620-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="e6620-108">Members</span></span>

<span data-ttu-id="e6620-109">Объект **TaskService** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e6620-109">The **TaskService** object has these types of members:</span></span>

-   [<span data-ttu-id="e6620-110">Методы</span><span class="sxs-lookup"><span data-stu-id="e6620-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6620-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e6620-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e6620-112">Методы</span><span class="sxs-lookup"><span data-stu-id="e6620-112">Methods</span></span>

<span data-ttu-id="e6620-113">Объект **TaskService** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="e6620-113">The **TaskService** object has these methods.</span></span>



| <span data-ttu-id="e6620-114">Метод</span><span class="sxs-lookup"><span data-stu-id="e6620-114">Method</span></span>                                                 | <span data-ttu-id="e6620-115">Описание</span><span class="sxs-lookup"><span data-stu-id="e6620-115">Description</span></span>                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6620-116">**Подключение**</span><span class="sxs-lookup"><span data-stu-id="e6620-116">**Connect**</span></span>](taskservice-connect.md)                 | <span data-ttu-id="e6620-117">Подключается к удаленному компьютеру и связывает все последующие вызовы в этом интерфейсе с удаленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="e6620-117">Connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="e6620-118">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="e6620-118">**GetFolder**</span></span>](taskservice-getfolder.md)             | <span data-ttu-id="e6620-119">Возвращает путь к папке зарегистрированных задач.</span><span class="sxs-lookup"><span data-stu-id="e6620-119">Gets the path to a folder of registered tasks.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="e6620-120">**жетруннингтаскс**</span><span class="sxs-lookup"><span data-stu-id="e6620-120">**GetRunningTasks**</span></span>](taskservice-getrunningtasks.md) | <span data-ttu-id="e6620-121">Возвращает коллекцию выполняющихся задач.</span><span class="sxs-lookup"><span data-stu-id="e6620-121">Gets a collection of running tasks.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="e6620-122">**NewTask**</span><span class="sxs-lookup"><span data-stu-id="e6620-122">**NewTask**</span></span>](taskservice-newtask.md)                 | <span data-ttu-id="e6620-123">Возвращает пустой объект определения задачи, который заполняется параметрами и свойствами, а затем регистрируется с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="e6620-123">Returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e6620-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="e6620-124">Properties</span></span>

<span data-ttu-id="e6620-125">Объект **TaskService** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e6620-125">The **TaskService** object has these properties.</span></span>



| <span data-ttu-id="e6620-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="e6620-126">Property</span></span>                                                          | <span data-ttu-id="e6620-127">Описание</span><span class="sxs-lookup"><span data-stu-id="e6620-127">Description</span></span>                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6620-128">**Подключен**</span><span class="sxs-lookup"><span data-stu-id="e6620-128">**Connected**</span></span>](taskservice-connected.md)<br/>             | <span data-ttu-id="e6620-129">Возвращает логическое значение, указывающее, установлено ли соединение со службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="e6620-129">Gets a Boolean value that indicates if you are connected to the Task Scheduler service.</span></span><br/>                          |
| [<span data-ttu-id="e6620-130">**коннектеддомаин**</span><span class="sxs-lookup"><span data-stu-id="e6620-130">**ConnectedDomain**</span></span>](taskservice-connecteddomain.md)<br/> | <span data-ttu-id="e6620-131">Возвращает имя домена, к которому подключен компьютер [**TargetServer**](taskservice-targetserver.md) .</span><span class="sxs-lookup"><span data-stu-id="e6620-131">Gets the name of the domain to which the [**TargetServer**](taskservice-targetserver.md) computer is connected.</span></span><br/> |
| [<span data-ttu-id="e6620-132">**коннектедусер**</span><span class="sxs-lookup"><span data-stu-id="e6620-132">**ConnectedUser**</span></span>](taskservice-connecteduser.md)<br/>     | <span data-ttu-id="e6620-133">Возвращает имя пользователя, подключенного к службе планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="e6620-133">Gets the name of the user that is connected to the Task Scheduler service.</span></span><br/>                                       |
| <span data-ttu-id="e6620-134">хигхестверсион</span><span class="sxs-lookup"><span data-stu-id="e6620-134">HighestVersion</span></span><br/>                                         | <span data-ttu-id="e6620-135">Возвращает самую новую версию планировщик задач, поддерживаемую компьютером.</span><span class="sxs-lookup"><span data-stu-id="e6620-135">Gets the highest version of Task Scheduler that a computer supports.</span></span><br/>                                             |
| [<span data-ttu-id="e6620-136">**TargetServer**</span><span class="sxs-lookup"><span data-stu-id="e6620-136">**TargetServer**</span></span>](taskservice-targetserver.md)<br/>       | <span data-ttu-id="e6620-137">Возвращает имя компьютера, на котором запущена служба планировщик задач, к которой подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="e6620-137">Gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span><br/>          |



 

## <a name="examples"></a><span data-ttu-id="e6620-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="e6620-138">Examples</span></span>

<span data-ttu-id="e6620-139">Дополнительные сведения и примеры кода для этого объекта скрипта см. [пример триггера времени (сценарии)](time-trigger-example--scripting-.md), [пример триггера события (сценарии)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Пример ежедневного триггера (сценарии](daily-trigger-example--scripting-.md)), пример триггера [регистрации](registration-trigger-example--scripting-.md)(сценарии), пример триггера с [расписанием](weekly-trigger-example--scripting-.md)(скрипт), пример триггера [входа](logon-trigger-example--scripting-.md)(скрипт), пример триггера [загрузки](boot-trigger-example--scripting-.md)(сценарии), [а также имена и состояния задач (сценарии)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="e6620-139">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6620-140">Требования</span><span class="sxs-lookup"><span data-stu-id="e6620-140">Requirements</span></span>



| <span data-ttu-id="e6620-141">Требование</span><span class="sxs-lookup"><span data-stu-id="e6620-141">Requirement</span></span> | <span data-ttu-id="e6620-142">Значение</span><span class="sxs-lookup"><span data-stu-id="e6620-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6620-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6620-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e6620-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6620-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e6620-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6620-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e6620-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6620-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6620-147">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e6620-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6620-148"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e6620-148"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e6620-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e6620-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6620-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6620-150"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6620-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6620-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6620-152">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="e6620-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





