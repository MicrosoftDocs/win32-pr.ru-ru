---
description: Создает события с интервалами, аналогично \_ сообщению таймера WM в программировании Windows.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: Класс __IntervalTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703017"
---
# <a name="__intervaltimerinstruction-class"></a><span data-ttu-id="587dd-103">\_\_Класс Интервалтимеринструктион</span><span class="sxs-lookup"><span data-stu-id="587dd-103">\_\_IntervalTimerInstruction class</span></span>

<span data-ttu-id="587dd-104">Класс System **\_ \_ интервалтимеринструктион** создает события с интервалами, аналогично \_ сообщению таймера WM в программировании Windows.</span><span class="sxs-lookup"><span data-stu-id="587dd-104">The **\_\_IntervalTimerInstruction** system class generates events at intervals, similar to a WM\_TIMER message in Windows programming.</span></span> <span data-ttu-id="587dd-105">Потребитель событий регистрируется для получения событий таймера, создавая запрос события, ссылающийся на этот класс.</span><span class="sxs-lookup"><span data-stu-id="587dd-105">An event consumer registers to receive interval timer events by creating an event query that references this class.</span></span> <span data-ttu-id="587dd-106">Из-за поведения операционной системы не гарантируется, что события будут доставляться точно по запрошенному интервалу.</span><span class="sxs-lookup"><span data-stu-id="587dd-106">Due to operating system behavior, there are no guarantees that events will be delivered at precisely the requested interval.</span></span>

<span data-ttu-id="587dd-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="587dd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="587dd-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="587dd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="587dd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="587dd-109">Syntax</span></span>

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="587dd-110">Члены</span><span class="sxs-lookup"><span data-stu-id="587dd-110">Members</span></span>

<span data-ttu-id="587dd-111">Класс **\_ \_ интервалтимеринструктион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="587dd-111">The **\_\_IntervalTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="587dd-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="587dd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="587dd-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="587dd-113">Properties</span></span>

<span data-ttu-id="587dd-114">Класс **\_ \_ интервалтимеринструктион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="587dd-114">The **\_\_IntervalTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="587dd-115">**интервалбетвиневентс**</span><span class="sxs-lookup"><span data-stu-id="587dd-115">**IntervalBetweenEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="587dd-116">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="587dd-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="587dd-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="587dd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="587dd-118">Квалификаторы: [**единицы**](standard-qualifiers.md) (миллисекунды)</span><span class="sxs-lookup"><span data-stu-id="587dd-118">Qualifiers: [**Units**](standard-qualifiers.md) (milliseconds)</span></span>
</dt> </dl>

<span data-ttu-id="587dd-119">Количество миллисекунд между срабатыванием события.</span><span class="sxs-lookup"><span data-stu-id="587dd-119">Number of milliseconds between event firings.</span></span>

</dd> <dt>

<span data-ttu-id="587dd-120">**скипифпассед**</span><span class="sxs-lookup"><span data-stu-id="587dd-120">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="587dd-121">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="587dd-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="587dd-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="587dd-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="587dd-123">Если **значение — true**, это событие должно быть пропущено, если интервал уже прошел.</span><span class="sxs-lookup"><span data-stu-id="587dd-123">If **TRUE**, this event is to be skipped if the interval is already passed.</span></span> <span data-ttu-id="587dd-124">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="587dd-124">The default is **FALSE**.</span></span> <span data-ttu-id="587dd-125">Это свойство наследуется от [**\_ \_ тимеринструктион**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="587dd-125">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="587dd-126">FALSE</span><span class="sxs-lookup"><span data-stu-id="587dd-126">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="587dd-127">Когда WMI или потребитель снова становится доступным, будет создано и получено событие уведомления.</span><span class="sxs-lookup"><span data-stu-id="587dd-127">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="587dd-128">true</span><span class="sxs-lookup"><span data-stu-id="587dd-128">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="587dd-129">Событие Timer не возникает, если Инструментарий WMI недоступен для его создания в соответствующий интервал времени или если потребитель, запрашивающий получение события, недоступен.</span><span class="sxs-lookup"><span data-stu-id="587dd-129">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="587dd-130">**тимерид**</span><span class="sxs-lookup"><span data-stu-id="587dd-130">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="587dd-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="587dd-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="587dd-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="587dd-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="587dd-133">Квалификаторы: [ **ключ**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="587dd-133">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="587dd-134">Уникальный идентификатор для этого объекта **\_ \_ интервалтимеринструктион** .</span><span class="sxs-lookup"><span data-stu-id="587dd-134">Unique identifier for this **\_\_IntervalTimerInstruction** object.</span></span> <span data-ttu-id="587dd-135">Это свойство наследуется от [**\_ \_ тимеринструктион**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="587dd-135">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="587dd-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="587dd-136">Remarks</span></span>

