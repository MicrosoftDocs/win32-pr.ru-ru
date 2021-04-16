---
description: Определяет сопоставление типа ресурса с его классами реализации.
ms.assetid: 0911454D-2494-49D5-8480-212E9ADD1B45
title: Класс Msvm_ResourceTypeDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceTypeDefinition
- Msvm_ResourceTypeDefinition.ResourceType
- Msvm_ResourceTypeDefinition.OtherResourceType
- Msvm_ResourceTypeDefinition.ResourceSubType
- Msvm_ResourceTypeDefinition.LogicalDeviceClassName
- Msvm_ResourceTypeDefinition.SettingDataClassName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: edfbf2ec9772fa710df5fc0d024abfcad6d826d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683852"
---
# <a name="msvm_resourcetypedefinition-class"></a><span data-ttu-id="4b29c-103">\_Класс мсвм ресаурцетипедефинитион</span><span class="sxs-lookup"><span data-stu-id="4b29c-103">Msvm\_ResourceTypeDefinition class</span></span>

<span data-ttu-id="4b29c-104">Определяет сопоставление типа ресурса с его классами реализации.</span><span class="sxs-lookup"><span data-stu-id="4b29c-104">Defines a mapping of a resource type to its implementation classes.</span></span>

<span data-ttu-id="4b29c-105">Следующий синтаксис представляет собой упрощенный код MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4b29c-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b29c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b29c-106">Syntax</span></span>

``` syntax
class Msvm_ResourceTypeDefinition
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  string LogicalDeviceClassName;
  string SettingDataClassName;
};
```

## <a name="members"></a><span data-ttu-id="4b29c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4b29c-107">Members</span></span>

<span data-ttu-id="4b29c-108">Класс **мсвм \_ ресаурцетипедефинитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4b29c-108">The **Msvm\_ResourceTypeDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="4b29c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b29c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b29c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b29c-110">Properties</span></span>

<span data-ttu-id="4b29c-111">Класс **мсвм \_ ресаурцетипедефинитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4b29c-111">The **Msvm\_ResourceTypeDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b29c-112">**логикалдевицекласснаме**</span><span class="sxs-lookup"><span data-stu-id="4b29c-112">**LogicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b29c-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4b29c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b29c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b29c-115">Имя класса, производного от [**CIM \_ логическое**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , который реализует логическое устройство для этого типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b29c-115">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the logical device for this resource type.</span></span>

</dd> <dt>

<span data-ttu-id="4b29c-116">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="4b29c-116">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b29c-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4b29c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b29c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-119">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="4b29c-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4b29c-120">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="4b29c-120">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="4b29c-121">Существует соответствие свойству **Осерресаурцетипе** [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="4b29c-121">There is a correspondence with the **OtherResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4b29c-122">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="4b29c-122">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b29c-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4b29c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b29c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-125">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="4b29c-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4b29c-126">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b29c-126">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="4b29c-127">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b29c-127">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="4b29c-128">Существует соответствие свойству **Ресаурцесубтипе** [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="4b29c-128">There is a correspondence with the **ResourceSubType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4b29c-129">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="4b29c-129">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b29c-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4b29c-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b29c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-132">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="4b29c-132">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4b29c-133">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="4b29c-133">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="4b29c-134">Существует соответствие свойству **ResourceType** [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="4b29c-134">There is a correspondence with the **ResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="4b29c-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="4b29c-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="4b29c-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="4b29c-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="4b29c-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="4b29c-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="4b29c-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="4b29c-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="4b29c-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="4b29c-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="4b29c-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="4b29c-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="4b29c-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="4b29c-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>Дисковод **гибких дисков** (14)</span><span class="sxs-lookup"><span data-stu-id="4b29c-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="4b29c-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="4b29c-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Последовательный порт** (17)</span><span class="sxs-lookup"><span data-stu-id="4b29c-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Параллельный порт** (18)</span><span class="sxs-lookup"><span data-stu-id="4b29c-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-контроллер** (19)</span><span class="sxs-lookup"><span data-stu-id="4b29c-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Графический контроллер** (20)</span><span class="sxs-lookup"><span data-stu-id="4b29c-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Область хранения** (21)</span><span class="sxs-lookup"><span data-stu-id="4b29c-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Диск** (22)</span><span class="sxs-lookup"><span data-stu-id="4b29c-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Лента** (23)</span><span class="sxs-lookup"><span data-stu-id="4b29c-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Другое запоминающее устройство** (24)</span><span class="sxs-lookup"><span data-stu-id="4b29c-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Контроллер FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="4b29c-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="4b29c-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="4b29c-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Источник питания** (28)</span><span class="sxs-lookup"><span data-stu-id="4b29c-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Охлаждающее устройство** (29)</span><span class="sxs-lookup"><span data-stu-id="4b29c-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="4b29c-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="4b29c-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4b29c-166">**сеттингдатакласснаме**</span><span class="sxs-lookup"><span data-stu-id="4b29c-166">**SettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b29c-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4b29c-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b29c-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b29c-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b29c-169">Имя класса, производного от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , который реализует параметры для этого типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b29c-169">The name of the class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) that implements the settings for this resource type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b29c-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b29c-170">Remarks</span></span>

<span data-ttu-id="4b29c-171">Доступ к классу **\_ ресаурцетипедефинитион мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="4b29c-171">Access to the **Msvm\_ResourceTypeDefinition** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4b29c-172">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4b29c-172">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b29c-173">Требования</span><span class="sxs-lookup"><span data-stu-id="4b29c-173">Requirements</span></span>



| <span data-ttu-id="4b29c-174">Требование</span><span class="sxs-lookup"><span data-stu-id="4b29c-174">Requirement</span></span> | <span data-ttu-id="4b29c-175">Значение</span><span class="sxs-lookup"><span data-stu-id="4b29c-175">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b29c-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b29c-176">Minimum supported client</span></span><br/> | <span data-ttu-id="4b29c-177">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4b29c-177">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4b29c-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b29c-178">Minimum supported server</span></span><br/> | <span data-ttu-id="4b29c-179">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4b29c-179">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4b29c-180">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4b29c-180">End of client support</span></span><br/>    | <span data-ttu-id="4b29c-181">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4b29c-181">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4b29c-182">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4b29c-182">End of server support</span></span><br/>    | <span data-ttu-id="4b29c-183">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4b29c-183">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4b29c-184">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4b29c-184">Namespace</span></span><br/>                | <span data-ttu-id="4b29c-185">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4b29c-185">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4b29c-186">MOF</span><span class="sxs-lookup"><span data-stu-id="4b29c-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b29c-187"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b29c-187"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b29c-188">DLL</span><span class="sxs-lookup"><span data-stu-id="4b29c-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b29c-189"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b29c-189"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

