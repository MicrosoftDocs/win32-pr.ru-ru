---
title: Actions (taskType), элемент
description: Содержит действия, выполняемые задачей.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Actions (taskType), элемент планировщик задач
- планировщик задач действий, XML
- Элемент Actions планировщик задач
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415100"
---
# <a name="actions-tasktype-element"></a><span data-ttu-id="08337-106">Actions (taskType), элемент</span><span class="sxs-lookup"><span data-stu-id="08337-106">Actions (taskType) Element</span></span>

<span data-ttu-id="08337-107">Содержит действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="08337-107">Contains the actions performed by the task.</span></span>

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

<span data-ttu-id="08337-108">Элемент **Actions** определяется сложным типом [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="08337-108">The **Actions** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="08337-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="08337-109">Parent element</span></span>



| <span data-ttu-id="08337-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="08337-110">Element</span></span>                                          | <span data-ttu-id="08337-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="08337-111">Derived from</span></span>                                                 | <span data-ttu-id="08337-112">Описание</span><span class="sxs-lookup"><span data-stu-id="08337-112">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="08337-113">**Задача**</span><span class="sxs-lookup"><span data-stu-id="08337-113">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="08337-114">**taskType**</span><span class="sxs-lookup"><span data-stu-id="08337-114">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="08337-115">Описывает задачу, выполняемую службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="08337-115">Describes the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="08337-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="08337-116">Child elements</span></span>



| <span data-ttu-id="08337-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="08337-117">Element</span></span>                                                                    | <span data-ttu-id="08337-118">Тип</span><span class="sxs-lookup"><span data-stu-id="08337-118">Type</span></span>                                                                       | <span data-ttu-id="08337-119">Описание</span><span class="sxs-lookup"><span data-stu-id="08337-119">Description</span></span>                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="08337-120">**комхандлер**</span><span class="sxs-lookup"><span data-stu-id="08337-120">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="08337-121">**комхандлертипе**</span><span class="sxs-lookup"><span data-stu-id="08337-121">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="08337-122">Указывает действие, которое вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="08337-122">Specifies an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="08337-123">**Exec**</span><span class="sxs-lookup"><span data-stu-id="08337-123">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="08337-124">**ексектипе**</span><span class="sxs-lookup"><span data-stu-id="08337-124">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="08337-125">Указывает действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="08337-125">Specifies an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="08337-126">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="08337-126">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="08337-127">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="08337-127">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="08337-128">Указывает действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="08337-128">Specifies an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="08337-129">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="08337-129">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="08337-130">**шовмессажетипе**</span><span class="sxs-lookup"><span data-stu-id="08337-130">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="08337-131">Указывает действие, которое отображает окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="08337-131">Specifies an action that shows a message box.</span></span><br/>               |



## <a name="attributes"></a><span data-ttu-id="08337-132">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="08337-132">Attributes</span></span>



| <span data-ttu-id="08337-133">Имя</span><span class="sxs-lookup"><span data-stu-id="08337-133">Name</span></span>    | <span data-ttu-id="08337-134">Тип</span><span class="sxs-lookup"><span data-stu-id="08337-134">Type</span></span> | <span data-ttu-id="08337-135">Описание</span><span class="sxs-lookup"><span data-stu-id="08337-135">Description</span></span>                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08337-136">Контекст</span><span class="sxs-lookup"><span data-stu-id="08337-136">Context</span></span> |      | <span data-ttu-id="08337-137">Идентификатор субъекта пользователя, который является контекстом безопасности для действий задачи.</span><span class="sxs-lookup"><span data-stu-id="08337-137">Principal identifier of the user who is the security context for the actions of the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="08337-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08337-138">Remarks</span></span>

<span data-ttu-id="08337-139">Дочерние элементы, перечисленные ранее (максимум 32), определяются группой [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="08337-139">The child elements listed previously (maximum 32) are defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) group.</span></span> <span data-ttu-id="08337-140">Эти элементы можно добавлять в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="08337-140">These elements can be added in any order.</span></span>

<span data-ttu-id="08337-141">Для разработки на C++ действия задачи определяются в интерфейсе [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) .</span><span class="sxs-lookup"><span data-stu-id="08337-141">For C++ development, the actions of a task are defined in the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface.</span></span>

<span data-ttu-id="08337-142">Для разработки скриптов действия задачи определяются в объекте [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="08337-142">For script development, the actions of a task are defined in the [**ActionCollection**](actioncollection.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="08337-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="08337-143">Examples</span></span>

<span data-ttu-id="08337-144">Дополнительные сведения и полный пример XML-кода для задачи, содержащей одно действие выполнения, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="08337-144">For more information and a complete example of the XML for a task that contains a single execution action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08337-145">Требования</span><span class="sxs-lookup"><span data-stu-id="08337-145">Requirements</span></span>



| <span data-ttu-id="08337-146">Требование</span><span class="sxs-lookup"><span data-stu-id="08337-146">Requirement</span></span> | <span data-ttu-id="08337-147">Значение</span><span class="sxs-lookup"><span data-stu-id="08337-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="08337-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08337-148">Minimum supported client</span></span><br/> | <span data-ttu-id="08337-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08337-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="08337-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08337-150">Minimum supported server</span></span><br/> | <span data-ttu-id="08337-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="08337-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08337-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08337-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08337-153">**taskType**</span><span class="sxs-lookup"><span data-stu-id="08337-153">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[<span data-ttu-id="08337-154">**actionGroup**</span><span class="sxs-lookup"><span data-stu-id="08337-154">**actionGroup**</span></span>](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[<span data-ttu-id="08337-155">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="08337-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="08337-156">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="08337-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





