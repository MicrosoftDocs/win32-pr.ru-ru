---
title: Таскфолдер. Регистертаск, метод
description: Для создания скрипта регистрирует (создает) новую задачу в папке с помощью XML для определения задачи.
ms.assetid: 9bf5c59b-5aa1-42b3-a307-f583cdf59a39
keywords:
- планировщик задач метода Регистертаск
- Планировщик задач метода Регистертаск, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, метод Регистертаск
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc0ed00ec736a90f716d895199812899d972930
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989112"
---
# <a name="taskfolderregistertask-method"></a><span data-ttu-id="0e954-106">Таскфолдер. Регистертаск, метод</span><span class="sxs-lookup"><span data-stu-id="0e954-106">TaskFolder.RegisterTask method</span></span>

<span data-ttu-id="0e954-107">Для создания скрипта регистрирует (создает) новую задачу в папке с помощью XML для определения задачи.</span><span class="sxs-lookup"><span data-stu-id="0e954-107">For scripting, registers (creates) a new task in the folder using XML to define the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e954-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e954-108">Syntax</span></span>


```VB
TaskFolder.RegisterTask( _
  ByVal path, _
  ByVal xmlText, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef pTask _
)
```



## <a name="parameters"></a><span data-ttu-id="0e954-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e954-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e954-110">*путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e954-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e954-111">Имя данной задачи.</span><span class="sxs-lookup"><span data-stu-id="0e954-111">The name of the task.</span></span> <span data-ttu-id="0e954-112">Если это значение равно **Nothing**, задача будет зарегистрирована в корневой папке задач, а имя задачи будет иметь значение GUID, созданное службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="0e954-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="0e954-113">Имя задачи не может начинаться или заканчиваться символом пробела.</span><span class="sxs-lookup"><span data-stu-id="0e954-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="0e954-114">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="0e954-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="0e954-115">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="0e954-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="0e954-116">*xmltext* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e954-116">*xmlText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e954-117">Описание задачи в формате XML.</span><span class="sxs-lookup"><span data-stu-id="0e954-117">An XML-formatted description of the task.</span></span>

<span data-ttu-id="0e954-118">В следующих разделах содержатся задачи, определенные с помощью XML.</span><span class="sxs-lookup"><span data-stu-id="0e954-118">The following topics contain tasks defined using XML.</span></span>

