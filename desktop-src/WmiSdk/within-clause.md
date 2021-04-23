---
description: Используйте предложение WITHIN в запросах событий, чтобы указать интервал опроса или интервал группировки.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: ВНУТРИ предложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d863e2e71d52fe60aeed7697feeb1231164c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155998"
---
# <a name="within-clause"></a><span data-ttu-id="b936f-103">ВНУТРИ предложения</span><span class="sxs-lookup"><span data-stu-id="b936f-103">WITHIN Clause</span></span>

<span data-ttu-id="b936f-104">Потребители событий используют предложение in в запросах событий для указания *интервала опроса* или *интервала группировки*.</span><span class="sxs-lookup"><span data-stu-id="b936f-104">Event consumers use the WITHIN clause in event queries to specify a *polling interval* or a *grouping interval*.</span></span>

<span data-ttu-id="b936f-105">Интервал опроса — это интервал, который инструментарий управления Windows (WMI) (WMI) использует для опроса поставщика данных, ответственного за класс для [внутренних событий](determining-the-type-of-event-to-receive.md), для которых запрашиваемое событие является элементом.</span><span class="sxs-lookup"><span data-stu-id="b936f-105">A polling interval is the interval that Windows Management Instrumentation (WMI) uses to poll the data provider responsible for the class for [intrinsic events](determining-the-type-of-event-to-receive.md), of which the event queried is a member.</span></span> <span data-ttu-id="b936f-106">Этот интервал представляет собой максимальный интервал времени, которое может пройти до доставки уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="b936f-106">This interval is the maximum amount of time that can pass before notification of an event must be delivered.</span></span> <span data-ttu-id="b936f-107">Потребитель использует интервал опроса в предложении WITHIN, когда потребитель требует уведомления об изменениях в классе, а поставщик событий недоступен.</span><span class="sxs-lookup"><span data-stu-id="b936f-107">A consumer uses a polling interval in a WITHIN clause when the consumer requires notification of changes to a class, and an event provider is unavailable.</span></span> <span data-ttu-id="b936f-108">Потребитель регистрируется для внутреннего события и включает интервал опроса.</span><span class="sxs-lookup"><span data-stu-id="b936f-108">The consumer registers for an intrinsic event and includes the polling interval.</span></span>

<span data-ttu-id="b936f-109">Чтобы задать интервал опроса, поместите предложение WITHIN непосредственно перед предложением WHERE, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="b936f-109">To specify a polling interval, place the WITHIN clause immediately before the WHERE clause, as shown following:</span></span>


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



<span data-ttu-id="b936f-110">Интринсицевенткласс — это встроенный класс событий, членом которого является событие, Interval — интервал опроса, а value — это значение для свойства, для которого потребителю требуется уведомление.</span><span class="sxs-lookup"><span data-stu-id="b936f-110">IntrinsicEventClass is the intrinsic event class of which the event is a member, interval is the polling interval, and value is the value for the property on which the consumer requires notification.</span></span>

<span data-ttu-id="b936f-111">Интервал опроса — это число с плавающей запятой, которое может быть дробным, чтобы принимать значения меньше 1 секунды.</span><span class="sxs-lookup"><span data-stu-id="b936f-111">The polling interval is a floating-point number, and can be fractional to accept values smaller than 1 second.</span></span> <span data-ttu-id="b936f-112">Однако интервал должен представлять собой количество секунд, а не очень маленькое значение, такое как 0,001, поскольку указание слишком маленького значения может привести к тому, что инструментарий WMI отклонит недопустимый оператор из-за интенсивного опроса ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b936f-112">However, the interval should represent a number of seconds rather than an extremely small value such as 0.001, because specifying a value that is too small can cause WMI to reject the statement as not valid—due to the resource-intensive nature of polling.</span></span> <span data-ttu-id="b936f-113">Поскольку большинство потребителей событий не требует немедленного уведомления, рекомендуется использовать интервал, превышающий 5 минут.</span><span class="sxs-lookup"><span data-stu-id="b936f-113">Because most event consumers do not require immediate notification, it is recommended that they use an interval that is greater than 5 minutes.</span></span>

