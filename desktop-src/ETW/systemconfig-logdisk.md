---
description: SystemConfig_LogDisk класс — этот класс является классом типа события для событий конфигурации логического диска.
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: Класс SystemConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_LogDisk
- SystemConfig_LogDisk.StartOffset
- SystemConfig_LogDisk.PartitionSize
- SystemConfig_LogDisk.DiskNumber
- SystemConfig_LogDisk.Size
- SystemConfig_LogDisk.DriveType
- SystemConfig_LogDisk.DriveLetterString
- SystemConfig_LogDisk.Pad1
- SystemConfig_LogDisk.PartitionNumber
- SystemConfig_LogDisk.SectorsPerCluster
- SystemConfig_LogDisk.BytesPerSector
- SystemConfig_LogDisk.Pad2
- SystemConfig_LogDisk.NumberOfFreeClusters
- SystemConfig_LogDisk.TotalNumberOfClusters
- SystemConfig_LogDisk.FileSystem
- SystemConfig_LogDisk.VolumeExt
- SystemConfig_LogDisk.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1d7ca8dc3f632e88c250715292a27e18ff36e3af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106112"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="b5f0a-103">\_Класс системконфиг логдиск</span><span class="sxs-lookup"><span data-stu-id="b5f0a-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="b5f0a-104">Этот класс является классом типа событий для событий конфигурации логического диска.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="b5f0a-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f0a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5f0a-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_LogDisk : SystemConfig
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad1;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  uint32 Pad2;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
  uint32 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="b5f0a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="b5f0a-107">Members</span></span>

<span data-ttu-id="b5f0a-108">Класс **системконфиг \_ логдиск** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b5f0a-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="b5f0a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="b5f0a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5f0a-110">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="b5f0a-110">Properties</span></span>

<span data-ttu-id="b5f0a-111">Класс **системконфиг \_ логдиск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5f0a-112">**битесперсектор**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-115">Квалификаторы: **вмидатаид** (10)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-116">Число байтов в каждом секторе для физического диска.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-117">**дискнумбер**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-120">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-121">Номер индекса диска, содержащего этот раздел.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-122">**дривелеттерстринг**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-123">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-125">Квалификаторы: **вмидатаид** (6), **Max** (4), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-126">Буква диска в формате " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="b5f0a-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-128">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-130">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-131">Тип диска.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-131">Type of disk drive.</span></span> <span data-ttu-id="b5f0a-132">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b5f0a-132">Possible values are:</span></span>



| <span data-ttu-id="b5f0a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b5f0a-133">Value</span></span>                                                                        | <span data-ttu-id="b5f0a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b5f0a-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="b5f0a-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b5f0a-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b5f0a-136">Partition (Раздел)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="b5f0a-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b5f0a-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b5f0a-138">Том</span><span class="sxs-lookup"><span data-stu-id="b5f0a-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="b5f0a-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b5f0a-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b5f0a-140">Дополнительный раздел на нескольких дисках</span><span class="sxs-lookup"><span data-stu-id="b5f0a-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b5f0a-141">**Системой**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-142">Тип данных: **Char16**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-144">Квалификаторы: **вмидатаид** (14), **Max** (16), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-145">Файловая система на логическом диске, например NTFS.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-146">**нумбероффриклустерс**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-147">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-149">Квалификаторы: **вмидатаид** (12)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-150">Количество свободных кластеров в указанном томе.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-154">Квалификаторы: **вмидатаид** (7)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-155">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-159">Квалификаторы: **вмидатаид** (11)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-160">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-164">Квалификаторы: **вмидатаид** (16)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-165">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-167">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-169">Квалификаторы: **вмидатаид** (8)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-170">Номер индекса секции.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-172">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-174">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-175">Общий размер секции в байтах.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-176">**секторсперклустер**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-177">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-179">Квалификаторы: **вмидатаид** (9)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-180">Количество секторов в томе.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-181">**Размер**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-182">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-184">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-185">Размер диска в байтах.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-186">**стартоффсет**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-187">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-189">Квалификаторы: **вмидатаид** (1)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-190">Начальное смещение (в байтах) секции от начала диска.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-191">**тоталнумберофклустерс**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-192">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-194">Квалификаторы: **вмидатаид** (13)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-195">Количество используемых и свободных кластеров в томе.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0a-196">**волумикст**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f0a-197">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5f0a-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f0a-199">Квалификаторы: **вмидатаид** (15)</span><span class="sxs-lookup"><span data-stu-id="b5f0a-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="b5f0a-200">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="b5f0a-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5f0a-201">Требования</span><span class="sxs-lookup"><span data-stu-id="b5f0a-201">Requirements</span></span>



| <span data-ttu-id="b5f0a-202">Требование</span><span class="sxs-lookup"><span data-stu-id="b5f0a-202">Requirement</span></span> | <span data-ttu-id="b5f0a-203">Значение</span><span class="sxs-lookup"><span data-stu-id="b5f0a-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b5f0a-204">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5f0a-204">Minimum supported client</span></span><br/> | <span data-ttu-id="b5f0a-205">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5f0a-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b5f0a-206">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5f0a-206">Minimum supported server</span></span><br/> | <span data-ttu-id="b5f0a-207">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b5f0a-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5f0a-208">См. также</span><span class="sxs-lookup"><span data-stu-id="b5f0a-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f0a-209">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="b5f0a-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




