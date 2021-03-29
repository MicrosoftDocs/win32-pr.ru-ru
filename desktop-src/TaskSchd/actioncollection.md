---
title: Объект ActionCollection
description: Объект скрипта, содержащий действия, выполняемые задачей.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- действия планировщик задач, объект Collection
- планировщик задач объекта ActionCollection
- Планировщик задач объекта ActionCollection, описание
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535507"
---
# <a name="actioncollection-object"></a><span data-ttu-id="fd248-106">Объект ActionCollection</span><span class="sxs-lookup"><span data-stu-id="fd248-106">ActionCollection object</span></span>

<span data-ttu-id="fd248-107">Объект скрипта, содержащий действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="fd248-107">Scripting object that contains the actions performed by the task.</span></span>

## <a name="members"></a><span data-ttu-id="fd248-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="fd248-108">Members</span></span>

<span data-ttu-id="fd248-109">Объект **ActionCollection** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fd248-109">The **ActionCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="fd248-110">Методы</span><span class="sxs-lookup"><span data-stu-id="fd248-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="fd248-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="fd248-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fd248-112">Методы</span><span class="sxs-lookup"><span data-stu-id="fd248-112">Methods</span></span>

<span data-ttu-id="fd248-113">Объект **ActionCollection** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="fd248-113">The **ActionCollection** object has these methods.</span></span>



| <span data-ttu-id="fd248-114">Метод</span><span class="sxs-lookup"><span data-stu-id="fd248-114">Method</span></span>                                    | <span data-ttu-id="fd248-115">Описание</span><span class="sxs-lookup"><span data-stu-id="fd248-115">Description</span></span>                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="fd248-116">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="fd248-116">**Clear**</span></span>](actioncollection-clear.md)   | <span data-ttu-id="fd248-117">Удаляет все действия из коллекции.</span><span class="sxs-lookup"><span data-stu-id="fd248-117">Clears all the actions from the collection.</span></span><br/>      |
| [<span data-ttu-id="fd248-118">**Создать**</span><span class="sxs-lookup"><span data-stu-id="fd248-118">**Create**</span></span>](actioncollection-create.md) | <span data-ttu-id="fd248-119">Создает и добавляет новое действие в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="fd248-119">Creates and adds a new action to the collection.</span></span><br/> |
| [<span data-ttu-id="fd248-120">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="fd248-120">**Remove**</span></span>](actioncollection-remove.md) | <span data-ttu-id="fd248-121">Удаляет указанное действие из коллекции.</span><span class="sxs-lookup"><span data-stu-id="fd248-121">Removes a specified action from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="fd248-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="fd248-122">Properties</span></span>

<span data-ttu-id="fd248-123">Объект **ActionCollection** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fd248-123">The **ActionCollection** object has these properties.</span></span>



| <span data-ttu-id="fd248-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="fd248-124">Property</span></span>                                               | <span data-ttu-id="fd248-125">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="fd248-125">Access type</span></span>           | <span data-ttu-id="fd248-126">Описание</span><span class="sxs-lookup"><span data-stu-id="fd248-126">Description</span></span>                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="fd248-127">**Контекст**</span><span class="sxs-lookup"><span data-stu-id="fd248-127">**Context**</span></span>](actioncollection-context.md)<br/> | <span data-ttu-id="fd248-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="fd248-128">Read/write</span></span><br/> | <span data-ttu-id="fd248-129">Возвращает или задает идентификатор участника для задачи.</span><span class="sxs-lookup"><span data-stu-id="fd248-129">Gets or sets the identifier of the principal for the task.</span></span><br/> |
| [<span data-ttu-id="fd248-130">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="fd248-130">**Count**</span></span>](actioncollection-count.md)<br/>     | <span data-ttu-id="fd248-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="fd248-131">Read-only</span></span><br/>  | <span data-ttu-id="fd248-132">Возвращает количество действий в коллекции.</span><span class="sxs-lookup"><span data-stu-id="fd248-132">Gets the number of actions in the collection.</span></span><br/>              |
| [<span data-ttu-id="fd248-133">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fd248-133">**Item**</span></span>](actioncollection-item.md)<br/>       | <span data-ttu-id="fd248-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="fd248-134">Read-only</span></span><br/>  | <span data-ttu-id="fd248-135">Возвращает указанное действие из коллекции.</span><span class="sxs-lookup"><span data-stu-id="fd248-135">Gets a specified action from the collection.</span></span><br/>               |
| [<span data-ttu-id="fd248-136">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="fd248-136">**XmlText**</span></span>](actioncollection-xmltext.md)<br/> | <span data-ttu-id="fd248-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="fd248-137">Read/write</span></span><br/> | <span data-ttu-id="fd248-138">Возвращает или задает версию коллекции в формате XML.</span><span class="sxs-lookup"><span data-stu-id="fd248-138">Gets or sets an XML-formatted version of the collection.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="fd248-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd248-139">Remarks</span></span>

<span data-ttu-id="fd248-140">При чтении или записи XML действия задачи указываются в элементе [**Actions**](taskschedulerschema-actions-tasktype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="fd248-140">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="fd248-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd248-141">Examples</span></span>

<span data-ttu-id="fd248-142">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии](time-trigger-example--scripting-.md)), пример триггера [события (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))сценарии) [, пример ежедневного триггера](daily-trigger-example--scripting-.md)(сценарии), пример триггера [регистрации](registration-trigger-example--scripting-.md)(сценарии) [, пример](weekly-trigger-example--scripting-.md)триггера [входа](logon-trigger-example--scripting-.md)(скрипт), пример триггера [загрузки](boot-trigger-example--scripting-.md)(скрипт).</span><span class="sxs-lookup"><span data-stu-id="fd248-142">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd248-143">Требования</span><span class="sxs-lookup"><span data-stu-id="fd248-143">Requirements</span></span>



| <span data-ttu-id="fd248-144">Требование</span><span class="sxs-lookup"><span data-stu-id="fd248-144">Requirement</span></span> | <span data-ttu-id="fd248-145">Значение</span><span class="sxs-lookup"><span data-stu-id="fd248-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd248-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd248-146">Minimum supported client</span></span><br/> | <span data-ttu-id="fd248-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd248-147">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fd248-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd248-148">Minimum supported server</span></span><br/> | <span data-ttu-id="fd248-149">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd248-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd248-150">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fd248-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd248-151"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fd248-151"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fd248-152">DLL</span><span class="sxs-lookup"><span data-stu-id="fd248-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd248-153"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd248-153"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





