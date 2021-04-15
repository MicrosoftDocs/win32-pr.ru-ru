---
title: Объект Таскдефинитион
description: Объект скрипта, который определяет все компоненты задачи, такие как параметры задачи, триггеры, действия и сведения о регистрации.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- планировщик задач объекта Таскдефинитион
- Планировщик задач объекта Таскдефинитион, описание
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534463"
---
# <a name="taskdefinition-object"></a><span data-ttu-id="ab71e-105">Объект Таскдефинитион</span><span class="sxs-lookup"><span data-stu-id="ab71e-105">TaskDefinition object</span></span>

<span data-ttu-id="ab71e-106">Объект скрипта, который определяет все компоненты задачи, такие как параметры задачи, триггеры, действия и сведения о регистрации.</span><span class="sxs-lookup"><span data-stu-id="ab71e-106">Scripting object that defines all the components of a task, such as the task settings, triggers, actions, and registration information.</span></span>

## <a name="members"></a><span data-ttu-id="ab71e-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="ab71e-107">Members</span></span>

<span data-ttu-id="ab71e-108">Объект **таскдефинитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ab71e-108">The **TaskDefinition** object has these types of members:</span></span>

-   [<span data-ttu-id="ab71e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab71e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab71e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab71e-110">Properties</span></span>

<span data-ttu-id="ab71e-111">Объект **таскдефинитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ab71e-111">The **TaskDefinition** object has these properties.</span></span>



| <span data-ttu-id="ab71e-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="ab71e-112">Property</span></span>                                                               | <span data-ttu-id="ab71e-113">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="ab71e-113">Access type</span></span>           | <span data-ttu-id="ab71e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ab71e-114">Description</span></span>                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab71e-115">**Действия**</span><span class="sxs-lookup"><span data-stu-id="ab71e-115">**Actions**</span></span>](taskdefinition-actions.md)<br/>                   | <span data-ttu-id="ab71e-116">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ab71e-116">Read/write</span></span><br/> | <span data-ttu-id="ab71e-117">Возвращает или задает коллекцию действий, выполняемых задачей.</span><span class="sxs-lookup"><span data-stu-id="ab71e-117">Gets or sets a collection of actions that are performed by the task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="ab71e-118">**Data**</span><span class="sxs-lookup"><span data-stu-id="ab71e-118">**Data**</span></span>](taskdefinition-data.md)<br/>                         | <span data-ttu-id="ab71e-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ab71e-119">Read/write</span></span><br/> | <span data-ttu-id="ab71e-120">Возвращает или задает данные, связанные с задачей.</span><span class="sxs-lookup"><span data-stu-id="ab71e-120">Gets or sets the data that is associated with the task.</span></span> <span data-ttu-id="ab71e-121">Эти данные пропускаются службой планировщик задач, но используются сторонними производителями, которые хотят расширить формат задачи.</span><span class="sxs-lookup"><span data-stu-id="ab71e-121">This data is ignored by the Task Scheduler service, but is used by third-parties who wish to extend the task format.</span></span><br/> |
| [<span data-ttu-id="ab71e-122">**Основного**</span><span class="sxs-lookup"><span data-stu-id="ab71e-122">**Principal**</span></span>](taskdefinition-principal.md)<br/>               | <span data-ttu-id="ab71e-123">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ab71e-123">Read/write</span></span><br/> | <span data-ttu-id="ab71e-124">Возвращает или задает участника задачи, предоставляющей учетные данные безопасности для задачи.</span><span class="sxs-lookup"><span data-stu-id="ab71e-124">Gets or sets the principal for the task that provides the security credentials for the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="ab71e-125">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="ab71e-125">**RegistrationInfo**</span></span>](taskdefinition-registrationinfo.md)<br/> | <span data-ttu-id="ab71e-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ab71e-126">Read/write</span></span><br/> | <span data-ttu-id="ab71e-127">Возвращает или задает сведения о регистрации, используемые для описания задачи, например описание задачи, автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="ab71e-127">Gets or sets the registration information that is used to describe a task, such as the description of the task, the author of the task, and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="ab71e-128">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ab71e-128">**Settings**</span></span>](taskdefinition-settings.md)<br/>                 | <span data-ttu-id="ab71e-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ab71e-129">Read/write</span></span><br/> | <span data-ttu-id="ab71e-130">Возвращает или задает параметры, определяющие, как служба планировщик задач выполняет задачу.</span><span class="sxs-lookup"><span data-stu-id="ab71e-130">Gets or sets the settings that define how the Task Scheduler service performs the task.</span></span><br/>                                                                                      |
| [<span data-ttu-id="ab71e-131">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="ab71e-131">**Triggers**</span></span>](taskdefinition-triggers.md)<br/>                 | <span data-ttu-id="ab71e-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ab71e-132">Read/write</span></span><br/> | <span data-ttu-id="ab71e-133">Возвращает или задает коллекцию триггеров, которые используются для запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="ab71e-133">Gets or sets a collection of triggers that are used to start a task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="ab71e-134">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="ab71e-134">**XmlText**</span></span>](taskdefinition-xmltext.md)<br/>                   | <span data-ttu-id="ab71e-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ab71e-135">Read/write</span></span><br/> | <span data-ttu-id="ab71e-136">Возвращает или задает определение задачи в формате XML.</span><span class="sxs-lookup"><span data-stu-id="ab71e-136">Gets or sets the XML-formatted definition of the task.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="ab71e-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab71e-137">Remarks</span></span>

<span data-ttu-id="ab71e-138">При чтении или записи собственного XML-кода для задачи определение задачи указывается с помощью элемента [**Task**](taskschedulerschema-task-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="ab71e-138">When reading or writing your own XML for a task, a task definition is specified using the [**Task**](taskschedulerschema-task-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="ab71e-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="ab71e-139">Examples</span></span>

<span data-ttu-id="ab71e-140">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии](time-trigger-example--scripting-.md) ), пример триггера [события (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))сценарии) [, пример ежедневного триггера](daily-trigger-example--scripting-.md)(сценарии), пример триггера [регистрации](registration-trigger-example--scripting-.md)(сценарии) [, пример](weekly-trigger-example--scripting-.md)триггера [входа](logon-trigger-example--scripting-.md)(скрипт), пример триггера [загрузки](boot-trigger-example--scripting-.md)(скрипт).</span><span class="sxs-lookup"><span data-stu-id="ab71e-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab71e-141">Требования</span><span class="sxs-lookup"><span data-stu-id="ab71e-141">Requirements</span></span>



| <span data-ttu-id="ab71e-142">Требование</span><span class="sxs-lookup"><span data-stu-id="ab71e-142">Requirement</span></span> | <span data-ttu-id="ab71e-143">Значение</span><span class="sxs-lookup"><span data-stu-id="ab71e-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab71e-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab71e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ab71e-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab71e-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ab71e-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab71e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ab71e-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab71e-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab71e-148">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ab71e-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab71e-149"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ab71e-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ab71e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ab71e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab71e-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab71e-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





