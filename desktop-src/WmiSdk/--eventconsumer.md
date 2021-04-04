---
description: Является абстрактным базовым классом, который используется при регистрации постоянного потребителя событий.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: Класс __EventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999656"
---
# <a name="__eventconsumer-class"></a><span data-ttu-id="ecd28-103">\_\_Класс Евентконсумер</span><span class="sxs-lookup"><span data-stu-id="ecd28-103">\_\_EventConsumer class</span></span>

<span data-ttu-id="ecd28-104">Класс System **\_ \_ евентконсумер** является абстрактным базовым классом, который используется при регистрации постоянного потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="ecd28-104">The **\_\_EventConsumer** system class is an abstract base class that is used in the registration of a permanent event consumer.</span></span> <span data-ttu-id="ecd28-105">Новый класс потребителя событий можно создать из **\_ \_ евентконсумер**.</span><span class="sxs-lookup"><span data-stu-id="ecd28-105">You can derive a new event consumer class from **\_\_EventConsumer**.</span></span>

<span data-ttu-id="ecd28-106">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ecd28-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ecd28-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ecd28-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd28-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecd28-108">Syntax</span></span>

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a><span data-ttu-id="ecd28-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ecd28-109">Members</span></span>

<span data-ttu-id="ecd28-110">Класс **\_ \_ евентконсумер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ecd28-110">The **\_\_EventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="ecd28-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ecd28-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ecd28-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ecd28-112">Properties</span></span>

<span data-ttu-id="ecd28-113">Класс **\_ \_ евентконсумер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ecd28-113">The **\_\_EventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ecd28-114">**креаторсид**</span><span class="sxs-lookup"><span data-stu-id="ecd28-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecd28-115">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ecd28-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ecd28-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ecd28-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecd28-117">Идентификатор безопасности (SID), однозначно определяющий пользователя, который создает фильтр.</span><span class="sxs-lookup"><span data-stu-id="ecd28-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="ecd28-118">WMI хранит идентификатор безопасности пользователя, создающего экземпляр **\_ \_ евентконсумер** , или идентификатор безопасности администратора в зависимости от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ecd28-118">WMI stores the SID of the user who creates an instance of **\_\_EventConsumer** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="ecd28-119">Дополнительные сведения см. в статьях [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md) и [мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="ecd28-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecd28-120">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="ecd28-120">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecd28-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ecd28-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecd28-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ecd28-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecd28-123">Имя компьютера, на который инструментарий управления Windows (WMI) (WMI) отправляет события.</span><span class="sxs-lookup"><span data-stu-id="ecd28-123">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

</dd> <dt>

<span data-ttu-id="ecd28-124">**максимумкуеуесизе**</span><span class="sxs-lookup"><span data-stu-id="ecd28-124">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecd28-125">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecd28-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecd28-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ecd28-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecd28-127">Максимальная очередь для конкретного потребителя в байтах.</span><span class="sxs-lookup"><span data-stu-id="ecd28-127">Maximum queue for a specific consumer, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecd28-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ecd28-128">Remarks</span></span>

<span data-ttu-id="ecd28-129">Класс **\_ \_ евентконсумер** является производным от [**\_ \_ индикатионрелатед**](--indicationrelated.md), у которого нет свойств.</span><span class="sxs-lookup"><span data-stu-id="ecd28-129">The **\_\_EventConsumer** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which does not have properties.</span></span>

<span data-ttu-id="ecd28-130">Постоянные потребители определяют новые классы потребителей, описывающие действия, которые необходимо выполнить, и данные, которые должны обрабатываться, когда потребители получают уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="ecd28-130">Permanent consumers define new consumer classes to describe an action to take and data to be processed when consumers receive event notifications.</span></span> <span data-ttu-id="ecd28-131">Постоянные потребители имеют особые соображения безопасности.</span><span class="sxs-lookup"><span data-stu-id="ecd28-131">Permanent consumers have special security concerns.</span></span> <span data-ttu-id="ecd28-132">Дополнительные сведения см. в разделе [Защита событий WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="ecd28-132">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd28-133">Требования</span><span class="sxs-lookup"><span data-stu-id="ecd28-133">Requirements</span></span>



| <span data-ttu-id="ecd28-134">Требование</span><span class="sxs-lookup"><span data-stu-id="ecd28-134">Requirement</span></span> | <span data-ttu-id="ecd28-135">Значение</span><span class="sxs-lookup"><span data-stu-id="ecd28-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ecd28-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecd28-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ecd28-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecd28-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ecd28-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecd28-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ecd28-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecd28-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ecd28-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ecd28-140">Namespace</span></span><br/>                | <span data-ttu-id="ecd28-141">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="ecd28-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ecd28-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecd28-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd28-143">**\_\_индикатионрелатед**</span><span class="sxs-lookup"><span data-stu-id="ecd28-143">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="ecd28-144">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="ecd28-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="ecd28-145">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="ecd28-145">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="ecd28-146">Создание нового класса постоянного потребителя событий</span><span class="sxs-lookup"><span data-stu-id="ecd28-146">Creating a New Permanent Event Consumer Class</span></span>](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[<span data-ttu-id="ecd28-147">Создание логического потребителя</span><span class="sxs-lookup"><span data-stu-id="ecd28-147">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="ecd28-148">Защита событий WMI</span><span class="sxs-lookup"><span data-stu-id="ecd28-148">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

