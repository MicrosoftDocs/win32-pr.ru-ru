---
title: TaskService. Жетруннингтаскс, метод
description: Для создания скриптов Возвращает коллекцию выполняющихся задач.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- планировщик задач метода Жетруннингтаскс
- Планировщик задач метода Жетруннингтаскс, объект TaskService
- Планировщик задач объекта TaskService, метод Жетруннингтаскс
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803953"
---
# <a name="taskservicegetrunningtasks-method"></a><span data-ttu-id="5e782-106">TaskService. Жетруннингтаскс, метод</span><span class="sxs-lookup"><span data-stu-id="5e782-106">TaskService.GetRunningTasks method</span></span>

<span data-ttu-id="5e782-107">Для создания скриптов Возвращает коллекцию выполняющихся задач.</span><span class="sxs-lookup"><span data-stu-id="5e782-107">For scripting, gets a collection of running tasks.</span></span>

> [!Note]  
> <span data-ttu-id="5e782-108">**TaskService. жетруннингтаскс** будет возвращать только коллекцию выполняющихся задач, выполняемых в контексте безопасности пользователя или ниже.</span><span class="sxs-lookup"><span data-stu-id="5e782-108">**TaskService.GetRunningTasks** will only return a collection of running tasks that are running at or below a user's security context.</span></span> <span data-ttu-id="5e782-109">Например, для членов группы "Администраторы" **жетруннингтаскс** будет возвращать коллекцию всех выполняемых задач, но для членов группы "Пользователи" **жетруннингтаскс** будет возвращать только коллекцию задач, которые выполняются в контексте безопасности группы "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="5e782-109">For example, for members of the Administrators group, **GetRunningTasks** will return a collection of all running tasks, but for members of the Users group, **GetRunningTasks** will only return a collection of tasks that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5e782-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e782-110">Syntax</span></span>


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="5e782-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e782-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e782-112">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e782-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e782-113">Передайте значение 1, чтобы вернуть все выполняемые задачи, включая скрытые задачи.</span><span class="sxs-lookup"><span data-stu-id="5e782-113">Pass in 1 to return all running tasks, including hidden tasks.</span></span> <span data-ttu-id="5e782-114">Передайте значение 0, чтобы получить коллекцию выполняющихся задач, которые не являются скрытыми.</span><span class="sxs-lookup"><span data-stu-id="5e782-114">Pass in 0 to return a collection of running tasks that are not hidden tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e782-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e782-115">Return value</span></span>

<span data-ttu-id="5e782-116">Объект [**руннингтаскколлектион**](runningtaskcollection.md) , содержащий выполняемые в данный момент задачи.</span><span class="sxs-lookup"><span data-stu-id="5e782-116">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains the currently running tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e782-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5e782-117">Requirements</span></span>



| <span data-ttu-id="5e782-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5e782-118">Requirement</span></span> | <span data-ttu-id="5e782-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5e782-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e782-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e782-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5e782-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e782-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5e782-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e782-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5e782-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e782-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e782-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5e782-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e782-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5e782-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5e782-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5e782-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e782-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e782-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e782-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e782-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e782-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="5e782-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





