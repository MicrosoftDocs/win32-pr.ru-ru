---
description: Класс Снмпнотификатион сопоставляет макрос типа уведомления с инкапсулированным классом CIM.
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: Класс Снмпнотификатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: 89b50d04b435f862a329953f14b47646937a1d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546970"
---
# <a name="snmpnotification-class"></a><span data-ttu-id="e75c3-103">Класс Снмпнотификатион</span><span class="sxs-lookup"><span data-stu-id="e75c3-103">SnmpNotification class</span></span>

<span data-ttu-id="e75c3-104">Класс **снмпнотификатион** СОПОСТАВЛЯЕТ макрос [типа уведомления](notification-type-macro.md) с инкапсулированным классом CIM.</span><span class="sxs-lookup"><span data-stu-id="e75c3-104">The **SnmpNotification** class maps from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class.</span></span> <span data-ttu-id="e75c3-105">Это базовый класс, используемый [поставщиком SNMP](snmp-provider.md) для любого класса, сопоставленного с макросом [типа уведомления](notification-type-macro.md) , с инкапсулированным классом CIM поставщиком SNMP.</span><span class="sxs-lookup"><span data-stu-id="e75c3-105">It is a base class used by the [SNMP Provider](snmp-provider.md) for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class by the SNMP Provider.</span></span>

> [!Note]  
> <span data-ttu-id="e75c3-106">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e75c3-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e75c3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e75c3-107">Syntax</span></span>

