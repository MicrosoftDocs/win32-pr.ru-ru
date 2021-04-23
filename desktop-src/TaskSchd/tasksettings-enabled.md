---
title: Тасксеттингс. Enabled, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача включена. Задачу можно выполнить, только если этот параметр имеет значение true.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Включенное свойство планировщик задач
- Включенное свойство планировщик задач, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Enabled
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415781"
---
# <a name="tasksettingsenabled-property"></a><span data-ttu-id="a316d-107">Тасксеттингс. Enabled, свойство</span><span class="sxs-lookup"><span data-stu-id="a316d-107">TaskSettings.Enabled property</span></span>

<span data-ttu-id="a316d-108">Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача включена.</span><span class="sxs-lookup"><span data-stu-id="a316d-108">For scripting, gets or sets a Boolean value that indicates that the task is enabled.</span></span> <span data-ttu-id="a316d-109">Задачу можно выполнить, только если этот параметр имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="a316d-109">The task can be performed only when this setting is True.</span></span>

<span data-ttu-id="a316d-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a316d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a316d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a316d-111">Syntax</span></span>


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a316d-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a316d-112">Property value</span></span>

<span data-ttu-id="a316d-113">Если задано значение true, задача включена.</span><span class="sxs-lookup"><span data-stu-id="a316d-113">If True, the task is enabled.</span></span> <span data-ttu-id="a316d-114">Если задано значение false, задача не включена.</span><span class="sxs-lookup"><span data-stu-id="a316d-114">If False, the task is not enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="a316d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a316d-115">Remarks</span></span>

<span data-ttu-id="a316d-116">При чтении или записи XML для задачи этот параметр указывается в элементе [**Enabled (сеттингстипе)**](taskschedulerschema-enabled-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="a316d-116">When reading or writing XML for a task, this setting is specified in the [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a316d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a316d-117">Requirements</span></span>



| <span data-ttu-id="a316d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a316d-118">Requirement</span></span> | <span data-ttu-id="a316d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a316d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a316d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a316d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a316d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a316d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a316d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a316d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a316d-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a316d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a316d-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a316d-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="a316d-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a316d-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a316d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a316d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a316d-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a316d-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a316d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a316d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a316d-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a316d-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





