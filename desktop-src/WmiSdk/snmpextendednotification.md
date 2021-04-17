---
description: Класс Снмпекстендеднотификатион является базовым классом для любого класса, сопоставленного с макросом типа уведомления с классом CIM поставщика SNMP.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: Класс Снмпекстендеднотификатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: e21fcc32976c42f41cd33a519e5fa6c684acdfc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711656"
---
# <a name="snmpextendednotification-class"></a><span data-ttu-id="92142-103">Класс Снмпекстендеднотификатион</span><span class="sxs-lookup"><span data-stu-id="92142-103">SnmpExtendedNotification class</span></span>

<span data-ttu-id="92142-104">Класс **снмпекстендеднотификатион** является базовым классом для любого класса, сопоставленного с макросом [типа уведомления](notification-type-macro.md) с классом CIM [поставщика SNMP](snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="92142-104">The **SnmpExtendedNotification** class is the base class for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to a CIM class by the [SNMP Provider](snmp-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="92142-105">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="92142-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="92142-106">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="92142-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="92142-107">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="92142-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="92142-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92142-108">Syntax</span></span>

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
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

## <a name="members"></a><span data-ttu-id="92142-109">Члены</span><span class="sxs-lookup"><span data-stu-id="92142-109">Members</span></span>

<span data-ttu-id="92142-110">Класс **снмпекстендеднотификатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="92142-110">The **SnmpExtendedNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="92142-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="92142-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92142-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="92142-112">Properties</span></span>

<span data-ttu-id="92142-113">Класс **снмпекстендеднотификатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="92142-113">The **SnmpExtendedNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92142-114">**ажентаддресс**</span><span class="sxs-lookup"><span data-stu-id="92142-114">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92142-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92142-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92142-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92142-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92142-117">Сетевой адрес сущности, создавшей уведомление.</span><span class="sxs-lookup"><span data-stu-id="92142-117">Network address of the entity that created the notification.</span></span> <span data-ttu-id="92142-118">Это фактический адрес устройства.</span><span class="sxs-lookup"><span data-stu-id="92142-118">This is the actual address of the device.</span></span> <span data-ttu-id="92142-119">Если в сущности управления используется протокол SNMP через UDP, адрес транспорта ссылается на IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="92142-119">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="92142-120">Если в сущности управления используется протокол SNMP через IPX, адрес транспорта устанавливается в **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="92142-120">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="92142-121">Это свойство является допустимым только для в исключительной мере.</span><span class="sxs-lookup"><span data-stu-id="92142-121">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="92142-122">**аженттранспорт**</span><span class="sxs-lookup"><span data-stu-id="92142-122">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92142-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92142-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92142-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92142-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92142-125">Транспортный протокол, используемый отправляющей сущностью.</span><span class="sxs-lookup"><span data-stu-id="92142-125">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="92142-126">Это свойство допустимо для on и SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="92142-126">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="92142-127">**аженттранспортаддресс**</span><span class="sxs-lookup"><span data-stu-id="92142-127">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92142-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92142-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92142-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92142-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92142-130">Сетевой адрес сущности, отправившего уведомление.</span><span class="sxs-lookup"><span data-stu-id="92142-130">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="92142-131">Это адрес последней сущности, которая перенаправляла уведомление.</span><span class="sxs-lookup"><span data-stu-id="92142-131">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="92142-132">Если в сущности управления используется протокол SNMP через UDP, адрес транспорта ссылается на IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="92142-132">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="92142-133">Если сущность управления использует SNMP через IPX, адрес транспорта ссылается на IPX-адрес.</span><span class="sxs-lookup"><span data-stu-id="92142-133">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="92142-134">Это свойство допустимо для on и SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="92142-134">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="92142-135">**аженттранспортпротокол**</span><span class="sxs-lookup"><span data-stu-id="92142-135">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92142-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92142-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92142-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92142-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92142-138">Транспортный протокол, используемый отправляющей сущностью.</span><span class="sxs-lookup"><span data-stu-id="92142-138">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="92142-139">**Сообщество**</span><span class="sxs-lookup"><span data-stu-id="92142-139">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92142-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92142-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92142-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92142-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92142-142">Имя сообщества, связанное с экземпляром PDU.</span><span class="sxs-lookup"><span data-stu-id="92142-142">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="92142-143">Имя сообщества выполняет проверку подлинности инициатора PDU.</span><span class="sxs-lookup"><span data-stu-id="92142-143">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="92142-144">Это свойство является допустимым для типов и SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="92142-144">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="92142-145">**Идентификация**</span><span class="sxs-lookup"><span data-stu-id="92142-145">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92142-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92142-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92142-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92142-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92142-148">Квалификаторы: **текстовое \_ соглашение** ("OBJECTIDENTIFIER"), **Кодировка** ("OBJECTIDENTIFIER") **, \_ синтаксис объекта** ("OBJECTIDENTIFIER") **, \_ идентификатор объекта** ("1.3.6.1.6.3.1.1.4.1")</span><span class="sxs-lookup"><span data-stu-id="92142-148">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="92142-149">Удостоверяющая идентификация этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="92142-149">Authoritative identification of this notification.</span></span> <span data-ttu-id="92142-150">Сопоставляется непосредственно с записью MIB, привязкой к переменной Снмптрапоид.</span><span class="sxs-lookup"><span data-stu-id="92142-150">Maps directly to the MIB entry SnmpTrapOID variable binding.</span></span> <span data-ttu-id="92142-151">Это свойство допустимо только для SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="92142-151">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="92142-152">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="92142-152">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92142-153">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="92142-153">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="92142-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92142-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92142-155">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="92142-155">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="92142-156">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="92142-156">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="92142-157">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="92142-157">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="92142-158">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="92142-158">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92142-159">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92142-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92142-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92142-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92142-161">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="92142-161">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="92142-162">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="92142-162">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="92142-163">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="92142-163">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="92142-164">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="92142-164">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="92142-165">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="92142-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="92142-166">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="92142-166">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92142-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92142-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92142-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92142-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92142-169">Квалификаторы: **текстовое \_ соглашение** ("значение TIMETICKS"), **Кодировка** ("значение TIMETICKS") **, \_ синтаксис объекта** ("значение TIMETICKS") **, \_ идентификатор объекта** ("1.3.6.1.2.1.1.3")</span><span class="sxs-lookup"><span data-stu-id="92142-169">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="92142-170">Время в сотых долях секунды с момента последней повторной инициализации части управления сетью агента.</span><span class="sxs-lookup"><span data-stu-id="92142-170">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="92142-171">Он сопоставляется с переменной MIB Сисуптиме. 0, которая относится к типу **INTEGER32**.</span><span class="sxs-lookup"><span data-stu-id="92142-171">This maps to the MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="92142-172">Это свойство сопоставляется с **меткой времени** свойства класса CIM, которая относится к типу **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="92142-172">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="92142-173">Это свойство допустимо только для SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="92142-173">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92142-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92142-174">Remarks</span></span>

<span data-ttu-id="92142-175">Макрос [типа уведомления](notification-type-macro.md) , содержащий ссылки на макрос [типа объекта](object-type-macro.md) с именем **timestamp** или **Identification** , приводит к конфликту сопоставления.</span><span class="sxs-lookup"><span data-stu-id="92142-175">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="92142-176">В случае возникновения этого конфликта требуемые свойства имеют приоритет, и конфликтующие ссылки должны быть переименованы.</span><span class="sxs-lookup"><span data-stu-id="92142-176">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="92142-177">Макрос [типа уведомления](notification-type-macro.md) , содержащий ссылки на макрос [типа объекта](object-type-macro.md) с именем **Community** , вызывает конфликт сопоставления.</span><span class="sxs-lookup"><span data-stu-id="92142-177">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="92142-178">В случае возникновения этого конфликта требуемые свойства имеют приоритет, и конфликтующие ссылки должны быть переименованы.</span><span class="sxs-lookup"><span data-stu-id="92142-178">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="92142-179">Требования</span><span class="sxs-lookup"><span data-stu-id="92142-179">Requirements</span></span>



| <span data-ttu-id="92142-180">Требование</span><span class="sxs-lookup"><span data-stu-id="92142-180">Requirement</span></span> | <span data-ttu-id="92142-181">Значение</span><span class="sxs-lookup"><span data-stu-id="92142-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92142-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92142-182">Minimum supported client</span></span><br/> | <span data-ttu-id="92142-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92142-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92142-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92142-184">Minimum supported server</span></span><br/> | <span data-ttu-id="92142-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92142-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92142-186">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="92142-186">Namespace</span></span><br/>                | <span data-ttu-id="92142-187">Корневой \\ \\ Смир SNMP</span><span class="sxs-lookup"><span data-stu-id="92142-187">Root\\snmp\\SMIR</span></span><br/>                                                             |
| <span data-ttu-id="92142-188">MOF</span><span class="sxs-lookup"><span data-stu-id="92142-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92142-189"><dt>Снмпсмир. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92142-189"><dt>SnmpSmiR.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92142-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92142-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92142-191">**\_\_екстринсицевент**</span><span class="sxs-lookup"><span data-stu-id="92142-191">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="92142-192">Макрос типа уведомления</span><span class="sxs-lookup"><span data-stu-id="92142-192">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

