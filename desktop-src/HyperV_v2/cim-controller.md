---
description: Суперкласс для различных устройств, связанных с контролем, которые предоставляют классическую основную модель шины.
ms.assetid: eaa8711b-11e9-4f69-b81e-49a3c8a99fa7
title: Класс CIM_Controller (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller
- CIM_Controller.TimeOfLastReset
- CIM_Controller.ProtocolSupported
- CIM_Controller.MaxNumberControlled
- CIM_Controller.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 139d9c9b8a9ac1b28253551f7d37510f4a1bd53b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662605"
---
# <a name="cim_controller-class-hyper-v-management"></a><span data-ttu-id="09b9c-103">Класс CIM_Controller (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="09b9c-103">CIM_Controller class (Hyper-V management)</span></span>

<span data-ttu-id="09b9c-104">Суперкласс для различных устройств, связанных с контролем, которые предоставляют классическую основную модель шины.</span><span class="sxs-lookup"><span data-stu-id="09b9c-104">A superclass for miscellaneous control-related devices that provide a classic bus master interface.</span></span> <span data-ttu-id="09b9c-105">Класс контроллера является абстракцией для устройств с одним стеком протокола и существует для управления обменом данными (данные, управление и сброс) к подчиненным устройствам.</span><span class="sxs-lookup"><span data-stu-id="09b9c-105">The controller class is an abstraction for devices with a single protocol stack, and exist to control communications (data, control, and reset) to downstream devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b9c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09b9c-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_Controller : CIM_LogicalDevice
{
  datetime TimeOfLastReset;
  uint16   ProtocolSupported;
  uint32   MaxNumberControlled;
  string   ProtocolDescription;
};
```

## <a name="members"></a><span data-ttu-id="09b9c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="09b9c-107">Members</span></span>

<span data-ttu-id="09b9c-108">Класс **\_ контроллера CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="09b9c-108">The **CIM\_Controller** class has these types of members:</span></span>

-   [<span data-ttu-id="09b9c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="09b9c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09b9c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="09b9c-110">Properties</span></span>

<span data-ttu-id="09b9c-111">Класс **\_ контроллера CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="09b9c-111">The **CIM\_Controller** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09b9c-112">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="09b9c-112">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09b9c-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09b9c-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09b9c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09b9c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09b9c-115">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="09b9c-115">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="09b9c-116">Максимальное число поддерживаемых устройств, которыми может управлять контроллер.</span><span class="sxs-lookup"><span data-stu-id="09b9c-116">The maximum number of devices supported that can be managed by the controller.</span></span> <span data-ttu-id="09b9c-117">Значение "0" указывает, что число неизвестно или неограниченно.</span><span class="sxs-lookup"><span data-stu-id="09b9c-117">A "0" value indicates that the number is unknown or unlimited.</span></span>

</dd> <dt>

<span data-ttu-id="09b9c-118">**протоколдескриптион**</span><span class="sxs-lookup"><span data-stu-id="09b9c-118">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09b9c-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09b9c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09b9c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09b9c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09b9c-121">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 004,3 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Controller**.**Протоколсуппортед**")</span><span class="sxs-lookup"><span data-stu-id="09b9c-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|004.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Controller**.**ProtocolSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="09b9c-122">Произвольная строка, которая содержит дополнительные сведения, связанные с протоколом, поддерживаемым контроллером.</span><span class="sxs-lookup"><span data-stu-id="09b9c-122">A free-form string that provides more information that is related to the protocol supported by the controller.</span></span>

</dd> <dt>

<span data-ttu-id="09b9c-123">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="09b9c-123">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09b9c-124">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09b9c-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09b9c-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09b9c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09b9c-126">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 004,2 "," MIF. \|Диски DMTF \| 003,3 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Controller**.**Протоколдескриптион**")</span><span class="sxs-lookup"><span data-stu-id="09b9c-126">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|004.2", "MIF.DMTF\|Disks\|003.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Controller**.**ProtocolDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="09b9c-127">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="09b9c-127">The protocol used by the controller to access controlled devices.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="09b9c-128">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="09b9c-128">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="09b9c-129">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="09b9c-129">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="09b9c-130">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="09b9c-130">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="09b9c-131">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="09b9c-131">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="09b9c-132">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="09b9c-132">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="09b9c-133">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="09b9c-133">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="09b9c-134">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="09b9c-134">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="09b9c-135">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="09b9c-135">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="09b9c-136">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="09b9c-136">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="09b9c-137">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="09b9c-137">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="09b9c-138">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="09b9c-138">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="09b9c-139">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="09b9c-139">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="09b9c-140">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="09b9c-140">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="09b9c-141">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="09b9c-141">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="09b9c-142">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="09b9c-142">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="09b9c-143">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="09b9c-143">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="09b9c-144">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="09b9c-144">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="09b9c-145">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="09b9c-145">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="09b9c-146">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="09b9c-146">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="09b9c-147">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="09b9c-147">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="09b9c-148">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="09b9c-148">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="09b9c-149">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="09b9c-149">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="09b9c-150">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="09b9c-150">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="09b9c-151">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="09b9c-151">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="09b9c-152">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="09b9c-152">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="09b9c-153">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="09b9c-153">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="09b9c-154">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="09b9c-154">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="09b9c-155">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="09b9c-155">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="09b9c-156">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="09b9c-156">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="09b9c-157">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="09b9c-157">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="09b9c-158">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="09b9c-158">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="09b9c-159">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="09b9c-159">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="09b9c-160">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="09b9c-160">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="09b9c-161">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="09b9c-161">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="09b9c-162">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="09b9c-162">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="09b9c-163">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="09b9c-163">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="09b9c-164">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="09b9c-164">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="09b9c-165">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="09b9c-165">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="09b9c-166">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="09b9c-166">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="09b9c-167">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="09b9c-167">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="09b9c-168">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="09b9c-168">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="09b9c-169">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="09b9c-169">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="09b9c-170">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="09b9c-170">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="09b9c-171">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="09b9c-171">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="09b9c-172">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="09b9c-172">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="09b9c-173">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="09b9c-173">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="09b9c-174">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="09b9c-174">**IrBus** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_ATA"></span><span id="serial_ata"></span><span id="SERIAL_ATA"></span>

<span data-ttu-id="09b9c-175">**Serial ATA** (48)</span><span class="sxs-lookup"><span data-stu-id="09b9c-175">**Serial ATA** (48)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="09b9c-176">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="09b9c-176">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09b9c-177">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09b9c-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09b9c-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09b9c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09b9c-179">Время последнего сброса контроллера.</span><span class="sxs-lookup"><span data-stu-id="09b9c-179">The last time when the controller was reset.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09b9c-180">Требования</span><span class="sxs-lookup"><span data-stu-id="09b9c-180">Requirements</span></span>



| <span data-ttu-id="09b9c-181">Требование</span><span class="sxs-lookup"><span data-stu-id="09b9c-181">Requirement</span></span> | <span data-ttu-id="09b9c-182">Значение</span><span class="sxs-lookup"><span data-stu-id="09b9c-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09b9c-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09b9c-183">Minimum supported client</span></span><br/> | <span data-ttu-id="09b9c-184">Windows 8</span><span class="sxs-lookup"><span data-stu-id="09b9c-184">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="09b9c-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09b9c-185">Minimum supported server</span></span><br/> | <span data-ttu-id="09b9c-186">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09b9c-186">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="09b9c-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="09b9c-187">Namespace</span></span><br/>                | <span data-ttu-id="09b9c-188">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="09b9c-188">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="09b9c-189">MOF</span><span class="sxs-lookup"><span data-stu-id="09b9c-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09b9c-190"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09b9c-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09b9c-191">DLL</span><span class="sxs-lookup"><span data-stu-id="09b9c-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09b9c-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09b9c-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="09b9c-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09b9c-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b9c-194">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="09b9c-194">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

