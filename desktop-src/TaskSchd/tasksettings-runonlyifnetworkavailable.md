---
title: Тасксеттингс. Рунонлифнетворкаваилабле, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач будет выполнять задачу только при доступности сети.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- планировщик задач свойства Рунонлифнетворкаваилабле
- Планировщик задач свойства Рунонлифнетворкаваилабле, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Рунонлифнетворкаваилабле
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892413"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a><span data-ttu-id="bc104-106">Тасксеттингс. Рунонлифнетворкаваилабле, свойство</span><span class="sxs-lookup"><span data-stu-id="bc104-106">TaskSettings.RunOnlyIfNetworkAvailable property</span></span>

<span data-ttu-id="bc104-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач будет выполнять задачу только при доступности сети.</span><span class="sxs-lookup"><span data-stu-id="bc104-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available.</span></span>

<span data-ttu-id="bc104-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bc104-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc104-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc104-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="bc104-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bc104-110">Property value</span></span>

<span data-ttu-id="bc104-111">Если значение — true, свойство указывает, что планировщик задач будет выполнять задачу только при доступности сети.</span><span class="sxs-lookup"><span data-stu-id="bc104-111">If True, the property indicates that the Task Scheduler will run the task only when a network is available.</span></span> <span data-ttu-id="bc104-112">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="bc104-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc104-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc104-113">Remarks</span></span>

<span data-ttu-id="bc104-114">При чтении или записи XML для задачи этот параметр указывается в элементе [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="bc104-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc104-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bc104-115">Requirements</span></span>



| <span data-ttu-id="bc104-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bc104-116">Requirement</span></span> | <span data-ttu-id="bc104-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bc104-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc104-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc104-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bc104-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc104-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bc104-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc104-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bc104-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc104-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc104-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bc104-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc104-123"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bc104-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bc104-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bc104-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc104-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc104-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc104-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc104-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc104-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="bc104-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





