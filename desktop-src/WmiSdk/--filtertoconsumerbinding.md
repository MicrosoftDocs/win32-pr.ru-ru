---
description: Используется при регистрации постоянных потребителей событий, чтобы связать экземпляр \_ \_ евентконсумер с экземпляром \_ \_ EventFilter.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: Класс __FilterToConsumerBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
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
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712778"
---
# <a name="__filtertoconsumerbinding-class"></a><span data-ttu-id="bd88f-103">\_\_Класс Филтертоконсумербиндинг</span><span class="sxs-lookup"><span data-stu-id="bd88f-103">\_\_FilterToConsumerBinding class</span></span>

<span data-ttu-id="bd88f-104">Класс System **\_ \_ филтертоконсумербиндинг** используется при регистрации постоянных потребителей событий, чтобы связать экземпляр [**\_ \_ евентконсумер**](--eventconsumer.md) с экземпляром [**\_ \_ EventFilter**](--eventfilter.md).**\_ \_ Филтертоконсумербиндинг** является классом ассоциации.</span><span class="sxs-lookup"><span data-stu-id="bd88f-104">The **\_\_FilterToConsumerBinding** system class is used in the registration of permanent event consumers to relate an instance of the [**\_\_EventConsumer**](--eventconsumer.md) to an instance of [**\_\_EventFilter**](--eventfilter.md).**\_\_FilterToConsumerBinding** is an association class.</span></span>

<span data-ttu-id="bd88f-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="bd88f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bd88f-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="bd88f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd88f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd88f-107">Syntax</span></span>

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a><span data-ttu-id="bd88f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="bd88f-108">Members</span></span>

<span data-ttu-id="bd88f-109">Класс **\_ \_ филтертоконсумербиндинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bd88f-109">The **\_\_FilterToConsumerBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="bd88f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="bd88f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd88f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="bd88f-111">Properties</span></span>

<span data-ttu-id="bd88f-112">Класс **\_ \_ филтертоконсумербиндинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bd88f-112">The **\_\_FilterToConsumerBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd88f-113">**Потребители**</span><span class="sxs-lookup"><span data-stu-id="bd88f-113">**Consumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd88f-114">Тип данных: **\_ \_ евентконсумер**</span><span class="sxs-lookup"><span data-stu-id="bd88f-114">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="bd88f-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bd88f-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bd88f-116">Квалификаторы: [ **ключ**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bd88f-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bd88f-117">Ссылка на экземпляр [**\_ \_ евентконсумер**](--eventconsumer.md) , представляющий путь к объекту для логического потребителя, получателя события.</span><span class="sxs-lookup"><span data-stu-id="bd88f-117">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the object path to a logical consumer, the recipient of an event.</span></span> <span data-ttu-id="bd88f-118">Логический потребитель — это экземпляр класса, производного от **\_ \_ евентконсумер**.</span><span class="sxs-lookup"><span data-stu-id="bd88f-118">A logical consumer is an instance of a class derived from **\_\_EventConsumer**.</span></span>

</dd> <dt>

<span data-ttu-id="bd88f-119">**креаторсид**</span><span class="sxs-lookup"><span data-stu-id="bd88f-119">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd88f-120">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bd88f-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="bd88f-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bd88f-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bd88f-122">Идентификатор безопасности (SID), однозначно определяющий пользователя, создавшего привязку.</span><span class="sxs-lookup"><span data-stu-id="bd88f-122">Security identifier (SID) that uniquely identifies the user who created the binding.</span></span> <span data-ttu-id="bd88f-123">В зависимости от операционной системы WMI хранит идентификатор безопасности администратора или идентификатор безопасности пользователя, который создает экземпляр **\_ \_ филтертоконсумербиндинг**.</span><span class="sxs-lookup"><span data-stu-id="bd88f-123">Depending on the operating system, WMI stores the Administrator SID or the SID of the user that creates an instance of **\_\_FilterToConsumerBinding**.</span></span> <span data-ttu-id="bd88f-124">Дополнительные сведения см. в статьях [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md) и [мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="bd88f-124">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd88f-125">**деливерсинчронаусли**</span><span class="sxs-lookup"><span data-stu-id="bd88f-125">**DeliverSynchronously**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd88f-126">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bd88f-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd88f-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bd88f-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bd88f-128">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="bd88f-128">Obsolete.</span></span> <span data-ttu-id="bd88f-129">Вместо этого используйте свойство **деливерикос** на месте этого свойства, поскольку если **Деливерсинчронаусли** имеет значение **true** , переопределяет значение свойства **деливерикос** .</span><span class="sxs-lookup"><span data-stu-id="bd88f-129">Instead use the **DeliveryQoS** property in place of this property, because if **DeliverSynchronously** is set to **True** it overrides the setting of the **DeliveryQoS** property.</span></span>

