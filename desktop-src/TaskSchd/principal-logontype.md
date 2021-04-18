---
title: Свойство Principal. LogonType
description: Для сценариев Возвращает или задает метод входа в систему безопасности, необходимый для выполнения задач, связанных с участником.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- планировщик задач свойства LogonType
- Планировщик задач свойства LogonType, объект Principal
- Объект Principal планировщик задач, свойство LogonType
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491091"
---
# <a name="principallogontype-property"></a><span data-ttu-id="77a42-106">Свойство Principal. LogonType</span><span class="sxs-lookup"><span data-stu-id="77a42-106">Principal.LogonType property</span></span>

<span data-ttu-id="77a42-107">Для сценариев Возвращает или задает метод входа в систему безопасности, необходимый для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="77a42-107">For scripting, gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="77a42-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77a42-108">Syntax</span></span>


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a><span data-ttu-id="77a42-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="77a42-109">Property value</span></span>

<span data-ttu-id="77a42-110">Задайте одну из следующих констант перечисления [**\_ типа входа в задачу**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) .</span><span class="sxs-lookup"><span data-stu-id="77a42-110">Set to one of the following [**TASK\_LOGON TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) enumeration constants.</span></span>



| <span data-ttu-id="77a42-111">Значение</span><span class="sxs-lookup"><span data-stu-id="77a42-111">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="77a42-112">Значение</span><span class="sxs-lookup"><span data-stu-id="77a42-112">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="77a42-113"><dt>**Задача \_ \_Нет подключения**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="77a42-113"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="77a42-114">Метод logon не указан.</span><span class="sxs-lookup"><span data-stu-id="77a42-114">The logon method is not specified.</span></span> <span data-ttu-id="77a42-115">Используется для учетных данных, не относящихся к NT.</span><span class="sxs-lookup"><span data-stu-id="77a42-115">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="77a42-116"><dt>**Задача \_ \_Пароль для входа**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="77a42-116"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="77a42-117">Используйте пароль для входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="77a42-117">Use a password for logging on the user.</span></span> <span data-ttu-id="77a42-118">Пароль должен указываться во время регистрации.</span><span class="sxs-lookup"><span data-stu-id="77a42-118">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="77a42-119"><dt>**Задача \_ Вход в систему \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="77a42-119"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="77a42-120">Использовать существующий интерактивный токен для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="77a42-120">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="77a42-121">Пользователь должен войти в систему, используя службу для входа пользователя (S4U).</span><span class="sxs-lookup"><span data-stu-id="77a42-121">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="77a42-122">При использовании имени входа S4U система не хранит пароль и не имеет доступа к сети или зашифрованным файлам.</span><span class="sxs-lookup"><span data-stu-id="77a42-122">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="77a42-123"><dt>**Задача \_ \_Интерактивный \_ маркер входа**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="77a42-123"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="77a42-124">Пользователь уже должен войти в систему.</span><span class="sxs-lookup"><span data-stu-id="77a42-124">User must already be logged on.</span></span> <span data-ttu-id="77a42-125">Задача будет запущена только в существующем интерактивном сеансе.</span><span class="sxs-lookup"><span data-stu-id="77a42-125">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="77a42-126"><dt>**Задача \_ \_Группа входа**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="77a42-126"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="77a42-127">Активация группы.</span><span class="sxs-lookup"><span data-stu-id="77a42-127">Group activation.</span></span> <span data-ttu-id="77a42-128">Поле userId указывает группу.</span><span class="sxs-lookup"><span data-stu-id="77a42-128">The userId field specifies the group.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="77a42-129"><dt>**Задача \_ \_ \_ Учетная запись службы входа**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="77a42-129"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="77a42-130">Указывает, что в качестве контекста безопасности для выполнения задачи используется локальная система, локальная служба или учетная запись сетевой службы.</span><span class="sxs-lookup"><span data-stu-id="77a42-130">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="77a42-131"><dt>**Задача \_ \_Интерактивный \_ маркер входа \_ или \_ пароль**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="77a42-131"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="77a42-132">Сначала используйте интерактивный токен.</span><span class="sxs-lookup"><span data-stu-id="77a42-132">First use the interactive token.</span></span> <span data-ttu-id="77a42-133">Если пользователь не вошел в систему (интерактивный маркер недоступен), то используется пароль.</span><span class="sxs-lookup"><span data-stu-id="77a42-133">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="77a42-134">При регистрации задачи необходимо указать пароль.</span><span class="sxs-lookup"><span data-stu-id="77a42-134">The password must be specified when a task is registered.</span></span> <span data-ttu-id="77a42-135">Этот флаг не рекомендуется для новых задач, так как он менее надежен, чем \_ пароль для входа в систему \_ .</span><span class="sxs-lookup"><span data-stu-id="77a42-135">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="77a42-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77a42-136">Remarks</span></span>

<span data-ttu-id="77a42-137">Это свойство допустимо, только если идентификатор пользователя задан свойством [**UserID**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="77a42-137">This property is valid only when a user identifier is specified by the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="77a42-138">При чтении или записи XML для задачи тип входа указывается в [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) элементе схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="77a42-138">When reading or writing XML for a task, the logon type is specified in the [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="77a42-139">Для задачи, которая содержит действие «окно сообщения», появится окно сообщения, если задача активирована, а задача имеет интерактивный тип входа в систему.</span><span class="sxs-lookup"><span data-stu-id="77a42-139">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="77a42-140">Чтобы установить для параметра Тип входа в интерактивный режим, укажите значение 3 (**\_ \_ Интерактивный \_ маркер входа в систему**) или 4 (**\_ \_ Группа входа** в систему) в свойстве **LogonType** участника задачи или в параметре *LogonType* [**таскфолдер. регистертаск**](taskfolder-registertask.md) или [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="77a42-140">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the **LogonType** property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77a42-141">Требования</span><span class="sxs-lookup"><span data-stu-id="77a42-141">Requirements</span></span>



| <span data-ttu-id="77a42-142">Требование</span><span class="sxs-lookup"><span data-stu-id="77a42-142">Requirement</span></span> | <span data-ttu-id="77a42-143">Значение</span><span class="sxs-lookup"><span data-stu-id="77a42-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77a42-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77a42-144">Minimum supported client</span></span><br/> | <span data-ttu-id="77a42-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77a42-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="77a42-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77a42-146">Minimum supported server</span></span><br/> | <span data-ttu-id="77a42-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77a42-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77a42-148">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="77a42-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="77a42-149"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="77a42-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="77a42-150">DLL</span><span class="sxs-lookup"><span data-stu-id="77a42-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77a42-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77a42-151"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77a42-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77a42-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77a42-153">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="77a42-153">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="77a42-154">**Основного**</span><span class="sxs-lookup"><span data-stu-id="77a42-154">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





