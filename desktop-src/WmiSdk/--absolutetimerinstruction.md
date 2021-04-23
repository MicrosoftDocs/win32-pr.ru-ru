---
description: Вызывает создание события на определенную дату в определенное время.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: Класс __AbsoluteTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693799"
---
# <a name="__absolutetimerinstruction-class"></a><span data-ttu-id="90831-103">\_\_Класс Абсолутетимеринструктион</span><span class="sxs-lookup"><span data-stu-id="90831-103">\_\_AbsoluteTimerInstruction class</span></span>

<span data-ttu-id="90831-104">Класс System **\_ \_ абсолутетимеринструктион** вызывает создание события на определенную дату в определенное время.</span><span class="sxs-lookup"><span data-stu-id="90831-104">The **\_\_AbsoluteTimerInstruction** system class causes an event to be generated on a specific date at a specific time.</span></span> <span data-ttu-id="90831-105">Потребитель событий регистрируется для получения абсолютного события таймера путем создания экземпляра этого класса.</span><span class="sxs-lookup"><span data-stu-id="90831-105">An event consumer registers to receive an absolute timer event by creating an instance of this class.</span></span> <span data-ttu-id="90831-106">Событие создается один раз.</span><span class="sxs-lookup"><span data-stu-id="90831-106">The event is generated one time.</span></span>

<span data-ttu-id="90831-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="90831-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="90831-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="90831-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="90831-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90831-109">Syntax</span></span>

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a><span data-ttu-id="90831-110">Члены</span><span class="sxs-lookup"><span data-stu-id="90831-110">Members</span></span>

<span data-ttu-id="90831-111">Класс **\_ \_ абсолутетимеринструктион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="90831-111">The **\_\_AbsoluteTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="90831-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="90831-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90831-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="90831-113">Properties</span></span>

<span data-ttu-id="90831-114">Класс **\_ \_ абсолутетимеринструктион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="90831-114">The **\_\_AbsoluteTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90831-115">**Одно eventdatetime**</span><span class="sxs-lookup"><span data-stu-id="90831-115">**EventDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90831-116">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="90831-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="90831-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="90831-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="90831-118">Строка фиксированной длины в [формате DMTF](date-and-time-format.md) , указывающая время срабатывания таймера.</span><span class="sxs-lookup"><span data-stu-id="90831-118">Fixed-length string in [DMTF format](date-and-time-format.md) that specifies when the timer fires.</span></span>

</dd> <dt>

<span data-ttu-id="90831-119">**скипифпассед**</span><span class="sxs-lookup"><span data-stu-id="90831-119">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90831-120">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="90831-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90831-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="90831-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90831-122">Если **значение равно true**, событие таймера возникает, если Инструментарий WMI не может создать его в нужном интервале времени или если потребитель, запрашивающий получение события, недоступен.</span><span class="sxs-lookup"><span data-stu-id="90831-122">If **TRUE**, the timer event occurs if WMI cannot generate it at the correct time interval, or the consumer requesting to receive the event is unavailable.</span></span> <span data-ttu-id="90831-123">Если **значение равно true**, событие не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90831-123">If **TRUE**, the event will not occur.</span></span> <span data-ttu-id="90831-124">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="90831-124">The default is **FALSE**.</span></span> <span data-ttu-id="90831-125">Когда WMI или потребитель становится доступным, создается и получается событие уведомления.</span><span class="sxs-lookup"><span data-stu-id="90831-125">When WMI or the consumer becomes available, a notification event is generated and received.</span></span> <span data-ttu-id="90831-126">Это свойство наследуется от [**\_ \_ тимеринструктион**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="90831-126">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="90831-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="90831-127">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="90831-128">Когда WMI или потребитель снова становится доступным, будет создано и получено событие уведомления.</span><span class="sxs-lookup"><span data-stu-id="90831-128">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="90831-129">true</span><span class="sxs-lookup"><span data-stu-id="90831-129">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="90831-130">Событие Timer не возникает, если Инструментарий WMI недоступен для его создания в соответствующий интервал времени или если потребитель, запрашивающий получение события, недоступен.</span><span class="sxs-lookup"><span data-stu-id="90831-130">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="90831-131">**тимерид**</span><span class="sxs-lookup"><span data-stu-id="90831-131">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90831-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="90831-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90831-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="90831-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90831-134">Квалификаторы: [ **ключ**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="90831-134">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="90831-135">Уникальная строка, назначенная пользователем, которая определяет конкретное событие таймера.</span><span class="sxs-lookup"><span data-stu-id="90831-135">Unique user-assigned string that identifies a specific timer event.</span></span> <span data-ttu-id="90831-136">Чтобы избежать конфликтов имен с другими идентификаторами таймера, можно использовать строку в форме GUID стиля среды распределенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="90831-136">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment style GUID can be used.</span></span> <span data-ttu-id="90831-137">Это свойство наследуется от [**\_ \_ тимеринструктион**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="90831-137">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90831-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90831-138">Remarks</span></span>

<span data-ttu-id="90831-139">Класс **\_ \_ абсолутетимеринструктион** является производным от [**\_ \_ тимеринструктион**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="90831-139">The **\_\_AbsoluteTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="90831-140">Инструментарий WMI создает абсолютное событие таймера, создавая экземпляр класса [**\_ \_ тимеревент**](--timerevent.md) .</span><span class="sxs-lookup"><span data-stu-id="90831-140">WMI generates the absolute timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="90831-141">Требования</span><span class="sxs-lookup"><span data-stu-id="90831-141">Requirements</span></span>



| <span data-ttu-id="90831-142">Требование</span><span class="sxs-lookup"><span data-stu-id="90831-142">Requirement</span></span> | <span data-ttu-id="90831-143">Значение</span><span class="sxs-lookup"><span data-stu-id="90831-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="90831-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90831-144">Minimum supported client</span></span><br/> | <span data-ttu-id="90831-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90831-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="90831-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90831-146">Minimum supported server</span></span><br/> | <span data-ttu-id="90831-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90831-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="90831-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="90831-148">Namespace</span></span><br/>                | <span data-ttu-id="90831-149">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="90831-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="90831-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90831-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90831-151">**\_\_тимеринструктион**</span><span class="sxs-lookup"><span data-stu-id="90831-151">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="90831-152">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="90831-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="90831-153">Получение событий времени или повторений</span><span class="sxs-lookup"><span data-stu-id="90831-153">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[<span data-ttu-id="90831-154">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="90831-154">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="90831-155">Получение событий для длительности вашего приложения</span><span class="sxs-lookup"><span data-stu-id="90831-155">Receiving Events for the Duration of Your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

