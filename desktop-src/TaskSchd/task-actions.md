---
title: Действия задач
description: Рабочие элементы, выполняемые задачей, называются действиями. Задача может иметь одно действие или не более 32 действий. Имейте в виду, что если указано несколько действий, они выполняются последовательно.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- действия планировщик задач
- действия планировщик задач, описание
- действия планировщик задач, выполнение действия
- действия планировщик задач, действие обработчика COM
- выполнить действие планировщик задач
- планировщик задач действия обработчика COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "103787597"
---
# <a name="task-actions"></a><span data-ttu-id="410c5-111">Действия задач</span><span class="sxs-lookup"><span data-stu-id="410c5-111">Task Actions</span></span>

<span data-ttu-id="410c5-112">Рабочие элементы, выполняемые задачей, называются действиями.</span><span class="sxs-lookup"><span data-stu-id="410c5-112">The work items performed by a task are called actions.</span></span> <span data-ttu-id="410c5-113">Задача может иметь одно действие или не более 32 действий.</span><span class="sxs-lookup"><span data-stu-id="410c5-113">A task can have a single action or a maximum of 32 actions.</span></span> <span data-ttu-id="410c5-114">Имейте в виду, что если указано несколько действий, они выполняются последовательно.</span><span class="sxs-lookup"><span data-stu-id="410c5-114">Be aware that when multiple actions are specified, they are executed sequentially.</span></span>

## <a name="types-of-actions"></a><span data-ttu-id="410c5-115">Типы действий</span><span class="sxs-lookup"><span data-stu-id="410c5-115">Types of Actions</span></span>

<span data-ttu-id="410c5-116">В следующей таблице действий описывается тип работы или действий, которые могут быть выполнены задачей.</span><span class="sxs-lookup"><span data-stu-id="410c5-116">The following table of actions describes the type of work or actions that can be accomplished by a task.</span></span>

| <span data-ttu-id="410c5-117">Тип действия</span><span class="sxs-lookup"><span data-stu-id="410c5-117">Type of Action</span></span>      | <span data-ttu-id="410c5-118">Описание</span><span class="sxs-lookup"><span data-stu-id="410c5-118">Description</span></span>                                                             |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="410c5-119">Действие Комхандлер</span><span class="sxs-lookup"><span data-stu-id="410c5-119">ComHandler Action</span></span>   | <span data-ttu-id="410c5-120">Это действие запускает обработчик COM.</span><span class="sxs-lookup"><span data-stu-id="410c5-120">This action fires a COM handler.</span></span>                                        |
| <span data-ttu-id="410c5-121">Действие Exec</span><span class="sxs-lookup"><span data-stu-id="410c5-121">Exec Action</span></span>         | <span data-ttu-id="410c5-122">Это действие выполняет операцию командной строки, например запуск Блокнота.</span><span class="sxs-lookup"><span data-stu-id="410c5-122">This action executes a command-line operation such as starting Notepad.</span></span> |
| <span data-ttu-id="410c5-123">Действие электронной почты</span><span class="sxs-lookup"><span data-stu-id="410c5-123">E-mail Action</span></span>       | <span data-ttu-id="410c5-124">Это действие отправляет сообщение электронной почты при активации задачи.</span><span class="sxs-lookup"><span data-stu-id="410c5-124">This action sends an email when a task is triggered.</span></span>                    |
| <span data-ttu-id="410c5-125">Отобразить действие сообщения</span><span class="sxs-lookup"><span data-stu-id="410c5-125">Show Message Action</span></span> | <span data-ttu-id="410c5-126">Это действие отображает окно сообщения с указанным сообщением и заголовком.</span><span class="sxs-lookup"><span data-stu-id="410c5-126">This action shows a message box with a specified message and title.</span></span>     |



 

## <a name="specifying-actions"></a><span data-ttu-id="410c5-127">Указание действий</span><span class="sxs-lookup"><span data-stu-id="410c5-127">Specifying Actions</span></span>

<span data-ttu-id="410c5-128">Действия задачи указываются, когда задача определяется и сохраняется в коллекции действий, используемых службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="410c5-128">The actions of a task are specified when the task is defined and stored in a collection of actions used by the Task Scheduler service.</span></span> <span data-ttu-id="410c5-129">В следующей таблице перечислены ссылки на справочные материалы по интерфейсам API и XML-элементам, связанным с действиями.</span><span class="sxs-lookup"><span data-stu-id="410c5-129">The following table lists links to reference topics for the APIs and XML elements that are associated with actions.</span></span>

