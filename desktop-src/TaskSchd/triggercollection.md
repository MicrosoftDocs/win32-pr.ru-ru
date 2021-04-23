---
title: Объект Тригжерколлектион (Windows. UI. XAML. h)
description: Объект скрипта, который используется для добавления, удаления из и получения триггеров задачи.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- триггеры планировщик задач, объект коллекции триггеров
- планировщик задач объекта Тригжерколлектион
- Планировщик задач объекта Тригжерколлектион, описание
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135507"
---
# <a name="triggercollection-object"></a><span data-ttu-id="53c71-106">Объект Тригжерколлектион</span><span class="sxs-lookup"><span data-stu-id="53c71-106">TriggerCollection object</span></span>

<span data-ttu-id="53c71-107">Объект скрипта, который используется для добавления, удаления из и получения триггеров задачи.</span><span class="sxs-lookup"><span data-stu-id="53c71-107">Scripting object that is used to add to, remove from, and retrieve the triggers of a task.</span></span>

## <a name="members"></a><span data-ttu-id="53c71-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="53c71-108">Members</span></span>

<span data-ttu-id="53c71-109">Объект **тригжерколлектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="53c71-109">The **TriggerCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="53c71-110">Методы</span><span class="sxs-lookup"><span data-stu-id="53c71-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="53c71-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="53c71-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="53c71-112">Методы</span><span class="sxs-lookup"><span data-stu-id="53c71-112">Methods</span></span>

<span data-ttu-id="53c71-113">Объект **тригжерколлектион** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="53c71-113">The **TriggerCollection** object has these methods.</span></span>



| <span data-ttu-id="53c71-114">Метод</span><span class="sxs-lookup"><span data-stu-id="53c71-114">Method</span></span>                                     | <span data-ttu-id="53c71-115">Описание</span><span class="sxs-lookup"><span data-stu-id="53c71-115">Description</span></span>                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53c71-116">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="53c71-116">**Clear**</span></span>](triggercollection-clear.md)   | <span data-ttu-id="53c71-117">Удаляет все триггеры из коллекции.</span><span class="sxs-lookup"><span data-stu-id="53c71-117">Clears all triggers from the collection.</span></span><br/>                                        |
| [<span data-ttu-id="53c71-118">**Создать**</span><span class="sxs-lookup"><span data-stu-id="53c71-118">**Create**</span></span>](triggercollection-create.md) | <span data-ttu-id="53c71-119">Создает новый триггер для задачи.</span><span class="sxs-lookup"><span data-stu-id="53c71-119">Creates a new trigger for the task.</span></span><br/>                                             |
| [<span data-ttu-id="53c71-120">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="53c71-120">**Remove**</span></span>](triggercollection-remove.md) | <span data-ttu-id="53c71-121">Удаляет указанный триггер из коллекции триггеров, используемых задачей.</span><span class="sxs-lookup"><span data-stu-id="53c71-121">Removes the specified trigger from the collection of triggers used by the task.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="53c71-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="53c71-122">Properties</span></span>

<span data-ttu-id="53c71-123">Объект **тригжерколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="53c71-123">The **TriggerCollection** object has these properties.</span></span>



| <span data-ttu-id="53c71-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="53c71-124">Property</span></span>                                            | <span data-ttu-id="53c71-125">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="53c71-125">Access type</span></span>          | <span data-ttu-id="53c71-126">Описание</span><span class="sxs-lookup"><span data-stu-id="53c71-126">Description</span></span>                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="53c71-127">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="53c71-127">**Count**</span></span>](triggercollection-count.md)<br/> | <span data-ttu-id="53c71-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="53c71-128">Read-only</span></span><br/> | <span data-ttu-id="53c71-129">Возвращает число триггеров в коллекции.</span><span class="sxs-lookup"><span data-stu-id="53c71-129">Gets the number of triggers in the collection.</span></span><br/>  |
| [<span data-ttu-id="53c71-130">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="53c71-130">**Item**</span></span>](triggercollection-item.md)<br/>   | <span data-ttu-id="53c71-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="53c71-131">Read-only</span></span><br/> | <span data-ttu-id="53c71-132">Возвращает указанный триггер из коллекции.</span><span class="sxs-lookup"><span data-stu-id="53c71-132">Gets the specified trigger from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="53c71-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53c71-133">Remarks</span></span>

<span data-ttu-id="53c71-134">При чтении или записи XML для задачи триггеры для задачи задаются в элементе [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="53c71-134">When reading or writing XML for a task, the triggers for the task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="53c71-135">Сведения о каждом типе триггера см. в разделе [типы триггеров](trigger-types.md).</span><span class="sxs-lookup"><span data-stu-id="53c71-135">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="examples"></a><span data-ttu-id="53c71-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="53c71-136">Examples</span></span>

<span data-ttu-id="53c71-137">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="53c71-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53c71-138">Требования</span><span class="sxs-lookup"><span data-stu-id="53c71-138">Requirements</span></span>



| <span data-ttu-id="53c71-139">Требование</span><span class="sxs-lookup"><span data-stu-id="53c71-139">Requirement</span></span> | <span data-ttu-id="53c71-140">Значение</span><span class="sxs-lookup"><span data-stu-id="53c71-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="53c71-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53c71-141">Minimum supported client</span></span><br/> | <span data-ttu-id="53c71-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53c71-142">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="53c71-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53c71-143">Minimum supported server</span></span><br/> | <span data-ttu-id="53c71-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53c71-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="53c71-145">Header</span><span class="sxs-lookup"><span data-stu-id="53c71-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c71-146"><dt>Windows. UI. XAML. h</dt></span><span class="sxs-lookup"><span data-stu-id="53c71-146"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="53c71-147">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="53c71-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="53c71-148"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="53c71-148"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="53c71-149">DLL</span><span class="sxs-lookup"><span data-stu-id="53c71-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53c71-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53c71-150"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="53c71-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53c71-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c71-152">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="53c71-152">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