``` syntax
class SnmpNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="e75c3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e75c3-108">Members</span></span>

<span data-ttu-id="e75c3-109">Класс **снмпнотификатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e75c3-109">The **SnmpNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="e75c3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e75c3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e75c3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e75c3-111">Properties</span></span>

<span data-ttu-id="e75c3-112">Класс **снмпнотификатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e75c3-112">The **SnmpNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e75c3-113">**ажентаддресс**</span><span class="sxs-lookup"><span data-stu-id="e75c3-113">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e75c3-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e75c3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e75c3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e75c3-116">Сетевой адрес сущности, создавшей уведомление.</span><span class="sxs-lookup"><span data-stu-id="e75c3-116">Network address of the entity that created the notification.</span></span> <span data-ttu-id="e75c3-117">Это фактический адрес устройства.</span><span class="sxs-lookup"><span data-stu-id="e75c3-117">This is the actual address of the device.</span></span> <span data-ttu-id="e75c3-118">Если в сущности управления используется протокол SNMP через UDP, адрес транспорта ссылается на IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e75c3-118">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="e75c3-119">Если в сущности управления используется протокол SNMP через IPX, адрес транспорта устанавливается в **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e75c3-119">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="e75c3-120">Это свойство является допустимым только для в исключительной мере.</span><span class="sxs-lookup"><span data-stu-id="e75c3-120">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="e75c3-121">**аженттранспорт**</span><span class="sxs-lookup"><span data-stu-id="e75c3-121">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e75c3-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e75c3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e75c3-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e75c3-124">Транспортный протокол, используемый отправляющей сущностью.</span><span class="sxs-lookup"><span data-stu-id="e75c3-124">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="e75c3-125">Это свойство допустимо для on и SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="e75c3-125">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="e75c3-126">**аженттранспортаддресс**</span><span class="sxs-lookup"><span data-stu-id="e75c3-126">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e75c3-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e75c3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e75c3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e75c3-129">Сетевой адрес сущности, отправившего уведомление.</span><span class="sxs-lookup"><span data-stu-id="e75c3-129">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="e75c3-130">Это адрес последней сущности, которая перенаправляла уведомление.</span><span class="sxs-lookup"><span data-stu-id="e75c3-130">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="e75c3-131">Если в сущности управления используется протокол SNMP через UDP, адрес транспорта ссылается на IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e75c3-131">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="e75c3-132">Если сущность управления использует SNMP через IPX, адрес транспорта ссылается на IPX-адрес.</span><span class="sxs-lookup"><span data-stu-id="e75c3-132">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="e75c3-133">Это свойство допустимо для on и SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="e75c3-133">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="e75c3-134">**аженттранспортпротокол**</span><span class="sxs-lookup"><span data-stu-id="e75c3-134">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e75c3-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e75c3-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e75c3-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e75c3-137">Транспортный протокол, используемый отправляющей сущностью.</span><span class="sxs-lookup"><span data-stu-id="e75c3-137">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="e75c3-138">**Сообщество**</span><span class="sxs-lookup"><span data-stu-id="e75c3-138">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e75c3-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e75c3-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e75c3-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e75c3-141">Имя сообщества, связанное с экземпляром PDU.</span><span class="sxs-lookup"><span data-stu-id="e75c3-141">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="e75c3-142">Имя сообщества выполняет проверку подлинности инициатора PDU.</span><span class="sxs-lookup"><span data-stu-id="e75c3-142">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="e75c3-143">Это свойство является допустимым для типов и SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="e75c3-143">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="e75c3-144">**Идентификация**</span><span class="sxs-lookup"><span data-stu-id="e75c3-144">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e75c3-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e75c3-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e75c3-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-147">Квалификаторы: **текстовое \_ соглашение** ("OBJECTIDENTIFIER"), **Кодировка** ("OBJECTIDENTIFIER") **, \_ синтаксис объекта** ("OBJECTIDENTIFIER") **, \_ идентификатор объекта** ("1.3.6.1.6.3.1.1.4.1")</span><span class="sxs-lookup"><span data-stu-id="e75c3-147">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="e75c3-148">Удостоверяющая идентификация этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="e75c3-148">Authoritative identification of this notification.</span></span> <span data-ttu-id="e75c3-149">Напрямую сопоставляется с привязкой к переменной Снмптрапоид.</span><span class="sxs-lookup"><span data-stu-id="e75c3-149">Maps directly to the SnmpTrapOID variable binding.</span></span> <span data-ttu-id="e75c3-150">Это свойство допустимо только для SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="e75c3-150">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="e75c3-151">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="e75c3-151">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e75c3-152">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e75c3-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e75c3-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e75c3-154">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="e75c3-154">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="e75c3-155">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="e75c3-155">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="e75c3-156">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e75c3-156">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e75c3-157">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="e75c3-157">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e75c3-158">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e75c3-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e75c3-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e75c3-160">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="e75c3-160">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="e75c3-161">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="e75c3-161">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="e75c3-162">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="e75c3-162">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="e75c3-163">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="e75c3-163">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="e75c3-164">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e75c3-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e75c3-165">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="e75c3-165">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e75c3-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e75c3-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e75c3-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e75c3-168">Квалификаторы: **текстовое \_ соглашение** ("значение TIMETICKS"), **Кодировка** ("значение TIMETICKS") **, \_ синтаксис объекта** ("значение TIMETICKS") **, \_ идентификатор объекта** ("1.3.6.1.2.1.1.3")</span><span class="sxs-lookup"><span data-stu-id="e75c3-168">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="e75c3-169">Время в сотых долях секунды с момента последней повторной инициализации части управления сетью агента.</span><span class="sxs-lookup"><span data-stu-id="e75c3-169">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="e75c3-170">Переменная MIB Сисуптиме. 0, которая имеет тип **INTEGER32**.</span><span class="sxs-lookup"><span data-stu-id="e75c3-170">MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="e75c3-171">Это свойство сопоставляется с **меткой времени** свойства класса CIM, которая относится к типу **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="e75c3-171">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="e75c3-172">Это свойство допустимо только для SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="e75c3-172">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e75c3-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e75c3-173">Remarks</span></span>

<span data-ttu-id="e75c3-174">Макрос [типа уведомления](notification-type-macro.md) , содержащий ссылки на макрос [типа объекта](object-type-macro.md) с именем **timestamp** или **Identification** , приводит к конфликту сопоставления.</span><span class="sxs-lookup"><span data-stu-id="e75c3-174">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="e75c3-175">В случае возникновения этого конфликта требуемые свойства имеют приоритет, и конфликтующие ссылки должны быть переименованы.</span><span class="sxs-lookup"><span data-stu-id="e75c3-175">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="e75c3-176">Макрос [типа уведомления](notification-type-macro.md) , содержащий ссылки на макрос [типа объекта](object-type-macro.md) с именем **Community** , вызывает конфликт сопоставления.</span><span class="sxs-lookup"><span data-stu-id="e75c3-176">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="e75c3-177">В случае возникновения этого конфликта требуемые свойства имеют приоритет, и конфликтующие ссылки должны быть переименованы.</span><span class="sxs-lookup"><span data-stu-id="e75c3-177">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e75c3-178">Требования</span><span class="sxs-lookup"><span data-stu-id="e75c3-178">Requirements</span></span>



| <span data-ttu-id="e75c3-179">Требование</span><span class="sxs-lookup"><span data-stu-id="e75c3-179">Requirement</span></span> | <span data-ttu-id="e75c3-180">Значение</span><span class="sxs-lookup"><span data-stu-id="e75c3-180">Value</span></span> |
|-------------------------------------|----------------------------------|
| <span data-ttu-id="e75c3-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e75c3-181">Minimum supported client</span></span><br/> | <span data-ttu-id="e75c3-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e75c3-182">Windows Vista</span></span><br/>         |
| <span data-ttu-id="e75c3-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e75c3-183">Minimum supported server</span></span><br/> | <span data-ttu-id="e75c3-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e75c3-184">Windows Server 2008</span></span><br/>   |
| <span data-ttu-id="e75c3-185">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e75c3-185">Namespace</span></span><br/>                | <span data-ttu-id="e75c3-186">Корневой узел \\ \\ localhost SNMP</span><span class="sxs-lookup"><span data-stu-id="e75c3-186">Root\\snmp\\localhost</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e75c3-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e75c3-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e75c3-188">**\_\_екстринсицевент**</span><span class="sxs-lookup"><span data-stu-id="e75c3-188">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="e75c3-189">Макрос типа уведомления</span><span class="sxs-lookup"><span data-stu-id="e75c3-189">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