<span data-ttu-id="410c5-130">Дополнительные сведения и примеры использования интерфейсов планировщик задач, сценариев и XML см. [в разделе использование Планировщик задач](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="410c5-130">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="interface-apis-for-c-development"></a><span data-ttu-id="410c5-131">API интерфейса для разработки на C++</span><span class="sxs-lookup"><span data-stu-id="410c5-131">Interface APIs for C++ Development</span></span>



| <span data-ttu-id="410c5-132">API</span><span class="sxs-lookup"><span data-stu-id="410c5-132">API</span></span>                                                                    | <span data-ttu-id="410c5-133">Описание</span><span class="sxs-lookup"><span data-stu-id="410c5-133">Description</span></span>                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="410c5-134">**Свойство Actions объекта Итаскдефинитион**</span><span class="sxs-lookup"><span data-stu-id="410c5-134">**Actions Property of ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | <span data-ttu-id="410c5-135">Возвращает или задает действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="410c5-135">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="410c5-136">**IActionCollection**</span><span class="sxs-lookup"><span data-stu-id="410c5-136">**IActionCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | <span data-ttu-id="410c5-137">Содержит действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="410c5-137">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="410c5-138">**икомхандлерактион**</span><span class="sxs-lookup"><span data-stu-id="410c5-138">**IComHandlerAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | <span data-ttu-id="410c5-139">Представляет действие, которое вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="410c5-139">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="410c5-140">**иексекактион**</span><span class="sxs-lookup"><span data-stu-id="410c5-140">**IExecAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | <span data-ttu-id="410c5-141">Представляет действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="410c5-141">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="410c5-142">**иемаилактион**</span><span class="sxs-lookup"><span data-stu-id="410c5-142">**IEmailAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | <span data-ttu-id="410c5-143">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="410c5-143">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="410c5-144">**ишовмессажеактион**</span><span class="sxs-lookup"><span data-stu-id="410c5-144">**IShowMessageAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | <span data-ttu-id="410c5-145">Представляет действие, показывающее окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="410c5-145">Represents an action that shows a message box.</span></span>               |



 

### <a name="scripting-object-apis-for-scripting-development"></a><span data-ttu-id="410c5-146">Создание сценариев для API объектов для разработки сценариев</span><span class="sxs-lookup"><span data-stu-id="410c5-146">Scripting Object APIs for Scripting Development</span></span>



| <span data-ttu-id="410c5-147">API</span><span class="sxs-lookup"><span data-stu-id="410c5-147">API</span></span>                                                      | <span data-ttu-id="410c5-148">Описание</span><span class="sxs-lookup"><span data-stu-id="410c5-148">Description</span></span>                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="410c5-149">**Таскдефинитион. Actions**</span><span class="sxs-lookup"><span data-stu-id="410c5-149">**TaskDefinition.Actions**</span></span>](taskdefinition-actions.md) | <span data-ttu-id="410c5-150">Возвращает или задает действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="410c5-150">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="410c5-151">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="410c5-151">**ActionCollection**</span></span>](actioncollection.md)             | <span data-ttu-id="410c5-152">Содержит действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="410c5-152">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="410c5-153">**комхандлерактион**</span><span class="sxs-lookup"><span data-stu-id="410c5-153">**ComHandlerAction**</span></span>](comhandleraction.md)             | <span data-ttu-id="410c5-154">Представляет действие, которое вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="410c5-154">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="410c5-155">**ексекактион**</span><span class="sxs-lookup"><span data-stu-id="410c5-155">**ExecAction**</span></span>](execaction.md)                         | <span data-ttu-id="410c5-156">Представляет действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="410c5-156">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="410c5-157">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="410c5-157">**EmailAction**</span></span>](emailaction.md)                       | <span data-ttu-id="410c5-158">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="410c5-158">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="410c5-159">**шовмессажеактион**</span><span class="sxs-lookup"><span data-stu-id="410c5-159">**ShowMessageAction**</span></span>](showmessageaction.md)           | <span data-ttu-id="410c5-160">Представляет действие, показывающее окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="410c5-160">Represents an action that shows a message box.</span></span>               |



 

### <a name="xml-elements"></a><span data-ttu-id="410c5-161">Элементы XML</span><span class="sxs-lookup"><span data-stu-id="410c5-161">XML Elements</span></span>



