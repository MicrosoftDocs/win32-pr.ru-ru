---
title: Тасксеттингс. Идлесеттингс, свойство
description: Для создания скриптов Возвращает или задает сведения, указывающие, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- планировщик задач свойства Идлесеттингс
- Планировщик задач свойства Идлесеттингс, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Идлесеттингс
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672755"
---
# <a name="tasksettingsidlesettings-property"></a><span data-ttu-id="83be3-106">Тасксеттингс. Идлесеттингс, свойство</span><span class="sxs-lookup"><span data-stu-id="83be3-106">TaskSettings.IdleSettings property</span></span>

<span data-ttu-id="83be3-107">Для создания скриптов Возвращает или задает сведения, указывающие, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="83be3-107">For scripting, gets or sets the information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="83be3-108">Сведения об условиях простоя см. в разделе [условия простоя задачи](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="83be3-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="83be3-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="83be3-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="83be3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83be3-110">Syntax</span></span>


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a><span data-ttu-id="83be3-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="83be3-111">Property value</span></span>

<span data-ttu-id="83be3-112">Объект [**идлесеттингс**](idlesettings.md) , указывающий, как планировщик задач обрабатывает задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="83be3-112">An [**IdleSettings**](idlesettings.md) object that specifies how the Task Scheduler handles the task when the computer goes into an idle condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="83be3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83be3-113">Remarks</span></span>

<span data-ttu-id="83be3-114">При чтении или записи XML для задачи этот параметр указывается в элементе [**идлесеттингс**](taskschedulerschema-idlesettings-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="83be3-114">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="83be3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="83be3-115">Requirements</span></span>



| <span data-ttu-id="83be3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="83be3-116">Requirement</span></span> | <span data-ttu-id="83be3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="83be3-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83be3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83be3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="83be3-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83be3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="83be3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83be3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="83be3-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="83be3-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="83be3-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="83be3-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="83be3-123"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="83be3-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="83be3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="83be3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83be3-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83be3-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83be3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83be3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83be3-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="83be3-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





