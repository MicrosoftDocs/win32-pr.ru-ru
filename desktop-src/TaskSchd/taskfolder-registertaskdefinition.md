---
title: Таскфолдер. Регистертаскдефинитион, метод
description: Для создания скрипта регистрирует (создает) задачу в указанном расположении, используя объект Таскдефинитион для определения задачи.
ms.assetid: 198c8848-c89d-4883-b111-4ac0b009b7b3
keywords:
- планировщик задач метода Регистертаскдефинитион
- Планировщик задач метода Регистертаскдефинитион, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, метод Регистертаскдефинитион
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616d917dd0bb5516fdf8d474d293ba370775c786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415792"
---
# <a name="taskfolderregistertaskdefinition-method"></a><span data-ttu-id="d7015-106">Таскфолдер. Регистертаскдефинитион, метод</span><span class="sxs-lookup"><span data-stu-id="d7015-106">TaskFolder.RegisterTaskDefinition method</span></span>

<span data-ttu-id="d7015-107">Для создания скрипта регистрирует (создает) задачу в указанном расположении, используя объект [**таскдефинитион**](taskdefinition.md) для определения задачи.</span><span class="sxs-lookup"><span data-stu-id="d7015-107">For scripting, registers (creates) a task in a specified location using the [**TaskDefinition**](taskdefinition.md) object to define a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7015-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7015-108">Syntax</span></span>


```VB
TaskFolder.RegisterTaskDefinition( _
  ByVal path, _
  ByVal definition, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef task _
)
```



## <a name="parameters"></a><span data-ttu-id="d7015-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7015-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7015-110">*путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7015-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7015-111">Имя данной задачи.</span><span class="sxs-lookup"><span data-stu-id="d7015-111">The name of the task.</span></span> <span data-ttu-id="d7015-112">Если это значение равно **Nothing**, задача будет зарегистрирована в корневой папке задач, а имя задачи будет иметь значение GUID, созданное службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="d7015-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="d7015-113">Имя задачи не может начинаться или заканчиваться символом пробела.</span><span class="sxs-lookup"><span data-stu-id="d7015-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="d7015-114">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="d7015-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="d7015-115">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="d7015-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="d7015-116">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7015-116">*definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7015-117">Определение зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="d7015-117">The definition of the task that is registered.</span></span>

</dd> <dt>

<span data-ttu-id="d7015-118">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7015-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7015-119">Константа [**\_ создания задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .</span><span class="sxs-lookup"><span data-stu-id="d7015-119">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="d7015-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d7015-120">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="d7015-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d7015-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="d7015-122"><dt>**Задача \_ ПРОВЕРЯТЬ \_ только**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-122"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="d7015-123">Планировщик задач проверяет синтаксис XML, который описывает задачу, но не регистрирует задачу.</span><span class="sxs-lookup"><span data-stu-id="d7015-123">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="d7015-124">Эту константу нельзя сочетать с **\_ созданием \_ или \_ обновлением** значений задач " **\_ создать**", " **\_ обновление задачи**" или "задача".</span><span class="sxs-lookup"><span data-stu-id="d7015-124">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                            |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="d7015-125"><dt>**Задача \_ СОЗДАТЬ**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-125"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="d7015-126">Планировщик задач регистрирует задачу в качестве новой задачи.</span><span class="sxs-lookup"><span data-stu-id="d7015-126">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="d7015-127"><dt>**Задача \_ Обновление**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-127"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="d7015-128">Планировщик задач регистрирует задачу в качестве обновленной версии существующей задачи.</span><span class="sxs-lookup"><span data-stu-id="d7015-128">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="d7015-129">При обновлении задачи с триггером регистрации задача будет выполнена после обновления.</span><span class="sxs-lookup"><span data-stu-id="d7015-129">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                                      |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="d7015-130"><dt>**Задача \_ Создание \_ или \_ Обновление**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-130"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="d7015-131">Планировщик задач либо регистрирует задачу в качестве новой задачи, либо в виде обновленной версии, если задача уже существует.</span><span class="sxs-lookup"><span data-stu-id="d7015-131">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="d7015-132">Эквивалентно \_ \| обновлению задачи Create Task \_ .</span><span class="sxs-lookup"><span data-stu-id="d7015-132">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="d7015-133"><dt>**Задача \_ Отключение**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-133"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="d7015-134">Планировщик задач отключает существующую задачу.</span><span class="sxs-lookup"><span data-stu-id="d7015-134">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="d7015-135"><dt>**Задача \_ НЕ \_ Добавить \_ субъект \_ ACE**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d7015-135"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="d7015-136">Планировщик задач не допускает добавления записи управления доступом (ACE) для участника контекста.</span><span class="sxs-lookup"><span data-stu-id="d7015-136">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="d7015-137">При вызове функции **таскфолдер. регистертаскдефинитион** с этим флагом для обновления задачи служба Планировщик задач не добавляет ACE для нового участника контекста и не удаляет ACE из старого участника контекста.</span><span class="sxs-lookup"><span data-stu-id="d7015-137">When the **TaskFolder.RegisterTaskDefinition** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="d7015-138"><dt>**Задача \_ ИГНОРИРОВАТЬ \_ \_ триггеры регистрации**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-138"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="d7015-139">Планировщик задач создает задачу, но игнорирует триггеры регистрации в задаче.</span><span class="sxs-lookup"><span data-stu-id="d7015-139">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="d7015-140">При игнорировании триггеров регистрации задача не будет выполняться при регистрации, если триггер, основанный на времени, не приводит к его выполнению при регистрации.</span><span class="sxs-lookup"><span data-stu-id="d7015-140">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="d7015-141">*UserID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7015-141">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7015-142">Учетные данные пользователя, которые используются для регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="d7015-142">The user credentials that are used to register the task.</span></span> <span data-ttu-id="d7015-143">При наличии эти учетные данные имеют приоритет над учетными данными, указанными в объекте определения задачи, на который указывает параметр *определения* .</span><span class="sxs-lookup"><span data-stu-id="d7015-143">If present, these credentials take priority over the credentials specified in the task definition object pointed to by the *definition* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="d7015-144">Если задача определена как задача планировщик задач 1,0, не используйте в этом параметре userId имя группы (а не определенное имя пользователя).</span><span class="sxs-lookup"><span data-stu-id="d7015-144">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="d7015-145">Задача определяется как задача планировщик задач 1,0, если свойство [**Compatibility**](tasksettings-compatibility.md) имеет значение 1 в параметрах задачи.</span><span class="sxs-lookup"><span data-stu-id="d7015-145">A task is defined as a Task Scheduler 1.0 task when the [**Compatibility**](tasksettings-compatibility.md) property is set to 1 in the task's settings.</span></span>

 