<span data-ttu-id="b936f-114">В следующем примере запроса выполняется проверка WMI каждые 10 секунд для изменений, происходящих в экземплярах класса [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="b936f-114">The following query example requests that WMI check every 10 seconds for changes that occur to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="b936f-115">Если экземпляр класса изменяется в пределах указанного интервала опроса, для каждого изменения отправляется событие уведомления.</span><span class="sxs-lookup"><span data-stu-id="b936f-115">If an instance of the class is modified within the specified polling interval, a notification event is sent for each modification.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="b936f-116">В зависимости от запроса поставщик событий и WMI могут совместно использовать задачу предоставления событий.</span><span class="sxs-lookup"><span data-stu-id="b936f-116">Depending on the query, an event provider and WMI can share the task of providing events.</span></span> <span data-ttu-id="b936f-117">Например, поставщик событий, который поддерживает события системных классов [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md) и [**\_ \_ инстанцемодификатионевент**](--instancemodificationevent.md) , а не события класса System [**\_ \_ инстанцеделетионевент**](--instancedeletionevent.md) .</span><span class="sxs-lookup"><span data-stu-id="b936f-117">For example, an event provider that supports events of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) and [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system classes, and not events of the [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) system class.</span></span> <span data-ttu-id="b936f-118">Следующий запрос позволяет поставщику событий создавать события создания и изменения по мере их возникновения и доставлять их при создании.</span><span class="sxs-lookup"><span data-stu-id="b936f-118">The following query enables the event provider to generate the creation and modification events as they occur and have them delivered when they are created.</span></span> <span data-ttu-id="b936f-119">Запрос также позволяет инструментарию WMI создавать события **\_ \_ инстанцеделетионевент** каждые 10 (десять) секунд с помощью механизма опроса.</span><span class="sxs-lookup"><span data-stu-id="b936f-119">The query also allows WMI to generate **\_\_InstanceDeletionEvent** events every 10 (ten) seconds using the polling mechanism.</span></span>


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



<span data-ttu-id="b936f-120">Можно также использовать предложение in для указания интервала группировки.</span><span class="sxs-lookup"><span data-stu-id="b936f-120">You can also use the WITHIN clause to specify a grouping interval.</span></span> <span data-ttu-id="b936f-121">Интервал группирования — это 32-разрядное целое число без знака, указывающее период времени после получения начального события, в течение которого WMI должен собираются аналогичные события.</span><span class="sxs-lookup"><span data-stu-id="b936f-121">A grouping interval is an unsigned 32-bit integer that specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span> <span data-ttu-id="b936f-122">По истечении этого периода WMI предоставляет статистическое событие, состоящие из всех аналогичных событий.</span><span class="sxs-lookup"><span data-stu-id="b936f-122">When this time period expires, WMI delivers the aggregate event, made up of all the similar events.</span></span> <span data-ttu-id="b936f-123">Дополнительные сведения см. в разделе [предложение Group](group-clause.md).</span><span class="sxs-lookup"><span data-stu-id="b936f-123">For more information, see [GROUP Clause](group-clause.md).</span></span>

<span data-ttu-id="b936f-124">Потребители событий, регистрируемые для часто встречающихся событий, используют интервал группировки с предложением WITHIN.</span><span class="sxs-lookup"><span data-stu-id="b936f-124">Event consumers that register for frequently occurring events use a grouping interval with the WITHIN clause.</span></span> <span data-ttu-id="b936f-125">Добавление группы в предложение WHERE в запросе события приводит к отправке WMI одного агрегатного события вместо многих событий.</span><span class="sxs-lookup"><span data-stu-id="b936f-125">Adding GROUP WITHIN to the WHERE clause in an event query results in WMI sending one aggregate event rather than many events.</span></span> <span data-ttu-id="b936f-126">Статистическое событие представлено системным классом [**\_ \_ аггрегативент**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="b936f-126">The aggregate event is represented by the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span>

<span data-ttu-id="b936f-127">Чтобы задать интервал группировки, поместите предложение WITHIN сразу после предложения GROUP.</span><span class="sxs-lookup"><span data-stu-id="b936f-127">To specify a grouping interval, place the WITHIN clause immediately after the GROUP clause.</span></span>


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



<span data-ttu-id="b936f-128">EventClass — это класс событий, членом которого является событие, value — это значение свойства, для которого потребитель требует уведомления, а Interval — интервал группирования.</span><span class="sxs-lookup"><span data-stu-id="b936f-128">EventClass is the event class of which the event is a member, value is the value for the property on which the consumer requires notification, and Interval is the grouping interval.</span></span>

<span data-ttu-id="b936f-129">Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="b936f-129">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="b936f-130">Постоянные потребители событий можно создавать с помощью опросных запросов только в том случае, если у вас есть права администратора.</span><span class="sxs-lookup"><span data-stu-id="b936f-130">Permanent event consumers can be created with polling queries only if you have administrator privileges.</span></span>

 

 
