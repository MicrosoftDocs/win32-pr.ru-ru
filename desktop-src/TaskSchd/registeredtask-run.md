---
title: Регистередтаск. Run, метод
description: Для сценариев запускает зарегистрированную задачу немедленно.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Метод Run планировщик задач
- Метод Run планировщик задач, объект Регистередтаск
- Планировщик задач объекта Регистередтаск, метод Run
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682033"
---
# <a name="registeredtaskrun-method"></a><span data-ttu-id="18da6-106">Регистередтаск. Run, метод</span><span class="sxs-lookup"><span data-stu-id="18da6-106">RegisteredTask.Run method</span></span>

<span data-ttu-id="18da6-107">Для сценариев запускает зарегистрированную задачу немедленно.</span><span class="sxs-lookup"><span data-stu-id="18da6-107">For scripting, runs the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="18da6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18da6-108">Syntax</span></span>


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="18da6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="18da6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18da6-110">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18da6-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18da6-111">Параметры, используемые в качестве значений в действиях задач.</span><span class="sxs-lookup"><span data-stu-id="18da6-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="18da6-112">Чтобы не указывать значения параметров для действий задач, присвойте этому параметру значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="18da6-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="18da6-113">В противном случае можно указать одно строковое значение или массив строковых значений.</span><span class="sxs-lookup"><span data-stu-id="18da6-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="18da6-114">Указанные строковые значения связаны с именами и хранятся в виде пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="18da6-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="18da6-115">Если указать одно строковое значение, то Arg0 будет иметь имя, присвоенное значению.</span><span class="sxs-lookup"><span data-stu-id="18da6-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="18da6-116">Значение может использоваться в действии задачи, где переменная $ (Arg0) используется в свойствах действия.</span><span class="sxs-lookup"><span data-stu-id="18da6-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="18da6-117">Если передать значения, такие как "0", "100" и "250", в виде массива строковых значений, "0" заменит переменные $ (Arg0), "100" заменит переменные $ (arg1), а "250" заменит переменные $ (arg2), используемые в свойствах действия.</span><span class="sxs-lookup"><span data-stu-id="18da6-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="18da6-118">Можно указать не более 32 строковых значений.</span><span class="sxs-lookup"><span data-stu-id="18da6-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="18da6-119">Дополнительные сведения и список свойств действий, которые могут использовать переменные $ (Arg0), $ (arg1),..., $ (Arg32) в своих значениях, см. в разделе [действия задач](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="18da6-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="18da6-120">*ппруннингтаск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="18da6-120">*ppRunningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18da6-121">Объект [**руннингтаск**](runningtask.md) , определяющий новый экземпляр задачи.</span><span class="sxs-lookup"><span data-stu-id="18da6-121">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18da6-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18da6-122">Return value</span></span>

<span data-ttu-id="18da6-123">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="18da6-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18da6-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18da6-124">Remarks</span></span>

<span data-ttu-id="18da6-125">Функция **регистередтаск. Run** эквивалентна функции [**регистередтаск. рунекс**](registeredtask-runex.md) с параметром flags, равным 0, и ничего не указано для параметра пользователя.</span><span class="sxs-lookup"><span data-stu-id="18da6-125">The **RegisteredTask.Run** function is equivalent to the [**RegisteredTask.RunEx**](registeredtask-runex.md) function with the flags parameter equal to 0 and nothing specified for the user parameter.</span></span>

<span data-ttu-id="18da6-126">Этот метод будет возвращать значение без ошибок, но задача не будет выполняться, если для зарегистрированной задачи свойство [**тасксеттингс. алловдемандстарт**](tasksettings-allowdemandstart.md) имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="18da6-126">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="18da6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="18da6-127">Requirements</span></span>



| <span data-ttu-id="18da6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="18da6-128">Requirement</span></span> | <span data-ttu-id="18da6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="18da6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18da6-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18da6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="18da6-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18da6-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="18da6-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18da6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="18da6-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18da6-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18da6-134">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="18da6-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="18da6-135"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="18da6-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="18da6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="18da6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18da6-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18da6-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18da6-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18da6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18da6-139">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="18da6-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="18da6-140">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="18da6-140">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





