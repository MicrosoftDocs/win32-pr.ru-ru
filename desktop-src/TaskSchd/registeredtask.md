---
title: Объект Регистередтаск
description: Объект скрипта, предоставляющий методы, которые используются для немедленного выполнения задачи, получают все выполняющиеся экземпляры задачи, получают или задают учетные данные, используемые для регистрации задачи, а также свойства, описывающие задачу.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- планировщик задач объекта Регистередтаск
- Планировщик задач объекта Регистередтаск, описание
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801504"
---
# <a name="registeredtask-object"></a><span data-ttu-id="db431-105">Объект Регистередтаск</span><span class="sxs-lookup"><span data-stu-id="db431-105">RegisteredTask object</span></span>

<span data-ttu-id="db431-106">Объект скрипта, предоставляющий методы, которые используются для немедленного выполнения задачи, получают все выполняющиеся экземпляры задачи, получают или задают учетные данные, используемые для регистрации задачи, а также свойства, описывающие задачу.</span><span class="sxs-lookup"><span data-stu-id="db431-106">Scripting object that provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the properties that describe the task.</span></span>

## <a name="members"></a><span data-ttu-id="db431-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="db431-107">Members</span></span>

<span data-ttu-id="db431-108">Объект **регистередтаск** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="db431-108">The **RegisteredTask** object has these types of members:</span></span>

-   [<span data-ttu-id="db431-109">Методы</span><span class="sxs-lookup"><span data-stu-id="db431-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="db431-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="db431-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="db431-111">Методы</span><span class="sxs-lookup"><span data-stu-id="db431-111">Methods</span></span>

<span data-ttu-id="db431-112">Объект **регистередтаск** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="db431-112">The **RegisteredTask** object has these methods.</span></span>



| <span data-ttu-id="db431-113">Метод</span><span class="sxs-lookup"><span data-stu-id="db431-113">Method</span></span>                                                                | <span data-ttu-id="db431-114">Описание</span><span class="sxs-lookup"><span data-stu-id="db431-114">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db431-115">**Экземпляры экземпляров**</span><span class="sxs-lookup"><span data-stu-id="db431-115">**GetInstances**</span></span>](registeredtask-getinstances.md)                   | <span data-ttu-id="db431-116">Возвращает все экземпляры зарегистрированной задачи, которые выполняются в данный момент.</span><span class="sxs-lookup"><span data-stu-id="db431-116">Returns all instances of the registered task that are currently running.</span></span><br/>             |
| [<span data-ttu-id="db431-117">**Среды выполнения**</span><span class="sxs-lookup"><span data-stu-id="db431-117">**GetRunTimes**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | <span data-ttu-id="db431-118">Возвращает время, которое запланировано для выполнения зарегистрированной задачи в течение заданного времени.</span><span class="sxs-lookup"><span data-stu-id="db431-118">Gets the times that the registered task is scheduled to run during a specified time.</span></span><br/> |
| [<span data-ttu-id="db431-119">**жетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="db431-119">**GetSecurityDescriptor**</span></span>](registeredtask-getsecuritydescriptor.md) | <span data-ttu-id="db431-120">Возвращает дескриптор безопасности, который используется в качестве учетных данных для зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="db431-120">Gets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="db431-121">**Выполнить**</span><span class="sxs-lookup"><span data-stu-id="db431-121">**Run**</span></span>](registeredtask-run.md)                                     | <span data-ttu-id="db431-122">Немедленно запускает зарегистрированную задачу.</span><span class="sxs-lookup"><span data-stu-id="db431-122">Runs the registered task immediately.</span></span><br/>                                                |
| [<span data-ttu-id="db431-123">**рунекс**</span><span class="sxs-lookup"><span data-stu-id="db431-123">**RunEx**</span></span>](registeredtask-runex.md)                                 | <span data-ttu-id="db431-124">Выполняет зарегистрированную задачу сразу же с помощью указанных флагов и идентификатора сеанса.</span><span class="sxs-lookup"><span data-stu-id="db431-124">Runs the registered task immediately using specified flags and a session identifier.</span></span><br/> |
| [<span data-ttu-id="db431-125">**сетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="db431-125">**SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md) | <span data-ttu-id="db431-126">Задает дескриптор безопасности, используемый в качестве учетных данных для зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="db431-126">Sets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="db431-127">**Stop**</span><span class="sxs-lookup"><span data-stu-id="db431-127">**Stop**</span></span>](registeredtask-stop.md)                                   | <span data-ttu-id="db431-128">Немедленно останавливает зарегистрированную задачу.</span><span class="sxs-lookup"><span data-stu-id="db431-128">Stops the registered task immediately.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="db431-129">Свойства</span><span class="sxs-lookup"><span data-stu-id="db431-129">Properties</span></span>

<span data-ttu-id="db431-130">Объект **регистередтаск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="db431-130">The **RegisteredTask** object has these properties.</span></span>



