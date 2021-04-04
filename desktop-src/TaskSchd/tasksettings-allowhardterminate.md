---
title: Тасксеттингс. Алловхардтерминате, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача может быть завершена планировщик задачной службой с помощью Терминатепроцесс.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- планировщик задач свойства Алловхардтерминате
- Планировщик задач свойства Алловхардтерминате, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Алловхардтерминате
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802962"
---
# <a name="tasksettingsallowhardterminate-property"></a><span data-ttu-id="18911-106">Тасксеттингс. Алловхардтерминате, свойство</span><span class="sxs-lookup"><span data-stu-id="18911-106">TaskSettings.AllowHardTerminate property</span></span>

<span data-ttu-id="18911-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача может быть завершена планировщик задачной службой с помощью [**терминатепроцесс**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span><span class="sxs-lookup"><span data-stu-id="18911-107">For scripting, gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="18911-108">Служба попытается закрыть выполняющуюся задачу, отправив уведомление [**о \_ закрытии WM**](../winmsg/wm-close.md) . Если задача не отвечает, задача будет прервана, только если для этого свойства задано значение true.</span><span class="sxs-lookup"><span data-stu-id="18911-108">The service will try to close the running task by sending the [**WM\_CLOSE**](../winmsg/wm-close.md) notification, and if the task does not respond, the task will be terminated only if this property is set to true.</span></span>

<span data-ttu-id="18911-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="18911-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="18911-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18911-110">Syntax</span></span>


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="18911-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="18911-111">Property value</span></span>

<span data-ttu-id="18911-112">Если значение — true, задача может быть прервана с помощью [**терминатепроцесс**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span><span class="sxs-lookup"><span data-stu-id="18911-112">If True, the task can be terminated by using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="18911-113">Если задано значение false, задача не может быть завершена с помощью **терминатепроцесс**.</span><span class="sxs-lookup"><span data-stu-id="18911-113">If False, the task cannot be terminated by using **TerminateProcess**.</span></span>

## <a name="remarks"></a><span data-ttu-id="18911-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18911-114">Remarks</span></span>

<span data-ttu-id="18911-115">При чтении или записи XML для задачи этот параметр указывается в элементе [алловхардтерминате](taskschedulerschema-allowhardterminate-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="18911-115">When reading or writing XML for a task, this setting is specified in the [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="18911-116">Требования</span><span class="sxs-lookup"><span data-stu-id="18911-116">Requirements</span></span>



| <span data-ttu-id="18911-117">Требование</span><span class="sxs-lookup"><span data-stu-id="18911-117">Requirement</span></span> | <span data-ttu-id="18911-118">Значение</span><span class="sxs-lookup"><span data-stu-id="18911-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18911-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18911-119">Minimum supported client</span></span><br/> | <span data-ttu-id="18911-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18911-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="18911-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18911-121">Minimum supported server</span></span><br/> | <span data-ttu-id="18911-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18911-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18911-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="18911-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="18911-124"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="18911-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="18911-125">DLL</span><span class="sxs-lookup"><span data-stu-id="18911-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18911-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18911-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18911-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18911-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18911-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="18911-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

