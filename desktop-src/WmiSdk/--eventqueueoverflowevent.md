---
description: Сообщает, когда событие удаляется в результате переполнения очереди доставки.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: Класс __EventQueueOverflowEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712780"
---
# <a name="__eventqueueoverflowevent-class"></a><span data-ttu-id="c6226-103">\_\_Класс Евенткуеуеоверфловевент</span><span class="sxs-lookup"><span data-stu-id="c6226-103">\_\_EventQueueOverflowEvent class</span></span>

<span data-ttu-id="c6226-104">Класс System **\_ \_ евенткуеуеоверфловевент** сообщает, когда событие удаляется в результате переполнения очереди доставки.</span><span class="sxs-lookup"><span data-stu-id="c6226-104">The **\_\_EventQueueOverflowEvent** system class reports when an event is dropped as a result of delivery queue overflow.</span></span>

<span data-ttu-id="c6226-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c6226-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c6226-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c6226-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6226-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6226-107">Syntax</span></span>

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="c6226-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c6226-108">Members</span></span>

<span data-ttu-id="c6226-109">Класс **\_ \_ евенткуеуеоверфловевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c6226-109">The **\_\_EventQueueOverflowEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="c6226-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c6226-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6226-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c6226-111">Properties</span></span>

<span data-ttu-id="c6226-112">Класс **\_ \_ евенткуеуеоверфловевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c6226-112">The **\_\_EventQueueOverflowEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6226-113">**курренткуеуесизе**</span><span class="sxs-lookup"><span data-stu-id="c6226-113">**CurrentQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6226-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6226-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6226-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c6226-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6226-116">Текущий размер очереди в байтах.</span><span class="sxs-lookup"><span data-stu-id="c6226-116">Current queue size, in bytes.</span></span> <span data-ttu-id="c6226-117">По умолчанию это свойство имеет значение 10 МБ для всех очередей.</span><span class="sxs-lookup"><span data-stu-id="c6226-117">This property defaults to 10 MB for all queues combined.</span></span>

</dd> <dt>

<span data-ttu-id="c6226-118">**Событие**</span><span class="sxs-lookup"><span data-stu-id="c6226-118">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6226-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="c6226-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6226-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c6226-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6226-121">Событие, представляющее интерес.</span><span class="sxs-lookup"><span data-stu-id="c6226-121">Event of interest.</span></span> <span data-ttu-id="c6226-122">Это свойство наследуется от [**\_ \_ евентдроппедевент**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="c6226-122">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6226-123">**интендедконсумер**</span><span class="sxs-lookup"><span data-stu-id="c6226-123">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6226-124">Тип данных: **\_ \_ евентконсумер**</span><span class="sxs-lookup"><span data-stu-id="c6226-124">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="c6226-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c6226-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6226-126">Ссылка на предполагаемого потребителя.</span><span class="sxs-lookup"><span data-stu-id="c6226-126">Reference to the intended consumer.</span></span> <span data-ttu-id="c6226-127">Это свойство наследуется от [**\_ \_ евентдроппедевент**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="c6226-127">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6226-128">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="c6226-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6226-129">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c6226-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c6226-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c6226-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6226-131">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="c6226-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="c6226-132">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="c6226-132">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6226-133">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="c6226-133">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6226-134">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6226-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c6226-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c6226-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6226-136">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="c6226-136">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="c6226-137">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="c6226-137">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="c6226-138">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="c6226-138">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="c6226-139">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="c6226-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="c6226-140">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c6226-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6226-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6226-141">Remarks</span></span>

<span data-ttu-id="c6226-142">Только пользователи с правами администратора могут получить это событие.</span><span class="sxs-lookup"><span data-stu-id="c6226-142">Only users with administrator privileges are able to receive this event.</span></span> <span data-ttu-id="c6226-143">Класс **\_ \_ евенткуеуеоверфловевент** является производным от [**\_ \_ евентдроппедевент**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="c6226-143">The **\_\_EventQueueOverflowEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

<span data-ttu-id="c6226-144">Дополнительные сведения см. в описании свойства [**максимумкуеуесизе**](--eventconsumer.md) класса [**\_ \_ евентконсумер**](--eventconsumer.md) и свойства [**хигхсрешолдоневентс**](/windows/desktop/CIMWin32Prov/win32-wmisetting) в классе **Win32 \_ вмисеттинг** .</span><span class="sxs-lookup"><span data-stu-id="c6226-144">For more information, see the [**MaximumQueueSize**](--eventconsumer.md) property in the [**\_\_EventConsumer**](--eventconsumer.md) class and the [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property in the **Win32\_WMISetting** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6226-145">Требования</span><span class="sxs-lookup"><span data-stu-id="c6226-145">Requirements</span></span>



| <span data-ttu-id="c6226-146">Требование</span><span class="sxs-lookup"><span data-stu-id="c6226-146">Requirement</span></span> | <span data-ttu-id="c6226-147">Значение</span><span class="sxs-lookup"><span data-stu-id="c6226-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c6226-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6226-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c6226-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6226-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c6226-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6226-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c6226-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6226-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c6226-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c6226-152">Namespace</span></span><br/>                | <span data-ttu-id="c6226-153">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="c6226-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c6226-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6226-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6226-155">**\_\_евентдроппедевент**</span><span class="sxs-lookup"><span data-stu-id="c6226-155">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="c6226-156">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="c6226-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

