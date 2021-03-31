---
title: Элемент Subscription (Евенттригжертипе)
description: Указывает запрос XPath, определяющий событие, вызвавшее срабатывание триггера.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Элемент Subscription планировщик задач
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803976"
---
# <a name="subscription-eventtriggertype-element"></a><span data-ttu-id="4a89f-104">Элемент Subscription (Евенттригжертипе)</span><span class="sxs-lookup"><span data-stu-id="4a89f-104">Subscription (eventTriggerType) Element</span></span>

<span data-ttu-id="4a89f-105">Указывает запрос XPath, определяющий событие, вызвавшее срабатывание триггера.</span><span class="sxs-lookup"><span data-stu-id="4a89f-105">Specifies the XPath query that identifies the event that fires the trigger.</span></span>

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

<span data-ttu-id="4a89f-106">Элемент **Subscription** определяется сложным типом [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4a89f-106">The **Subscription** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4a89f-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="4a89f-107">Parent element</span></span>



| <span data-ttu-id="4a89f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="4a89f-108">Element</span></span>                                                                       | <span data-ttu-id="4a89f-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="4a89f-109">Derived from</span></span>                                                                 | <span data-ttu-id="4a89f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4a89f-110">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="4a89f-111">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="4a89f-111">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="4a89f-112">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="4a89f-112">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="4a89f-113">Указывает триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="4a89f-113">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4a89f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a89f-114">Remarks</span></span>

<span data-ttu-id="4a89f-115">Для разработки скриптов подписка на события задается свойством [**EventTrigger. Subscription**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="4a89f-115">For script development, the event subscription is specified by the [**EventTrigger.Subscription**](eventtrigger-subscription.md) property.</span></span>

<span data-ttu-id="4a89f-116">Для разработки на C++ подписка на события задается свойством [**иевенттригжер:: Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .</span><span class="sxs-lookup"><span data-stu-id="4a89f-116">For C++ development, the event subscription is specified by the [**IEventTrigger::Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a89f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4a89f-117">Requirements</span></span>



| <span data-ttu-id="4a89f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4a89f-118">Requirement</span></span> | <span data-ttu-id="4a89f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4a89f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4a89f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a89f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a89f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a89f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4a89f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a89f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a89f-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a89f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a89f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a89f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a89f-125">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="4a89f-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4a89f-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="4a89f-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





