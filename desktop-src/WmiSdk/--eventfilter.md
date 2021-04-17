---
description: Для регистрации постоянного потребителя событий требуется экземпляр \_ \_ класса System EventFilter.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: Класс __EventFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
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
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702565"
---
# <a name="__eventfilter-class"></a><span data-ttu-id="3b302-103">\_\_Класс EventFilter</span><span class="sxs-lookup"><span data-stu-id="3b302-103">\_\_EventFilter class</span></span>

<span data-ttu-id="3b302-104">Для регистрации постоянного потребителя событий требуется экземпляр класса System **\_ \_ EventFilter** .</span><span class="sxs-lookup"><span data-stu-id="3b302-104">The registration of a permanent event consumer requires an instance of the **\_\_EventFilter** system class.</span></span>

<span data-ttu-id="3b302-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3b302-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3b302-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="3b302-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b302-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b302-107">Syntax</span></span>

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a><span data-ttu-id="3b302-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3b302-108">Members</span></span>

<span data-ttu-id="3b302-109">Класс **\_ \_ EventFilter** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3b302-109">The **\_\_EventFilter** class has these types of members:</span></span>

-   [<span data-ttu-id="3b302-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3b302-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b302-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3b302-111">Properties</span></span>

<span data-ttu-id="3b302-112">Класс **\_ \_ EventFilter** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3b302-112">The **\_\_EventFilter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b302-113">**креаторсид**</span><span class="sxs-lookup"><span data-stu-id="3b302-113">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b302-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3b302-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3b302-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b302-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b302-116">Идентификатор безопасности (SID), однозначно определяющий пользователя, который создает этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="3b302-116">Security identifier (SID) that uniquely identifies the user who creates this filter.</span></span> <span data-ttu-id="3b302-117">Инструментарий управления Windows (WMI) (WMI) хранит идентификатор безопасности пользователя, который создает экземпляр **\_ \_ EventFilter** или идентификатор безопасности администратора в зависимости от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3b302-117">Windows Management Instrumentation (WMI) stores the SID of the user that creates an instance of **\_\_EventFilter** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="3b302-118">Дополнительные сведения см. в статьях [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md) и [мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="3b302-118">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b302-119">**евентакцесс**</span><span class="sxs-lookup"><span data-stu-id="3b302-119">**EventAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b302-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3b302-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b302-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b302-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b302-122">Дескриптор безопасности (SD) в языке определения дескрипторов безопасности (SDDL), который управляет доступом к событиям, доставляемым в фильтр.</span><span class="sxs-lookup"><span data-stu-id="3b302-122">Security descriptor (SD) in Security Descriptor Definition Language (SDDL) that controls access for events delivered to the filter.</span></span> <span data-ttu-id="3b302-123">Используйте это свойство, чтобы указать, что в этот фильтр могут доставляться только события в контексте безопасности конкретных учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3b302-123">Use this property to specify that only events in the security context of specific accounts can be delivered to this filter.</span></span> <span data-ttu-id="3b302-124">Например, постоянный потребитель событий может очищать журналы безопасности только в том случае, если конкретный пользователь создает определенное событие.</span><span class="sxs-lookup"><span data-stu-id="3b302-124">For example, a permanent event consumer may clear the security logs only when a specific event is generated by a specific user.</span></span> <span data-ttu-id="3b302-125">Чтобы указать, кто может публиковать события в этом фильтре, используйте маску **\_ \_ публикации WBEM справа** в записи управления доступом (ACE) для свойства " [**\_ дескриптор безопасности**](--event.md) ".</span><span class="sxs-lookup"><span data-stu-id="3b302-125">To specify who can publish events to this filter, use the **WBEM\_RIGHT\_PUBLISH** mask in the Access Control Entry (ACE) for the [**SECURITY\_DESCRIPTOR**](--event.md) property.</span></span> <span data-ttu-id="3b302-126">Дополнительные сведения см. в разделе [язык определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="3b302-126">For more information, see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span> <span data-ttu-id="3b302-127">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3b302-127">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span> <span data-ttu-id="3b302-128">Дополнительные сведения и примеры см. в разделе Replace:[получение событий безопасно](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="3b302-128">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="3b302-129">Можно настроить дескриптор безопасности доступа к событиям, чтобы разрешить доставку события только в том случае, если локальная системная учетная запись создает событие.</span><span class="sxs-lookup"><span data-stu-id="3b302-129">You can configure an event access security descriptor to allow an event to be delivered only when the local system account generates the event.</span></span> <span data-ttu-id="3b302-130">Дополнительные сведения о создании дескриптора безопасности и авторизации доступа см. в разделе [Управление доступом](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="3b302-130">For more information about creating security descriptor and authorizing access, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="3b302-131">Пример. Следующая строка SDDL позволяет только администраторам предоставлять события в фильтре.</span><span class="sxs-lookup"><span data-stu-id="3b302-131">Example: The following SDDL string allows only administrators to provide events to the filter.</span></span> <span data-ttu-id="3b302-132">Для предоставления событий требуется право на **\_ \_ публикацию WBEM** (x80).</span><span class="sxs-lookup"><span data-stu-id="3b302-132">The right required to provide events is **WBEM\_RIGHT\_PUBLISH** (x80).</span></span>


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

<span data-ttu-id="3b302-133">**евентнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="3b302-133">**EventNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b302-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3b302-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b302-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b302-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b302-136">Пространство имен экземпляра события, используемого для подписок между пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="3b302-136">Namespace of the event instance used for cross-namespace subscriptions.</span></span>

</dd> <dt>

<span data-ttu-id="3b302-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="3b302-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b302-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3b302-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b302-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b302-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3b302-140">Квалификаторы: [ **ключ**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="3b302-140">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="3b302-141">Уникальный идентификатор фильтра событий.</span><span class="sxs-lookup"><span data-stu-id="3b302-141">Unique identifier of an event filter.</span></span> <span data-ttu-id="3b302-142">Поскольку фильтр событий используется только внутри инструментария WMI, рекомендуется присвоить этому свойству значение глобального уникального идентификатора (**GUID**), преобразованного в строку.</span><span class="sxs-lookup"><span data-stu-id="3b302-142">Because an event filter is only used internally by WMI, it is recommended that you set this property to a globally unique identifier (**GUID**) converted to a string.</span></span> <span data-ttu-id="3b302-143">Однако потребители могут использовать любую закрытую схему для имени фильтра, если нет конфликтов с другими фильтрами.</span><span class="sxs-lookup"><span data-stu-id="3b302-143">However, consumers can use any private scheme for a filter name as long as there is not a conflict with other filters.</span></span>

</dd> <dt>

<span data-ttu-id="3b302-144">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="3b302-144">**Query**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b302-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3b302-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b302-146">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b302-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b302-147">Запрос события языка запросов инструментарий управления Windows (WMI) (WQL), указывающий набор событий для уведомления потребителя и конкретные условия для уведомления.</span><span class="sxs-lookup"><span data-stu-id="3b302-147">Windows Management Instrumentation Query Language (WQL) event query that specifies the set of events for consumer notification, and the specific conditions for notification.</span></span>

</dd> <dt>

<span data-ttu-id="3b302-148">**куерилангуаже**</span><span class="sxs-lookup"><span data-stu-id="3b302-148">**QueryLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b302-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3b302-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b302-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b302-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b302-151">Язык, используемый для запроса.</span><span class="sxs-lookup"><span data-stu-id="3b302-151">Language used for the query.</span></span> <span data-ttu-id="3b302-152">Так как инструментарий WMI в настоящее время поддерживает только язык запросов WMI (WQL) в качестве языка запросов, для этого свойства необходимо задать значение WQL.</span><span class="sxs-lookup"><span data-stu-id="3b302-152">Because WMI currently supports only WMI Query Language (WQL) as a query language, this property must be set to "WQL".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b302-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b302-153">Remarks</span></span>

<span data-ttu-id="3b302-154">Класс **\_ \_ EventFilter** является производным от [**\_ \_ индикатионрелатед**](--indicationrelated.md).</span><span class="sxs-lookup"><span data-stu-id="3b302-154">The **\_\_EventFilter** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3b302-155">Примеры</span><span class="sxs-lookup"><span data-stu-id="3b302-155">Examples</span></span>

<span data-ttu-id="3b302-156">[Процедура создания постоянной регистрации событий WMI для мониторинга файлов](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) в коллекции TechNet использует **\_ \_ EventFilter** в составе сложного сценария для настройки постоянной регистрации событий WMI.</span><span class="sxs-lookup"><span data-stu-id="3b302-156">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_EventFilter** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b302-157">Требования</span><span class="sxs-lookup"><span data-stu-id="3b302-157">Requirements</span></span>



| <span data-ttu-id="3b302-158">Требование</span><span class="sxs-lookup"><span data-stu-id="3b302-158">Requirement</span></span> | <span data-ttu-id="3b302-159">Значение</span><span class="sxs-lookup"><span data-stu-id="3b302-159">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3b302-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b302-160">Minimum supported client</span></span><br/> | <span data-ttu-id="3b302-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b302-161">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3b302-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b302-162">Minimum supported server</span></span><br/> | <span data-ttu-id="3b302-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b302-163">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="3b302-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3b302-164">Namespace</span></span><br/>                | <span data-ttu-id="3b302-165">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="3b302-165">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3b302-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b302-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b302-167">**\_\_индикатионрелатед**</span><span class="sxs-lookup"><span data-stu-id="3b302-167">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="3b302-168">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="3b302-168">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="3b302-169">Создание фильтра событий</span><span class="sxs-lookup"><span data-stu-id="3b302-169">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="3b302-170">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="3b302-170">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="3b302-171">Мониторинг событий и реагирование на них с помощью стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="3b302-171">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="3b302-172">Мониторинг событий</span><span class="sxs-lookup"><span data-stu-id="3b302-172">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="3b302-173">Классы стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="3b302-173">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="3b302-174">Защита событий WMI</span><span class="sxs-lookup"><span data-stu-id="3b302-174">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

