---
description: Представляет вхождение события, которое удаляется. Удаленное событие — это событие, которое не доставляется потребителю события.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: Класс __EventDroppedEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702753"
---
# <a name="__eventdroppedevent-class"></a><span data-ttu-id="1c770-104">\_\_Класс Евентдроппедевент</span><span class="sxs-lookup"><span data-stu-id="1c770-104">\_\_EventDroppedEvent class</span></span>

<span data-ttu-id="1c770-105">Класс System **\_ \_ евентдроппедевент** представляет вхождение события, которое удаляется.</span><span class="sxs-lookup"><span data-stu-id="1c770-105">The **\_\_EventDroppedEvent** system class represents the occurrence of an event that is dropped.</span></span> <span data-ttu-id="1c770-106">Удаленное событие — это событие, которое не доставляется потребителю события.</span><span class="sxs-lookup"><span data-stu-id="1c770-106">A dropped event is an event that is not delivered to an event consumer.</span></span>

<span data-ttu-id="1c770-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1c770-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1c770-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1c770-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c770-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c770-109">Syntax</span></span>

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="1c770-110">Члены</span><span class="sxs-lookup"><span data-stu-id="1c770-110">Members</span></span>

<span data-ttu-id="1c770-111">Класс **\_ \_ евентдроппедевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1c770-111">The **\_\_EventDroppedEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="1c770-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c770-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c770-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c770-113">Properties</span></span>

<span data-ttu-id="1c770-114">Класс **\_ \_ евентдроппедевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1c770-114">The **\_\_EventDroppedEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c770-115">**Событие**</span><span class="sxs-lookup"><span data-stu-id="1c770-115">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c770-116">Тип данных: **\_ \_ событие**</span><span class="sxs-lookup"><span data-stu-id="1c770-116">Data type: **\_\_Event**</span></span>
</dt> <dt>

<span data-ttu-id="1c770-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c770-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c770-118">Событие, которое удаляется.</span><span class="sxs-lookup"><span data-stu-id="1c770-118">Event that is dropped.</span></span>

</dd> <dt>

<span data-ttu-id="1c770-119">**интендедконсумер**</span><span class="sxs-lookup"><span data-stu-id="1c770-119">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c770-120">Тип данных: **\_ \_ евентконсумер**</span><span class="sxs-lookup"><span data-stu-id="1c770-120">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="1c770-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c770-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c770-122">Ссылка на экземпляр [**\_ \_ евентконсумер**](--eventconsumer.md) , представляющий постоянный потребитель, который определяется для получения события.</span><span class="sxs-lookup"><span data-stu-id="1c770-122">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the permanent consumer you identify to receive an event.</span></span> <span data-ttu-id="1c770-123">Различные постоянные потребители, которые подписываются на событие, могут продолжать получение события.</span><span class="sxs-lookup"><span data-stu-id="1c770-123">Different permanent consumers that subscribe to an event can continue to receive the event.</span></span>

</dd> <dt>

<span data-ttu-id="1c770-124">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="1c770-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c770-125">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1c770-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1c770-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c770-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c770-127">Дескриптор, используемый поставщиком событий для определения пользователей, которые могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="1c770-127">Descriptor that an event provider uses to determine the users who can receive an event.</span></span> <span data-ttu-id="1c770-128">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="1c770-128">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c770-129">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="1c770-129">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c770-130">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c770-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c770-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c770-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c770-132">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="1c770-132">Unique value that indicates the time when an event is generated.</span></span> <span data-ttu-id="1c770-133">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="1c770-133">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="1c770-134">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="1c770-134">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="1c770-135">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="1c770-135">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="1c770-136">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1c770-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c770-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c770-137">Remarks</span></span>

<span data-ttu-id="1c770-138">Класс **\_ \_ евентдроппедевент** является производным от [**\_ \_ системевент**](--systemevent.md).</span><span class="sxs-lookup"><span data-stu-id="1c770-138">The **\_\_EventDroppedEvent** class is derived from [**\_\_SystemEvent**](--systemevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c770-139">Требования</span><span class="sxs-lookup"><span data-stu-id="1c770-139">Requirements</span></span>



| <span data-ttu-id="1c770-140">Требование</span><span class="sxs-lookup"><span data-stu-id="1c770-140">Requirement</span></span> | <span data-ttu-id="1c770-141">Значение</span><span class="sxs-lookup"><span data-stu-id="1c770-141">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1c770-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c770-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1c770-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c770-143">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1c770-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c770-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1c770-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c770-145">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1c770-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1c770-146">Namespace</span></span><br/>                | <span data-ttu-id="1c770-147">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="1c770-147">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1c770-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c770-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c770-149">**\_\_системевент**</span><span class="sxs-lookup"><span data-stu-id="1c770-149">**\_\_SystemEvent**</span></span>](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[<span data-ttu-id="1c770-150">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="1c770-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

