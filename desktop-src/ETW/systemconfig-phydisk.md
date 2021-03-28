---
description: Этот класс является классом типа событий для событий конфигурации физического диска.
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: Класс SystemConfig_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PhyDisk
- SystemConfig_PhyDisk.DiskNumber
- SystemConfig_PhyDisk.BytesPerSector
- SystemConfig_PhyDisk.SectorsPerTrack
- SystemConfig_PhyDisk.TracksPerCylinder
- SystemConfig_PhyDisk.Cylinders
- SystemConfig_PhyDisk.SCSIPort
- SystemConfig_PhyDisk.SCSIPath
- SystemConfig_PhyDisk.SCSITarget
- SystemConfig_PhyDisk.SCSILun
- SystemConfig_PhyDisk.Manufacturer
- SystemConfig_PhyDisk.PartitionCount
- SystemConfig_PhyDisk.WriteCacheEnabled
- SystemConfig_PhyDisk.Pad
- SystemConfig_PhyDisk.BootDriveLetter
- SystemConfig_PhyDisk.Spare
api_type:
- NA
api_location: ''
ms.openlocfilehash: d868e3943f22a71b4513f4f77841ddea9204ffea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984400"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="88b5b-103">\_Класс системконфиг фидиск</span><span class="sxs-lookup"><span data-stu-id="88b5b-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="88b5b-104">Этот класс является классом типа событий для событий конфигурации физического диска.</span><span class="sxs-lookup"><span data-stu-id="88b5b-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="88b5b-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="88b5b-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b5b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88b5b-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_PhyDisk : SystemConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  char16 Manufacturer[];
  uint32 PartitionCount;
  uint8  WriteCacheEnabled;
  uint8  Pad;
  char16 BootDriveLetter[];
  char16 Spare[];
};
```

## <a name="members"></a><span data-ttu-id="88b5b-107">Участники</span><span class="sxs-lookup"><span data-stu-id="88b5b-107">Members</span></span>

<span data-ttu-id="88b5b-108">Класс **системконфиг \_ фидиск** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="88b5b-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="88b5b-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="88b5b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88b5b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="88b5b-110">Properties</span></span>

<span data-ttu-id="88b5b-111">Класс **системконфиг \_ фидиск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="88b5b-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88b5b-112">**бутдривелеттер**</span><span class="sxs-lookup"><span data-stu-id="88b5b-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-113">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="88b5b-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-115">Квалификаторы: **вмидатаид** (14), **Max** (3), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="88b5b-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-116">Буква загрузочного диска в формате " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="88b5b-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-117">**битесперсектор**</span><span class="sxs-lookup"><span data-stu-id="88b5b-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88b5b-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-120">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="88b5b-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-121">Число байтов в каждом секторе для физического диска.</span><span class="sxs-lookup"><span data-stu-id="88b5b-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-122">**Цилиндров**</span><span class="sxs-lookup"><span data-stu-id="88b5b-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-123">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88b5b-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-125">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="88b5b-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-126">Общее число цилиндров на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="88b5b-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="88b5b-127">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="88b5b-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="88b5b-128">Значение может быть неточным, если диск использует схему перевода для поддержки размера дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="88b5b-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="88b5b-129">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="88b5b-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-130">**дискнумбер**</span><span class="sxs-lookup"><span data-stu-id="88b5b-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88b5b-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-133">Квалификаторы: **вмидатаид** (1)</span><span class="sxs-lookup"><span data-stu-id="88b5b-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-134">Номер индекса диска, содержащего этот раздел.</span><span class="sxs-lookup"><span data-stu-id="88b5b-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-135">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="88b5b-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-136">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="88b5b-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-138">Квалификаторы: **вмидатаид** (10), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="88b5b-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-139">Имя изготовителя диска.</span><span class="sxs-lookup"><span data-stu-id="88b5b-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-140">**Коммутаци**</span><span class="sxs-lookup"><span data-stu-id="88b5b-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-141">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="88b5b-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-143">Квалификаторы: **вмидатаид** (13)</span><span class="sxs-lookup"><span data-stu-id="88b5b-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-144">Не используется.</span><span class="sxs-lookup"><span data-stu-id="88b5b-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="88b5b-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88b5b-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-148">Квалификаторы: **вмидатаид** (11)</span><span class="sxs-lookup"><span data-stu-id="88b5b-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-149">Количество разделов на этом физическом диске, распознаваемых операционной системой.</span><span class="sxs-lookup"><span data-stu-id="88b5b-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-150">**сксилун**</span><span class="sxs-lookup"><span data-stu-id="88b5b-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88b5b-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-153">Квалификаторы: **вмидатаид** (9)</span><span class="sxs-lookup"><span data-stu-id="88b5b-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-154">Логический номер устройства (LUN) SCSI адаптера SCSI.</span><span class="sxs-lookup"><span data-stu-id="88b5b-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-155">**сксипас**</span><span class="sxs-lookup"><span data-stu-id="88b5b-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-156">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88b5b-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-158">Квалификаторы: **вмидатаид** (7)</span><span class="sxs-lookup"><span data-stu-id="88b5b-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-159">Номер шины SCSI адаптера SCSI.</span><span class="sxs-lookup"><span data-stu-id="88b5b-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="88b5b-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-161">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88b5b-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-163">Квалификаторы: **вмидатаид** (6)</span><span class="sxs-lookup"><span data-stu-id="88b5b-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-164">Номер SCSI адаптера SCSI.</span><span class="sxs-lookup"><span data-stu-id="88b5b-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-165">**скситаржет**</span><span class="sxs-lookup"><span data-stu-id="88b5b-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-166">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88b5b-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-168">Квалификаторы: **вмидатаид** (8)</span><span class="sxs-lookup"><span data-stu-id="88b5b-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-169">Содержит номер целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="88b5b-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-170">**секторспертракк**</span><span class="sxs-lookup"><span data-stu-id="88b5b-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-171">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88b5b-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-173">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="88b5b-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-174">Количество секторов в каждой дорожке для этого физического диска.</span><span class="sxs-lookup"><span data-stu-id="88b5b-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-175">**Перенести**</span><span class="sxs-lookup"><span data-stu-id="88b5b-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-176">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="88b5b-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-178">Квалификаторы: **вмидатаид** (15), **Max** (2), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="88b5b-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-179">Не используется.</span><span class="sxs-lookup"><span data-stu-id="88b5b-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-180">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="88b5b-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-181">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88b5b-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-183">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="88b5b-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-184">Количество дорожек в каждом цилиндре на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="88b5b-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="88b5b-185">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="88b5b-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="88b5b-186">Значение может быть неточным, если диск использует схему перевода для поддержки размера дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="88b5b-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="88b5b-187">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="88b5b-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="88b5b-188">**вритекачинаблед**</span><span class="sxs-lookup"><span data-stu-id="88b5b-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b5b-189">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="88b5b-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b5b-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b5b-191">Квалификаторы: **вмидатаид** (12)</span><span class="sxs-lookup"><span data-stu-id="88b5b-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="88b5b-192">Значение true, если кэш записи включен.</span><span class="sxs-lookup"><span data-stu-id="88b5b-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88b5b-193">Требования</span><span class="sxs-lookup"><span data-stu-id="88b5b-193">Requirements</span></span>



| <span data-ttu-id="88b5b-194">Требование</span><span class="sxs-lookup"><span data-stu-id="88b5b-194">Requirement</span></span> | <span data-ttu-id="88b5b-195">Значение</span><span class="sxs-lookup"><span data-stu-id="88b5b-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88b5b-196">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88b5b-196">Minimum supported client</span></span><br/> | <span data-ttu-id="88b5b-197">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88b5b-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88b5b-198">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88b5b-198">Minimum supported server</span></span><br/> | <span data-ttu-id="88b5b-199">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88b5b-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88b5b-200">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88b5b-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b5b-201">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="88b5b-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




