---
description: Логическое представление сетевого порта на сетевом устройстве.
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: Класс CIM_NetworkPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e3ac64b55e17d0526527ebbaca168c3f7b289f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272079"
---
# <a name="cim_networkport-class"></a><span data-ttu-id="92c78-103">\_Класс CIM нетворкпорт</span><span class="sxs-lookup"><span data-stu-id="92c78-103">CIM\_NetworkPort class</span></span>

<span data-ttu-id="92c78-104">Логическое представление сетевого порта на сетевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="92c78-104">A logical representation of a network port on a network device.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92c78-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a><span data-ttu-id="92c78-106">Члены</span><span class="sxs-lookup"><span data-stu-id="92c78-106">Members</span></span>

<span data-ttu-id="92c78-107">Класс **CIM \_ нетворкпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="92c78-107">The **CIM\_NetworkPort** class has these types of members:</span></span>

-   [<span data-ttu-id="92c78-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="92c78-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92c78-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="92c78-109">Properties</span></span>

<span data-ttu-id="92c78-110">Класс **CIM \_ нетворкпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="92c78-110">The **CIM\_NetworkPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92c78-111">**активемаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="92c78-111">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-112">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c78-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c78-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c78-114">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="92c78-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="92c78-115">Активный или согласованный максимальный блок передачи (MTU), поддерживаемый портом.</span><span class="sxs-lookup"><span data-stu-id="92c78-115">The active or negotiated maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> <dt>

<span data-ttu-id="92c78-116">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="92c78-116">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-117">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="92c78-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c78-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c78-119">**значение true** , если порт может автоматически определять скорость или другие характеристики связи подключенного сетевого носителя; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="92c78-119">**true** if the port can automatically determine the speed or other communications characteristic of the attached network media; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="92c78-120">**фуллдуплекс**</span><span class="sxs-lookup"><span data-stu-id="92c78-120">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-121">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="92c78-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c78-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c78-123">**значение true** , если порт работает в режиме полного дуплекса; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="92c78-123">**true** if the port is operating in full duplex mode; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="92c78-124">**линктечнологи**</span><span class="sxs-lookup"><span data-stu-id="92c78-124">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c78-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c78-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c78-127">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ нетворкпорт**.**Осерлинктечнологи**")</span><span class="sxs-lookup"><span data-stu-id="92c78-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**OtherLinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="92c78-128">Технология компоновки, используемая портом.</span><span class="sxs-lookup"><span data-stu-id="92c78-128">The link technology used by the port.</span></span> <span data-ttu-id="92c78-129">Если задано значение "1" (другое), свойство **осерлинктечнологи** содержит описание типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="92c78-129">When set to "1" (other), the **OtherLinkTechnology** property contains a description of the link type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92c78-130">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="92c78-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="92c78-131">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="92c78-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="92c78-132">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="92c78-132">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

<span data-ttu-id="92c78-133">**ГЕО(3** )</span><span class="sxs-lookup"><span data-stu-id="92c78-133">**IB** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

<span data-ttu-id="92c78-134">**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="92c78-134">**FC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="92c78-135">**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="92c78-135">**FDDI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="92c78-136">**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="92c78-136">**ATM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="92c78-137">**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="92c78-137">**Token Ring** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="92c78-138">**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="92c78-138">**Frame Relay** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="92c78-139">**Инфракрасная связь** (9)</span><span class="sxs-lookup"><span data-stu-id="92c78-139">**Infrared** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

<span data-ttu-id="92c78-140">**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="92c78-140">**BlueTooth** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

<span data-ttu-id="92c78-141">**Беспроводная локальная сеть** (11)</span><span class="sxs-lookup"><span data-stu-id="92c78-141">**Wireless LAN** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92c78-142">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="92c78-142">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-143">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="92c78-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="92c78-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c78-145">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -сетевой адаптер 802, порт \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="92c78-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="92c78-146">Массив, содержащий сетевые адреса порта.</span><span class="sxs-lookup"><span data-stu-id="92c78-146">An array that contains the network addresses for the port.</span></span>

</dd> <dt>

<span data-ttu-id="92c78-147">**осерлинктечнологи**</span><span class="sxs-lookup"><span data-stu-id="92c78-147">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92c78-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c78-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c78-150">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ нетворкпорт**.**Линктечнологи**")</span><span class="sxs-lookup"><span data-stu-id="92c78-150">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**LinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="92c78-151">Технология Link, если для **линктечнологи** задано значение "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="92c78-151">The link technology when **LinkTechnology** is set to "1", (other).</span></span>

