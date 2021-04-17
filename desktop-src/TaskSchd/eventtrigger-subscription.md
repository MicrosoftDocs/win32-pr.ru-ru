---
title: EventTrigger. Subscription, свойство
description: Для создания скриптов Возвращает или задает строку запроса, определяющую событие, вызвавшее срабатывание триггера.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- планировщик задач Свойства подписки
- Свойство подписки планировщик задач, объект EventTrigger
- Объект EventTrigger планировщик задач, свойство подписки
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682034"
---
# <a name="eventtriggersubscription-property"></a><span data-ttu-id="c5c30-106">EventTrigger. Subscription, свойство</span><span class="sxs-lookup"><span data-stu-id="c5c30-106">EventTrigger.Subscription property</span></span>

<span data-ttu-id="c5c30-107">Для создания скриптов Возвращает или задает строку запроса, определяющую событие, вызвавшее срабатывание триггера.</span><span class="sxs-lookup"><span data-stu-id="c5c30-107">For scripting, gets or sets a query string that identifies the event that fires the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c30-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5c30-108">Syntax</span></span>


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a><span data-ttu-id="c5c30-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c5c30-109">Property value</span></span>

<span data-ttu-id="c5c30-110">Строка запроса, определяющая событие, вызвавшее срабатывание триггера.</span><span class="sxs-lookup"><span data-stu-id="c5c30-110">A query string that identifies the event that fires the trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5c30-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5c30-111">Remarks</span></span>

<span data-ttu-id="c5c30-112">При чтении или записи собственного XML-кода для задачи подписка на событие указывается с помощью элемента [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="c5c30-112">When reading or writing your own XML for a task, the event subscription is specified using the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="c5c30-113">Дополнительные сведения о записи строки запроса для определенных событий см. в разделе [Выбор событий](/previous-versions//aa385231(v=vs.85)) и [Подписка на события](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="c5c30-113">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c5c30-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="c5c30-114">Examples</span></span>

<span data-ttu-id="c5c30-115">Следующая строка запроса определяет подписку на все события уровня 2 в системном канале:</span><span class="sxs-lookup"><span data-stu-id="c5c30-115">The following query string defines a subscription to all level 2 events in the System channel:</span></span>


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



## <a name="requirements"></a><span data-ttu-id="c5c30-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c5c30-116">Requirements</span></span>



| <span data-ttu-id="c5c30-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c5c30-117">Requirement</span></span> | <span data-ttu-id="c5c30-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c5c30-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c30-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5c30-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c30-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5c30-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c5c30-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5c30-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c30-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5c30-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c5c30-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c5c30-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5c30-124"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c5c30-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c5c30-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c5c30-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5c30-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5c30-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5c30-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5c30-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c30-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="c5c30-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c5c30-129">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="c5c30-129">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

