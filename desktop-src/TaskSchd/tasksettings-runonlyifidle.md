---
title: Тасксеттингс. Рунонлифидле, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач будет выполнять задачу только в том случае, если компьютер находится в состоянии простоя.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- планировщик задач свойства Рунонлифидле
- Планировщик задач свойства Рунонлифидле, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Рунонлифидле
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415217"
---
# <a name="tasksettingsrunonlyifidle-property"></a><span data-ttu-id="de600-106">Тасксеттингс. Рунонлифидле, свойство</span><span class="sxs-lookup"><span data-stu-id="de600-106">TaskSettings.RunOnlyIfIdle property</span></span>

<span data-ttu-id="de600-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач будет выполнять задачу только в том случае, если компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="de600-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span>

<span data-ttu-id="de600-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="de600-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="de600-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de600-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="de600-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="de600-110">Property value</span></span>

<span data-ttu-id="de600-111">Если значение — true, свойство указывает, что планировщик задач будет выполнять задачу только в том случае, если компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="de600-111">If True, the property indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span> <span data-ttu-id="de600-112">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="de600-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="de600-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de600-113">Remarks</span></span>

<span data-ttu-id="de600-114">При чтении или записи XML для задачи этот параметр указывается в элементе [**рунонлифидле**](taskschedulerschema-runonlyifidle-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="de600-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="de600-115">Требования</span><span class="sxs-lookup"><span data-stu-id="de600-115">Requirements</span></span>



| <span data-ttu-id="de600-116">Требование</span><span class="sxs-lookup"><span data-stu-id="de600-116">Requirement</span></span> | <span data-ttu-id="de600-117">Значение</span><span class="sxs-lookup"><span data-stu-id="de600-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de600-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de600-118">Minimum supported client</span></span><br/> | <span data-ttu-id="de600-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de600-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="de600-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de600-120">Minimum supported server</span></span><br/> | <span data-ttu-id="de600-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de600-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de600-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="de600-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="de600-123"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="de600-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="de600-124">DLL</span><span class="sxs-lookup"><span data-stu-id="de600-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de600-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de600-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de600-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de600-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de600-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="de600-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





