---
description: Предложение HAVING используется для фильтрации событий, полученных в течение интервала группировки, указанного в предложении WITHIN.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: HAVING, предложение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f93fbe082fb2f655dfad59d7642e1d0ff9a33e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703119"
---
# <a name="having-clause"></a><span data-ttu-id="507fa-103">HAVING, предложение</span><span class="sxs-lookup"><span data-stu-id="507fa-103">HAVING Clause</span></span>

<span data-ttu-id="507fa-104">Предложение HAVING используется для фильтрации событий, полученных в течение интервала группировки, указанного в [предложении Within](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="507fa-104">The HAVING clause is used to filter the events that are received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="507fa-105">Например, можно создать инструкцию SELECT таким образом, чтобы она возвращала Nothing, если в течение последнего 30-секундного ИНТЕРВАЛа не было по крайней мере 5 событий.</span><span class="sxs-lookup"><span data-stu-id="507fa-105">For example, a SELECT statement could be constructed so that it returns nothing unless there HAVE been at least 5 events within the past 30 second INTERVAL.</span></span>

<span data-ttu-id="507fa-106">Предложение WITHIN сразу же в [инструкции SELECT](select-statement-for-event-queries.md) после предложения [Group](group-clause.md) .</span><span class="sxs-lookup"><span data-stu-id="507fa-106">The WITHIN clause follows immediately in the [SELECT statement](select-statement-for-event-queries.md) after the [GROUP](group-clause.md) clause.</span></span> <span data-ttu-id="507fa-107">Предложение HAVING работает со свойством **NumberOfEvents** класса System [**\_ \_ аггрегативент**](--aggregateevent.md) , для которого группа, созданная предложением Group, является членом.</span><span class="sxs-lookup"><span data-stu-id="507fa-107">The HAVING clause operates on the **NumberOfEvents** property of the [**\_\_AggregateEvent**](--aggregateevent.md) system class, of which the group created by the GROUP clause is a member.</span></span> <span data-ttu-id="507fa-108">Предложение HAVING может использовать все стандартные операторы отношения.</span><span class="sxs-lookup"><span data-stu-id="507fa-108">The HAVING clause can use all of the standard relational operators.</span></span>

<span data-ttu-id="507fa-109">Синтаксис выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="507fa-109">The syntax is as follows:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

<span data-ttu-id="507fa-110">Значение *EventClass* — это класс событий, членом которого является событие, а *value* — это значение свойства, для которого требуется уведомление.</span><span class="sxs-lookup"><span data-stu-id="507fa-110">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="507fa-111">Интервал представляет собой целое число без знака, представляющее интервал группирования (в секундах) после получения первого события.</span><span class="sxs-lookup"><span data-stu-id="507fa-111">The interval is an unsigned integer that represents the grouping interval (in seconds) after receiving the first event.</span></span> <span data-ttu-id="507fa-112">Список свойств представляет собой список с разделителями-запятыми одного или нескольких свойств, включенных в класс событий.</span><span class="sxs-lookup"><span data-stu-id="507fa-112">The property list is a comma-delimited list of one or more properties that are included in the event class.</span></span> <span data-ttu-id="507fa-113">Оператор является любым реляционным оператором.</span><span class="sxs-lookup"><span data-stu-id="507fa-113">The operator is any relational operator.</span></span> <span data-ttu-id="507fa-114">Постоянное значение — это любое 32-разрядное целое число без знака, указывающее количество событий, используемых для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="507fa-114">The constant value is any unsigned 32-bit integer indicating the number of events used for filtering.</span></span>

<span data-ttu-id="507fa-115">При использовании предложения HAVING предложения WHERE и BY являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="507fa-115">When using the HAVING clause, the WHERE and BY clauses are optional.</span></span>

<span data-ttu-id="507fa-116">Следующий запрос события требует, чтобы уведомления класса **емаилевент** были сгруппированы в одно событие 300 секунд после первого события, полученного WMI.</span><span class="sxs-lookup"><span data-stu-id="507fa-116">The following event query requests that notifications of the **EmailEvent** class be grouped into one event 300 seconds after the first event that WMI receives.</span></span> <span data-ttu-id="507fa-117">Кроме того, запрос запрашивает экземпляр [**\_ \_ аггрегативент**](--aggregateevent.md) , только если Инструментарий WMI получит более пяти событий электронной почты за 300 секунд.</span><span class="sxs-lookup"><span data-stu-id="507fa-117">Also, the query requests the [**\_\_AggregateEvent**](--aggregateevent.md) instance should be delivered only if WMI receives more than five email events in that 300 seconds.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



<span data-ttu-id="507fa-118">В следующем примере все события, полученные в течение 600 секунд (то есть 10 минут), группируются **TargetInstance**. **SourceName** , свойство.</span><span class="sxs-lookup"><span data-stu-id="507fa-118">The following example groups all events received in 600 seconds (that is, 10 minutes) by the **TargetInstance**.**SourceName** property.</span></span> <span data-ttu-id="507fa-119">В этом примере агрегатные события доставляются только в том случае, если количество событий [**Win32 \_ нтложевент**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) , полученных из одного источника, превышает 25.</span><span class="sxs-lookup"><span data-stu-id="507fa-119">In this example, aggregate events are delivered only if the number of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) events received from the same source exceeds 25.</span></span> <span data-ttu-id="507fa-120">Помните, что оператор ISA вызывает свойство **TargetInstance** класса System [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md) для представления экземпляра класса **Win32 \_ нтложевент** .</span><span class="sxs-lookup"><span data-stu-id="507fa-120">Keep in mind that the ISA operator causes the **TargetInstance** property of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) system class to represent an instance of the **Win32\_NTLogEvent** class.</span></span>


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