| <span data-ttu-id="db431-131">Свойство</span><span class="sxs-lookup"><span data-stu-id="db431-131">Property</span></span>                                                                   | <span data-ttu-id="db431-132">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="db431-132">Access type</span></span>           | <span data-ttu-id="db431-133">Описание</span><span class="sxs-lookup"><span data-stu-id="db431-133">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db431-134">**Определение**</span><span class="sxs-lookup"><span data-stu-id="db431-134">**Definition**</span></span>](registeredtask-definition.md)<br/>                 | <span data-ttu-id="db431-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db431-135">Read-only</span></span><br/>  | <span data-ttu-id="db431-136">Возвращает определение задачи.</span><span class="sxs-lookup"><span data-stu-id="db431-136">Gets the definition of the task.</span></span><br/>                                               |
| [<span data-ttu-id="db431-137">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="db431-137">**Enabled**</span></span>](registeredtask-enabled.md)<br/>                       | <span data-ttu-id="db431-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="db431-138">Read/write</span></span><br/> | <span data-ttu-id="db431-139">Возвращает или задает логическое значение, указывающее, включена ли зарегистрированная задача.</span><span class="sxs-lookup"><span data-stu-id="db431-139">Gets or set a Boolean value that indicates if the registered task is enabled.</span></span><br/>  |
| [<span data-ttu-id="db431-140">**ластрунтиме**</span><span class="sxs-lookup"><span data-stu-id="db431-140">**LastRunTime**</span></span>](registeredtask-lastruntime.md)<br/>               | <span data-ttu-id="db431-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db431-141">Read-only</span></span><br/>  | <span data-ttu-id="db431-142">Возвращает время последнего запуска зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="db431-142">Gets the time the registered task was last run.</span></span><br/>                                |
| [<span data-ttu-id="db431-143">**ласттаскресулт**</span><span class="sxs-lookup"><span data-stu-id="db431-143">**LastTaskResult**</span></span>](registeredtask-lasttaskresult.md)<br/>         | <span data-ttu-id="db431-144">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db431-144">Read-only</span></span><br/>  | <span data-ttu-id="db431-145">Возвращает результаты, которые были возвращены при последнем запуске зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="db431-145">Gets the results that were returned the last time the registered task was run.</span></span><br/> |
| [<span data-ttu-id="db431-146">**Имя**</span><span class="sxs-lookup"><span data-stu-id="db431-146">**Name**</span></span>](registeredtask-name.md)<br/>                             | <span data-ttu-id="db431-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db431-147">Read-only</span></span><br/>  | <span data-ttu-id="db431-148">Возвращает имя зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="db431-148">Gets the name of the registered task.</span></span><br/>                                          |
| [<span data-ttu-id="db431-149">**Расчетное nextruntime**</span><span class="sxs-lookup"><span data-stu-id="db431-149">**NextRunTime**</span></span>](registeredtask-nextruntime.md)<br/>               | <span data-ttu-id="db431-150">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db431-150">Read-only</span></span><br/>  | <span data-ttu-id="db431-151">Возвращает время следующего запланированного выполнения зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="db431-151">Gets the time when the registered task is next scheduled to run.</span></span><br/>               |
| [<span data-ttu-id="db431-152">**нумберофмисседрунс**</span><span class="sxs-lookup"><span data-stu-id="db431-152">**NumberOfMissedRuns**</span></span>](registeredtask-numberofmissedruns.md)<br/> | <span data-ttu-id="db431-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db431-153">Read-only</span></span><br/>  | <span data-ttu-id="db431-154">Возвращает количество случаев, когда зарегистрированная задача пропустила запланированное выполнение.</span><span class="sxs-lookup"><span data-stu-id="db431-154">Gets the number of times the registered task has missed a scheduled run.</span></span><br/>       |
| [<span data-ttu-id="db431-155">**Путь**</span><span class="sxs-lookup"><span data-stu-id="db431-155">**Path**</span></span>](registeredtask-path.md)<br/>                             | <span data-ttu-id="db431-156">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db431-156">Read-only</span></span><br/>  | <span data-ttu-id="db431-157">Возвращает путь, по которому хранится зарегистрированная задача.</span><span class="sxs-lookup"><span data-stu-id="db431-157">Gets the path to where the registered task is stored.</span></span><br/>                          |
| [<span data-ttu-id="db431-158">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="db431-158">**State**</span></span>](registeredtask-state.md)<br/>                           | <span data-ttu-id="db431-159">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db431-159">Read-only</span></span><br/>  | <span data-ttu-id="db431-160">Возвращает операционное состояние зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="db431-160">Gets the operational state of the registered task.</span></span><br/>                             |
| [<span data-ttu-id="db431-161">**XML**</span><span class="sxs-lookup"><span data-stu-id="db431-161">**XML**</span></span>](registeredtask-xml.md)<br/>                               | <span data-ttu-id="db431-162">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db431-162">Read-only</span></span><br/>  | <span data-ttu-id="db431-163">Возвращает сведения о регистрации в формате XML для зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="db431-163">Gets the XML-formatted registration information for the registered task.</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="db431-164">Примеры</span><span class="sxs-lookup"><span data-stu-id="db431-164">Examples</span></span>

<span data-ttu-id="db431-165">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии)](time-trigger-example--scripting-.md) и [Отображение имен и состояний задач (создание сценариев)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="db431-165">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) and [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db431-166">Требования</span><span class="sxs-lookup"><span data-stu-id="db431-166">Requirements</span></span>



| <span data-ttu-id="db431-167">Требование</span><span class="sxs-lookup"><span data-stu-id="db431-167">Requirement</span></span> | <span data-ttu-id="db431-168">Значение</span><span class="sxs-lookup"><span data-stu-id="db431-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db431-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db431-169">Minimum supported client</span></span><br/> | <span data-ttu-id="db431-170">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db431-170">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="db431-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db431-171">Minimum supported server</span></span><br/> | <span data-ttu-id="db431-172">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="db431-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db431-173">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="db431-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="db431-174"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="db431-174"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="db431-175">DLL</span><span class="sxs-lookup"><span data-stu-id="db431-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db431-176"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db431-176"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