-   [<span data-ttu-id="0e954-119">Пример триггера времени (XML)</span><span class="sxs-lookup"><span data-stu-id="0e954-119">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)
-   <span data-ttu-id="0e954-120">[Пример триггера события (XML)](/previous-versions//aa446889(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e954-120">[Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85))</span></span>
-   [<span data-ttu-id="0e954-121">Пример ежедневного триггера (XML)</span><span class="sxs-lookup"><span data-stu-id="0e954-121">Daily Trigger Example (XML)</span></span>](daily-trigger-example--xml-.md)
-   [<span data-ttu-id="0e954-122">Пример триггера регистрации (XML)</span><span class="sxs-lookup"><span data-stu-id="0e954-122">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)
-   [<span data-ttu-id="0e954-123">Пример еженедельного триггера (XML)</span><span class="sxs-lookup"><span data-stu-id="0e954-123">Weekly Trigger Example (XML)</span></span>](weekly-trigger-example--xml-.md)
-   [<span data-ttu-id="0e954-124">Пример триггера LOGON (XML)</span><span class="sxs-lookup"><span data-stu-id="0e954-124">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)
-   [<span data-ttu-id="0e954-125">Пример триггера Boot (XML)</span><span class="sxs-lookup"><span data-stu-id="0e954-125">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

</dd> <dt>

<span data-ttu-id="0e954-126">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e954-126">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e954-127">Константа [**\_ создания задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .</span><span class="sxs-lookup"><span data-stu-id="0e954-127">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="0e954-128">Значение</span><span class="sxs-lookup"><span data-stu-id="0e954-128">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="0e954-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0e954-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="0e954-130"><dt>**Задача \_ ПРОВЕРЯТЬ \_ только**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-130"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="0e954-131">Планировщик задач проверяет синтаксис XML, который описывает задачу, но не регистрирует задачу.</span><span class="sxs-lookup"><span data-stu-id="0e954-131">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="0e954-132">Эту константу нельзя сочетать с **\_ созданием \_ или \_ обновлением** значений задач " **\_ создать**", " **\_ обновление задачи**" или "задача".</span><span class="sxs-lookup"><span data-stu-id="0e954-132">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="0e954-133"><dt>**Задача \_ СОЗДАТЬ**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-133"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="0e954-134">Планировщик задач регистрирует задачу в качестве новой задачи.</span><span class="sxs-lookup"><span data-stu-id="0e954-134">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="0e954-135"><dt>**Задача \_ Обновление**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-135"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="0e954-136">Планировщик задач регистрирует задачу в качестве обновленной версии существующей задачи.</span><span class="sxs-lookup"><span data-stu-id="0e954-136">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="0e954-137">При обновлении задачи с триггером регистрации задача будет выполнена после обновления.</span><span class="sxs-lookup"><span data-stu-id="0e954-137">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="0e954-138"><dt>**Задача \_ Создание \_ или \_ Обновление**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-138"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="0e954-139">Планировщик задач либо регистрирует задачу в качестве новой задачи, либо в виде обновленной версии, если задача уже существует.</span><span class="sxs-lookup"><span data-stu-id="0e954-139">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="0e954-140">Эквивалентно \_ \| обновлению задачи Create Task \_ .</span><span class="sxs-lookup"><span data-stu-id="0e954-140">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="0e954-141"><dt>**Задача \_ Отключение**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-141"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="0e954-142">Планировщик задач отключает существующую задачу.</span><span class="sxs-lookup"><span data-stu-id="0e954-142">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="0e954-143"><dt>**Задача \_ НЕ \_ Добавить \_ субъект \_ ACE**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0e954-143"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="0e954-144">Планировщик задач не допускает добавления записи управления доступом (ACE) для участника контекста.</span><span class="sxs-lookup"><span data-stu-id="0e954-144">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="0e954-145">При вызове функции **таскфолдер. регистертаск** с этим флагом для обновления задачи служба Планировщик задач не добавляет ACE для нового участника контекста и не удаляет ACE из старого участника контекста.</span><span class="sxs-lookup"><span data-stu-id="0e954-145">When the **TaskFolder.RegisterTask** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="0e954-146"><dt>**Задача \_ ИГНОРИРОВАТЬ \_ \_ триггеры регистрации**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-146"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="0e954-147">Планировщик задач создает задачу, но игнорирует триггеры регистрации в задаче.</span><span class="sxs-lookup"><span data-stu-id="0e954-147">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="0e954-148">При игнорировании триггеров регистрации задача не будет выполняться при регистрации, если триггер, основанный на времени, не приводит к его выполнению при регистрации.</span><span class="sxs-lookup"><span data-stu-id="0e954-148">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                               |



 

</dd> <dt>

<span data-ttu-id="0e954-149">*UserID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e954-149">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e954-150">Учетные данные пользователя, которые используются для регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="0e954-150">The user credentials that are used to register the task.</span></span>

> [!Note]  
> <span data-ttu-id="0e954-151">Если задача определена как задача планировщик задач 1,0, не используйте в этом параметре userId имя группы (а не определенное имя пользователя).</span><span class="sxs-lookup"><span data-stu-id="0e954-151">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="0e954-152">Задача определяется как задача планировщик задач 1,0, если атрибут Version элемента Task в XML-файле задачи имеет значение 1,1.</span><span class="sxs-lookup"><span data-stu-id="0e954-152">A task is defined as a Task Scheduler 1.0 task when the version attribute of the Task element in the task's XML is set to 1.1.</span></span>

 

</dd> <dt>

<span data-ttu-id="0e954-153">*пароль* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e954-153">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e954-154">Пароль для userId, который используется для регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="0e954-154">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="0e954-155">При \_ \_ \_ использовании типа входа учетной записи службы входа в систему пароль должен быть пустым значением **типа Variant** , таким как **VT \_ null** или **VT \_ Empty**.</span><span class="sxs-lookup"><span data-stu-id="0e954-155">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="0e954-156">*logonType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e954-156">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e954-157">Определяет, какой метод входа используется для выполнения зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="0e954-157">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="0e954-158">Значение</span><span class="sxs-lookup"><span data-stu-id="0e954-158">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0e954-159">Значение</span><span class="sxs-lookup"><span data-stu-id="0e954-159">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="0e954-160"><dt>**Задача \_ \_Нет подключения**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-160"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="0e954-161">Метод logon не указан.</span><span class="sxs-lookup"><span data-stu-id="0e954-161">The logon method is not specified.</span></span> <span data-ttu-id="0e954-162">Используется для учетных данных, не относящихся к NT.</span><span class="sxs-lookup"><span data-stu-id="0e954-162">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="0e954-163"><dt>**Задача \_ \_Пароль для входа**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-163"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="0e954-164">Используйте пароль для входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="0e954-164">Use a password for logging on the user.</span></span> <span data-ttu-id="0e954-165">Пароль должен указываться во время регистрации.</span><span class="sxs-lookup"><span data-stu-id="0e954-165">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="0e954-166"><dt>**Задача \_ Вход в систему \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-166"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="0e954-167">Использовать существующий интерактивный токен для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="0e954-167">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="0e954-168">Пользователь должен войти в систему, используя службу для входа пользователя (S4U).</span><span class="sxs-lookup"><span data-stu-id="0e954-168">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="0e954-169">При использовании имени входа S4U система не хранит пароль и не имеет доступа к сети или к зашифрованным файлам.</span><span class="sxs-lookup"><span data-stu-id="0e954-169">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="0e954-170"><dt>**Задача \_ \_Интерактивный \_ маркер входа**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-170"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="0e954-171">Пользователь уже должен войти в систему.</span><span class="sxs-lookup"><span data-stu-id="0e954-171">User must already be logged on.</span></span> <span data-ttu-id="0e954-172">Задача будет запущена только в существующем интерактивном сеансе.</span><span class="sxs-lookup"><span data-stu-id="0e954-172">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="0e954-173"><dt>**Задача \_ \_Группа входа**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-173"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="0e954-174">Активация группы.</span><span class="sxs-lookup"><span data-stu-id="0e954-174">Group activation.</span></span> <span data-ttu-id="0e954-175">Поле **groupId** указывает группу.</span><span class="sxs-lookup"><span data-stu-id="0e954-175">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="0e954-176"><dt>**Задача \_ \_ \_ Учетная запись службы входа**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-176"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="0e954-177">Указывает, что в качестве контекста безопасности для выполнения задачи используется локальная система, локальная служба или учетная запись сетевой службы.</span><span class="sxs-lookup"><span data-stu-id="0e954-177">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="0e954-178"><dt>**Задача \_ \_Интерактивный \_ маркер входа \_ или \_ пароль**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-178"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="0e954-179">Сначала используйте интерактивный токен.</span><span class="sxs-lookup"><span data-stu-id="0e954-179">First use the interactive token.</span></span> <span data-ttu-id="0e954-180">Если пользователь не вошел в систему (интерактивный маркер недоступен), то используется пароль.</span><span class="sxs-lookup"><span data-stu-id="0e954-180">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="0e954-181">При регистрации задачи необходимо указать пароль.</span><span class="sxs-lookup"><span data-stu-id="0e954-181">The password must be specified when a task is registered.</span></span> <span data-ttu-id="0e954-182">Этот флаг не рекомендуется для новых задач, так как он менее надежен, чем \_ пароль для входа в систему \_ .</span><span class="sxs-lookup"><span data-stu-id="0e954-182">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0e954-183">*SDDL* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0e954-183">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e954-184">Дескриптор безопасности, связанный с зарегистрированной задачей.</span><span class="sxs-lookup"><span data-stu-id="0e954-184">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="0e954-185">Вы можете указать список управления доступом (ACL) в дескрипторе безопасности задачи, чтобы разрешить или запретить определенным пользователям и группам доступ к задаче.</span><span class="sxs-lookup"><span data-stu-id="0e954-185">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="0e954-186">Если локальной системной учетной записи запрещен доступ к задаче, то служба планировщик задач может получить непредвиденные результаты.</span><span class="sxs-lookup"><span data-stu-id="0e954-186">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="0e954-187">*птаск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0e954-187">*pTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e954-188">Объект [**регистередтаск**](registeredtask.md) , представляющий новую задачу.</span><span class="sxs-lookup"><span data-stu-id="0e954-188">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e954-189">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e954-189">Return value</span></span>

<span data-ttu-id="0e954-190">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0e954-190">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e954-191">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e954-191">Remarks</span></span>

<span data-ttu-id="0e954-192">Для задачи, которая содержит действие «окно сообщения», появится окно сообщения, если задача активирована, а задача имеет интерактивный тип входа в систему.</span><span class="sxs-lookup"><span data-stu-id="0e954-192">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="0e954-193">Чтобы установить для параметра Тип входа в интерактивный режим, укажите значение 3 (**\_ \_ Интерактивный \_ маркер входа в систему**) или 4 (**\_ \_ Группа входа** в систему) в свойстве [**LogonType**](principal-logontype.md) участника задачи или в параметре *LogonType* **таскфолдер. регистертаск** или [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="0e954-193">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="0e954-194">Только член группы "Администраторы" может создать задачу с триггером загрузки.</span><span class="sxs-lookup"><span data-stu-id="0e954-194">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="0e954-195">Вы можете успешно зарегистрировать задачу с группой, указанной в параметре *UserID* , и 3 (**\_ \_ Интерактивный \_ токен входа задачи**), указанный в параметре *logonType* **таскфолдер. регистертаск** или [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md), но задача не будет запущена.</span><span class="sxs-lookup"><span data-stu-id="0e954-195">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e954-196">Требования</span><span class="sxs-lookup"><span data-stu-id="0e954-196">Requirements</span></span>



| <span data-ttu-id="0e954-197">Требование</span><span class="sxs-lookup"><span data-stu-id="0e954-197">Requirement</span></span> | <span data-ttu-id="0e954-198">Значение</span><span class="sxs-lookup"><span data-stu-id="0e954-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e954-199">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e954-199">Minimum supported client</span></span><br/> | <span data-ttu-id="0e954-200">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e954-200">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0e954-201">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e954-201">Minimum supported server</span></span><br/> | <span data-ttu-id="0e954-202">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e954-202">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e954-203">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0e954-203">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e954-204"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-204"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e954-205">DLL</span><span class="sxs-lookup"><span data-stu-id="0e954-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e954-206"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e954-206"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e954-207">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e954-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e954-208">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="0e954-208">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0e954-209">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="0e954-209">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="0e954-210">**таскфолдер**</span><span class="sxs-lookup"><span data-stu-id="0e954-210">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

