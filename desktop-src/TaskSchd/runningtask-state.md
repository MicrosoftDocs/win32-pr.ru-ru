---
title: Руннингтаск. State, свойство
description: Для создания скриптов возвращает идентификатор для состояния выполняющейся задачи.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- Свойство State планировщик задач
- Свойство State планировщик задач, объект Руннингтаск
- Планировщик задач объекта Руннингтаск, свойство State
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b962de116eef1301be209828181147dfe03273e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801792"
---
# <a name="runningtaskstate-property"></a><span data-ttu-id="d9a8a-106">Руннингтаск. State, свойство</span><span class="sxs-lookup"><span data-stu-id="d9a8a-106">RunningTask.State property</span></span>

<span data-ttu-id="d9a8a-107">Для создания скриптов возвращает идентификатор для состояния выполняющейся задачи.</span><span class="sxs-lookup"><span data-stu-id="d9a8a-107">For scripting, gets an identifier for the state of the running task.</span></span>

<span data-ttu-id="d9a8a-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d9a8a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a8a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9a8a-109">Syntax</span></span>


```VB
RunningTask.State As String
```



## <a name="property-value"></a><span data-ttu-id="d9a8a-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d9a8a-110">Property value</span></span>

<span data-ttu-id="d9a8a-111">Идентификатор состояния выполняемой задачи.</span><span class="sxs-lookup"><span data-stu-id="d9a8a-111">An identifier for the state of the running task.</span></span>



| <span data-ttu-id="d9a8a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d9a8a-112">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="d9a8a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d9a8a-113">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="d9a8a-114"><dt>**Задача \_ \_Неизвестное состояние**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d9a8a-114"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="d9a8a-115">Состояние задачи неизвестно.</span><span class="sxs-lookup"><span data-stu-id="d9a8a-115">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="d9a8a-116"><dt>**Задача \_ СОСТОЯНИЕ " \_ отключено**</dt> <dt>1</dt> "</span><span class="sxs-lookup"><span data-stu-id="d9a8a-116"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="d9a8a-117">Задача зарегистрирована, но отключена и ни одна из экземпляров задачи не поставлена в очередь или запущена.</span><span class="sxs-lookup"><span data-stu-id="d9a8a-117">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="d9a8a-118">Задача не может быть выполнена, пока она не будет включена.</span><span class="sxs-lookup"><span data-stu-id="d9a8a-118">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="d9a8a-119"><dt>**Задача \_ СОСТОЯНИЕ \_ поставлено в очередь**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d9a8a-119"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="d9a8a-120">Экземпляры задачи поставлены в очередь.</span><span class="sxs-lookup"><span data-stu-id="d9a8a-120">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="d9a8a-121"><dt>**Задача \_ СОСТОЯНИЕ \_ готовности**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d9a8a-121"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="d9a8a-122">Задача готова к выполнению, но экземпляры не поставлены в очередь или запущены.</span><span class="sxs-lookup"><span data-stu-id="d9a8a-122">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="d9a8a-123"><dt>**Задача \_ СОСТОЯНИЕ \_ выполнения**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d9a8a-123"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="d9a8a-124">Выполняется один или несколько экземпляров задачи.</span><span class="sxs-lookup"><span data-stu-id="d9a8a-124">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="d9a8a-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9a8a-125">Remarks</span></span>

<span data-ttu-id="d9a8a-126">Метод [**руннингтаск. Refresh**](runningtask-refresh.md) вызывается перед возвратом значения свойства.</span><span class="sxs-lookup"><span data-stu-id="d9a8a-126">The [**RunningTask.Refresh**](runningtask-refresh.md) method is called before the property value is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a8a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d9a8a-127">Requirements</span></span>



| <span data-ttu-id="d9a8a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d9a8a-128">Requirement</span></span> | <span data-ttu-id="d9a8a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d9a8a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a8a-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9a8a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d9a8a-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9a8a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d9a8a-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9a8a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d9a8a-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d9a8a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9a8a-134">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d9a8a-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9a8a-135"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d9a8a-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d9a8a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d9a8a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9a8a-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9a8a-137"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





