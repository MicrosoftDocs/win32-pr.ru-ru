---
description: Предложение GROUP заставляет Инструментарий WMI создать одно уведомление для представления группы событий.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: Group, предложение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032a8e86c84c0b317b3739c0e203a249b432b0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703122"
---
# <a name="group-clause"></a><span data-ttu-id="b6ae2-103">Group, предложение</span><span class="sxs-lookup"><span data-stu-id="b6ae2-103">GROUP Clause</span></span>

<span data-ttu-id="b6ae2-104">Предложение GROUP заставляет Инструментарий WMI создать одно уведомление для представления группы событий.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-104">The GROUP clause causes WMI to generate a single notification to represent a group of events.</span></span> <span data-ttu-id="b6ae2-105">Репрезентативное уведомление является экземпляром системного класса [**\_ \_ аггрегативент**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="b6ae2-105">The representative notification is an instance of the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span> <span data-ttu-id="b6ae2-106">Класс System **\_ \_ аггрегативент** содержит два свойства: « **представители** » и « **NumberOfEvents**».</span><span class="sxs-lookup"><span data-stu-id="b6ae2-106">The **\_\_AggregateEvent** system class contains two properties: **Representative** and **NumberOfEvents**.</span></span> <span data-ttu-id="b6ae2-107">Свойство « **репрезентативный** » — это внедренный объект, который содержит один из экземпляров, полученных в рамках интервала группировки, указанного в [предложении](within-clause.md)in.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-107">The **Representative** property is an embedded object that contains one of the instances received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="b6ae2-108">Например, если создается статистическое событие для уведомления о событиях изменения экземпляра, то **репрезентативный** класс содержит один экземпляр класса [**\_ \_ инстанцемодификатионевент**](--instancemodificationevent.md) .</span><span class="sxs-lookup"><span data-stu-id="b6ae2-108">For example, if an aggregate event is generated to notify of instance modification events, **Representative** contains one instance of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) class.</span></span> <span data-ttu-id="b6ae2-109">Свойство **NumberOfEvents** содержит количество событий, полученных в течение интервала группировки.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-109">The **NumberOfEvents** property contains the number of events received during the grouping interval.</span></span> <span data-ttu-id="b6ae2-110">Интервал группировки задает период времени после получения начального события, в течение которого Инструментарий WMI должен собираются аналогичные события.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-110">The grouping interval specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span>

<span data-ttu-id="b6ae2-111">Предложение GROUP должно содержать предложение WITHIN для указания интервала группирования и может содержать ключевое слово BY или HAVING или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-111">The GROUP clause must contain a WITHIN clause to specify the grouping interval and can contain the BY or HAVING keyword, or both.</span></span> <span data-ttu-id="b6ae2-112">Предложение GROUP помещается после предложения WHERE, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="b6ae2-112">The GROUP clause is placed after the WHERE clause, as shown following:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

<span data-ttu-id="b6ae2-113">Значение *EventClass* — это класс событий, членом которого является событие, а *value* — это значение свойства, для которого требуется уведомление.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-113">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="b6ae2-114">Интервал представляет собой целое число без знака, представляющее интервал группирования после получения первого события.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-114">The interval is an unsigned integer that represents the grouping interval after receiving the first event.</span></span> <span data-ttu-id="b6ae2-115">Целое число без знака представляет собой число секунд.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-115">The unsigned integer is a number of seconds.</span></span> <span data-ttu-id="b6ae2-116">Список свойств представляет собой список с разделителями-запятыми одного или нескольких свойств, включенных в класс событий. *оператор* является любым реляционным оператором; *целое* число — это 32-разрядное целое число без знака, указывающее количество событий.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-116">The property list is a comma-delimited list of one or more properties that are included in the event class; *operator* is any relational operator; and *integer* is an unsigned 32-bit integer indicating a number of events.</span></span>

<span data-ttu-id="b6ae2-117">При использовании предложения GROUP предложения WHERE, BY и HAVING являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-117">When using the GROUP clause, the WHERE, BY, and HAVING clauses are optional.</span></span>

<span data-ttu-id="b6ae2-118">Базовое использование предложения GROUP может запрашивать Группирование событий в интервале времени, который начинается при получении первого события.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-118">A basic use of the GROUP clause might request a grouping of events within a time interval that starts when the first event is received.</span></span> <span data-ttu-id="b6ae2-119">Например, следующий запрос группирует все события электронной почты, отправленные в течение 5 минут.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-119">For example, the following query groups all of the email events sent within 5 minutes.</span></span> <span data-ttu-id="b6ae2-120">Вместо разбиения пользователя на страницы каждый раз, когда получен новый адрес электронной почты, постоянный потребитель может использовать этот запрос для информирования пользователя, только если в течение последних 5 минут было получено новое сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-120">Instead of paging a user every time a piece of new email is received, the permanent consumer might use this query to inform the user only if new email has been received within the last 5 minutes.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



<span data-ttu-id="b6ae2-121">Если требуются более подробные сведения, события могут быть сгруппированы по одному или нескольким свойствам класса событий.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-121">If more detailed information is required, events can be grouped by one or more properties of the event class.</span></span> <span data-ttu-id="b6ae2-122">Следующий запрос требует, чтобы события электронной почты были объединены с другими событиями, которые имеют одно и то же значение в свойстве **sender** :</span><span class="sxs-lookup"><span data-stu-id="b6ae2-122">The following query requests that email events be combined with other events that have the same value in the **Sender** property:</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



<span data-ttu-id="b6ae2-123">Еще более подробный уровень детализации можно достичь, добавив предложение WHERE.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-123">A still greater level of detail can be achieved by adding a WHERE clause.</span></span> <span data-ttu-id="b6ae2-124">Например, следующий запрос уведомляет пользователя о новом сообщении электронной почты от конкретного отправителя, полученного за последние 10 минут, в сочетании с другими событиями, которые имеют то же значение в свойстве **важности** :</span><span class="sxs-lookup"><span data-stu-id="b6ae2-124">For example, the following query notifies a user of new email from a particular sender that has arrived within the last 10 minutes, combined with other events that have the same value in the **Importance** property:</span></span>


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