</dd> <dt>

<span data-ttu-id="bd88f-130">**деливерикос**</span><span class="sxs-lookup"><span data-stu-id="bd88f-130">**DeliveryQoS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd88f-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd88f-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd88f-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bd88f-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bd88f-133">Качество обслуживания для подписки.</span><span class="sxs-lookup"><span data-stu-id="bd88f-133">Quality of service for a subscription.</span></span> <span data-ttu-id="bd88f-134">Если свойство **деливерсинчронаусли** имеет значение **true**, оно переопределяет значение свойства **деливерикос** .</span><span class="sxs-lookup"><span data-stu-id="bd88f-134">If the **DeliverSynchronously** property is set to **True**, it overrides the setting of the **DeliveryQoS** property.</span></span>

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span data-ttu-id="bd88f-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**Вмимсг \_ Отмечать \_ \_ синхронное качество обслуживания** (0)</span><span class="sxs-lookup"><span data-stu-id="bd88f-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG\_FLAG\_QOS\_SYNCHRONOUS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bd88f-136">Синхронная Доставка</span><span class="sxs-lookup"><span data-stu-id="bd88f-136">Synchronous delivery</span></span>

<span data-ttu-id="bd88f-137">**False**.</span><span class="sxs-lookup"><span data-stu-id="bd88f-137">**False**.</span></span> <span data-ttu-id="bd88f-138">Событие отправляется логическому потребителю синхронно.</span><span class="sxs-lookup"><span data-stu-id="bd88f-138">The event is delivered to the logical consumer synchronously.</span></span>

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span data-ttu-id="bd88f-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**Вмимсг \_ ОТМЕТИТЬ \_ QoS \_ Express** (1)</span><span class="sxs-lookup"><span data-stu-id="bd88f-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG\_FLAG\_QOS\_EXPRESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bd88f-140">Быстрая доставка</span><span class="sxs-lookup"><span data-stu-id="bd88f-140">Express delivery</span></span>

<span data-ttu-id="bd88f-141">**True**.</span><span class="sxs-lookup"><span data-stu-id="bd88f-141">**True**.</span></span> <span data-ttu-id="bd88f-142">Событие доставляется логическому потребителю асинхронно.</span><span class="sxs-lookup"><span data-stu-id="bd88f-142">The event is delivered to the logical consumer asynchronously.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd88f-143">**Фильтр**</span><span class="sxs-lookup"><span data-stu-id="bd88f-143">**Filter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd88f-144">Тип данных: **\_ \_ EventFilter**</span><span class="sxs-lookup"><span data-stu-id="bd88f-144">Data type: **\_\_EventFilter**</span></span>
</dt> <dt>

