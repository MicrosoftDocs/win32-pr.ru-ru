---
description: Указывает инструкции по созданию событий таймера для потребителей.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: Класс __TimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350095"
---
# <a name="__timerinstruction-class"></a><span data-ttu-id="5320d-103">\_\_Класс Тимеринструктион</span><span class="sxs-lookup"><span data-stu-id="5320d-103">\_\_TimerInstruction class</span></span>

<span data-ttu-id="5320d-104">Абстрактный системный класс **\_ \_ тимеринструктион** указывает инструкции по созданию [событий таймера](receiving-a-timed-or-repeating-event.md) для потребителей.</span><span class="sxs-lookup"><span data-stu-id="5320d-104">The **\_\_TimerInstruction** abstract system class specifies instructions on how [timer events](receiving-a-timed-or-repeating-event.md) should be generated for consumers.</span></span>

<span data-ttu-id="5320d-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5320d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5320d-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="5320d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5320d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5320d-107">Syntax</span></span>

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="5320d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5320d-108">Members</span></span>

<span data-ttu-id="5320d-109">Класс **\_ \_ тимеринструктион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5320d-109">The **\_\_TimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="5320d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5320d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5320d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5320d-111">Properties</span></span>

<span data-ttu-id="5320d-112">Класс **\_ \_ тимеринструктион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5320d-112">The **\_\_TimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5320d-113">**скипифпассед**</span><span class="sxs-lookup"><span data-stu-id="5320d-113">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5320d-114">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5320d-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5320d-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5320d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5320d-116">Описывает, будет ли создаваться событие уведомления и получать сообщение, когда потребитель становится доступным.</span><span class="sxs-lookup"><span data-stu-id="5320d-116">Describes whether a notification event will be generated and receive when a consumer becomes available.</span></span>

<dt>

<span data-ttu-id="5320d-117">FALSE</span><span class="sxs-lookup"><span data-stu-id="5320d-117">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="5320d-118">Когда WMI или потребитель снова становится доступным, будет создано и получено событие уведомления.</span><span class="sxs-lookup"><span data-stu-id="5320d-118">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="5320d-119">true</span><span class="sxs-lookup"><span data-stu-id="5320d-119">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="5320d-120">Событие Timer не возникает, если Инструментарий WMI недоступен для его создания в соответствующий интервал времени или если потребитель, запрашивающий получение события, недоступен.</span><span class="sxs-lookup"><span data-stu-id="5320d-120">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5320d-121">**тимерид**</span><span class="sxs-lookup"><span data-stu-id="5320d-121">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5320d-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5320d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5320d-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5320d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5320d-124">Квалификаторы: [ **ключ**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5320d-124">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5320d-125">Уникальная пользовательская строка, идентифицирующая данное событие таймера.</span><span class="sxs-lookup"><span data-stu-id="5320d-125">Unique user-assigned string that identifies this particular timer event.</span></span> <span data-ttu-id="5320d-126">Чтобы избежать конфликтов имен с другими идентификаторами таймера, можно использовать строку в форме GUID типа распределенной среды компьютера (DCE).</span><span class="sxs-lookup"><span data-stu-id="5320d-126">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment (DCE)-style GUID can be used.</span></span> <span data-ttu-id="5320d-127">Это свойство является частью экземпляра [**\_ \_ тимеревент**](--timerevent.md) , представляющего событие.</span><span class="sxs-lookup"><span data-stu-id="5320d-127">This property is part of the [**\_\_TimerEvent**](--timerevent.md) instance that represents the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5320d-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5320d-128">Remarks</span></span>

<span data-ttu-id="5320d-129">Класс **\_ \_ тимеринструктион** является производным от [**\_ \_ евентженератор**](--eventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="5320d-129">The **\_\_TimerInstruction** class is derived from [**\_\_EventGenerator**](--eventgenerator.md).</span></span>

<span data-ttu-id="5320d-130">Подклассы **\_ \_ тимеринструктион** — это [**\_ \_ абсолутетимеринструктион**](--absolutetimerinstruction.md), используемые потребителями для регистрации в отношении абсолютного события таймера и [**\_ \_ интервалтимеринструктион**](--intervaltimerinstruction.md), которые используются для регистрации события интервала времени.</span><span class="sxs-lookup"><span data-stu-id="5320d-130">The **\_\_TimerInstruction** subclasses are [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md), used by consumers to register for an absolute timer event, and [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md), used to register for an interval timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="5320d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="5320d-131">Requirements</span></span>



| <span data-ttu-id="5320d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="5320d-132">Requirement</span></span> | <span data-ttu-id="5320d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="5320d-133">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5320d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5320d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5320d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5320d-135">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5320d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5320d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5320d-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5320d-137">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5320d-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5320d-138">Namespace</span></span><br/>                | <span data-ttu-id="5320d-139">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="5320d-139">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5320d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5320d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5320d-141">**\_\_евентженератор**</span><span class="sxs-lookup"><span data-stu-id="5320d-141">**\_\_EventGenerator**</span></span>](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[<span data-ttu-id="5320d-142">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="5320d-142">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

