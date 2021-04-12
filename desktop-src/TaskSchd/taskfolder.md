---
title: Объект Таскфолдер
description: Объект скрипта, предоставляющий методы, используемые для регистрации (создания) задач в папке, удаления задач из папки и создания или удаления вложенных папок из папки.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- планировщик задач объекта Таскфолдер
- Планировщик задач объекта Таскфолдер, описание
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534985"
---
# <a name="taskfolder-object"></a><span data-ttu-id="177d9-105">Объект Таскфолдер</span><span class="sxs-lookup"><span data-stu-id="177d9-105">TaskFolder object</span></span>

<span data-ttu-id="177d9-106">Объект скрипта, предоставляющий методы, используемые для регистрации (создания) задач в папке, удаления задач из папки и создания или удаления вложенных папок из папки.</span><span class="sxs-lookup"><span data-stu-id="177d9-106">Scripting object that provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.</span></span>

## <a name="members"></a><span data-ttu-id="177d9-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="177d9-107">Members</span></span>

<span data-ttu-id="177d9-108">Объект **таскфолдер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="177d9-108">The **TaskFolder** object has these types of members:</span></span>

-   [<span data-ttu-id="177d9-109">Методы</span><span class="sxs-lookup"><span data-stu-id="177d9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="177d9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="177d9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="177d9-111">Методы</span><span class="sxs-lookup"><span data-stu-id="177d9-111">Methods</span></span>

<span data-ttu-id="177d9-112">Объект **таскфолдер** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="177d9-112">The **TaskFolder** object has these methods.</span></span>



| <span data-ttu-id="177d9-113">Метод</span><span class="sxs-lookup"><span data-stu-id="177d9-113">Method</span></span>                                                              | <span data-ttu-id="177d9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="177d9-114">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="177d9-115">**CreateFolder**</span><span class="sxs-lookup"><span data-stu-id="177d9-115">**CreateFolder**</span></span>](taskfolder-createfolder.md)                     | <span data-ttu-id="177d9-116">Создает папку для связанных задач.</span><span class="sxs-lookup"><span data-stu-id="177d9-116">Creates a folder for related tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="177d9-117">**DeleteFolder**</span><span class="sxs-lookup"><span data-stu-id="177d9-117">**DeleteFolder**</span></span>](taskfolder-deletefolder.md)                     | <span data-ttu-id="177d9-118">Удаляет вложенную папку из родительской папки.</span><span class="sxs-lookup"><span data-stu-id="177d9-118">Deletes a subfolder from the parent folder.</span></span><br/>                                                                                         |
| [<span data-ttu-id="177d9-119">**делететаск**</span><span class="sxs-lookup"><span data-stu-id="177d9-119">**DeleteTask**</span></span>](taskfolder-deletetask.md)                         | <span data-ttu-id="177d9-120">Удаляет задачу из папки.</span><span class="sxs-lookup"><span data-stu-id="177d9-120">Deletes a task from the folder.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="177d9-121">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="177d9-121">**GetFolder**</span></span>](taskfolder-getfolder.md)                           | <span data-ttu-id="177d9-122">Возвращает папку, содержащую задачи в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="177d9-122">Gets a folder that contains tasks at a specified location.</span></span><br/>                                                                          |
| [<span data-ttu-id="177d9-123">**GetFolders**</span><span class="sxs-lookup"><span data-stu-id="177d9-123">**GetFolders**</span></span>](taskfolder-getfolders.md)                         | <span data-ttu-id="177d9-124">Возвращает все вложенные папки в папке.</span><span class="sxs-lookup"><span data-stu-id="177d9-124">Gets all the subfolders in the folder.</span></span><br/>                                                                                              |
| [<span data-ttu-id="177d9-125">**жетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="177d9-125">**GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)   | <span data-ttu-id="177d9-126">Возвращает дескриптор безопасности для папки.</span><span class="sxs-lookup"><span data-stu-id="177d9-126">Gets the security descriptor for the folder.</span></span><br/>                                                                                        |
| [<span data-ttu-id="177d9-127">**Задача задания**</span><span class="sxs-lookup"><span data-stu-id="177d9-127">**GetTask**</span></span>](taskfolder-gettask.md)                               | <span data-ttu-id="177d9-128">Возвращает задачу в указанном месте в папке.</span><span class="sxs-lookup"><span data-stu-id="177d9-128">Gets a task at a specified location in a folder.</span></span><br/>                                                                                    |
| [<span data-ttu-id="177d9-129">**Задачи**</span><span class="sxs-lookup"><span data-stu-id="177d9-129">**GetTasks**</span></span>](taskfolder-gettasks.md)                             | <span data-ttu-id="177d9-130">Возвращает все задачи в папке.</span><span class="sxs-lookup"><span data-stu-id="177d9-130">Gets all the tasks in the folder.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="177d9-131">**регистертаск**</span><span class="sxs-lookup"><span data-stu-id="177d9-131">**RegisterTask**</span></span>](taskfolder-registertask.md)                     | <span data-ttu-id="177d9-132">Регистрирует (создает) новую задачу в папке с помощью XML для определения задачи.</span><span class="sxs-lookup"><span data-stu-id="177d9-132">Registers (creates) a new task in the folder using XML to define the task.</span></span><br/>                                                          |
| [<span data-ttu-id="177d9-133">**регистертаскдефинитион**</span><span class="sxs-lookup"><span data-stu-id="177d9-133">**RegisterTaskDefinition**</span></span>](taskfolder-registertaskdefinition.md) | <span data-ttu-id="177d9-134">Регистрирует (создает) задачу в указанном расположении с помощью интерфейса [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) для определения задачи.</span><span class="sxs-lookup"><span data-stu-id="177d9-134">Registers (creates) a task in a specified location using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define a task.</span></span><br/> |
| [<span data-ttu-id="177d9-135">**сетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="177d9-135">**SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)   | <span data-ttu-id="177d9-136">Задает дескриптор безопасности для папки.</span><span class="sxs-lookup"><span data-stu-id="177d9-136">Sets the security descriptor for the folder.</span></span><br/>                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="177d9-137">Свойства</span><span class="sxs-lookup"><span data-stu-id="177d9-137">Properties</span></span>