</dd> <dt>

<span data-ttu-id="92c78-152">**осернетворкпорттипе**</span><span class="sxs-lookup"><span data-stu-id="92c78-152">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92c78-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c78-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c78-155">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ нетворкпорт**.**Осерпорттипе**"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ логикалпорт**](cim-logicalport.md).**PortType**")</span><span class="sxs-lookup"><span data-stu-id="92c78-155">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalPort**](cim-logicalport.md).**PortType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="92c78-156">Нерекомендуемое описание: тип модуля для порта, если свойство **portType** содержит значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="92c78-156">Deprecated description: The module type of the port, when the **PortType** property contains 1 (other).</span></span>

 

<span data-ttu-id="92c78-157">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="92c78-157">This property is deprecated.</span></span> <span data-ttu-id="92c78-158">Вместо этого мы советуем использовать свойство **portType** в классе [**CIM \_ логикалпорт**](cim-logicalport.md) .</span><span class="sxs-lookup"><span data-stu-id="92c78-158">Instead, we recommend the **PortType** property in the [**CIM\_LogicalPort**](cim-logicalport.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="92c78-159">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="92c78-159">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92c78-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c78-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c78-162">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -сетевой адаптер 802, порт \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="92c78-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="92c78-163">Сетевой адрес, жестко закодированный в порт.</span><span class="sxs-lookup"><span data-stu-id="92c78-163">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="92c78-164">Жестко заданный адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="92c78-164">The hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="92c78-165">При внесении этого изменения это свойство следует обновлять одновременно.</span><span class="sxs-lookup"><span data-stu-id="92c78-165">When this change is made, this property should be updated at the same time.</span></span> <span data-ttu-id="92c78-166">Если адрес не существует, **перманентаддресс** должен оставаться пустым.</span><span class="sxs-lookup"><span data-stu-id="92c78-166">**PermanentAddress** should be left blank if the address doesn't exist.</span></span>

</dd> <dt>

<span data-ttu-id="92c78-167">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="92c78-167">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-168">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c78-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c78-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c78-170">Номер порта сетевого порта.</span><span class="sxs-lookup"><span data-stu-id="92c78-170">The port number of the network port.</span></span> <span data-ttu-id="92c78-171">Сетевые порты часто нумеруются относительно логического модуля или сетевого элемента.</span><span class="sxs-lookup"><span data-stu-id="92c78-171">Network ports are often numbered relative to either a logical module or a network element.</span></span>

</dd> <dt>

<span data-ttu-id="92c78-172">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="92c78-172">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-173">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c78-173">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c78-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c78-175">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("скорость"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II. ифспид "," MIF. DMTF \| Network Adapter 802 \| , порт 001,5 "), **Пунит** (" бит/сек ")</span><span class="sxs-lookup"><span data-stu-id="92c78-175">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="92c78-176">Текущая пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="92c78-176">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="92c78-177">Для портов, которые зависят от пропускной способности или для тех, для которых не удается выполнить точную оценку, это свойство должно содержать номинальную пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="92c78-177">For ports that vary in bandwidth, or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="92c78-178">**суппортедмаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="92c78-178">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c78-179">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c78-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c78-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92c78-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c78-181">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="92c78-181">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="92c78-182">Максимальный размер блока передачи (MTU), поддерживаемый портом.</span><span class="sxs-lookup"><span data-stu-id="92c78-182">The maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92c78-183">Требования</span><span class="sxs-lookup"><span data-stu-id="92c78-183">Requirements</span></span>



| <span data-ttu-id="92c78-184">Требование</span><span class="sxs-lookup"><span data-stu-id="92c78-184">Requirement</span></span> | <span data-ttu-id="92c78-185">Значение</span><span class="sxs-lookup"><span data-stu-id="92c78-185">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92c78-186">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92c78-186">Minimum supported client</span></span><br/> | <span data-ttu-id="92c78-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="92c78-187">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="92c78-188">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92c78-188">Minimum supported server</span></span><br/> | <span data-ttu-id="92c78-189">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92c78-189">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="92c78-190">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="92c78-190">Namespace</span></span><br/>                | <span data-ttu-id="92c78-191">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="92c78-191">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="92c78-192">MOF</span><span class="sxs-lookup"><span data-stu-id="92c78-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92c78-193"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92c78-193"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="92c78-194">DLL</span><span class="sxs-lookup"><span data-stu-id="92c78-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92c78-195"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="92c78-195"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="92c78-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92c78-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c78-197">**\_ЛОГИКАЛПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="92c78-197">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> </dl>

 