</dd> <dt>

<span data-ttu-id="d7015-146">*пароль* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7015-146">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7015-147">Пароль для userId, который используется для регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="d7015-147">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="d7015-148">При \_ \_ \_ использовании типа входа учетной записи службы входа в систему пароль должен быть пустым значением **типа Variant** , таким как **VT \_ null** или **VT \_ Empty**.</span><span class="sxs-lookup"><span data-stu-id="d7015-148">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="d7015-149">*logonType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7015-149">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7015-150">Определяет, какой метод входа используется для выполнения зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="d7015-150">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="d7015-151">Значение</span><span class="sxs-lookup"><span data-stu-id="d7015-151">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="d7015-152">Значение</span><span class="sxs-lookup"><span data-stu-id="d7015-152">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="d7015-153"><dt>**Задача \_ \_Нет подключения**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-153"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="d7015-154">Метод logon не указан.</span><span class="sxs-lookup"><span data-stu-id="d7015-154">The logon method is not specified.</span></span> <span data-ttu-id="d7015-155">Используется для учетных данных, не относящихся к NT.</span><span class="sxs-lookup"><span data-stu-id="d7015-155">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="d7015-156"><dt>**Задача \_ \_Пароль для входа**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-156"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="d7015-157">Используйте пароль для входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="d7015-157">Use a password for logging on the user.</span></span> <span data-ttu-id="d7015-158">Пароль должен указываться во время регистрации.</span><span class="sxs-lookup"><span data-stu-id="d7015-158">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="d7015-159"><dt>**Задача \_ Вход в систему \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-159"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="d7015-160">Использовать существующий интерактивный токен для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="d7015-160">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="d7015-161">Пользователь должен войти в систему, используя службу для входа пользователя (S4U).</span><span class="sxs-lookup"><span data-stu-id="d7015-161">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="d7015-162">При использовании имени входа S4U система не хранит пароль и не имеет доступа к сети или к зашифрованным файлам.</span><span class="sxs-lookup"><span data-stu-id="d7015-162">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="d7015-163"><dt>**Задача \_ \_Интерактивный \_ маркер входа**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-163"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="d7015-164">Пользователь уже должен войти в систему.</span><span class="sxs-lookup"><span data-stu-id="d7015-164">User must already be logged on.</span></span> <span data-ttu-id="d7015-165">Задача будет запущена только в существующем интерактивном сеансе.</span><span class="sxs-lookup"><span data-stu-id="d7015-165">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="d7015-166"><dt>**Задача \_ \_Группа входа**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-166"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="d7015-167">Активация группы.</span><span class="sxs-lookup"><span data-stu-id="d7015-167">Group activation.</span></span> <span data-ttu-id="d7015-168">Поле **groupId** указывает группу.</span><span class="sxs-lookup"><span data-stu-id="d7015-168">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="d7015-169"><dt>**Задача \_ \_ \_ Учетная запись службы входа**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-169"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="d7015-170">Указывает, что в качестве контекста безопасности для выполнения задачи используется локальная система, локальная служба или учетная запись сетевой службы.</span><span class="sxs-lookup"><span data-stu-id="d7015-170">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="d7015-171"><dt>**Задача \_ \_Интерактивный \_ маркер входа \_ или \_ пароль**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-171"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="d7015-172">Сначала используйте интерактивный токен.</span><span class="sxs-lookup"><span data-stu-id="d7015-172">First use the interactive token.</span></span> <span data-ttu-id="d7015-173">Если пользователь не вошел в систему (интерактивный маркер недоступен), то используется пароль.</span><span class="sxs-lookup"><span data-stu-id="d7015-173">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="d7015-174">При регистрации задачи необходимо указать пароль.</span><span class="sxs-lookup"><span data-stu-id="d7015-174">The password must be specified when a task is registered.</span></span> <span data-ttu-id="d7015-175">Этот флаг не рекомендуется для новых задач, так как он менее надежен, чем \_ пароль для входа в систему \_ .</span><span class="sxs-lookup"><span data-stu-id="d7015-175">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d7015-176">*SDDL* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d7015-176">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7015-177">Дескриптор безопасности, связанный с зарегистрированной задачей.</span><span class="sxs-lookup"><span data-stu-id="d7015-177">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="d7015-178">Вы можете указать список управления доступом (ACL) в дескрипторе безопасности задачи, чтобы разрешить или запретить определенным пользователям и группам доступ к задаче.</span><span class="sxs-lookup"><span data-stu-id="d7015-178">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="d7015-179">Если локальной системной учетной записи запрещен доступ к задаче, то служба планировщик задач может получить непредвиденные результаты.</span><span class="sxs-lookup"><span data-stu-id="d7015-179">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="d7015-180">*задача* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7015-180">*task* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7015-181">Объект [**регистередтаск**](registeredtask.md) , представляющий новую задачу.</span><span class="sxs-lookup"><span data-stu-id="d7015-181">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7015-182">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7015-182">Return value</span></span>