<span data-ttu-id="177d9-138">Объект **таскфолдер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="177d9-138">The **TaskFolder** object has these properties.</span></span>



| <span data-ttu-id="177d9-139">Свойство</span><span class="sxs-lookup"><span data-stu-id="177d9-139">Property</span></span>                                   | <span data-ttu-id="177d9-140">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="177d9-140">Access type</span></span>          | <span data-ttu-id="177d9-141">Описание</span><span class="sxs-lookup"><span data-stu-id="177d9-141">Description</span></span>                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="177d9-142">**Имя**</span><span class="sxs-lookup"><span data-stu-id="177d9-142">**Name**</span></span>](taskfolder-name.md)<br/> | <span data-ttu-id="177d9-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="177d9-143">Read-only</span></span><br/> | <span data-ttu-id="177d9-144">Возвращает имя, используемое для задания папки, содержащей задачу.</span><span class="sxs-lookup"><span data-stu-id="177d9-144">Gets the name that is used to identify the folder that contains a task.</span></span><br/> |
| [<span data-ttu-id="177d9-145">**Путь**</span><span class="sxs-lookup"><span data-stu-id="177d9-145">**Path**</span></span>](taskfolder-path.md)<br/> | <span data-ttu-id="177d9-146">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="177d9-146">Read-only</span></span><br/> | <span data-ttu-id="177d9-147">Возвращает путь к месту хранения папки.</span><span class="sxs-lookup"><span data-stu-id="177d9-147">Gets the path to where the folder is stored.</span></span><br/>                            |



 

## <a name="examples"></a><span data-ttu-id="177d9-148">Примеры</span><span class="sxs-lookup"><span data-stu-id="177d9-148">Examples</span></span>

<span data-ttu-id="177d9-149">Дополнительные сведения и примеры кода для этого объекта скрипта см. [пример триггера времени (сценарии)](time-trigger-example--scripting-.md), [пример триггера события (сценарии)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Пример ежедневного триггера (сценарии](daily-trigger-example--scripting-.md)), пример триггера [регистрации](registration-trigger-example--scripting-.md)(сценарии), пример триггера с [расписанием](weekly-trigger-example--scripting-.md)(скрипт), пример триггера [входа](logon-trigger-example--scripting-.md)(скрипт), пример триггера [загрузки](boot-trigger-example--scripting-.md)(сценарии), [а также имена и состояния задач (сценарии)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="177d9-149">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="177d9-150">Требования</span><span class="sxs-lookup"><span data-stu-id="177d9-150">Requirements</span></span>



| <span data-ttu-id="177d9-151">Требование</span><span class="sxs-lookup"><span data-stu-id="177d9-151">Requirement</span></span> | <span data-ttu-id="177d9-152">Значение</span><span class="sxs-lookup"><span data-stu-id="177d9-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="177d9-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="177d9-153">Minimum supported client</span></span><br/> | <span data-ttu-id="177d9-154">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="177d9-154">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="177d9-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="177d9-155">Minimum supported server</span></span><br/> | <span data-ttu-id="177d9-156">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="177d9-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="177d9-157">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="177d9-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="177d9-158"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="177d9-158"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="177d9-159">DLL</span><span class="sxs-lookup"><span data-stu-id="177d9-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="177d9-160"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="177d9-160"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="177d9-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="177d9-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="177d9-162">планировщик задач объекты</span><span class="sxs-lookup"><span data-stu-id="177d9-162">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="177d9-163">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="177d9-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





