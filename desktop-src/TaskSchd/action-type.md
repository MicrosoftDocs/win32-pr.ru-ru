---
title: Action. Type, свойство
description: Для сценариев Возвращает тип действия.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Тип свойства планировщик задач
- Свойство Type планировщик задач, объект Action
- Объект Action планировщик задач, свойство Type
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491703"
---
# <a name="actiontype-property"></a><span data-ttu-id="e7cb6-106">Action. Type, свойство</span><span class="sxs-lookup"><span data-stu-id="e7cb6-106">Action.Type property</span></span>

<span data-ttu-id="e7cb6-107">Для сценариев Возвращает тип действия.</span><span class="sxs-lookup"><span data-stu-id="e7cb6-107">For scripting, gets the type of the action.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7cb6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7cb6-108">Syntax</span></span>


```VB
Action.Type As Integer
```



## <a name="property-value"></a><span data-ttu-id="e7cb6-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e7cb6-109">Property value</span></span>

<span data-ttu-id="e7cb6-110">Это свойство возвращает одну из следующих констант [**перечисления \_ \_ типа действия задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .</span><span class="sxs-lookup"><span data-stu-id="e7cb6-110">This property returns one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="e7cb6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e7cb6-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="e7cb6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e7cb6-112">Meaning</span></span>                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="e7cb6-113"><dt>**Задача \_ ДЕЙСТВИЕ \_ exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e7cb6-113"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="e7cb6-114">Это действие выполняет операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="e7cb6-114">This action performs a command-line operation.</span></span> <span data-ttu-id="e7cb6-115">Например, действие может выполнить сценарий, запустить исполняемый файл или, если указано имя документа, найти связанное с ним приложение и запустить приложение с документом.</span><span class="sxs-lookup"><span data-stu-id="e7cb6-115">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="e7cb6-116"><dt>**Задача \_ \_ \_ Обработчик com действия**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e7cb6-116"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="e7cb6-117">Это действие вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="e7cb6-117">This action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="e7cb6-118"><dt>**Задача \_ ДЕЙСТВИЕ \_ Отправить \_ электронное письмо**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e7cb6-118"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="e7cb6-119">Это действие отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e7cb6-119">This action sends an email message.</span></span><br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="e7cb6-120"><dt>**Задача \_ ДЕЙСТВИЕ \_ Показывать \_ сообщение**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e7cb6-120"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="e7cb6-121">Это действие отображает окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7cb6-121">This action shows a message box.</span></span><br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="e7cb6-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7cb6-122">Remarks</span></span>

<span data-ttu-id="e7cb6-123">Тип действия определяется при создании действия и не может быть изменен позже.</span><span class="sxs-lookup"><span data-stu-id="e7cb6-123">The action type is defined when the action is created and cannot be changed later.</span></span> <span data-ttu-id="e7cb6-124">Сведения о создании действия см. в разделе [**ActionCollection. Create**](actioncollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="e7cb6-124">For information on creating an action, see [**ActionCollection.Create**](actioncollection-create.md).</span></span>

<span data-ttu-id="e7cb6-125">Сведения о совместной работе действий и задач см. в разделе [действия задач](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="e7cb6-125">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7cb6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e7cb6-126">Requirements</span></span>



| <span data-ttu-id="e7cb6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e7cb6-127">Requirement</span></span> | <span data-ttu-id="e7cb6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e7cb6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7cb6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7cb6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e7cb6-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7cb6-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e7cb6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7cb6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e7cb6-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7cb6-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7cb6-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e7cb6-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7cb6-134"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e7cb6-134"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e7cb6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e7cb6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7cb6-136"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7cb6-136"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7cb6-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7cb6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7cb6-138">**\_тип действия \_ задачи**</span><span class="sxs-lookup"><span data-stu-id="e7cb6-138">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="e7cb6-139">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="e7cb6-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e7cb6-140">**Действие**</span><span class="sxs-lookup"><span data-stu-id="e7cb6-140">**Action**</span></span>](action.md)
</dt> </dl>

 

 





