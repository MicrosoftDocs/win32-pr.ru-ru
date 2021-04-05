---
title: Регистередтаск. Расчетное nextruntime, свойство
description: Для создания сценариев Возвращает время следующего запланированного выполнения зарегистрированной задачи.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- планировщик задач свойства расчетное nextruntime
- Планировщик задач свойства расчетное nextruntime, объект Регистередтаск
- Планировщик задач объекта Регистередтаск, свойство расчетное nextruntime
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803233"
---
# <a name="registeredtasknextruntime-property"></a><span data-ttu-id="f7903-106">Регистередтаск. Расчетное nextruntime, свойство</span><span class="sxs-lookup"><span data-stu-id="f7903-106">RegisteredTask.NextRunTime property</span></span>

<span data-ttu-id="f7903-107">Для создания сценариев Возвращает время следующего запланированного выполнения зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="f7903-107">For scripting, gets the time when the registered task is next scheduled to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7903-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7903-108">Syntax</span></span>


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a><span data-ttu-id="f7903-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f7903-109">Property value</span></span>

<span data-ttu-id="f7903-110">Время следующего запланированного выполнения зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="f7903-110">The time when the registered task is next scheduled to run.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7903-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7903-111">Remarks</span></span>

<span data-ttu-id="f7903-112">Если зарегистрированная задача содержит триггеры, которые по отдельности отключены, эти триггеры будут влиять на следующее запланированное время выполнения, которое возвращается, даже если они отключены.</span><span class="sxs-lookup"><span data-stu-id="f7903-112">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7903-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f7903-113">Requirements</span></span>



| <span data-ttu-id="f7903-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f7903-114">Requirement</span></span> | <span data-ttu-id="f7903-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f7903-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7903-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7903-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f7903-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7903-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f7903-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7903-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f7903-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f7903-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f7903-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f7903-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7903-121"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f7903-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f7903-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f7903-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7903-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7903-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7903-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7903-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7903-125">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="f7903-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f7903-126">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="f7903-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





