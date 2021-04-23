---
title: Тасксеттингс. Мултиплеинстанцес, свойство
description: Для создания скриптов Возвращает или задает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- планировщик задач свойства Мултиплеинстанцес
- Планировщик задач свойства Мултиплеинстанцес, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Мултиплеинстанцес
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533854"
---
# <a name="tasksettingsmultipleinstances-property"></a><span data-ttu-id="893f0-106">Тасксеттингс. Мултиплеинстанцес, свойство</span><span class="sxs-lookup"><span data-stu-id="893f0-106">TaskSettings.MultipleInstances property</span></span>

<span data-ttu-id="893f0-107">Для создания скриптов Возвращает или задает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.</span><span class="sxs-lookup"><span data-stu-id="893f0-107">For scripting, gets or sets the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

<span data-ttu-id="893f0-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="893f0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="893f0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="893f0-109">Syntax</span></span>


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a><span data-ttu-id="893f0-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="893f0-110">Property value</span></span>

<span data-ttu-id="893f0-111">[**Задача \_ Константы \_ политики экземпляров**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) .</span><span class="sxs-lookup"><span data-stu-id="893f0-111">[**TASK\_INSTANCES\_POLICY**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) constants.</span></span>



| <span data-ttu-id="893f0-112">Значение</span><span class="sxs-lookup"><span data-stu-id="893f0-112">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="893f0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="893f0-113">Meaning</span></span>                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <span data-ttu-id="893f0-114"><dt>**Задача \_ \_Параллельные экземпляры**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="893f0-114"><dt>**TASK\_INSTANCES\_PARALLEL**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="893f0-115">Запускает новый экземпляр, пока запущен существующий экземпляр задачи.</span><span class="sxs-lookup"><span data-stu-id="893f0-115">Starts a new instance while an existing instance of the task is running.</span></span><br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <span data-ttu-id="893f0-116"><dt>**Задача \_ \_Очередь экземпляров**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="893f0-116"><dt>**TASK\_INSTANCES\_QUEUE**</dt> <dt>1</dt></span></span> </dl>                          | <span data-ttu-id="893f0-117">Запускает новый экземпляр задачи после завершения всех остальных экземпляров задачи.</span><span class="sxs-lookup"><span data-stu-id="893f0-117">Starts a new instance of the task after all other instances of the task are complete.</span></span><br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <span data-ttu-id="893f0-118"><dt>**Задача \_ ЭКЗЕМПЛЯРЫ, не \_ пропускаемые \_ New**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="893f0-118"><dt>**TASK\_INSTANCES\_IGNORE\_NEW**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="893f0-119">Не запускает новый экземпляр, если запущен существующий экземпляр задачи.</span><span class="sxs-lookup"><span data-stu-id="893f0-119">Does not start a new instance if an existing instance of the task is running.</span></span><br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <span data-ttu-id="893f0-120"><dt>**Задача \_ ЭКЗЕМПЛЯРЫ \_ прекращают \_ существующие**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="893f0-120"><dt>**TASK\_INSTANCES\_STOP\_EXISTING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="893f0-121">Останавливает существующий экземпляр задачи перед запуском нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="893f0-121">Stops an existing instance of the task before it starts new instance.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="893f0-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="893f0-122">Remarks</span></span>

<span data-ttu-id="893f0-123">При чтении или записи XML для задачи этот параметр указывается в элементе [**мултиплеинстанцесполици**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="893f0-123">When reading or writing XML for a task, this setting is specified in the [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="893f0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="893f0-124">Requirements</span></span>



| <span data-ttu-id="893f0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="893f0-125">Requirement</span></span> | <span data-ttu-id="893f0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="893f0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="893f0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="893f0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="893f0-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="893f0-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="893f0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="893f0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="893f0-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="893f0-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="893f0-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="893f0-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="893f0-132"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="893f0-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="893f0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="893f0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="893f0-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="893f0-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="893f0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="893f0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="893f0-136">**\_политика экземпляров \_ задач**</span><span class="sxs-lookup"><span data-stu-id="893f0-136">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[<span data-ttu-id="893f0-137">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="893f0-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





