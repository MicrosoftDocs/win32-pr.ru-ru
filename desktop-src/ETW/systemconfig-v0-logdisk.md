---
description: Этот класс является классом типа событий для событий конфигурации логического диска.
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: Класс SystemConfig_V0_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: dbc1ee189bae1fe71f42267f38bd40763764dea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985933"
---
# <a name="systemconfig_v0_logdisk-class"></a><span data-ttu-id="71126-103">\_Класс системконфиг v0 \_ логдиск</span><span class="sxs-lookup"><span data-stu-id="71126-103">SystemConfig\_V0\_LogDisk class</span></span>

<span data-ttu-id="71126-104">Этот класс является классом типа событий для событий конфигурации логического диска.</span><span class="sxs-lookup"><span data-stu-id="71126-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="71126-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="71126-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="71126-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71126-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a><span data-ttu-id="71126-107">Участники</span><span class="sxs-lookup"><span data-stu-id="71126-107">Members</span></span>

<span data-ttu-id="71126-108">Класс **системконфиг \_ v0 \_ логдиск** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="71126-108">The **SystemConfig\_V0\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="71126-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="71126-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71126-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="71126-110">Properties</span></span>

<span data-ttu-id="71126-111">Класс **системконфиг \_ v0 \_ логдиск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="71126-111">The **SystemConfig\_V0\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71126-112">**битесперсектор**</span><span class="sxs-lookup"><span data-stu-id="71126-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71126-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71126-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-115">Квалификаторы: **вмидатаид** (10)</span><span class="sxs-lookup"><span data-stu-id="71126-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="71126-116">Число байтов в каждом секторе для физического диска.</span><span class="sxs-lookup"><span data-stu-id="71126-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="71126-117">**дискнумбер**</span><span class="sxs-lookup"><span data-stu-id="71126-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71126-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71126-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-120">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="71126-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="71126-121">Номер индекса диска, содержащего этот раздел.</span><span class="sxs-lookup"><span data-stu-id="71126-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="71126-122">**дривелеттерстринг**</span><span class="sxs-lookup"><span data-stu-id="71126-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-123">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="71126-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="71126-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-125">Квалификаторы: **вмидатаид** (6), **Max** (4)</span><span class="sxs-lookup"><span data-stu-id="71126-125">Qualifiers: **WmiDataId** (6), **Max** (4)</span></span>
</dt> </dl>

<span data-ttu-id="71126-126">Буква диска в формате " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="71126-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="71126-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="71126-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-128">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71126-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71126-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-130">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="71126-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="71126-131">Тип диска.</span><span class="sxs-lookup"><span data-stu-id="71126-131">Type of disk drive.</span></span> <span data-ttu-id="71126-132">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="71126-132">Possible values are:</span></span>



| <span data-ttu-id="71126-133">Значение</span><span class="sxs-lookup"><span data-stu-id="71126-133">Value</span></span>                                                                        | <span data-ttu-id="71126-134">Значение</span><span class="sxs-lookup"><span data-stu-id="71126-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="71126-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="71126-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="71126-136">Секция</span><span class="sxs-lookup"><span data-stu-id="71126-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="71126-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="71126-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="71126-138">Том</span><span class="sxs-lookup"><span data-stu-id="71126-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="71126-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="71126-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="71126-140">Дополнительный раздел на нескольких дисках</span><span class="sxs-lookup"><span data-stu-id="71126-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="71126-141">**Системой**</span><span class="sxs-lookup"><span data-stu-id="71126-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-142">Тип данных: **Char16**</span><span class="sxs-lookup"><span data-stu-id="71126-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="71126-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-144">Квалификаторы: **вмидатаид** (13), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="71126-144">Qualifiers: **WmiDataId** (13), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="71126-145">Файловая система на логическом диске, например NTFS.</span><span class="sxs-lookup"><span data-stu-id="71126-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="71126-146">**нумбероффриклустерс**</span><span class="sxs-lookup"><span data-stu-id="71126-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-147">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="71126-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="71126-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-149">Квалификаторы: **вмидатаид** (11)</span><span class="sxs-lookup"><span data-stu-id="71126-149">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="71126-150">Количество свободных кластеров в указанном томе.</span><span class="sxs-lookup"><span data-stu-id="71126-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="71126-151">**Коммутаци**</span><span class="sxs-lookup"><span data-stu-id="71126-151">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71126-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71126-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-154">Квалификаторы: **вмидатаид** (7)</span><span class="sxs-lookup"><span data-stu-id="71126-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="71126-155">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="71126-155">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="71126-156">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="71126-156">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71126-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71126-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-159">Квалификаторы: **вмидатаид** (8)</span><span class="sxs-lookup"><span data-stu-id="71126-159">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="71126-160">Номер индекса секции.</span><span class="sxs-lookup"><span data-stu-id="71126-160">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="71126-161">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="71126-161">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-162">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71126-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71126-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-164">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="71126-164">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="71126-165">Общий размер секции в байтах.</span><span class="sxs-lookup"><span data-stu-id="71126-165">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="71126-166">**секторсперклустер**</span><span class="sxs-lookup"><span data-stu-id="71126-166">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-167">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71126-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71126-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-169">Квалификаторы: **вмидатаид** (9)</span><span class="sxs-lookup"><span data-stu-id="71126-169">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="71126-170">Количество секторов в томе.</span><span class="sxs-lookup"><span data-stu-id="71126-170">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="71126-171">**Размер**</span><span class="sxs-lookup"><span data-stu-id="71126-171">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71126-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71126-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-174">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="71126-174">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="71126-175">Размер диска в байтах.</span><span class="sxs-lookup"><span data-stu-id="71126-175">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="71126-176">**стартоффсет**</span><span class="sxs-lookup"><span data-stu-id="71126-176">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-177">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71126-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71126-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-179">Квалификаторы: **вмидатаид** (1)</span><span class="sxs-lookup"><span data-stu-id="71126-179">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="71126-180">Начальное смещение (в байтах) секции от начала диска.</span><span class="sxs-lookup"><span data-stu-id="71126-180">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="71126-181">**тоталнумберофклустерс**</span><span class="sxs-lookup"><span data-stu-id="71126-181">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-182">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="71126-182">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="71126-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-184">Квалификаторы: **вмидатаид** (12)</span><span class="sxs-lookup"><span data-stu-id="71126-184">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="71126-185">Количество используемых и свободных кластеров в томе.</span><span class="sxs-lookup"><span data-stu-id="71126-185">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="71126-186">**волумикст**</span><span class="sxs-lookup"><span data-stu-id="71126-186">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71126-187">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71126-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71126-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71126-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71126-189">Квалификаторы: **вмидатаид** (14)</span><span class="sxs-lookup"><span data-stu-id="71126-189">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="71126-190">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="71126-190">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71126-191">Требования</span><span class="sxs-lookup"><span data-stu-id="71126-191">Requirements</span></span>



| <span data-ttu-id="71126-192">Требование</span><span class="sxs-lookup"><span data-stu-id="71126-192">Requirement</span></span> | <span data-ttu-id="71126-193">Значение</span><span class="sxs-lookup"><span data-stu-id="71126-193">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="71126-194">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71126-194">Minimum supported client</span></span><br/> | <span data-ttu-id="71126-195">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="71126-195">None supported</span></span><br/>                            |
| <span data-ttu-id="71126-196">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71126-196">Minimum supported server</span></span><br/> | <span data-ttu-id="71126-197">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71126-197">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71126-198">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71126-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71126-199">**Системконфиг \_ v0**</span><span class="sxs-lookup"><span data-stu-id="71126-199">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




