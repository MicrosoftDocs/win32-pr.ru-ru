---
title: Свойство EventTrigger. Валуекуериес
description: Для создания скриптов Возвращает или задает коллекцию именованных запросов XPath. Каждый запрос в коллекции применяется к последнему соответствующему XML-событию, возвращенному из запроса подписки, указанного в свойстве Subscription.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- планировщик задач свойства Валуекуериес
- Планировщик задач свойства Валуекуериес, объект EventTrigger
- Объект EventTrigger планировщик задач, свойство Валуекуериес
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534895"
---
# <a name="eventtriggervaluequeries-property"></a><span data-ttu-id="021dd-107">Свойство EventTrigger. Валуекуериес</span><span class="sxs-lookup"><span data-stu-id="021dd-107">EventTrigger.ValueQueries property</span></span>

<span data-ttu-id="021dd-108">Для создания скриптов Возвращает или задает коллекцию именованных запросов XPath.</span><span class="sxs-lookup"><span data-stu-id="021dd-108">For scripting, gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="021dd-109">Каждый запрос в коллекции применяется к последнему соответствующему XML-событию, возвращенному из запроса подписки, указанного в свойстве [**Subscription**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="021dd-109">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="021dd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="021dd-110">Syntax</span></span>


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a><span data-ttu-id="021dd-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="021dd-111">Property value</span></span>

<span data-ttu-id="021dd-112">Коллекция пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="021dd-112">A collection of of name-value pairs.</span></span> <span data-ttu-id="021dd-113">Каждая пара «имя-значение» в коллекции определяет уникальное имя для значения свойства события, запускающего триггер события.</span><span class="sxs-lookup"><span data-stu-id="021dd-113">Each name-value pair in the collection defines a unique name for a property value of the event that triggers the event trigger.</span></span> <span data-ttu-id="021dd-114">Значение свойства события определяется как запрос события XPath.</span><span class="sxs-lookup"><span data-stu-id="021dd-114">The property value of the event is defined as an XPath event query.</span></span> <span data-ttu-id="021dd-115">Дополнительные сведения о запросах событий XPath см. в разделе [Выбор события](/previous-versions//aa385231(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="021dd-115">For more information about XPath event queries, see [Event Selection](/previous-versions//aa385231(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="021dd-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="021dd-116">Remarks</span></span>

<span data-ttu-id="021dd-117">Имя запроса можно использовать в качестве переменной в следующих свойствах действия:</span><span class="sxs-lookup"><span data-stu-id="021dd-117">The name of the query can be used as a variable in the following action properties:</span></span>

-   [<span data-ttu-id="021dd-118">**Шовмессажеактион. MessageBody**</span><span class="sxs-lookup"><span data-stu-id="021dd-118">**ShowMessageAction.MessageBody**</span></span>](showmessageaction-messagebody.md)
-   [<span data-ttu-id="021dd-119">**Шовмессажеактион. Title**</span><span class="sxs-lookup"><span data-stu-id="021dd-119">**ShowMessageAction.Title**</span></span>](showmessageaction-title.md)
-   [<span data-ttu-id="021dd-120">**Ексекактион. Arguments**</span><span class="sxs-lookup"><span data-stu-id="021dd-120">**ExecAction.Arguments**</span></span>](execaction-arguments.md)
-   [<span data-ttu-id="021dd-121">**Ексекактион. WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="021dd-121">**ExecAction.WorkingDirectory**</span></span>](execaction-workingdirectory.md)
-   [<span data-ttu-id="021dd-122">**Емаилактион. Server**</span><span class="sxs-lookup"><span data-stu-id="021dd-122">**EmailAction.Server**</span></span>](emailaction-server.md)
-   [<span data-ttu-id="021dd-123">**Емаилактион. subject**</span><span class="sxs-lookup"><span data-stu-id="021dd-123">**EmailAction.Subject**</span></span>](emailaction-subject.md)
-   [<span data-ttu-id="021dd-124">**EmailAction.To**</span><span class="sxs-lookup"><span data-stu-id="021dd-124">**EmailAction.To**</span></span>](emailaction-to.md)
-   [<span data-ttu-id="021dd-125">**EmailAction.Cc**</span><span class="sxs-lookup"><span data-stu-id="021dd-125">**EmailAction.Cc**</span></span>](emailaction-cc.md)
-   [<span data-ttu-id="021dd-126">**Емаилактион. СК**</span><span class="sxs-lookup"><span data-stu-id="021dd-126">**EmailAction.Bcc**</span></span>](emailaction-bcc.md)
-   [<span data-ttu-id="021dd-127">**Емаилактион. ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="021dd-127">**EmailAction.ReplyTo**</span></span>](emailaction-replyto.md)
-   [<span data-ttu-id="021dd-128">**Емаилактион. from**</span><span class="sxs-lookup"><span data-stu-id="021dd-128">**EmailAction.From**</span></span>](emailaction-from.md)
-   [<span data-ttu-id="021dd-129">**Емаилактион. Body**</span><span class="sxs-lookup"><span data-stu-id="021dd-129">**EmailAction.Body**</span></span>](emailaction-body.md)
-   [<span data-ttu-id="021dd-130">**Комхандлерактион. Data**</span><span class="sxs-lookup"><span data-stu-id="021dd-130">**ComHandlerAction.Data**</span></span>](comhandleraction-data.md)

<span data-ttu-id="021dd-131">В следующих примерах кода показаны две пары "имя-значение", которые можно использовать в коллекции "имя — значение".</span><span class="sxs-lookup"><span data-stu-id="021dd-131">The following code example strings show two name value pairs that can be used in a name-value collection.</span></span> <span data-ttu-id="021dd-132">Значения, возвращаемые запросами XPath, могут заменять переменные в свойстве действия.</span><span class="sxs-lookup"><span data-stu-id="021dd-132">The values returned by the XPath queries can replace variables in an action's property.</span></span> <span data-ttu-id="021dd-133">Ссылки на значения указываются по имени, с помощью `$(user)` и `$(machine)` в свойстве Action.</span><span class="sxs-lookup"><span data-stu-id="021dd-133">The values are referenced by name, with `$(user)` and `$(machine)`, in the action property.</span></span> <span data-ttu-id="021dd-134">Например, если `$(user)` `$(machine)` переменные и используются в строке [**шовмессажеактион. MessageBody**](showmessageaction-messagebody.md) , то значение запросов XPath заменит переменные в строке.</span><span class="sxs-lookup"><span data-stu-id="021dd-134">For example, if the `$(user)` and `$(machine)` variables are used in the [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md) string, then the value of the XPath queries will replace the variables in the string.</span></span>

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

<span data-ttu-id="021dd-135">Дополнительные сведения о записи строки запроса для определенных событий см. в разделе [Выбор событий](/previous-versions//aa385231(v=vs.85)) и [Подписка на события](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="021dd-135">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="021dd-136">Требования</span><span class="sxs-lookup"><span data-stu-id="021dd-136">Requirements</span></span>



| <span data-ttu-id="021dd-137">Требование</span><span class="sxs-lookup"><span data-stu-id="021dd-137">Requirement</span></span> | <span data-ttu-id="021dd-138">Значение</span><span class="sxs-lookup"><span data-stu-id="021dd-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="021dd-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="021dd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="021dd-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="021dd-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="021dd-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="021dd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="021dd-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="021dd-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="021dd-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="021dd-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="021dd-144"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="021dd-144"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="021dd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="021dd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="021dd-146"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="021dd-146"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="021dd-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="021dd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="021dd-148">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="021dd-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="021dd-149">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="021dd-149">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