<span data-ttu-id="d7015-183">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d7015-183">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7015-184">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7015-184">Remarks</span></span>

<span data-ttu-id="d7015-185">Для задачи, которая содержит действие «окно сообщения», появится окно сообщения, если задача активирована, а задача имеет интерактивный тип входа в систему.</span><span class="sxs-lookup"><span data-stu-id="d7015-185">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="d7015-186">Чтобы установить для параметра Тип входа в интерактивный режим, укажите значение 3 (**\_ \_ Интерактивный \_ маркер входа в систему**) или 4 (**\_ \_ Группа входа** в систему) в свойстве [**LogonType**](principal-logontype.md) участника задачи или в параметре *LogonType* [**таскфолдер. регистертаск**](taskfolder-registertask.md) или **таскфолдер. регистертаскдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="d7015-186">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or **TaskFolder.RegisterTaskDefinition**.</span></span>

<span data-ttu-id="d7015-187">Только член группы "Администраторы" может создать задачу с триггером загрузки.</span><span class="sxs-lookup"><span data-stu-id="d7015-187">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="d7015-188">Вы можете успешно зарегистрировать задачу с группой, указанной в параметре *UserID* , и 3 (**\_ \_ Интерактивный \_ токен входа задачи**), указанный в параметре *logonType* [**таскфолдер. регистертаск**](taskfolder-registertask.md) или **таскфолдер. регистертаскдефинитион**, но задача не будет запущена.</span><span class="sxs-lookup"><span data-stu-id="d7015-188">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or **TaskFolder.RegisterTaskDefinition**, but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7015-189">Требования</span><span class="sxs-lookup"><span data-stu-id="d7015-189">Requirements</span></span>



| <span data-ttu-id="d7015-190">Требование</span><span class="sxs-lookup"><span data-stu-id="d7015-190">Requirement</span></span> | <span data-ttu-id="d7015-191">Значение</span><span class="sxs-lookup"><span data-stu-id="d7015-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7015-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7015-192">Minimum supported client</span></span><br/> | <span data-ttu-id="d7015-193">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7015-193">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d7015-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7015-194">Minimum supported server</span></span><br/> | <span data-ttu-id="d7015-195">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7015-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7015-196">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d7015-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7015-197"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-197"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7015-198">DLL</span><span class="sxs-lookup"><span data-stu-id="d7015-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7015-199"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-199"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7015-200">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7015-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7015-201">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d7015-201">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d7015-202">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="d7015-202">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="d7015-203">**таскфолдер**</span><span class="sxs-lookup"><span data-stu-id="d7015-203">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

 





