---
title: Регистередтаск. среды выполнения, метод
description: Для сценариев Возвращает время, которое запланировано для выполнения зарегистрированной задачи в течение заданного времени.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Метод среды выполнения планировщик задач
- Метод среды выполнения планировщик задач, объект Регистередтаск
- Планировщик задач объекта Регистередтаск, метод среды выполнения
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534889"
---
# <a name="registeredtaskgetruntimes-method"></a><span data-ttu-id="7f34a-106">Регистередтаск. среды выполнения, метод</span><span class="sxs-lookup"><span data-stu-id="7f34a-106">RegisteredTask.GetRunTimes method</span></span>

<span data-ttu-id="7f34a-107">Для сценариев Возвращает время, которое запланировано для выполнения зарегистрированной задачи в течение заданного времени.</span><span class="sxs-lookup"><span data-stu-id="7f34a-107">For scripting, gets the times that the registered task is scheduled to run during a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f34a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f34a-108">Syntax</span></span>


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a><span data-ttu-id="7f34a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f34a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f34a-110">*Начало* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f34a-110">*begin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f34a-111">Время начала запроса.</span><span class="sxs-lookup"><span data-stu-id="7f34a-111">The starting time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="7f34a-112">*конец* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f34a-112">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f34a-113">Время окончания запроса.</span><span class="sxs-lookup"><span data-stu-id="7f34a-113">The ending time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="7f34a-114">*количество* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f34a-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f34a-115">Количество запланированных запусков задачи.</span><span class="sxs-lookup"><span data-stu-id="7f34a-115">The number of scheduled times the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="7f34a-116">*ргсттасктимес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f34a-116">*rgstTaskTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f34a-117">Запланированное время выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="7f34a-117">The scheduled times that the task will run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f34a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f34a-118">Return value</span></span>

<span data-ttu-id="7f34a-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7f34a-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f34a-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f34a-120">Remarks</span></span>

<span data-ttu-id="7f34a-121">Если зарегистрированная задача содержит триггеры, которые по отдельности отключены, эти триггеры будут влиять на следующее запланированное время выполнения, которое возвращается, даже если они отключены.</span><span class="sxs-lookup"><span data-stu-id="7f34a-121">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f34a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7f34a-122">Requirements</span></span>



| <span data-ttu-id="7f34a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7f34a-123">Requirement</span></span> | <span data-ttu-id="7f34a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7f34a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f34a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f34a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7f34a-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f34a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7f34a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f34a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7f34a-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f34a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f34a-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7f34a-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="7f34a-130"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7f34a-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7f34a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7f34a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f34a-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f34a-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f34a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f34a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f34a-134">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="7f34a-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="7f34a-135">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="7f34a-135">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





