---
title: Идлесеттингс. Стопонидлинд, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач будет завершать задачу, если условие простоя заканчивается до завершения задачи.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- планировщик задач свойства Стопонидлинд
- Планировщик задач свойства Стопонидлинд, объект Идлесеттингс
- Планировщик задач объекта Идлесеттингс, свойство Стопонидлинд
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891617"
---
# <a name="idlesettingsstoponidleend-property"></a><span data-ttu-id="5bb21-106">Идлесеттингс. Стопонидлинд, свойство</span><span class="sxs-lookup"><span data-stu-id="5bb21-106">IdleSettings.StopOnIdleEnd property</span></span>

<span data-ttu-id="5bb21-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач будет завершать задачу, если условие простоя заканчивается до завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="5bb21-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb21-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5bb21-108">Syntax</span></span>


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="5bb21-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5bb21-109">Property value</span></span>

<span data-ttu-id="5bb21-110">Логическое значение, указывающее, что планировщик задач будет завершать задачу, если условие простоя заканчивается до завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="5bb21-110">A Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bb21-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5bb21-111">Remarks</span></span>

<span data-ttu-id="5bb21-112">При чтении или записи XML для задачи этот параметр указывается в элементе [**стопонидлинд**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="5bb21-112">When reading or writing XML for a task, this setting is specified in the [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb21-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5bb21-113">Requirements</span></span>



| <span data-ttu-id="5bb21-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5bb21-114">Requirement</span></span> | <span data-ttu-id="5bb21-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5bb21-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb21-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5bb21-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5bb21-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bb21-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5bb21-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5bb21-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5bb21-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bb21-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5bb21-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5bb21-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="5bb21-121"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5bb21-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5bb21-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5bb21-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bb21-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bb21-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bb21-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5bb21-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb21-125">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="5bb21-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="5bb21-126">**идлесеттингс**</span><span class="sxs-lookup"><span data-stu-id="5bb21-126">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





