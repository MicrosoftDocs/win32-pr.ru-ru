---
title: Свойство Triggered. Enabled
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, включен ли триггер.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Включенное свойство планировщик задач
- Включенное свойство планировщик задач, объект Trigger
- Триггер объекта планировщик задач, включенное свойство
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988415"
---
# <a name="triggerenabled-property"></a><span data-ttu-id="30da5-106">Свойство Triggered. Enabled</span><span class="sxs-lookup"><span data-stu-id="30da5-106">Trigger.Enabled property</span></span>

<span data-ttu-id="30da5-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="30da5-107">For scripting, gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="30da5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30da5-108">Syntax</span></span>


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="30da5-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="30da5-109">Property value</span></span>

<span data-ttu-id="30da5-110">Значение true, если триггер включен; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="30da5-110">True if the trigger is enabled; otherwise, false.</span></span> <span data-ttu-id="30da5-111">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="30da5-111">The default is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="30da5-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30da5-112">Remarks</span></span>

<span data-ttu-id="30da5-113">При чтении или записи XML для задачи свойство Enabled задается с помощью элемента [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="30da5-113">When reading or writing XML for a task, the enabled property is specified using the [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="30da5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="30da5-114">Requirements</span></span>



| <span data-ttu-id="30da5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="30da5-115">Requirement</span></span> | <span data-ttu-id="30da5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="30da5-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30da5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30da5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30da5-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30da5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="30da5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30da5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30da5-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="30da5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30da5-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="30da5-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="30da5-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30da5-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30da5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="30da5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30da5-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30da5-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30da5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30da5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30da5-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="30da5-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





