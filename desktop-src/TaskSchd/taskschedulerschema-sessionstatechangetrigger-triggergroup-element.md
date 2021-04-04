---
title: Сессионстатечанжетригжер (Тригжерграуп), элемент
description: Указывает триггер, который запускает задачу при изменении состояния сеанса сервера терминалов.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- планировщик задач элемента Сессионстатечанжетригжер
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803215"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a><span data-ttu-id="cc72f-104">Сессионстатечанжетригжер (Тригжерграуп), элемент</span><span class="sxs-lookup"><span data-stu-id="cc72f-104">SessionStateChangeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="cc72f-105">Указывает триггер, который запускает задачу при изменении состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="cc72f-105">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span>

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

<span data-ttu-id="cc72f-106">Элемент **сессионстатечанжетригжер** определяется параметром [**тригжерграуп**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="cc72f-106">The **SessionStateChangeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="cc72f-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="cc72f-107">Parent element</span></span>



| <span data-ttu-id="cc72f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="cc72f-108">Element</span></span>                                                           | <span data-ttu-id="cc72f-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="cc72f-109">Derived from</span></span>                                                         | <span data-ttu-id="cc72f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cc72f-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="cc72f-111">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="cc72f-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="cc72f-112">**тригжерстипе**</span><span class="sxs-lookup"><span data-stu-id="cc72f-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="cc72f-113">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="cc72f-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="cc72f-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cc72f-114">Child elements</span></span>



| <span data-ttu-id="cc72f-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="cc72f-115">Element</span></span>                                                                                      | <span data-ttu-id="cc72f-116">Тип</span><span class="sxs-lookup"><span data-stu-id="cc72f-116">Type</span></span>                                                                                    | <span data-ttu-id="cc72f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="cc72f-117">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc72f-118">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="cc72f-118">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="cc72f-119">длительность</span><span class="sxs-lookup"><span data-stu-id="cc72f-119">duration</span></span>                                                                                | <span data-ttu-id="cc72f-120">Задает значение, указывающее длину задержки перед запуском задачи при обнаружении изменения состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="cc72f-120">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="cc72f-121">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="cc72f-121">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="cc72f-122">**сессионстатечанжетипе**</span><span class="sxs-lookup"><span data-stu-id="cc72f-122">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="cc72f-123">Указывает тип изменения сеанса сервера терминалов, запускающего запуск задачи.</span><span class="sxs-lookup"><span data-stu-id="cc72f-123">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="cc72f-124">**UserId**</span><span class="sxs-lookup"><span data-stu-id="cc72f-124">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="cc72f-125">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="cc72f-125">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="cc72f-126">Указывает пользователя для сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="cc72f-126">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="cc72f-127">При обнаружении изменения состояния сеанса для этого пользователя запускается задача.</span><span class="sxs-lookup"><span data-stu-id="cc72f-127">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="cc72f-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc72f-128">Remarks</span></span>

<span data-ttu-id="cc72f-129">Для разработки сценариев триггер изменения состояния сеанса указывается с помощью объекта [**сессионстатечанжетригжер**](sessionstatechangetrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="cc72f-129">For scripting development, a session state change trigger is specified using the [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) object.</span></span>

<span data-ttu-id="cc72f-130">Для разработки на C++ триггер изменения состояния сеанса указывается с помощью интерфейса [**исессионстатечанжетригжер**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .</span><span class="sxs-lookup"><span data-stu-id="cc72f-130">For C++ development, a session state change trigger is specified using the [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc72f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="cc72f-131">Requirements</span></span>



| <span data-ttu-id="cc72f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="cc72f-132">Requirement</span></span> | <span data-ttu-id="cc72f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="cc72f-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc72f-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc72f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cc72f-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc72f-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc72f-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc72f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cc72f-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc72f-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





