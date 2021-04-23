---
description: Представляет параметры выделения ресурсов управляемого элемента для определенного типа ресурса.
ms.assetid: f27910c7-a88a-4694-80fe-7761945782e0
title: Класс CIM_AllocationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocationCapabilities
- CIM_AllocationCapabilities.ResourceType
- CIM_AllocationCapabilities.OtherResourceType
- CIM_AllocationCapabilities.ResourceSubType
- CIM_AllocationCapabilities.RequestTypesSupported
- CIM_AllocationCapabilities.SharingMode
- CIM_AllocationCapabilities.SupportedAddStates
- CIM_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d022023142b38905067e30a4c1be3b133e49a86f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662149"
---
# <a name="cim_allocationcapabilities-class"></a><span data-ttu-id="2c034-103">\_Класс CIM аллокатионкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="2c034-103">CIM\_AllocationCapabilities class</span></span>

<span data-ttu-id="2c034-104">Представляет параметры выделения ресурсов управляемого элемента для определенного типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c034-104">Represents the resource allocation settings of a managed element for a specific resource type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c034-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c034-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_AllocationCapabilities : CIM_Capabilities
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="2c034-106">Члены</span><span class="sxs-lookup"><span data-stu-id="2c034-106">Members</span></span>

<span data-ttu-id="2c034-107">Класс **CIM \_ аллокатионкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2c034-107">The **CIM\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="2c034-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="2c034-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c034-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="2c034-109">Properties</span></span>

<span data-ttu-id="2c034-110">Класс **CIM \_ аллокатионкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2c034-110">The **CIM\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c034-111">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="2c034-111">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c034-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c034-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c034-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c034-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c034-114">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="2c034-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="2c034-115">Тип ресурса для этого параметра выделения, если свойство **ResourceType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="2c034-115">The resource type for this allocation setting when the **ResourceType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="2c034-116">**рекуесттипессуппортед**</span><span class="sxs-lookup"><span data-stu-id="2c034-116">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c034-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c034-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c034-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c034-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c034-119">Указывает, поддерживается ли запрос определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c034-119">Indicates whether requesting a specific resource is supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c034-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2c034-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>

<span data-ttu-id="2c034-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Определено** (2)</span><span class="sxs-lookup"><span data-stu-id="2c034-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Specific** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2c034-122">Запрос может включать запрос определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c034-122">Request can include a request for specific resource.</span></span>

</dd> <dt>

<span id="General"></span><span id="general"></span><span id="GENERAL"></span>

<span data-ttu-id="2c034-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**Общие** (3)</span><span class="sxs-lookup"><span data-stu-id="2c034-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**General** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2c034-124">Запрос не включает конкретный ресурс.</span><span class="sxs-lookup"><span data-stu-id="2c034-124">Request does not include specific resource.</span></span>

</dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="2c034-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Оба** (4)</span><span class="sxs-lookup"><span data-stu-id="2c034-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Both** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2c034-126">Поддерживаются как конкретные, так и общие запросы.</span><span class="sxs-lookup"><span data-stu-id="2c034-126">Both specific and general requests are supported.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2c034-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="2c034-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2c034-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="2c034-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c034-129">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="2c034-129">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c034-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c034-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c034-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c034-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c034-132">Описание конкретного подтипа реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c034-132">A description of an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="2c034-133">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2c034-133">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="2c034-134">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="2c034-134">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c034-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c034-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c034-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c034-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c034-137">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ аллокатионкапабилитиес**.**Осерресаурцетипе**","[**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="2c034-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AllocationCapabilities**.**OtherResourceType**", "[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="2c034-138">Тип ресурса, назначенный этому параметру выделения.</span><span class="sxs-lookup"><span data-stu-id="2c034-138">The type of resource that is assigned to this allocation setting.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c034-139">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="2c034-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="2c034-140">**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="2c034-140">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="2c034-141">**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="2c034-141">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="2c034-142">**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="2c034-142">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="2c034-143">**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="2c034-143">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="2c034-144">**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="2c034-144">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="2c034-145">**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="2c034-145">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="2c034-146">**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="2c034-146">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="2c034-147">**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="2c034-147">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="2c034-148">**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="2c034-148">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="2c034-149">**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="2c034-149">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="2c034-150">**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="2c034-150">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="2c034-151">**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="2c034-151">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="2c034-152">Дисковод **гибких дисков** (14)</span><span class="sxs-lookup"><span data-stu-id="2c034-152">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="2c034-153">**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="2c034-153">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="2c034-154">**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="2c034-154">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="2c034-155">**Диск** (17)</span><span class="sxs-lookup"><span data-stu-id="2c034-155">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="2c034-156">**Ленточный накопитель** (18)</span><span class="sxs-lookup"><span data-stu-id="2c034-156">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="2c034-157">**Область хранения** (19)</span><span class="sxs-lookup"><span data-stu-id="2c034-157">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="2c034-158">**Другое запоминающее устройство** (20)</span><span class="sxs-lookup"><span data-stu-id="2c034-158">**Other Storage Device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="2c034-159">**Последовательный порт** (21)</span><span class="sxs-lookup"><span data-stu-id="2c034-159">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="2c034-160">**Параллельный порт** (22)</span><span class="sxs-lookup"><span data-stu-id="2c034-160">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="2c034-161">**Контроллер USB** (23)</span><span class="sxs-lookup"><span data-stu-id="2c034-161">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="2c034-162">**Графический контроллер** (24)</span><span class="sxs-lookup"><span data-stu-id="2c034-162">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="2c034-163">**Контроллер IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="2c034-163">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="2c034-164">**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="2c034-164">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="2c034-165">**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="2c034-165">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="2c034-166">**Мощность** (28)</span><span class="sxs-lookup"><span data-stu-id="2c034-166">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="2c034-167">**Емкость системы охлаждения** (29)</span><span class="sxs-lookup"><span data-stu-id="2c034-167">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="2c034-168">**Порт коммутатора Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="2c034-168">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="2c034-169">**Логический диск** (31)</span><span class="sxs-lookup"><span data-stu-id="2c034-169">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="2c034-170">**Том хранилища** (32)</span><span class="sxs-lookup"><span data-stu-id="2c034-170">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="2c034-171">**Ethernet-подключение** (33)</span><span class="sxs-lookup"><span data-stu-id="2c034-171">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2c034-172">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="2c034-172">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2c034-173">**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="2c034-173">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c034-174">**шарингмоде**</span><span class="sxs-lookup"><span data-stu-id="2c034-174">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c034-175">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c034-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c034-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c034-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c034-177">Указывает, как предоставляется доступ к базовому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2c034-177">Indicates how access to the underlying resource is granted.</span></span>

<span data-ttu-id="2c034-178">Фактическое количество зависит от минимального, максимального размера, веса и т. д.</span><span class="sxs-lookup"><span data-stu-id="2c034-178">Actual quantity is controlled by min, max size, weights, etc.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c034-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2c034-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="2c034-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (2)</span><span class="sxs-lookup"><span data-stu-id="2c034-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2c034-181">Монопольный доступ к базовому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2c034-181">Exclusive access to underlying resource.</span></span>

</dd> <dt>

<span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>

<span data-ttu-id="2c034-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Общий** (3)</span><span class="sxs-lookup"><span data-stu-id="2c034-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Shared** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2c034-183">Общее использование базового ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c034-183">Shared use of underlying resource.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2c034-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="2c034-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2c034-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="2c034-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c034-186">**суппортедаддстатес**</span><span class="sxs-lookup"><span data-stu-id="2c034-186">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c034-187">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="2c034-187">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2c034-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c034-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c034-189">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="2c034-189">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="2c034-190">Состояния системы, которые поддерживаются при создании нового ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c034-190">The system states that are supported when a new resource is created.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c034-191">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2c034-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2c034-192">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="2c034-192">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2c034-193">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="2c034-193">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="2c034-194">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="2c034-194">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2c034-195">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="2c034-195">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="2c034-196">**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="2c034-196">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2c034-197">**В тесте** (7)</span><span class="sxs-lookup"><span data-stu-id="2c034-197">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="2c034-198">**Отложено** (8)</span><span class="sxs-lookup"><span data-stu-id="2c034-198">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="2c034-199">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="2c034-199">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2c034-200">**Запуск** (10)</span><span class="sxs-lookup"><span data-stu-id="2c034-200">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2c034-201">**Приостановлено** (11)</span><span class="sxs-lookup"><span data-stu-id="2c034-201">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="2c034-202">**Приостановлено** (12)</span><span class="sxs-lookup"><span data-stu-id="2c034-202">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2c034-203">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="2c034-203">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2c034-204">**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="2c034-204">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c034-205">**суппортедремовестатес**</span><span class="sxs-lookup"><span data-stu-id="2c034-205">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c034-206">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="2c034-206">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2c034-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c034-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c034-208">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="2c034-208">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="2c034-209">Состояния системы, которые поддерживаются при удалении ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c034-209">The system states that are supported when a resource is removed.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c034-210">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2c034-210">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2c034-211">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="2c034-211">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2c034-212">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="2c034-212">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="2c034-213">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="2c034-213">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2c034-214">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="2c034-214">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="2c034-215">**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="2c034-215">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2c034-216">**В тесте** (7)</span><span class="sxs-lookup"><span data-stu-id="2c034-216">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="2c034-217">**Отложено** (8)</span><span class="sxs-lookup"><span data-stu-id="2c034-217">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="2c034-218">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="2c034-218">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2c034-219">**Запуск** (10)</span><span class="sxs-lookup"><span data-stu-id="2c034-219">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2c034-220">**Приостановлено** (11)</span><span class="sxs-lookup"><span data-stu-id="2c034-220">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="2c034-221">**Приостановлено** (12)</span><span class="sxs-lookup"><span data-stu-id="2c034-221">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2c034-222">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="2c034-222">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2c034-223">**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="2c034-223">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="2c034-224"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2c034-224"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2c034-225">Требования</span><span class="sxs-lookup"><span data-stu-id="2c034-225">Requirements</span></span>



| <span data-ttu-id="2c034-226">Требование</span><span class="sxs-lookup"><span data-stu-id="2c034-226">Requirement</span></span> | <span data-ttu-id="2c034-227">Значение</span><span class="sxs-lookup"><span data-stu-id="2c034-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c034-228">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c034-228">Minimum supported client</span></span><br/> | <span data-ttu-id="2c034-229">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2c034-229">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2c034-230">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c034-230">Minimum supported server</span></span><br/> | <span data-ttu-id="2c034-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c034-231">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2c034-232">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2c034-232">Namespace</span></span><br/>                | <span data-ttu-id="2c034-233">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2c034-233">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2c034-234">MOF</span><span class="sxs-lookup"><span data-stu-id="2c034-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c034-235"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c034-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c034-236">DLL</span><span class="sxs-lookup"><span data-stu-id="2c034-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c034-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c034-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c034-238">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c034-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c034-239">**\_Возможности CIM**</span><span class="sxs-lookup"><span data-stu-id="2c034-239">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

