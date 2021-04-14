---
description: Класс Win32 \_ сетевого адаптера является устаревшим. \_Вместо этого используйте класс MSFT NetAdapter. Класс Win32 \_ нетворкадаптервми представляет сетевой адаптер компьютера, работающего под управлением операционной системы Windows.
ms.assetid: f79cb2a1-a249-479d-a495-37a44fdea995
ms.tgt_platform: multiple
title: Класс Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter
- Win32_NetworkAdapter.Reset
- Win32_NetworkAdapter.SetPowerState
- Win32_NetworkAdapter.AdapterType
- Win32_NetworkAdapter.AdapterTypeID
- Win32_NetworkAdapter.AutoSense
- Win32_NetworkAdapter.Availability
- Win32_NetworkAdapter.Caption
- Win32_NetworkAdapter.ConfigManagerErrorCode
- Win32_NetworkAdapter.ConfigManagerUserConfig
- Win32_NetworkAdapter.CreationClassName
- Win32_NetworkAdapter.Description
- Win32_NetworkAdapter.DeviceID
- Win32_NetworkAdapter.ErrorCleared
- Win32_NetworkAdapter.ErrorDescription
- Win32_NetworkAdapter.GUID
- Win32_NetworkAdapter.Index
- Win32_NetworkAdapter.InstallDate
- Win32_NetworkAdapter.Installed
- Win32_NetworkAdapter.InterfaceIndex
- Win32_NetworkAdapter.LastErrorCode
- Win32_NetworkAdapter.MACAddress
- Win32_NetworkAdapter.Manufacturer
- Win32_NetworkAdapter.MaxNumberControlled
- Win32_NetworkAdapter.MaxSpeed
- Win32_NetworkAdapter.Name
- Win32_NetworkAdapter.NetConnectionID
- Win32_NetworkAdapter.NetConnectionStatus
- Win32_NetworkAdapter.NetEnabled
- Win32_NetworkAdapter.NetworkAddresses
- Win32_NetworkAdapter.PermanentAddress
- Win32_NetworkAdapter.PhysicalAdapter
- Win32_NetworkAdapter.PNPDeviceID
- Win32_NetworkAdapter.PowerManagementCapabilities
- Win32_NetworkAdapter.PowerManagementSupported
- Win32_NetworkAdapter.ProductName
- Win32_NetworkAdapter.ServiceName
- Win32_NetworkAdapter.Speed
- Win32_NetworkAdapter.Status
- Win32_NetworkAdapter.StatusInfo
- Win32_NetworkAdapter.SystemCreationClassName
- Win32_NetworkAdapter.SystemName
- Win32_NetworkAdapter.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 22718802370995cc0515e3f63e731cc86d37eb0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496602"
---
# <a name="win32_networkadapter-class"></a><span data-ttu-id="13a6d-105">\_Класс Win32 сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="13a6d-105">Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="13a6d-106">Класс **Win32 \_ сетевого адаптера** является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="13a6d-106">The **Win32\_NetworkAdapter** class is deprecated.</span></span> <span data-ttu-id="13a6d-107">Вместо этого используйте класс [**MSFT \_ NetAdapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="13a6d-107">Use the [**MSFT\_NetAdapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) class instead.</span></span> <span data-ttu-id="13a6d-108">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ сетевого адаптера для Win32** представляет сетевой адаптер компьютера, работающего под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="13a6d-108">The **Win32\_NetworkAdapter**[WMI class](../wmisdk/retrieving-a-class.md) represents a network adapter of a computer running a Windows operating system.</span></span>