<span data-ttu-id="587dd-137">Класс **\_ \_ интервалтимеринструктион** является производным от [**\_ \_ тимеринструктион**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="587dd-137">The **\_\_IntervalTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="587dd-138">Запрос события, указанный для регистрации события интервала времени, обычно основан на свойстве **тимерид** .</span><span class="sxs-lookup"><span data-stu-id="587dd-138">The event query entered to register for an interval timer event is usually based on the **TimerId** property.</span></span> <span data-ttu-id="587dd-139">События уведомления, созданные из события интервала времени, содержат свойство **нумфирингс** , содержащее данные, отражающие количество событий, инициированных в течение времени, когда события не удалось получить.</span><span class="sxs-lookup"><span data-stu-id="587dd-139">Notification events generated from an interval timer event contain the property **NumFirings** which contains data reflecting how many events fired during the time the events were unable to be received.</span></span> <span data-ttu-id="587dd-140">Если для **скипифпассед** задано **значение true**, эти сведения отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="587dd-140">If **SkipIfPassed** is set to **TRUE**, that information is discarded.</span></span>

<span data-ttu-id="587dd-141">Значение свойства **интервалбетвиневентс** должно быть достаточно большим.</span><span class="sxs-lookup"><span data-stu-id="587dd-141">The value for the **IntervalBetweenEvents** property should be reasonably large.</span></span> <span data-ttu-id="587dd-142">Если он слишком мал, Инструментарий WMI может игнорировать его и не создавать событие из-за ограничений в некоторых операционных системах.</span><span class="sxs-lookup"><span data-stu-id="587dd-142">If it is too small, WMI may ignore it and not generate the event due to limitations in some operating systems.</span></span>

<span data-ttu-id="587dd-143">Инструментарий WMI создает событие Interval Timer, создавая экземпляр класса [**\_ \_ тимеревент**](--timerevent.md) .</span><span class="sxs-lookup"><span data-stu-id="587dd-143">WMI generates the interval timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

<span data-ttu-id="587dd-144">Чтобы получить эти события таймера во временном потребителе события, выполните [**IWbemServices:: ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) со следующей строкой запроса события:</span><span class="sxs-lookup"><span data-stu-id="587dd-144">To receive these timer events in a temporary event consumer, execute [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) with the following event query string:</span></span>


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



<span data-ttu-id="587dd-145">Чтобы получить эти события таймера в постоянном потребителе события, необходимо загрузить предыдущий запрос в фильтр событий, определить логического потребителя и создать привязку фильтра к потребителю для фильтра и потребителя.</span><span class="sxs-lookup"><span data-stu-id="587dd-145">To receive these timer events in a permanent event consumer, you must load the previous query into an event filter, define a logical consumer, and create a filter-to-consumer binding for the filter and consumer.</span></span> <span data-ttu-id="587dd-146">Дополнительные сведения см. [в разделе Получение событий в любое время](receiving-events-at-all-times.md).</span><span class="sxs-lookup"><span data-stu-id="587dd-146">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

## <a name="examples"></a><span data-ttu-id="587dd-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="587dd-147">Examples</span></span>

<span data-ttu-id="587dd-148">В следующем объявлении MOF показано, как создать событие интервала таймера со свойством Key со значением "MyEvent" каждые 10 секунд:</span><span class="sxs-lookup"><span data-stu-id="587dd-148">The following MOF declaration shows how to generate an interval timer event with the key property set to "MyEvent" every 10 seconds:</span></span>


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a><span data-ttu-id="587dd-149">Требования</span><span class="sxs-lookup"><span data-stu-id="587dd-149">Requirements</span></span>



| <span data-ttu-id="587dd-150">Требование</span><span class="sxs-lookup"><span data-stu-id="587dd-150">Requirement</span></span> | <span data-ttu-id="587dd-151">Значение</span><span class="sxs-lookup"><span data-stu-id="587dd-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="587dd-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="587dd-152">Minimum supported client</span></span><br/> | <span data-ttu-id="587dd-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="587dd-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="587dd-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="587dd-154">Minimum supported server</span></span><br/> | <span data-ttu-id="587dd-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="587dd-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="587dd-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="587dd-156">Namespace</span></span><br/>                | <span data-ttu-id="587dd-157">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="587dd-157">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="587dd-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="587dd-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="587dd-159">**\_\_тимеринструктион**</span><span class="sxs-lookup"><span data-stu-id="587dd-159">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="587dd-160">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="587dd-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="587dd-161">Получение событий времени или повторений</span><span class="sxs-lookup"><span data-stu-id="587dd-161">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