<span data-ttu-id="bd88f-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bd88f-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bd88f-146">Квалификаторы: [ **ключ**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bd88f-146">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bd88f-147">Ссылка на экземпляр [**\_ \_ EventFilter**](--eventfilter.md) , представляющий путь к объекту для фильтра событий, который представляет собой запрос, указывающий тип получаемого события.</span><span class="sxs-lookup"><span data-stu-id="bd88f-147">Reference to an instance of [**\_\_EventFilter**](--eventfilter.md) that represents the object path to an event filter which is a query that specifies the type of event to be received.</span></span>

</dd> <dt>

<span data-ttu-id="bd88f-148">**маинтаинсекуритиконтекст**</span><span class="sxs-lookup"><span data-stu-id="bd88f-148">**MaintainSecurityContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd88f-149">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bd88f-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd88f-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bd88f-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bd88f-151">Если задано **значение true**, события доставляются в том же контексте безопасности, в котором они находились при их передаче поставщику.</span><span class="sxs-lookup"><span data-stu-id="bd88f-151">If **True**, the events are delivered in the same security context that the provider was in when it provided them.</span></span>

> [!Note]  
> <span data-ttu-id="bd88f-152">Только потребитель, реализованный в виде библиотеки DLL (внутрипроцессный потребитель), может получить события в контексте безопасности поставщика.</span><span class="sxs-lookup"><span data-stu-id="bd88f-152">Only a consumer implemented as a DLL (an in-process consumer) can receive events in the security context of the provider.</span></span> <span data-ttu-id="bd88f-153">Дополнительные сведения о внутрипроцессного поставщиках и безопасности см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="bd88f-153">For more information about in-process providers and security, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="bd88f-154">Дополнительные сведения и примеры см. в разделе Replace:[получение событий безопасно](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="bd88f-154">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

 

</dd> <dt>

<span data-ttu-id="bd88f-155">**словдовнпровидерс**</span><span class="sxs-lookup"><span data-stu-id="bd88f-155">**SlowDownProviders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd88f-156">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bd88f-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd88f-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bd88f-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bd88f-158">Если **значение равно true**, поставщики замедляют работу, если этот потребитель не может справиться.</span><span class="sxs-lookup"><span data-stu-id="bd88f-158">If **True**, providers are slowed down if this consumer cannot keep up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd88f-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd88f-159">Remarks</span></span>

<span data-ttu-id="bd88f-160">Класс **\_ \_ филтертоконсумербиндинг** является производным от [**\_ \_ индикатионрелатед**](--indicationrelated.md), у которого нет свойств.</span><span class="sxs-lookup"><span data-stu-id="bd88f-160">The **\_\_FilterToConsumerBinding** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="bd88f-161">Постоянные потребители событий используют класс System **\_ \_ филтертоконсумербиндинг** для привязки фильтров событий к конечным потребителям.</span><span class="sxs-lookup"><span data-stu-id="bd88f-161">Permanent event consumers use the **\_\_FilterToConsumerBinding** system class to bind event filters to final consumers.</span></span> <span data-ttu-id="bd88f-162">После того как фильтр и потребитель связываются друг с другом, Инструментарий WMI может пересылать события, соответствующие фильтру, соответствующему потребителю.</span><span class="sxs-lookup"><span data-stu-id="bd88f-162">After the filter and consumer are bound together, WMI can forward events that match the filter to the corresponding consumer.</span></span>

## <a name="examples"></a><span data-ttu-id="bd88f-163">Примеры</span><span class="sxs-lookup"><span data-stu-id="bd88f-163">Examples</span></span>

<span data-ttu-id="bd88f-164">[Процедура создания постоянной регистрации событий WMI для мониторинга файлов](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) в коллекции TechNet использует **\_ \_ филтертоконсумербиндинг** в составе сложного сценария для настройки постоянной регистрации событий WMI.</span><span class="sxs-lookup"><span data-stu-id="bd88f-164">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_FilterToConsumerBinding** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd88f-165">Требования</span><span class="sxs-lookup"><span data-stu-id="bd88f-165">Requirements</span></span>



| <span data-ttu-id="bd88f-166">Требование</span><span class="sxs-lookup"><span data-stu-id="bd88f-166">Requirement</span></span> | <span data-ttu-id="bd88f-167">Значение</span><span class="sxs-lookup"><span data-stu-id="bd88f-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="bd88f-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd88f-168">Minimum supported client</span></span><br/> | <span data-ttu-id="bd88f-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd88f-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="bd88f-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd88f-170">Minimum supported server</span></span><br/> | <span data-ttu-id="bd88f-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd88f-171">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="bd88f-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bd88f-172">Namespace</span></span><br/>                | <span data-ttu-id="bd88f-173">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="bd88f-173">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="bd88f-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd88f-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd88f-175">**\_\_индикатионрелатед**</span><span class="sxs-lookup"><span data-stu-id="bd88f-175">**\_\_IndicationRelated**</span></span>](--indicationrelated.md)
</dt> <dt>

[<span data-ttu-id="bd88f-176">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="bd88f-176">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="bd88f-177">Мониторинг событий и реагирование на них с помощью стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="bd88f-177">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="bd88f-178">Мониторинг событий</span><span class="sxs-lookup"><span data-stu-id="bd88f-178">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="bd88f-179">Создание фильтра событий</span><span class="sxs-lookup"><span data-stu-id="bd88f-179">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="bd88f-180">Защита событий WMI</span><span class="sxs-lookup"><span data-stu-id="bd88f-180">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




