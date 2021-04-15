---
title: ActionCollection. Create, метод
description: Для создания скрипта создает и добавляет в коллекцию новое действие.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- планировщик задач метода Create
- Создание планировщик задач метода, объект ActionCollection
- Планировщик задач объекта ActionCollection, метод Create
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534619"
---
# <a name="actioncollectioncreate-method"></a><span data-ttu-id="83865-106">ActionCollection. Create, метод</span><span class="sxs-lookup"><span data-stu-id="83865-106">ActionCollection.Create method</span></span>

<span data-ttu-id="83865-107">Для создания скрипта создает и добавляет в коллекцию новое действие.</span><span class="sxs-lookup"><span data-stu-id="83865-107">For scripting, creates and adds a new action to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="83865-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83865-108">Syntax</span></span>


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="83865-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="83865-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83865-110">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83865-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83865-111">Для этого параметра задается одна из следующих констант перечисления [**\_ \_ типов действий задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .</span><span class="sxs-lookup"><span data-stu-id="83865-111">This parameter is set to one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="83865-112">Значение</span><span class="sxs-lookup"><span data-stu-id="83865-112">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="83865-113">Значение</span><span class="sxs-lookup"><span data-stu-id="83865-113">Meaning</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="83865-114"><dt>**Задача \_ ДЕЙСТВИЕ \_ exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="83865-114"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="83865-115">Действие выполняет операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="83865-115">The action performs a command-line operation.</span></span> <span data-ttu-id="83865-116">Например, действие может выполнить сценарий, запустить исполняемый файл или, если указано имя документа, найти связанное с ним приложение и запустить приложение с документом.</span><span class="sxs-lookup"><span data-stu-id="83865-116">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="83865-117"><dt>**Задача \_ \_ \_ Обработчик com действия**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="83865-117"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="83865-118">Действие запускает обработчик.</span><span class="sxs-lookup"><span data-stu-id="83865-118">The action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="83865-119"><dt>**Задача \_ ДЕЙСТВИЕ \_ Отправить \_ электронное письмо**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="83865-119"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="83865-120">Это действие отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="83865-120">This action sends email message.</span></span><br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="83865-121"><dt>**Задача \_ ДЕЙСТВИЕ \_ Показывать \_ сообщение**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="83865-121"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="83865-122">Это действие отображает окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="83865-122">This action shows a message box.</span></span><br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83865-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83865-123">Return value</span></span>

<span data-ttu-id="83865-124">Объект [**Action**](action.md) , представляющий новое действие.</span><span class="sxs-lookup"><span data-stu-id="83865-124">An [**Action**](action.md) object that represents the new action.</span></span>

## <a name="remarks"></a><span data-ttu-id="83865-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83865-125">Remarks</span></span>

<span data-ttu-id="83865-126">К коллекции нельзя добавить более 32 действий.</span><span class="sxs-lookup"><span data-stu-id="83865-126">You cannot add more than 32 actions to the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="83865-127">Требования</span><span class="sxs-lookup"><span data-stu-id="83865-127">Requirements</span></span>



| <span data-ttu-id="83865-128">Требование</span><span class="sxs-lookup"><span data-stu-id="83865-128">Requirement</span></span> | <span data-ttu-id="83865-129">Значение</span><span class="sxs-lookup"><span data-stu-id="83865-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83865-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83865-130">Minimum supported client</span></span><br/> | <span data-ttu-id="83865-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83865-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="83865-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83865-132">Minimum supported server</span></span><br/> | <span data-ttu-id="83865-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="83865-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="83865-134">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="83865-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="83865-135"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="83865-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="83865-136">DLL</span><span class="sxs-lookup"><span data-stu-id="83865-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83865-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83865-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83865-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83865-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83865-139">**\_тип действия \_ задачи**</span><span class="sxs-lookup"><span data-stu-id="83865-139">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="83865-140">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="83865-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="83865-141">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="83865-141">**ActionCollection**</span></span>](actioncollection.md)
</dt> <dt>

[<span data-ttu-id="83865-142">**Действие**</span><span class="sxs-lookup"><span data-stu-id="83865-142">**Action**</span></span>](action.md)
</dt> <dt>

[<span data-ttu-id="83865-143">**ексекактион**</span><span class="sxs-lookup"><span data-stu-id="83865-143">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="83865-144">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="83865-144">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="83865-145">**шовмессажеактион**</span><span class="sxs-lookup"><span data-stu-id="83865-145">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> <dt>

[<span data-ttu-id="83865-146">**комхандлерактион**</span><span class="sxs-lookup"><span data-stu-id="83865-146">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