| <span data-ttu-id="410c5-162">Элемент</span><span class="sxs-lookup"><span data-stu-id="410c5-162">Element</span></span>                                                                    | <span data-ttu-id="410c5-163">Описание</span><span class="sxs-lookup"><span data-stu-id="410c5-163">Description</span></span>                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="410c5-164">**Действия**</span><span class="sxs-lookup"><span data-stu-id="410c5-164">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)            | <span data-ttu-id="410c5-165">Определяет действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="410c5-165">Defines the actions performed by the task.</span></span>                   |
| [<span data-ttu-id="410c5-166">**комхандлер**</span><span class="sxs-lookup"><span data-stu-id="410c5-166">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | <span data-ttu-id="410c5-167">Представляет действие, которое вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="410c5-167">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="410c5-168">**Exec**</span><span class="sxs-lookup"><span data-stu-id="410c5-168">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | <span data-ttu-id="410c5-169">Представляет действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="410c5-169">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="410c5-170">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="410c5-170">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | <span data-ttu-id="410c5-171">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="410c5-171">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="410c5-172">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="410c5-172">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | <span data-ttu-id="410c5-173">Представляет действие, показывающее окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="410c5-173">Represents an action that shows a message box.</span></span>               |



 

## <a name="using-variables-in-action-properties"></a><span data-ttu-id="410c5-174">Использование переменных в свойствах действия</span><span class="sxs-lookup"><span data-stu-id="410c5-174">Using Variables in Action Properties</span></span>

<span data-ttu-id="410c5-175">Некоторые свойства действий типа **BSTR** могут содержать переменные $ (Arg0), $ (arg1),..., $ (Arg32) в своих строковых значениях.</span><span class="sxs-lookup"><span data-stu-id="410c5-175">Some action properties that are of type **BSTR** can contain $(Arg0), $(Arg1), ..., $(Arg32) variables in their string values.</span></span> <span data-ttu-id="410c5-176">Эти переменные заменяются значениями, заданными в параметре *params* методов [**Ирегистередтаск:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) и [**ирегистередтаск:: рунекс**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) или содержащимися в триггере события для задачи.</span><span class="sxs-lookup"><span data-stu-id="410c5-176">These variables are replaced with the values that are specified in the *params* parameter of the [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) and [**IRegisteredTask::RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) methods or are contained within the event trigger for the task.</span></span> <span data-ttu-id="410c5-177">В следующей таблице перечислены свойства действий, которые могут использовать переменные в своих строковых значениях.</span><span class="sxs-lookup"><span data-stu-id="410c5-177">The following table lists the action properties that can use variables in their string values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="410c5-178">Действие</span><span class="sxs-lookup"><span data-stu-id="410c5-178">Action</span></span></th>
<th><span data-ttu-id="410c5-179">Свойства</span><span class="sxs-lookup"><span data-stu-id="410c5-179">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="410c5-180">Действие обработчика COM</span><span class="sxs-lookup"><span data-stu-id="410c5-180">COM Handler Action</span></span></td>
<td><span data-ttu-id="410c5-181">C++:</span><span class="sxs-lookup"><span data-stu-id="410c5-181">C++:</span></span>
<ul>
<li><span data-ttu-id="410c5-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Свойство ClassId объекта Икомхандлерактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>ClassId Property of IComHandlerAction</strong></a></span></span></li>
<li><span data-ttu-id="410c5-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Свойство Data объекта Икомхандлерактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Data Property of IComHandlerAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="410c5-184">Написание скриптов:</span><span class="sxs-lookup"><span data-stu-id="410c5-184">Scripting:</span></span>
<ul>
<li><span data-ttu-id="410c5-185"><a href="comhandleraction-classid.md"><strong>Комхандлерактион. ClassId</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction.ClassId</strong></a></span></span></li>
<li><span data-ttu-id="410c5-186"><a href="comhandleraction-data.md"><strong>Комхандлерактион. Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction.Data</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="410c5-187">Действие электронной почты</span><span class="sxs-lookup"><span data-stu-id="410c5-187">Email Action</span></span></td>
<td><span data-ttu-id="410c5-188">C++:</span><span class="sxs-lookup"><span data-stu-id="410c5-188">C++:</span></span>
<ul>
<li><span data-ttu-id="410c5-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Свойство Body объекта Иемаилактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Body Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="410c5-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Свойство сервера Иемаилактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Server Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="410c5-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Свойство Subject объекта Иемаилактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Subject Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="410c5-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>Для свойства Иемаилактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>To Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="410c5-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Свойство CC объекта Иемаилактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Cc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="410c5-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Свойство BCC объекта Иемаилактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Bcc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="410c5-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo, свойство Иемаилактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="410c5-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From, свойство объекта Иемаилактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From Property of IEmailAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="410c5-197">Написание скриптов:</span><span class="sxs-lookup"><span data-stu-id="410c5-197">Scripting:</span></span>
<ul>
<li><span data-ttu-id="410c5-198"><a href="emailaction-body.md"><strong>Емаилактион. Body</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-198"><a href="emailaction-body.md"><strong>EmailAction.Body</strong></a></span></span></li>
<li><span data-ttu-id="410c5-199"><a href="emailaction-server.md"><strong>Емаилактион. Server</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-199"><a href="emailaction-server.md"><strong>EmailAction.Server</strong></a></span></span></li>
<li><span data-ttu-id="410c5-200"><a href="emailaction-subject.md"><strong>Емаилактион. subject</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-200"><a href="emailaction-subject.md"><strong>EmailAction.Subject</strong></a></span></span></li>
<li><span data-ttu-id="410c5-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span></span></li>
<li><span data-ttu-id="410c5-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span></span></li>
<li><span data-ttu-id="410c5-203"><a href="emailaction-bcc.md"><strong>Емаилактион. СК</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-203"><a href="emailaction-bcc.md"><strong>EmailAction.Bcc</strong></a></span></span></li>
<li><span data-ttu-id="410c5-204"><a href="emailaction-replyto.md"><strong>Емаилактион. ReplyTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-204"><a href="emailaction-replyto.md"><strong>EmailAction.ReplyTo</strong></a></span></span></li>
<li><span data-ttu-id="410c5-205"><a href="emailaction-from.md"><strong>Емаилактион. from</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-205"><a href="emailaction-from.md"><strong>EmailAction.From</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="410c5-206">Действие Exec</span><span class="sxs-lookup"><span data-stu-id="410c5-206">Exec Action</span></span></td>
<td><span data-ttu-id="410c5-207">C++:</span><span class="sxs-lookup"><span data-stu-id="410c5-207">C++:</span></span>
<ul>
<li><span data-ttu-id="410c5-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Свойство Arguments объекта Иексекактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Arguments Property of IExecAction</strong></a></span></span></li>
<li><span data-ttu-id="410c5-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Свойство WorkingDirectory объекта Иексекактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>WorkingDirectory Property of IExecAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="410c5-210">Написание скриптов:</span><span class="sxs-lookup"><span data-stu-id="410c5-210">Scripting:</span></span>
<ul>
<li><span data-ttu-id="410c5-211"><a href="execaction-arguments.md"><strong>Ексекактион. Arguments</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-211"><a href="execaction-arguments.md"><strong>ExecAction.Arguments</strong></a></span></span></li>
<li><span data-ttu-id="410c5-212"><a href="execaction-workingdirectory.md"><strong>Ексекактион. WorkingDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-212"><a href="execaction-workingdirectory.md"><strong>ExecAction.WorkingDirectory</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="410c5-213">Отобразить действие сообщения</span><span class="sxs-lookup"><span data-stu-id="410c5-213">Show Message Action</span></span></td>
<td><span data-ttu-id="410c5-214">C++:</span><span class="sxs-lookup"><span data-stu-id="410c5-214">C++:</span></span>
<ul>
<li><span data-ttu-id="410c5-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Свойство Title объекта Ишовмессажеактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Title Property of IShowMessageAction</strong></a></span></span></li>
<li><span data-ttu-id="410c5-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Свойство MessageBody объекта Ишовмессажеактион</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>MessageBody Property of IShowMessageAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="410c5-217">Написание скриптов:</span><span class="sxs-lookup"><span data-stu-id="410c5-217">Scripting:</span></span>
<ul>
<li><span data-ttu-id="410c5-218"><a href="showmessageaction-title.md"><strong>Шовмессажеактион. Title</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction.Title</strong></a></span></span></li>
<li><span data-ttu-id="410c5-219"><a href="showmessageaction-messagebody.md"><strong>Шовмессажеактион. MessageBody</strong></a></span><span class="sxs-lookup"><span data-stu-id="410c5-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction.MessageBody</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="410c5-220">См. также</span><span class="sxs-lookup"><span data-stu-id="410c5-220">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="410c5-221">Сведения о планировщик задач</span><span class="sxs-lookup"><span data-stu-id="410c5-221">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 





