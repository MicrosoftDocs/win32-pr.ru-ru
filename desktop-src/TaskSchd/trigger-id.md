---
title: Trigger.Id, свойство
description: Для создания скриптов Возвращает или задает идентификатор триггера.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Свойство ID планировщик задач
- Свойство ID планировщик задач, объект Trigger
- Планировщик задач объекта триггера, свойство ID
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533944"
---
# <a name="triggerid-property"></a><span data-ttu-id="6509b-106">Trigger.Id, свойство</span><span class="sxs-lookup"><span data-stu-id="6509b-106">Trigger.Id property</span></span>

<span data-ttu-id="6509b-107">Для создания скриптов Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="6509b-107">For scripting, gets or sets the identifier for the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="6509b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6509b-108">Syntax</span></span>


```VB
Trigger.Id As String
```



## <a name="property-value"></a><span data-ttu-id="6509b-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6509b-109">Property value</span></span>

<span data-ttu-id="6509b-110">Идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="6509b-110">The identifier for the trigger.</span></span> <span data-ttu-id="6509b-111">Этот идентификатор используется планировщик задач в целях ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="6509b-111">This identifier is used by the Task Scheduler for logging purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="6509b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6509b-112">Remarks</span></span>

<span data-ttu-id="6509b-113">При чтении или записи XML-кода для задачи Идентификатор триггера задается в атрибуте ID отдельных элементов Trigger (например, атрибут ID элемента [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md) ) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="6509b-113">When reading or writing XML for a task, the trigger identifier is specified in the Id attribute of the individual trigger elements (for example, the Id attribute of the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element) of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6509b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6509b-114">Requirements</span></span>



| <span data-ttu-id="6509b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6509b-115">Requirement</span></span> | <span data-ttu-id="6509b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6509b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6509b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6509b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6509b-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6509b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6509b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6509b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6509b-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6509b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6509b-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6509b-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="6509b-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6509b-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6509b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6509b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6509b-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6509b-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6509b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6509b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6509b-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="6509b-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





