---
title: Свойство Trigger. повторения
description: Для создания скриптов Возвращает или задает значение, указывающее, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- планировщик задач свойства повторения
- Планировщик задач свойства повторения, объект триггера
- Триггер объекта планировщик задач, свойство повторения
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672585"
---
# <a name="triggerrepetition-property"></a><span data-ttu-id="15fb5-106">Свойство Trigger. повторения</span><span class="sxs-lookup"><span data-stu-id="15fb5-106">Trigger.Repetition property</span></span>

<span data-ttu-id="15fb5-107">Для создания скриптов Возвращает или задает значение, указывающее, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="15fb5-107">For scripting, gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="15fb5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15fb5-108">Syntax</span></span>


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a><span data-ttu-id="15fb5-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="15fb5-109">Property value</span></span>

<span data-ttu-id="15fb5-110">Объект [**репетитионпаттерн**](repetitionpattern.md) , который определяет, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="15fb5-110">A [**RepetitionPattern**](repetitionpattern.md) object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="15fb5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15fb5-111">Remarks</span></span>

<span data-ttu-id="15fb5-112">При чтении или записи собственного XML-кода для задачи шаблон повторения для триггера указывается в элементе [**повторения**](taskschedulerschema-repetition-triggerbasetype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="15fb5-112">When reading or writing your own XML for a task, the repetition pattern for a trigger is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="15fb5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="15fb5-113">Requirements</span></span>



| <span data-ttu-id="15fb5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="15fb5-114">Requirement</span></span> | <span data-ttu-id="15fb5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="15fb5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15fb5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15fb5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15fb5-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15fb5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="15fb5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15fb5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15fb5-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15fb5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15fb5-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="15fb5-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="15fb5-121"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15fb5-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15fb5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="15fb5-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15fb5-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15fb5-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15fb5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15fb5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15fb5-125">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="15fb5-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="15fb5-126">**репетитионпаттерн**</span><span class="sxs-lookup"><span data-stu-id="15fb5-126">**RepetitionPattern**</span></span>](repetitionpattern.md)
</dt> </dl>

 

 





