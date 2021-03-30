---
title: Тасксеттингс. Compatibility, свойство
description: Для создания скриптов Возвращает или задает целочисленное значение, указывающее версию планировщик задач, с которой совместима задача.
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Свойство Compatibility планировщик задач
- Свойство Compatibility планировщик задач, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Compatibility
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801762"
---
# <a name="tasksettingscompatibility-property"></a><span data-ttu-id="65254-106">Тасксеттингс. Compatibility, свойство</span><span class="sxs-lookup"><span data-stu-id="65254-106">TaskSettings.Compatibility property</span></span>

<span data-ttu-id="65254-107">Для создания скриптов Возвращает или задает целочисленное значение, указывающее версию планировщик задач, с которой совместима задача.</span><span class="sxs-lookup"><span data-stu-id="65254-107">For scripting, gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with.</span></span>

<span data-ttu-id="65254-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="65254-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65254-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65254-109">Syntax</span></span>


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a><span data-ttu-id="65254-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="65254-110">Property value</span></span>



| <span data-ttu-id="65254-111">Значение</span><span class="sxs-lookup"><span data-stu-id="65254-111">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="65254-112">Значение</span><span class="sxs-lookup"><span data-stu-id="65254-112">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <span data-ttu-id="65254-113"><dt>**Задача \_ СОВМЕСТИМОСТЬ \_ с**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="65254-113"><dt>**TASK\_COMPATIBILITY\_AT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="65254-114">Задача совместима с командой AT.</span><span class="sxs-lookup"><span data-stu-id="65254-114">The task is compatible with the AT command.</span></span><br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <span data-ttu-id="65254-115"><dt>**Задача \_ СОВМЕСТИМОСТЬ \_ v1**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="65254-115"><dt>**TASK\_COMPATIBILITY\_V1**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="65254-116">Задача совместима с планировщик задач 1,0.</span><span class="sxs-lookup"><span data-stu-id="65254-116">The task is compatible with Task Scheduler 1.0.</span></span><br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <span data-ttu-id="65254-117"><dt>**Задача \_ СОВМЕСТИМОСТЬ \_ v2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="65254-117"><dt>**TASK\_COMPATIBILITY\_V2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="65254-118">Задача совместима с планировщик задач 2,0.</span><span class="sxs-lookup"><span data-stu-id="65254-118">The task is compatible with Task Scheduler 2.0.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65254-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65254-119">Remarks</span></span>

<span data-ttu-id="65254-120">Совместимость задач, которая задается с помощью свойства [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , должна быть установлена только для \_ обеспечения совместимости задач, если требуется \_ доступ к задаче или ее изменение с компьютера под управлением Windows XP, Windows Server 2003 или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="65254-120">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task needs to be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="65254-121">В противном случае рекомендуется использовать совместимость с планировщик задач 2,0, так как задача будет иметь больше функций.</span><span class="sxs-lookup"><span data-stu-id="65254-121">Otherwise, it is recommended that Task Scheduler 2.0 compatibility be used because the task will have more features.</span></span>

<span data-ttu-id="65254-122">Задачи, совместимые с командой AT, могут иметь только один триггер времени.</span><span class="sxs-lookup"><span data-stu-id="65254-122">Tasks compatible with the AT command can only have one time trigger.</span></span>

<span data-ttu-id="65254-123">Задачи, совместимые с планировщик задач 1,0, могут иметь только триггер времени, триггер входа или загрузочный триггер, и задача может иметь только исполняемое действие.</span><span class="sxs-lookup"><span data-stu-id="65254-123">Tasks compatible with Task Scheduler 1.0 can only have a time trigger, a logon trigger, or a boot trigger, and the task can only have an executable action.</span></span>

<span data-ttu-id="65254-124">Дополнительные сведения о совместимости задач см. [в разделе новые возможности планировщик задач](what-s-new-in-task-scheduler.md) и [задач](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="65254-124">For more information about task compatibility, see [What's New in Task Scheduler](what-s-new-in-task-scheduler.md) and [Tasks](tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65254-125">Требования</span><span class="sxs-lookup"><span data-stu-id="65254-125">Requirements</span></span>



| <span data-ttu-id="65254-126">Требование</span><span class="sxs-lookup"><span data-stu-id="65254-126">Requirement</span></span> | <span data-ttu-id="65254-127">Значение</span><span class="sxs-lookup"><span data-stu-id="65254-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65254-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65254-128">Minimum supported client</span></span><br/> | <span data-ttu-id="65254-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65254-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="65254-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65254-130">Minimum supported server</span></span><br/> | <span data-ttu-id="65254-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65254-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65254-132">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="65254-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="65254-133"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="65254-133"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="65254-134">DLL</span><span class="sxs-lookup"><span data-stu-id="65254-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65254-135"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65254-135"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65254-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65254-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65254-137">**\_совместимость задач**</span><span class="sxs-lookup"><span data-stu-id="65254-137">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[<span data-ttu-id="65254-138">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="65254-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





