---
title: Регистередтаск. Рунекс, метод
description: Для сценариев запускает зарегистрированную задачу сразу же с помощью указанных флагов и идентификатора сеанса.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- планировщик задач метода Рунекс
- Планировщик задач метода Рунекс, объект Регистередтаск
- Планировщик задач объекта Регистередтаск, метод Рунекс
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136554"
---
# <a name="registeredtaskrunex-method"></a><span data-ttu-id="2210f-106">Регистередтаск. Рунекс, метод</span><span class="sxs-lookup"><span data-stu-id="2210f-106">RegisteredTask.RunEx method</span></span>

<span data-ttu-id="2210f-107">Для сценариев запускает зарегистрированную задачу сразу же с помощью указанных флагов и идентификатора сеанса.</span><span class="sxs-lookup"><span data-stu-id="2210f-107">For scripting, runs the registered task immediately using specified flags and a session identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="2210f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2210f-108">Syntax</span></span>


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="2210f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2210f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2210f-110">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2210f-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2210f-111">Параметры, используемые в качестве значений в действиях задач.</span><span class="sxs-lookup"><span data-stu-id="2210f-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="2210f-112">Чтобы не указывать значения параметров для действий задач, присвойте этому параметру значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="2210f-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="2210f-113">В противном случае можно указать одно строковое значение или массив строковых значений.</span><span class="sxs-lookup"><span data-stu-id="2210f-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="2210f-114">Указанные строковые значения связаны с именами и хранятся в виде пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="2210f-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="2210f-115">Если указать одно строковое значение, то Arg0 будет иметь имя, присвоенное значению.</span><span class="sxs-lookup"><span data-stu-id="2210f-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="2210f-116">Значение может использоваться в действии задачи, где переменная $ (Arg0) используется в свойствах действия.</span><span class="sxs-lookup"><span data-stu-id="2210f-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="2210f-117">Если передать значения, такие как "0", "100" и "250", в виде массива строковых значений, "0" заменит переменные $ (Arg0), "100" заменит переменные $ (arg1), а "250" заменит переменные $ (arg2), используемые в свойствах действия.</span><span class="sxs-lookup"><span data-stu-id="2210f-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="2210f-118">Можно указать не более 32 строковых значений.</span><span class="sxs-lookup"><span data-stu-id="2210f-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="2210f-119">Дополнительные сведения и список свойств действий, которые могут использовать переменные $ (Arg0), $ (arg1),..., $ (Arg32) в своих значениях, см. в разделе [действия задач](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="2210f-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="2210f-120">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2210f-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2210f-121">Константа [ \_ \_ флага запуска задачи](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) , определяющая, как выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="2210f-121">A [TASK\_RUN\_FLAGS](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) constant that defines how the task is run.</span></span>

</dd> <dt>

<span data-ttu-id="2210f-122">*идентификатор сеанса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2210f-122">*sessionID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2210f-123">Сеанс сервера терминалов, в котором требуется запустить задачу.</span><span class="sxs-lookup"><span data-stu-id="2210f-123">The terminal server session in which you want to launch the task.</span></span>

<span data-ttu-id="2210f-124">Если в \_ \_ \_ \_ параметре *flags* не передана константа с идентификатором сеанса, то значение, указанное в этом параметре, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2210f-124">If the TASK\_RUN\_USE\_SESSION\_ID constant (0x4) is not passed into the *flags* parameter, then the value specified in this parameter is ignored.</span></span> <span data-ttu-id="2210f-125">Если при \_ выполнении задачи \_ в \_ \_ параметре *flags* передается константа идентификатора сеанса, а значение SessionID меньше или равно 0, то возвращается ошибка недопустимого аргумента.</span><span class="sxs-lookup"><span data-stu-id="2210f-125">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is less than or equal to 0, then an invalid argument error will be returned.</span></span>

<span data-ttu-id="2210f-126">Если в \_ \_ \_ \_ параметре *flags* передается константа с идентификатором сеанса, а значение SessionID является допустимым идентификатором сеанса больше 0 и если для параметра *user* не указано значение, то служба Планировщик задач попытается запустить задачу в интерактивном режиме в качестве пользователя, выполнившего вход в указанный сеанс.</span><span class="sxs-lookup"><span data-stu-id="2210f-126">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if no value is specified for the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is logged on to the specified session.</span></span>

<span data-ttu-id="2210f-127">Если в \_ \_ \_ \_ параметре *flags* передается константа с идентификатором сеанса, а значением SessionID является допустимый идентификатор сеанса больше 0. Если пользователь указан в параметре *User* , то служба Планировщик задач попытается запустить задачу в интерактивном режиме в качестве пользователя, указанного в параметре *User* .</span><span class="sxs-lookup"><span data-stu-id="2210f-127">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if a user is specified in the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2210f-128">*руннингтаск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2210f-128">*runningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2210f-129">Объект [**руннингтаск**](runningtask.md) , определяющий новый экземпляр задачи.</span><span class="sxs-lookup"><span data-stu-id="2210f-129">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2210f-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2210f-130">Return value</span></span>

<span data-ttu-id="2210f-131">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2210f-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2210f-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2210f-132">Remarks</span></span>

<span data-ttu-id="2210f-133">Этот метод будет возвращать значение без ошибок, но задача не будет выполняться, если для зарегистрированной задачи свойство [**тасксеттингс. алловдемандстарт**](tasksettings-allowdemandstart.md) имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="2210f-133">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="2210f-134">Требования</span><span class="sxs-lookup"><span data-stu-id="2210f-134">Requirements</span></span>



| <span data-ttu-id="2210f-135">Требование</span><span class="sxs-lookup"><span data-stu-id="2210f-135">Requirement</span></span> | <span data-ttu-id="2210f-136">Значение</span><span class="sxs-lookup"><span data-stu-id="2210f-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2210f-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2210f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2210f-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2210f-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2210f-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2210f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2210f-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2210f-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2210f-141">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2210f-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="2210f-142"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2210f-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2210f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2210f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2210f-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2210f-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2210f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2210f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2210f-146">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="2210f-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="2210f-147">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="2210f-147">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





