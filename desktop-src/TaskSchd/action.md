---
title: Объект Action
description: Объект скрипта, предоставляющий общие свойства, наследуемые всеми объектами Action.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- планировщик задач объекта действия
- Объект Action планировщик задач, описание
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534625"
---
# <a name="action-object"></a><span data-ttu-id="4df52-105">Объект Action</span><span class="sxs-lookup"><span data-stu-id="4df52-105">Action object</span></span>

<span data-ttu-id="4df52-106">Объект скрипта, предоставляющий общие свойства, наследуемые всеми объектами Action.</span><span class="sxs-lookup"><span data-stu-id="4df52-106">Scripting object that provides the common properties that are inherited by all action objects.</span></span> <span data-ttu-id="4df52-107">Объект действия создается методом [**ActionCollection. Create**](actioncollection-create.md) .</span><span class="sxs-lookup"><span data-stu-id="4df52-107">An action object is created by the [**ActionCollection.Create**](actioncollection-create.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="4df52-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="4df52-108">Members</span></span>

<span data-ttu-id="4df52-109">Объект **Action** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4df52-109">The **Action** object has these types of members:</span></span>

-   [<span data-ttu-id="4df52-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4df52-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4df52-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="4df52-111">Properties</span></span>

<span data-ttu-id="4df52-112">Объект **Action** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4df52-112">The **Action** object has these properties.</span></span>



| <span data-ttu-id="4df52-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="4df52-113">Property</span></span>                               | <span data-ttu-id="4df52-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="4df52-114">Access type</span></span>           | <span data-ttu-id="4df52-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4df52-115">Description</span></span>                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [<span data-ttu-id="4df52-116">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="4df52-116">**Id**</span></span>](action-id.md)<br/>     | <span data-ttu-id="4df52-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4df52-117">Read/write</span></span><br/> | <span data-ttu-id="4df52-118">Возвращает или задает идентификатор действия.</span><span class="sxs-lookup"><span data-stu-id="4df52-118">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="4df52-119">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4df52-119">**Type**</span></span>](action-type.md)<br/> | <span data-ttu-id="4df52-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4df52-120">Read-only</span></span><br/>  | <span data-ttu-id="4df52-121">Возвращает тип действия.</span><span class="sxs-lookup"><span data-stu-id="4df52-121">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="4df52-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4df52-122">Remarks</span></span>

<span data-ttu-id="4df52-123">Сведения о совместной работе действий и задач см. в разделе [действия задач](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4df52-123">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span> <span data-ttu-id="4df52-124">В следующей таблице содержатся объекты скрипта, представляющие действия, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="4df52-124">The following table contains the scripting objects that represent the actions that can be performed:</span></span>



| <span data-ttu-id="4df52-125">API</span><span class="sxs-lookup"><span data-stu-id="4df52-125">API</span></span>                                            | <span data-ttu-id="4df52-126">Описание</span><span class="sxs-lookup"><span data-stu-id="4df52-126">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="4df52-127">**комхандлерактион**</span><span class="sxs-lookup"><span data-stu-id="4df52-127">**ComHandlerAction**</span></span>](comhandleraction.md)   | <span data-ttu-id="4df52-128">Представляет действие, которое вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="4df52-128">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="4df52-129">**ексекактион**</span><span class="sxs-lookup"><span data-stu-id="4df52-129">**ExecAction**</span></span>](execaction.md)               | <span data-ttu-id="4df52-130">Представляет действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="4df52-130">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="4df52-131">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="4df52-131">**EmailAction**</span></span>](emailaction.md)             | <span data-ttu-id="4df52-132">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4df52-132">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="4df52-133">**шовмессажеактион**</span><span class="sxs-lookup"><span data-stu-id="4df52-133">**ShowMessageAction**</span></span>](showmessageaction.md) | <span data-ttu-id="4df52-134">Представляет действие, показывающее окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="4df52-134">Represents an action that shows a message box.</span></span>               |



 

<span data-ttu-id="4df52-135">При чтении или записи XML действия задачи указываются в элементе [**Actions**](taskschedulerschema-actions-tasktype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="4df52-135">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="4df52-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="4df52-136">Examples</span></span>

<span data-ttu-id="4df52-137">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии](time-trigger-example--scripting-.md) ), пример триггера [события (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))сценарии) [, пример ежедневного триггера](daily-trigger-example--scripting-.md)(сценарии), пример триггера [регистрации](registration-trigger-example--scripting-.md)(сценарии) [, пример](weekly-trigger-example--scripting-.md)триггера [входа](logon-trigger-example--scripting-.md)(скрипт), пример триггера [загрузки](boot-trigger-example--scripting-.md)(скрипт).</span><span class="sxs-lookup"><span data-stu-id="4df52-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4df52-138">Требования</span><span class="sxs-lookup"><span data-stu-id="4df52-138">Requirements</span></span>



| <span data-ttu-id="4df52-139">Требование</span><span class="sxs-lookup"><span data-stu-id="4df52-139">Requirement</span></span> | <span data-ttu-id="4df52-140">Значение</span><span class="sxs-lookup"><span data-stu-id="4df52-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df52-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4df52-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4df52-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4df52-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4df52-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4df52-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4df52-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4df52-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4df52-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4df52-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="4df52-146"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4df52-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4df52-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4df52-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4df52-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4df52-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df52-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4df52-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df52-150">планировщик задач объектов скрипта</span><span class="sxs-lookup"><span data-stu-id="4df52-150">Task Scheduler Scripting Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="4df52-151">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="4df52-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





