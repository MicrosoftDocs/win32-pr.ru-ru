---
description: Этот класс является классом типа событий для событий конфигурации физического диска.
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: Класс SystemConfig_V0_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f7eab1cec90630e25ee5968e5740f787acb8662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985932"
---
# <a name="systemconfig_v0_phydisk-class"></a><span data-ttu-id="50e53-103">\_Класс системконфиг v0 \_ фидиск</span><span class="sxs-lookup"><span data-stu-id="50e53-103">SystemConfig\_V0\_PhyDisk class</span></span>

<span data-ttu-id="50e53-104">Этот класс является классом типа событий для событий конфигурации физического диска.</span><span class="sxs-lookup"><span data-stu-id="50e53-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="50e53-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="50e53-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e53-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50e53-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a><span data-ttu-id="50e53-107">Участники</span><span class="sxs-lookup"><span data-stu-id="50e53-107">Members</span></span>

<span data-ttu-id="50e53-108">Класс **системконфиг \_ v0 \_ фидиск** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="50e53-108">The **SystemConfig\_V0\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="50e53-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="50e53-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50e53-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="50e53-110">Properties</span></span>

<span data-ttu-id="50e53-111">Класс **системконфиг \_ v0 \_ фидиск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="50e53-111">The **SystemConfig\_V0\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50e53-112">**бутдривелеттер**</span><span class="sxs-lookup"><span data-stu-id="50e53-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-113">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="50e53-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="50e53-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-115">Квалификаторы: **вмидатаид** (13), **Max** (3)</span><span class="sxs-lookup"><span data-stu-id="50e53-115">Qualifiers: **WmiDataId** (13), **Max** (3)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-116">Буква загрузочного диска в формате " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="50e53-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="50e53-117">**битесперсектор**</span><span class="sxs-lookup"><span data-stu-id="50e53-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50e53-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-120">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="50e53-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-121">Число байтов в каждом секторе для физического диска.</span><span class="sxs-lookup"><span data-stu-id="50e53-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-122">**Цилиндров**</span><span class="sxs-lookup"><span data-stu-id="50e53-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-123">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="50e53-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-125">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="50e53-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-126">Общее число цилиндров на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="50e53-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="50e53-127">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="50e53-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="50e53-128">Значение может быть неточным, если диск использует схему перевода для поддержки размера дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="50e53-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="50e53-129">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="50e53-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-130">**дискнумбер**</span><span class="sxs-lookup"><span data-stu-id="50e53-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50e53-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-133">Квалификаторы: **вмидатаид** (1)</span><span class="sxs-lookup"><span data-stu-id="50e53-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-134">Номер индекса диска, содержащего этот раздел.</span><span class="sxs-lookup"><span data-stu-id="50e53-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-135">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="50e53-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-136">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="50e53-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="50e53-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-138">Квалификаторы: **вмидатаид** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="50e53-138">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-139">Имя изготовителя диска.</span><span class="sxs-lookup"><span data-stu-id="50e53-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-140">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="50e53-140">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-141">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50e53-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-143">Квалификаторы: **вмидатаид** (11)</span><span class="sxs-lookup"><span data-stu-id="50e53-143">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-144">Количество разделов на этом физическом диске, распознаваемых операционной системой.</span><span class="sxs-lookup"><span data-stu-id="50e53-144">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-145">**сксилун**</span><span class="sxs-lookup"><span data-stu-id="50e53-145">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50e53-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-148">Квалификаторы: **вмидатаид** (9)</span><span class="sxs-lookup"><span data-stu-id="50e53-148">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-149">Логический номер устройства (LUN) SCSI адаптера SCSI.</span><span class="sxs-lookup"><span data-stu-id="50e53-149">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-150">**сксипас**</span><span class="sxs-lookup"><span data-stu-id="50e53-150">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50e53-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-153">Квалификаторы: **вмидатаид** (7)</span><span class="sxs-lookup"><span data-stu-id="50e53-153">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-154">Номер шины SCSI адаптера SCSI.</span><span class="sxs-lookup"><span data-stu-id="50e53-154">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-155">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="50e53-155">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-156">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50e53-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-158">Квалификаторы: **вмидатаид** (6)</span><span class="sxs-lookup"><span data-stu-id="50e53-158">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-159">Номер SCSI адаптера SCSI.</span><span class="sxs-lookup"><span data-stu-id="50e53-159">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-160">**скситаржет**</span><span class="sxs-lookup"><span data-stu-id="50e53-160">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-161">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50e53-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-163">Квалификаторы: **вмидатаид** (8)</span><span class="sxs-lookup"><span data-stu-id="50e53-163">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-164">Содержит номер целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="50e53-164">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-165">**секторспертракк**</span><span class="sxs-lookup"><span data-stu-id="50e53-165">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-166">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50e53-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-168">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="50e53-168">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-169">Количество секторов в каждой дорожке для этого физического диска.</span><span class="sxs-lookup"><span data-stu-id="50e53-169">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-170">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="50e53-170">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-171">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50e53-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-173">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="50e53-173">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-174">Количество дорожек в каждом цилиндре на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="50e53-174">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="50e53-175">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="50e53-175">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="50e53-176">Значение может быть неточным, если диск использует схему перевода для поддержки размера дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="50e53-176">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="50e53-177">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="50e53-177">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-178">**вритекачинаблед**</span><span class="sxs-lookup"><span data-stu-id="50e53-178">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e53-179">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="50e53-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50e53-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50e53-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e53-181">Квалификаторы: **вмидатаид** (12)</span><span class="sxs-lookup"><span data-stu-id="50e53-181">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="50e53-182">Значение true, если кэш записи включен.</span><span class="sxs-lookup"><span data-stu-id="50e53-182">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50e53-183">Требования</span><span class="sxs-lookup"><span data-stu-id="50e53-183">Requirements</span></span>



| <span data-ttu-id="50e53-184">Требование</span><span class="sxs-lookup"><span data-stu-id="50e53-184">Requirement</span></span> | <span data-ttu-id="50e53-185">Значение</span><span class="sxs-lookup"><span data-stu-id="50e53-185">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50e53-186">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50e53-186">Minimum supported client</span></span><br/> | <span data-ttu-id="50e53-187">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="50e53-187">None supported</span></span><br/>                            |
| <span data-ttu-id="50e53-188">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50e53-188">Minimum supported server</span></span><br/> | <span data-ttu-id="50e53-189">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50e53-189">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50e53-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50e53-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e53-191">**Системконфиг \_ v0**</span><span class="sxs-lookup"><span data-stu-id="50e53-191">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