<span data-ttu-id="13a6d-109">**Win32 \_ Сетевого адаптера** предоставляет только данные IPv4.</span><span class="sxs-lookup"><span data-stu-id="13a6d-109">**Win32\_NetworkAdapter** only supplies IPv4 data.</span></span> <span data-ttu-id="13a6d-110">Дополнительные сведения см. [в разделе Поддержка IPv6 и IPv4 в WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-110">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="13a6d-111">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="13a6d-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="13a6d-112">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="13a6d-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a6d-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13a6d-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapter : CIM_NetworkAdapter
{
  string   AdapterType;
  uint16   AdapterTypeID;
  boolean  AutoSense;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   GUID;
  uint32   Index;
  datetime InstallDate;
  boolean  Installed;
  uint32   InterfaceIndex;
  uint32   LastErrorCode;
  string   MACAddress;
  string   Manufacturer;
  uint32   MaxNumberControlled;
  uint64   MaxSpeed;
  string   Name;
  string   NetConnectionID;
  uint16   NetConnectionStatus;
  boolean  NetEnabled;
  string   NetworkAddresses[];
  string   PermanentAddress;
  boolean  PhysicalAdapter;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   ServiceName;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="13a6d-114">Члены</span><span class="sxs-lookup"><span data-stu-id="13a6d-114">Members</span></span>

<span data-ttu-id="13a6d-115">Класс **Win32 \_ сетевого адаптера** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="13a6d-115">The **Win32\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="13a6d-116">Методы</span><span class="sxs-lookup"><span data-stu-id="13a6d-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="13a6d-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="13a6d-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="13a6d-118">Методы</span><span class="sxs-lookup"><span data-stu-id="13a6d-118">Methods</span></span>

<span data-ttu-id="13a6d-119">Класс **Win32 \_ сетевого адаптера** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="13a6d-119">The **Win32\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="13a6d-120">Метод</span><span class="sxs-lookup"><span data-stu-id="13a6d-120">Method</span></span>                                                          | <span data-ttu-id="13a6d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="13a6d-121">Description</span></span>                                                                                                                                                                                                                     |
|:----------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13a6d-122">**Отключить**</span><span class="sxs-lookup"><span data-stu-id="13a6d-122">**Disable**</span></span>](disable-method-in-class-win32-networkadapter.md) | <span data-ttu-id="13a6d-123">Отключает сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="13a6d-123">Disables the network adapter.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="13a6d-124">**Включить**</span><span class="sxs-lookup"><span data-stu-id="13a6d-124">**Enable**</span></span>](enable-method-in-class-win32-networkadapter.md)   | <span data-ttu-id="13a6d-125">Включает сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="13a6d-125">Enables the network adapter.</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="13a6d-126">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="13a6d-126">**Reset**</span></span>                                                       | <span data-ttu-id="13a6d-127">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="13a6d-127">Not implemented.</span></span> <span data-ttu-id="13a6d-128">Дополнительные сведения о том, как реализовать этот метод, см. в описании метода [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ сетевого адаптера**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-128">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/>                 |
| <span data-ttu-id="13a6d-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="13a6d-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="13a6d-130">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="13a6d-130">Not implemented.</span></span> <span data-ttu-id="13a6d-131">Дополнительные сведения о том, как реализовать этот метод, см. в описании метода [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ сетевого адаптера**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-131">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="13a6d-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="13a6d-132">Properties</span></span>

<span data-ttu-id="13a6d-133">Класс **Win32 \_ сетевого адаптера** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="13a6d-133">The **Win32\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13a6d-134">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="13a6d-134">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-137">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ , \_ \_ \_ используемый для генерации носителя](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="13a6d-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-138">Сетевой носитель используется.</span><span class="sxs-lookup"><span data-stu-id="13a6d-138">Network medium in use.</span></span> <span data-ttu-id="13a6d-139">Используются следующие сетевые адаптеры:</span><span class="sxs-lookup"><span data-stu-id="13a6d-139">The network adapters are as follows:</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="13a6d-140">**Ethernet 802,3** ("ethernet, 802,3")</span><span class="sxs-lookup"><span data-stu-id="13a6d-140">**Ethernet 802.3** ("Ethernet 802.3")</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="13a6d-141">**Token ring 802,5** («token Ring 802,5»)</span><span class="sxs-lookup"><span data-stu-id="13a6d-141">**Token Ring 802.5** ("Token Ring 802.5")</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="13a6d-142">**Оптоволоконный интерфейс распределенных данных (FDDI)** («оптоволоконный интерфейс распределенных данных» (FDDI))</span><span class="sxs-lookup"><span data-stu-id="13a6d-142">**Fiber Distributed Data Interface (FDDI)** ("Fiber Distributed Data Interface (FDDI)")</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="13a6d-143">Глобальная **сеть (WAN** ) (Глобальная сеть (WAN))</span><span class="sxs-lookup"><span data-stu-id="13a6d-143">**Wide Area Network (WAN)** ("Wide Area Network (WAN)")</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="13a6d-144">**LocalTalk** ("LocalTalk")</span><span class="sxs-lookup"><span data-stu-id="13a6d-144">**LocalTalk** ("LocalTalk")</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="13a6d-145">**Ethernet с использованием формата заголовка Dix** ("Ethernet с использованием формата заголовка Dix")</span><span class="sxs-lookup"><span data-stu-id="13a6d-145">**Ethernet using DIX header format** ("Ethernet using DIX header format")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="13a6d-146">**АркНет** ("АркНет")</span><span class="sxs-lookup"><span data-stu-id="13a6d-146">**ARCNET** ("ARCNET")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="13a6d-147">**АркНет (878,2)** ("аркнет (878,2)")</span><span class="sxs-lookup"><span data-stu-id="13a6d-147">**ARCNET (878.2)** ("ARCNET (878.2)")</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="13a6d-148">**ATM** ("ATM")</span><span class="sxs-lookup"><span data-stu-id="13a6d-148">**ATM** ("ATM")</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="13a6d-149">**Беспроводная связь** (беспроводной)</span><span class="sxs-lookup"><span data-stu-id="13a6d-149">**Wireless** ("Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="13a6d-150">**Инфракрасная** связь ("Инфракрасная связь")</span><span class="sxs-lookup"><span data-stu-id="13a6d-150">**Infrared Wireless** ("Infrared Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="13a6d-151">**Бит** /канал (бит/канал)</span><span class="sxs-lookup"><span data-stu-id="13a6d-151">**Bpc** ("Bpc")</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="13a6d-152">**Кован** ("Кован")</span><span class="sxs-lookup"><span data-stu-id="13a6d-152">**CoWan** ("CoWan")</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="13a6d-153">**1394** ("1394")</span><span class="sxs-lookup"><span data-stu-id="13a6d-153">**1394** ("1394")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13a6d-154">**адаптертипеид**</span><span class="sxs-lookup"><span data-stu-id="13a6d-154">**AdapterTypeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-155">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13a6d-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-157">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ , \_ \_ \_ используемый для генерации носителя](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="13a6d-157">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-158">Сетевой носитель используется.</span><span class="sxs-lookup"><span data-stu-id="13a6d-158">Network medium in use.</span></span> <span data-ttu-id="13a6d-159">Возвращает те же сведения, что и свойство **адаптертипе** , за исключением того, что сведения представлены в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="13a6d-159">Returns the same information as the **AdapterType** property, except that the information is in the form of an integer.</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="13a6d-160">**Ethernet 802,3** (0)</span><span class="sxs-lookup"><span data-stu-id="13a6d-160">**Ethernet 802.3** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="13a6d-161">**Token Ring 802,5** (1)</span><span class="sxs-lookup"><span data-stu-id="13a6d-161">**Token Ring 802.5** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="13a6d-162">**Оптоволоконный интерфейс распределенных данных (FDDI)** (2)</span><span class="sxs-lookup"><span data-stu-id="13a6d-162">**Fiber Distributed Data Interface (FDDI)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="13a6d-163">**Глобальная сеть (WAN)** (3)</span><span class="sxs-lookup"><span data-stu-id="13a6d-163">**Wide Area Network (WAN)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="13a6d-164">**LocalTalk** (4)</span><span class="sxs-lookup"><span data-stu-id="13a6d-164">**LocalTalk** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="13a6d-165">**Ethernet с использованием формата заголовка Dix** (5)</span><span class="sxs-lookup"><span data-stu-id="13a6d-165">**Ethernet using DIX header format** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="13a6d-166">**АркНет** (6)</span><span class="sxs-lookup"><span data-stu-id="13a6d-166">**ARCNET** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="13a6d-167">**АркНет (878,2)** (7)</span><span class="sxs-lookup"><span data-stu-id="13a6d-167">**ARCNET (878.2)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="13a6d-168">**ATM** (8)</span><span class="sxs-lookup"><span data-stu-id="13a6d-168">**ATM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="13a6d-169">**Беспроводная связь** (9)</span><span class="sxs-lookup"><span data-stu-id="13a6d-169">**Wireless** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="13a6d-170">**Инфракрасная** связь (10)</span><span class="sxs-lookup"><span data-stu-id="13a6d-170">**Infrared Wireless** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="13a6d-171">**Бит на канал** (11)</span><span class="sxs-lookup"><span data-stu-id="13a6d-171">**Bpc** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="13a6d-172">**Кован** (12)</span><span class="sxs-lookup"><span data-stu-id="13a6d-172">**CoWan** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="13a6d-173">**1394** (13)</span><span class="sxs-lookup"><span data-stu-id="13a6d-173">**1394** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13a6d-174">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="13a6d-174">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-175">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="13a6d-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-177">Если **значение — true**, сетевой адаптер может автоматически определять скорость подключения к подключенному или сетевому носителю.</span><span class="sxs-lookup"><span data-stu-id="13a6d-177">If **True**, the network adapter can automatically determine the speed of the attached or network media.</span></span>

<span data-ttu-id="13a6d-178">Это свойство наследуется от [**CIM \_ сетевого адаптера**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-178">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="13a6d-179">Это свойство еще не реализовано.</span><span class="sxs-lookup"><span data-stu-id="13a6d-179">This property has not been implemented yet.</span></span> <span data-ttu-id="13a6d-180">По умолчанию он возвращает значение **null** .</span><span class="sxs-lookup"><span data-stu-id="13a6d-180">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-181">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="13a6d-181">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-182">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13a6d-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-184">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="13a6d-184">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-185">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="13a6d-185">Availability and status of the device.</span></span>

<span data-ttu-id="13a6d-186">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13a6d-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="13a6d-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13a6d-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="13a6d-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="13a6d-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="13a6d-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-190">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="13a6d-190">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="13a6d-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="13a6d-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="13a6d-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="13a6d-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="13a6d-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="13a6d-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="13a6d-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="13a6d-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="13a6d-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="13a6d-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="13a6d-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="13a6d-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="13a6d-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="13a6d-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="13a6d-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="13a6d-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="13a6d-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="13a6d-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="13a6d-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="13a6d-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-201">Известно, что устройство находится в состоянии энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="13a6d-201">The device is known to be in a power save state, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="13a6d-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="13a6d-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-203">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="13a6d-203">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="13a6d-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="13a6d-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-205">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="13a6d-205">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="13a6d-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="13a6d-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="13a6d-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="13a6d-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-208">Устройство находится в состоянии предупреждения, но также в состоянии энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="13a6d-208">The device is in a warning state, though also in a power save state.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="13a6d-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="13a6d-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-210">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="13a6d-210">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="13a6d-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="13a6d-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-212">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="13a6d-212">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="13a6d-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="13a6d-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-214">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="13a6d-214">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="13a6d-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="13a6d-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-216">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="13a6d-216">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13a6d-217">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="13a6d-217">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-220">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="13a6d-220">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-221">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="13a6d-221">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="13a6d-222">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-223">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="13a6d-223">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-224">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-226">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="13a6d-226">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-227">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="13a6d-227">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="13a6d-228">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-228">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="13a6d-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="13a6d-230"> (0)</span><span class="sxs-lookup"><span data-stu-id="13a6d-230">(0)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-231">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="13a6d-231">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="13a6d-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="13a6d-233">(1)</span><span class="sxs-lookup"><span data-stu-id="13a6d-233">(1)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-234">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="13a6d-234">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="13a6d-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="13a6d-236">(2)</span><span class="sxs-lookup"><span data-stu-id="13a6d-236">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="13a6d-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="13a6d-238">(3)</span><span class="sxs-lookup"><span data-stu-id="13a6d-238">(3)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-239">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13a6d-239">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="13a6d-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="13a6d-241">(4)</span><span class="sxs-lookup"><span data-stu-id="13a6d-241">(4)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-242">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="13a6d-242">Device is not working properly.</span></span> <span data-ttu-id="13a6d-243">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="13a6d-243">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="13a6d-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="13a6d-245">(5)</span><span class="sxs-lookup"><span data-stu-id="13a6d-245">(5)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-246">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="13a6d-246">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="13a6d-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="13a6d-248"> (6)</span><span class="sxs-lookup"><span data-stu-id="13a6d-248">(6)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-249">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="13a6d-249">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="13a6d-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="13a6d-251">(7)</span><span class="sxs-lookup"><span data-stu-id="13a6d-251">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="13a6d-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="13a6d-253">(8)</span><span class="sxs-lookup"><span data-stu-id="13a6d-253">(8)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-254">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="13a6d-254">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="13a6d-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="13a6d-256">(9)</span><span class="sxs-lookup"><span data-stu-id="13a6d-256">(9)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-257">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="13a6d-257">Device is not working properly.</span></span> <span data-ttu-id="13a6d-258">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="13a6d-258">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="13a6d-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="13a6d-260">(10)</span><span class="sxs-lookup"><span data-stu-id="13a6d-260">(10)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-261">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="13a6d-261">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="13a6d-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="13a6d-263">(11)</span><span class="sxs-lookup"><span data-stu-id="13a6d-263">(11)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-264">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="13a6d-264">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="13a6d-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="13a6d-266">(12)</span><span class="sxs-lookup"><span data-stu-id="13a6d-266">(12)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-267">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="13a6d-267">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="13a6d-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="13a6d-269">(13)</span><span class="sxs-lookup"><span data-stu-id="13a6d-269">(13)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-270">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="13a6d-270">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="13a6d-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="13a6d-272">(14)</span><span class="sxs-lookup"><span data-stu-id="13a6d-272">(14)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-273">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="13a6d-273">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="13a6d-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="13a6d-275">(15)</span><span class="sxs-lookup"><span data-stu-id="13a6d-275">(15)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-276">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="13a6d-276">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="13a6d-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="13a6d-278">(16)</span><span class="sxs-lookup"><span data-stu-id="13a6d-278">(16)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-279">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="13a6d-279">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="13a6d-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="13a6d-281">(17)</span><span class="sxs-lookup"><span data-stu-id="13a6d-281">(17)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-282">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="13a6d-282">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="13a6d-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="13a6d-284">(18)</span><span class="sxs-lookup"><span data-stu-id="13a6d-284">(18)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-285">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="13a6d-285">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="13a6d-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="13a6d-287">(19)</span><span class="sxs-lookup"><span data-stu-id="13a6d-287">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="13a6d-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="13a6d-289">(20)</span><span class="sxs-lookup"><span data-stu-id="13a6d-289">(20)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-290">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="13a6d-290">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="13a6d-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="13a6d-292">(21)</span><span class="sxs-lookup"><span data-stu-id="13a6d-292">(21)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-293">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="13a6d-293">System failure.</span></span> <span data-ttu-id="13a6d-294">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="13a6d-294">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="13a6d-295">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="13a6d-295">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="13a6d-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="13a6d-297">(22)</span><span class="sxs-lookup"><span data-stu-id="13a6d-297">(22)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-298">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="13a6d-298">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="13a6d-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="13a6d-300">(23)</span><span class="sxs-lookup"><span data-stu-id="13a6d-300">(23)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-301">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="13a6d-301">System failure.</span></span> <span data-ttu-id="13a6d-302">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="13a6d-302">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="13a6d-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="13a6d-304">(24)</span><span class="sxs-lookup"><span data-stu-id="13a6d-304">(24)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-305">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="13a6d-305">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="13a6d-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="13a6d-307">(25)</span><span class="sxs-lookup"><span data-stu-id="13a6d-307">(25)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-308">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="13a6d-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="13a6d-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="13a6d-310">(26)</span><span class="sxs-lookup"><span data-stu-id="13a6d-310">(26)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-311">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="13a6d-311">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="13a6d-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="13a6d-313">(27)</span><span class="sxs-lookup"><span data-stu-id="13a6d-313">(27)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-314">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="13a6d-314">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="13a6d-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="13a6d-316">(28)</span><span class="sxs-lookup"><span data-stu-id="13a6d-316">(28)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-317">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="13a6d-317">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="13a6d-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="13a6d-319">(29)</span><span class="sxs-lookup"><span data-stu-id="13a6d-319">(29)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-320">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="13a6d-320">Device is disabled.</span></span> <span data-ttu-id="13a6d-321">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="13a6d-321">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="13a6d-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="13a6d-323">(30)</span><span class="sxs-lookup"><span data-stu-id="13a6d-323">(30)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-324">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="13a6d-324">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="13a6d-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="13a6d-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="13a6d-326">1-31</span><span class="sxs-lookup"><span data-stu-id="13a6d-326">(31)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-327">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="13a6d-327">Device is not working properly.</span></span> <span data-ttu-id="13a6d-328">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="13a6d-328">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13a6d-329">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="13a6d-329">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-330">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="13a6d-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-332">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="13a6d-332">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-333">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="13a6d-333">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="13a6d-334">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-335">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13a6d-335">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-336">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-338">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="13a6d-338">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-339">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="13a6d-339">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="13a6d-340">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="13a6d-340">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="13a6d-341">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-342">**Описание**</span><span class="sxs-lookup"><span data-stu-id="13a6d-342">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-343">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-345">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="13a6d-345">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-346">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="13a6d-346">Description of the object.</span></span>

<span data-ttu-id="13a6d-347">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-348">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="13a6d-348">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-351">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="13a6d-351">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-352">Уникальный идентификатор сетевого адаптера с других устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="13a6d-352">Unique identifier of the network adapter from other devices on the system.</span></span>

<span data-ttu-id="13a6d-353">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-354">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="13a6d-354">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-355">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="13a6d-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-357">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="13a6d-357">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="13a6d-358">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-359">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="13a6d-359">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-362">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="13a6d-362">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="13a6d-363">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-364">**GUID**</span><span class="sxs-lookup"><span data-stu-id="13a6d-364">**GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-365">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-367">Глобальный уникальный идентификатор соединения.</span><span class="sxs-lookup"><span data-stu-id="13a6d-367">Globally unique identifier for the connection.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-368">**Index**</span><span class="sxs-lookup"><span data-stu-id="13a6d-368">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-369">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-371">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ класс управления Win32Registry системы CurrentControlSet \\ \\ \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="13a6d-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-372">Номер индекса сетевого адаптера, хранящегося в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="13a6d-372">Index number of the network adapter, stored in the system registry.</span></span>

<span data-ttu-id="13a6d-373">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="13a6d-373">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-374">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="13a6d-374">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-375">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13a6d-375">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-377">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="13a6d-377">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-378">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="13a6d-378">Date and time the object was installed.</span></span> <span data-ttu-id="13a6d-379">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="13a6d-379">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="13a6d-380">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="13a6d-381">Это свойство еще не реализовано.</span><span class="sxs-lookup"><span data-stu-id="13a6d-381">This property has not been implemented yet.</span></span> <span data-ttu-id="13a6d-382">По умолчанию он возвращает значение **null** .</span><span class="sxs-lookup"><span data-stu-id="13a6d-382">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-383">**Установлено**</span><span class="sxs-lookup"><span data-stu-id="13a6d-383">**Installed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-384">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="13a6d-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-386">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WIN32REGISTRY \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ нетворккардс \| дривердате")</span><span class="sxs-lookup"><span data-stu-id="13a6d-386">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-387">Если **значение — true**, сетевой адаптер устанавливается в системе.</span><span class="sxs-lookup"><span data-stu-id="13a6d-387">If **True**, the network adapter is installed in the system.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-388">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="13a6d-388">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-389">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-391">Значение индекса, уникально идентифицирующего локальный сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="13a6d-391">Index value that uniquely identifies the local network interface.</span></span> <span data-ttu-id="13a6d-392">Значение этого свойства совпадает со значением свойства **InterfaceIndex** в экземпляре [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) , представляющем сетевой интерфейс в таблице маршрутов.</span><span class="sxs-lookup"><span data-stu-id="13a6d-392">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-393">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="13a6d-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-394">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-396">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="13a6d-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="13a6d-397">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-398">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="13a6d-398">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-399">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-401">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| входные и выходные функции устройства Win32API \| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span><span class="sxs-lookup"><span data-stu-id="13a6d-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-402">Адрес управления доступом к носителю для этого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="13a6d-402">Media access control address for this network adapter.</span></span> <span data-ttu-id="13a6d-403">MAC-адрес — это уникальный номер в 48 бит, назначенный сетевому адаптеру производителем.</span><span class="sxs-lookup"><span data-stu-id="13a6d-403">A MAC address is a unique 48-bit number assigned to the network adapter by the manufacturer.</span></span> <span data-ttu-id="13a6d-404">Он однозначно определяет этот сетевой адаптер и используется для сопоставления сетевых соединений TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="13a6d-404">It uniquely identifies this network adapter and is used for mapping TCP/IP network communications.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-405">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="13a6d-405">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-406">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-408">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ нетворккардс \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="13a6d-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-409">Имя производителя сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="13a6d-409">Name of the network adapter's manufacturer.</span></span>

<span data-ttu-id="13a6d-410">Пример: "3COM"</span><span class="sxs-lookup"><span data-stu-id="13a6d-410">Example: "3COM"</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-411">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="13a6d-411">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-412">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-414">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,9 \| Максимальное количество вложений ")</span><span class="sxs-lookup"><span data-stu-id="13a6d-414">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9\|Maximum Number of Attachments")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-415">Максимальное число напрямую обрабатываемых портов, поддерживаемых этим сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="13a6d-415">Maximum number of directly addressable ports supported by this network adapter.</span></span> <span data-ttu-id="13a6d-416">Если число неизвестно, следует использовать значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="13a6d-416">A value of 0 (zero) should be used if the number is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-417">**максспид**</span><span class="sxs-lookup"><span data-stu-id="13a6d-417">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-418">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a6d-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-420">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="13a6d-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-421">Максимальная скорость (в битах в секунду) для сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="13a6d-421">Maximum speed, in bits per second, for the network adapter.</span></span>

<span data-ttu-id="13a6d-422">Это свойство наследуется от [**CIM \_ сетевого адаптера**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-422">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="13a6d-423">Это свойство еще не реализовано.</span><span class="sxs-lookup"><span data-stu-id="13a6d-423">This property has not been implemented yet.</span></span> <span data-ttu-id="13a6d-424">По умолчанию он возвращает значение **null** .</span><span class="sxs-lookup"><span data-stu-id="13a6d-424">It returns a **NULL** value by default.</span></span>

<span data-ttu-id="13a6d-425">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="13a6d-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-426">**Name**</span><span class="sxs-lookup"><span data-stu-id="13a6d-426">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-429">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="13a6d-429">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-430">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="13a6d-430">Label by which the object is known.</span></span> <span data-ttu-id="13a6d-431">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="13a6d-431">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="13a6d-432">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-433">**нетконнектионид**</span><span class="sxs-lookup"><span data-stu-id="13a6d-433">**NetConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-435">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13a6d-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-436">Имя сетевого подключения, отображаемое в программе панели управления " **Сетевые подключения** ".</span><span class="sxs-lookup"><span data-stu-id="13a6d-436">Name of the network connection as it appears in the **Network Connections** Control Panel program.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-437">**нетконнектионстатус**</span><span class="sxs-lookup"><span data-stu-id="13a6d-437">**NetConnectionStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-438">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13a6d-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-439">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-440">Состояние подключения сетевого адаптера к сети.</span><span class="sxs-lookup"><span data-stu-id="13a6d-440">State of the network adapter connection to the network.</span></span>

<dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="13a6d-441">**Отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="13a6d-441">**Disconnected** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="13a6d-442">**Подключение** (1)</span><span class="sxs-lookup"><span data-stu-id="13a6d-442">**Connecting** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="13a6d-443">**Подключено** (2)</span><span class="sxs-lookup"><span data-stu-id="13a6d-443">**Connected** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnecting"></span><span id="disconnecting"></span><span id="DISCONNECTING"></span>

<span data-ttu-id="13a6d-444">**Отсоединение** (3)</span><span class="sxs-lookup"><span data-stu-id="13a6d-444">**Disconnecting** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Not_Present"></span><span id="hardware_not_present"></span><span id="HARDWARE_NOT_PRESENT"></span>

<span data-ttu-id="13a6d-445">**Оборудование отсутствует** (4)</span><span class="sxs-lookup"><span data-stu-id="13a6d-445">**Hardware Not Present** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Disabled"></span><span id="hardware_disabled"></span><span id="HARDWARE_DISABLED"></span>

<span data-ttu-id="13a6d-446">**Оборудование отключено** (5)</span><span class="sxs-lookup"><span data-stu-id="13a6d-446">**Hardware Disabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Malfunction"></span><span id="hardware_malfunction"></span><span id="HARDWARE_MALFUNCTION"></span>

<span data-ttu-id="13a6d-447">**Аппаратный сбой** (6)</span><span class="sxs-lookup"><span data-stu-id="13a6d-447">**Hardware Malfunction** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Disconnected"></span><span id="media_disconnected"></span><span id="MEDIA_DISCONNECTED"></span>

<span data-ttu-id="13a6d-448">**Носитель отключен** (7)</span><span class="sxs-lookup"><span data-stu-id="13a6d-448">**Media Disconnected** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Authenticating"></span><span id="authenticating"></span><span id="AUTHENTICATING"></span>

<span data-ttu-id="13a6d-449">**Проверка подлинности** (8)</span><span class="sxs-lookup"><span data-stu-id="13a6d-449">**Authenticating** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Succeeded"></span><span id="authentication_succeeded"></span><span id="AUTHENTICATION_SUCCEEDED"></span>

<span data-ttu-id="13a6d-450">**Проверка подлинности прошла удачно** (9)</span><span class="sxs-lookup"><span data-stu-id="13a6d-450">**Authentication Succeeded** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failed"></span><span id="authentication_failed"></span><span id="AUTHENTICATION_FAILED"></span>

<span data-ttu-id="13a6d-451">**Ошибка проверки подлинности** (10)</span><span class="sxs-lookup"><span data-stu-id="13a6d-451">**Authentication Failed** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Address"></span><span id="invalid_address"></span><span id="INVALID_ADDRESS"></span>

<span data-ttu-id="13a6d-452">**Недопустимый адрес** (11)</span><span class="sxs-lookup"><span data-stu-id="13a6d-452">**Invalid Address** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Credentials_Required"></span><span id="credentials_required"></span><span id="CREDENTIALS_REQUIRED"></span>

<span data-ttu-id="13a6d-453">**Требуются учетные данные** (12)</span><span class="sxs-lookup"><span data-stu-id="13a6d-453">**Credentials Required** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13a6d-454">**Другое**</span><span class="sxs-lookup"><span data-stu-id="13a6d-454">**Other**</span></span>


</dt> <dd><span data-ttu-id="13a6d-455">13 – 65535</span><span class="sxs-lookup"><span data-stu-id="13a6d-455">13–65535</span></span></dd> </dl>

</dd> <dt>

<span data-ttu-id="13a6d-456">**NetEnabled**</span><span class="sxs-lookup"><span data-stu-id="13a6d-456">**NetEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-457">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="13a6d-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-458">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-459">Указывает, включен ли адаптер.</span><span class="sxs-lookup"><span data-stu-id="13a6d-459">Indicates whether the adapter is enabled or not.</span></span> <span data-ttu-id="13a6d-460">Если **значение равно true**, адаптер включен.</span><span class="sxs-lookup"><span data-stu-id="13a6d-460">If **True**, the adapter is enabled.</span></span> <span data-ttu-id="13a6d-461">Включить или отключить сетевую карту можно с помощью методов [**включения**](enable-method-in-class-win32-networkadapter.md) и [**отключения**](disable-method-in-class-win32-networkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="13a6d-461">You can enable or disable the NIC by using the [**Enable**](enable-method-in-class-win32-networkadapter.md) and [**Disable**](disable-method-in-class-win32-networkadapter.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-462">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="13a6d-462">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-463">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="13a6d-463">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-464">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-465">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| -сетевой адаптер 802, порт \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="13a6d-465">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-466">Массив сетевых адресов для адаптера.</span><span class="sxs-lookup"><span data-stu-id="13a6d-466">Array of network addresses for an adapter.</span></span>

<span data-ttu-id="13a6d-467">Это свойство наследуется от [**CIM \_ сетевого адаптера**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-467">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="13a6d-468">Это свойство еще не реализовано.</span><span class="sxs-lookup"><span data-stu-id="13a6d-468">This property has not been implemented yet.</span></span> <span data-ttu-id="13a6d-469">По умолчанию он возвращает значение **null** .</span><span class="sxs-lookup"><span data-stu-id="13a6d-469">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-470">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="13a6d-470">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-471">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-473">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| -сетевой адаптер 802, порт \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="13a6d-473">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-474">Сетевой адрес жестко закодирован в адаптере.</span><span class="sxs-lookup"><span data-stu-id="13a6d-474">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="13a6d-475">Этот жестко заданный адрес может быть изменен с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="13a6d-475">This hard-coded address may be changed by firmware upgrade or software configuration.</span></span> <span data-ttu-id="13a6d-476">Если это так, это поле следует обновлять после внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="13a6d-476">If so, this field should be updated when the change is made.</span></span> <span data-ttu-id="13a6d-477">Если для сетевого адаптера не существует жестко закодированного адреса, свойство должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="13a6d-477">The property should be left blank if no hard-coded address exists for the network adapter.</span></span>

<span data-ttu-id="13a6d-478">Это свойство наследуется от [**CIM \_ сетевого адаптера**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-478">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="13a6d-479">Это свойство еще не реализовано.</span><span class="sxs-lookup"><span data-stu-id="13a6d-479">This property has not been implemented yet.</span></span> <span data-ttu-id="13a6d-480">По умолчанию он возвращает значение **null** .</span><span class="sxs-lookup"><span data-stu-id="13a6d-480">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-481">**фисикаладаптер**</span><span class="sxs-lookup"><span data-stu-id="13a6d-481">**PhysicalAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-482">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="13a6d-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-483">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-484">Указывает, является ли адаптер физическим или логическим.</span><span class="sxs-lookup"><span data-stu-id="13a6d-484">Indicates whether the adapter is a physical or a logical adapter.</span></span> <span data-ttu-id="13a6d-485">Если **значение равно true**, адаптер является физическим.</span><span class="sxs-lookup"><span data-stu-id="13a6d-485">If **True**, the adapter is physical.</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-486">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="13a6d-486">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-488">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-489">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="13a6d-489">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-490">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="13a6d-490">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="13a6d-491">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="13a6d-492">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="13a6d-492">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-493">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="13a6d-493">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-494">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="13a6d-494">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-495">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-496">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="13a6d-496">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="13a6d-497">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13a6d-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="13a6d-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="13a6d-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="13a6d-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="13a6d-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="13a6d-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="13a6d-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="13a6d-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-502">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="13a6d-502">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="13a6d-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="13a6d-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-504">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="13a6d-504">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="13a6d-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="13a6d-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-506">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="13a6d-506">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="13a6d-507">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="13a6d-507">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="13a6d-508">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-508">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="13a6d-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="13a6d-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-510">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="13a6d-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="13a6d-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="13a6d-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="13a6d-512">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="13a6d-512">Timed Power-On Supported</span></span>

<span data-ttu-id="13a6d-513">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="13a6d-513">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13a6d-514">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="13a6d-514">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-515">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="13a6d-515">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-516">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-517">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="13a6d-517">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="13a6d-518">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="13a6d-518">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="13a6d-519">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-519">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-520">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="13a6d-520">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-521">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-522">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-523">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ нетворккардс \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="13a6d-523">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-524">Имя продукта сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="13a6d-524">Product name of the network adapter.</span></span>

<span data-ttu-id="13a6d-525">Пример: "Fast Есерлинк XL"</span><span class="sxs-lookup"><span data-stu-id="13a6d-525">Example: "Fast EtherLink XL"</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-526">**Служба**</span><span class="sxs-lookup"><span data-stu-id="13a6d-526">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-527">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-528">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-529">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ нетворккардс \| ProductName")</span><span class="sxs-lookup"><span data-stu-id="13a6d-529">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ProductName")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-530">Имя службы сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="13a6d-530">Service name of the network adapter.</span></span> <span data-ttu-id="13a6d-531">Обычно это имя короче полного названия продукта.</span><span class="sxs-lookup"><span data-stu-id="13a6d-531">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="13a6d-532">Пример: "Елнкии"</span><span class="sxs-lookup"><span data-stu-id="13a6d-532">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-533">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="13a6d-533">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-534">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a6d-534">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-535">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-535">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-536">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| RFC1213-MIB. ифспид "," MIF. DMTF \| , сетевой адаптер 802 \| , порт 001,5 "), [**единиц**](../wmisdk/standard-qualifiers.md) (" бит в секунду ")</span><span class="sxs-lookup"><span data-stu-id="13a6d-536">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-537">Оценка текущей пропускной способности в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="13a6d-537">Estimate of the current bandwidth in bits per second.</span></span> <span data-ttu-id="13a6d-538">Для конечных точек, которые зависят от пропускной способности или для тех, для которых не может быть выполнена точная оценка, это свойство должно содержать номинальную пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="13a6d-538">For endpoints which vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="13a6d-539">Это свойство наследуется от [**CIM \_ сетевого адаптера**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-539">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="13a6d-540">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="13a6d-540">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-541">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="13a6d-541">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-542">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-543">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-544">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="13a6d-544">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-545">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="13a6d-545">Current status of the object.</span></span> <span data-ttu-id="13a6d-546">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-546">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="13a6d-547">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="13a6d-547">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="13a6d-548">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="13a6d-548">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="13a6d-549">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="13a6d-549">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="13a6d-550">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="13a6d-550">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13a6d-551">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="13a6d-551">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="13a6d-552">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="13a6d-552">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="13a6d-553">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="13a6d-553">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="13a6d-554">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="13a6d-554">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="13a6d-555">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="13a6d-555">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="13a6d-556">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="13a6d-556">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="13a6d-557">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="13a6d-557">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="13a6d-558">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="13a6d-558">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="13a6d-559">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="13a6d-559">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13a6d-560">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="13a6d-560">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-561">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13a6d-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-562">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-563">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="13a6d-563">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-564">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="13a6d-564">State of the logical device.</span></span> <span data-ttu-id="13a6d-565">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="13a6d-565">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="13a6d-566">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-566">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13a6d-567">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="13a6d-567">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13a6d-568">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="13a6d-568">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="13a6d-569">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="13a6d-569">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="13a6d-570">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="13a6d-570">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="13a6d-571">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="13a6d-571">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13a6d-572">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="13a6d-572">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-573">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-573">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-574">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-574">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-575">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="13a6d-575">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-576">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="13a6d-576">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="13a6d-577">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-577">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-578">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="13a6d-578">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-579">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13a6d-579">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-580">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-581">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="13a6d-581">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-582">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="13a6d-582">Name of the scoping system.</span></span>

<span data-ttu-id="13a6d-583">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="13a6d-583">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13a6d-584">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="13a6d-584">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a6d-585">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13a6d-585">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-586">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13a6d-586">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13a6d-587">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("программное обеспечение \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ PerfLib \\ \\ 009 \| системное время")</span><span class="sxs-lookup"><span data-stu-id="13a6d-587">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Perflib\\\\009\|System Up Time")</span></span>
</dt> </dl>

<span data-ttu-id="13a6d-588">Дата и время последнего сброса сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="13a6d-588">Date and time the network adapter was last reset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13a6d-589">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13a6d-589">Remarks</span></span>

<span data-ttu-id="13a6d-590">Класс **Win32 \_ сетевого адаптера** является производным от [**CIM \_ сетевого адаптера**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="13a6d-590">The **Win32\_NetworkAdapter** class is derived from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="13a6d-591">В следующем списке описываются классы соединителей для **Win32 \_ сетевого адаптера**.</span><span class="sxs-lookup"><span data-stu-id="13a6d-591">The following list describes the Associator classes for **Win32\_NetworkAdapter**:</span></span>

-   [<span data-ttu-id="13a6d-592">**\_Пнпентити Win32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-592">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
-   [<span data-ttu-id="13a6d-593">**Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="13a6d-593">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
-   [<span data-ttu-id="13a6d-594">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-594">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
-   [<span data-ttu-id="13a6d-595">**\_Иркресаурце Win32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-595">**Win32\_IRQResource**</span></span>](win32-irqresource.md)
-   [<span data-ttu-id="13a6d-596">**\_Девицемеморяддресс Win32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-596">**Win32\_DeviceMemoryAddress**</span></span>](win32-devicememoryaddress.md)
-   [<span data-ttu-id="13a6d-597">**\_Портресаурце Win32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-597">**Win32\_PortResource**</span></span>](win32-portresource.md)
-   [<span data-ttu-id="13a6d-598">**\_NetworkProtocol Win32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-598">**Win32\_NetworkProtocol**</span></span>](win32-networkprotocol.md)
-   [<span data-ttu-id="13a6d-599">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="13a6d-599">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)

<span data-ttu-id="13a6d-600">На многих системах имеется ряд сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="13a6d-600">Many systems have a number of network adapters on them.</span></span> <span data-ttu-id="13a6d-601">Используйте следующую ссылку для поиска текущих адаптеров:</span><span class="sxs-lookup"><span data-stu-id="13a6d-601">Consider using the following as a reference to find the current adapters:</span></span>

``` syntax
AdapterType: "Ethernet 802.3"
MACAddress: String Length > 16
Availability: 3
PNPDeviceID: InStr ( PNPDeviceID, "PCI") = 1
Installed: vbTrue
ConfigManagerErrorCode: 0
: <keep this as an index to Win32_NetworkAdapterConfiguration>
```

<span data-ttu-id="13a6d-602">Даже используя указанные выше квалификаторы, вы, скорее всего, получите более одного допустимого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="13a6d-602">Even using the above qualifiers, you will likely retrieve more than one valid network adapter.</span></span> <span data-ttu-id="13a6d-603">В этом случае можно использовать следующие сведения, чтобы уточнить поиск в \_ NetworkAdapterConfiguration Win32.</span><span class="sxs-lookup"><span data-stu-id="13a6d-603">If that is the case, Then you can use the following information to further qualify your search of the Win32\_NetworkAdapterConfiguration:</span></span>

``` syntax
Index: <match to DeviceID above>
MACAddress: Length > 16
DefaultIPGateway: String Length > 6
DNSServerSearchOrder: Array of strings with length > 6
IPEnabled: vbTrue
IPAddress: Array of strings with length > 6
```

<span data-ttu-id="13a6d-604">После этого вы, скорее всего, сократите список до одного или двух настроенных адаптеров.</span><span class="sxs-lookup"><span data-stu-id="13a6d-604">Once you have done so, you will likely have reduced your list to one or two configured adapters.</span></span>

<span data-ttu-id="13a6d-605">Для поиска адаптера по умолчанию можно также использовать следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="13a6d-605">You can also use the following procedure to find the default adapter:</span></span>

1.  <span data-ttu-id="13a6d-606">Выполните приведенный ниже запрос:</span><span class="sxs-lookup"><span data-stu-id="13a6d-606">Run the following query:</span></span>

    `"SELECT InterfaceIndex, Destination FROM Win32_IP4RouteTable WHERE Destination='0.0.0.0'"`

    <span data-ttu-id="13a6d-607">У вас должно быть только одно назначение сети по умолчанию 0.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="13a6d-607">You should only have one default network destination 0.0.0.0.</span></span>

2.  <span data-ttu-id="13a6d-608">Используйте **InterfaceIndex** для получения нужного сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="13a6d-608">Use the **InterfaceIndex** to retrieve the Network Adapter you want.</span></span>

    `"SELECT * FROM Win32_NetworkAdapter WHERE InterfaceIndex=" + insertVariableHere`

## <a name="examples"></a><span data-ttu-id="13a6d-609">Примеры</span><span class="sxs-lookup"><span data-stu-id="13a6d-609">Examples</span></span>

<span data-ttu-id="13a6d-610">Два примера кода PowerShell для [функций WMI](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) в коллекции TechNet используют **Win32 \_ сетевого адаптера** для повторного создания командлета Windows [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) .</span><span class="sxs-lookup"><span data-stu-id="13a6d-610">The [Two WMI Functions](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) PowerShell code example in the TechNet Gallery uses **Win32\_NetworkAdapter** to re-create the Windows [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) cmdlet.</span></span>

<span data-ttu-id="13a6d-611">Пример " [Get-компутеринфо-запрос компьютера с локального/удаленного компьютера" (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell в коллекции TechNet использует несколько вызовов оборудования и программного обеспечения, включая **Win32 \_ сетевого адаптера**, для вывода сведений о локальной или удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="13a6d-611">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapter**, to display information about a local or remote system.</span></span>

<span data-ttu-id="13a6d-612">В следующем \# образце кода C используется пространство имен [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) для получения текущих сетевых адаптеров на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="13a6d-612">The following C\# code sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace to retrieve the current network adapters on the local machine.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapter");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
                Console.WriteLine();
            }

            Console.ReadLine();
        }
```



<span data-ttu-id="13a6d-613">В следующем \# примере кода C используется https://msdn.microsoft.com/library/system.management.aspx пространство имен для получения текущих сетевых адаптеров на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="13a6d-613">The following C\# code sample uses https://msdn.microsoft.com/library/system.management.aspx namespace to retrieve the current network adapters on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="13a6d-614"> https://msdn.microsoft.com/library/system.management.aspx содержит исходные классы, используемые для доступа к WMI. Однако они считаются более медленными и обычно не масштабируются, а также их аналоги [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="13a6d-614">https://msdn.microsoft.com/library/system.management.aspx contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapter");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("MACAddress : {0}", m["Description"]);
                Console.WriteLine();
            }
            Console.ReadLine();

        }
```



<span data-ttu-id="13a6d-615">В следующем примере кода VBScript описывается, как получить текущие сетевые адаптеры на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="13a6d-615">The following VBScript code sample describes how to retrieve the current network adapters on the local machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapter")

For Each objItem in colItems 
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo
Next
```



## <a name="requirements"></a><span data-ttu-id="13a6d-616">Требования</span><span class="sxs-lookup"><span data-stu-id="13a6d-616">Requirements</span></span>



| <span data-ttu-id="13a6d-617">Требование</span><span class="sxs-lookup"><span data-stu-id="13a6d-617">Requirement</span></span> | <span data-ttu-id="13a6d-618">Значение</span><span class="sxs-lookup"><span data-stu-id="13a6d-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13a6d-619">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13a6d-619">Minimum supported client</span></span><br/> | <span data-ttu-id="13a6d-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13a6d-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13a6d-621">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13a6d-621">Minimum supported server</span></span><br/> | <span data-ttu-id="13a6d-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13a6d-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13a6d-623">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="13a6d-623">Namespace</span></span><br/>                | <span data-ttu-id="13a6d-624">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="13a6d-624">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13a6d-625">MOF</span><span class="sxs-lookup"><span data-stu-id="13a6d-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13a6d-626"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13a6d-626"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13a6d-627">DLL</span><span class="sxs-lookup"><span data-stu-id="13a6d-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13a6d-628"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13a6d-628"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a6d-629">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13a6d-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a6d-630">**\_Сетевого адаптера CIM**</span><span class="sxs-lookup"><span data-stu-id="13a6d-630">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="13a6d-631">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="13a6d-631">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="13a6d-632">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="13a6d-632">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="13a6d-633">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="13a6d-633">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
