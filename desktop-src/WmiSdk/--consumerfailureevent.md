---
description: Представляет вхождение другого события, которое отбрасывается из-за сбоя потребителя событий.
ms.assetid: bb6a1ce9-72a2-4528-8bc8-71ac053b6b1d
ms.tgt_platform: multiple
title: Класс __ConsumerFailureEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ConsumerFailureEvent
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 571785245c05d18678c10a65b192a25022fff8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703321"
---
# <a name="__consumerfailureevent-class"></a><span data-ttu-id="deac2-103">\_\_Класс Консумерфаилуривент</span><span class="sxs-lookup"><span data-stu-id="deac2-103">\_\_ConsumerFailureEvent class</span></span>

<span data-ttu-id="deac2-104">Класс System **\_ \_ консумерфаилуривент** представляет собой вхождение какого-либо другого события, которое отбрасывается из-за сбоя потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="deac2-104">The **\_\_ConsumerFailureEvent** system class represents the occurrence of some other event that is being dropped because of the failure of an event consumer.</span></span>

<span data-ttu-id="deac2-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="deac2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="deac2-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="deac2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="deac2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="deac2-107">Syntax</span></span>

``` syntax
class __ConsumerFailureEvent : __EventDroppedEvent
{
  uint32              ErrorCode;
  string              ErrorDescription;
  object              ErrorObject;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="deac2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="deac2-108">Members</span></span>

<span data-ttu-id="deac2-109">Класс **\_ \_ консумерфаилуривент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="deac2-109">The **\_\_ConsumerFailureEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="deac2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="deac2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="deac2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="deac2-111">Properties</span></span>

<span data-ttu-id="deac2-112">Класс **\_ \_ консумерфаилуривент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="deac2-112">The **\_\_ConsumerFailureEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="deac2-113">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="deac2-113">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deac2-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="deac2-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="deac2-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="deac2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deac2-116">Код ошибки, возвращенный потребителем.</span><span class="sxs-lookup"><span data-stu-id="deac2-116">Error code returned by the consumer.</span></span>

</dd> <dt>

<span data-ttu-id="deac2-117">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="deac2-117">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deac2-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="deac2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deac2-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="deac2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deac2-120">Расширенное описание кода ошибки, если оно доступно.</span><span class="sxs-lookup"><span data-stu-id="deac2-120">Extended error code description, if available.</span></span>

</dd> <dt>

<span data-ttu-id="deac2-121">**ерроробжект**</span><span class="sxs-lookup"><span data-stu-id="deac2-121">**ErrorObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deac2-122">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="deac2-122">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="deac2-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="deac2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deac2-124">Объект с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="deac2-124">Object in error.</span></span>

</dd> <dt>

<span data-ttu-id="deac2-125">**Событие**</span><span class="sxs-lookup"><span data-stu-id="deac2-125">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deac2-126">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="deac2-126">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="deac2-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="deac2-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deac2-128">Событие с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="deac2-128">Event in error.</span></span> <span data-ttu-id="deac2-129">Это свойство наследуется от [**\_ \_ евентдроппедевент**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="deac2-129">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="deac2-130">**интендедконсумер**</span><span class="sxs-lookup"><span data-stu-id="deac2-130">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deac2-131">Тип данных: **\_ \_ евентконсумер**</span><span class="sxs-lookup"><span data-stu-id="deac2-131">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="deac2-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="deac2-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deac2-133">Ссылка на предполагаемого потребителя.</span><span class="sxs-lookup"><span data-stu-id="deac2-133">Reference to the intended consumer.</span></span> <span data-ttu-id="deac2-134">Это свойство наследуется от [**\_ \_ евентдроппедевент**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="deac2-134">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="deac2-135">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="deac2-135">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deac2-136">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="deac2-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="deac2-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="deac2-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deac2-138">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="deac2-138">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="deac2-139">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="deac2-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="deac2-140">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="deac2-140">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deac2-141">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="deac2-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="deac2-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="deac2-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deac2-143">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="deac2-143">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="deac2-144">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="deac2-144">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="deac2-145">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="deac2-145">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="deac2-146">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="deac2-146">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="deac2-147">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="deac2-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="deac2-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="deac2-148">Remarks</span></span>

<span data-ttu-id="deac2-149">Класс **\_ \_ консумерфаилуривент** является производным от [**\_ \_ евентдроппедевент**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="deac2-149">The **\_\_ConsumerFailureEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="deac2-150">Требования</span><span class="sxs-lookup"><span data-stu-id="deac2-150">Requirements</span></span>



| <span data-ttu-id="deac2-151">Требование</span><span class="sxs-lookup"><span data-stu-id="deac2-151">Requirement</span></span> | <span data-ttu-id="deac2-152">Значение</span><span class="sxs-lookup"><span data-stu-id="deac2-152">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="deac2-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="deac2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="deac2-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="deac2-154">Windows Vista</span></span><br/>       |
| <span data-ttu-id="deac2-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="deac2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="deac2-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="deac2-156">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="deac2-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="deac2-157">Namespace</span></span><br/>                | <span data-ttu-id="deac2-158">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="deac2-158">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="deac2-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="deac2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deac2-160">**\_\_евентдроппедевент**</span><span class="sxs-lookup"><span data-stu-id="deac2-160">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="deac2-161">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="deac2-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

