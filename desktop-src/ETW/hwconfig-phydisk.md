---
description: Класс Хвконфиг \_ фидиск является классом типа событий для событий конфигурации физического диска. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: Класс HWConfig_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984488"
---
# <a name="hwconfig_phydisk-class"></a><span data-ttu-id="4c7f4-104">\_Класс хвконфиг фидиск</span><span class="sxs-lookup"><span data-stu-id="4c7f4-104">HWConfig\_PhyDisk class</span></span>

<span data-ttu-id="4c7f4-105">Класс **хвконфиг \_ фидиск** является классом типа событий для событий конфигурации физического диска.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-105">The **HWConfig\_PhyDisk** class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="4c7f4-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c7f4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c7f4-107">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
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
  string Manufacturer;
};
```

## <a name="members"></a><span data-ttu-id="4c7f4-108">Участники</span><span class="sxs-lookup"><span data-stu-id="4c7f4-108">Members</span></span>

<span data-ttu-id="4c7f4-109">Класс **хвконфиг \_ фидиск** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4c7f4-109">The **HWConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="4c7f4-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c7f4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c7f4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c7f4-111">Properties</span></span>

<span data-ttu-id="4c7f4-112">Класс **хвконфиг \_ фидиск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-112">The **HWConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c7f4-113">битесперсектор</span><span class="sxs-lookup"><span data-stu-id="4c7f4-113">BytesPerSector</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c7f4-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c7f4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-116">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="4c7f4-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4c7f4-117">Число байтов в каждом секторе для физического диска.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-117">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="4c7f4-118">Цилиндров</span><span class="sxs-lookup"><span data-stu-id="4c7f4-118">Cylinders</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c7f4-119">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c7f4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-121">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="4c7f4-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="4c7f4-122">Общее число цилиндров на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-122">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="4c7f4-123">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-123">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="4c7f4-124">Значение может быть неточным, если диск использует схему перевода для поддержки размера дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-124">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="4c7f4-125">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-125">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="4c7f4-126">дискнумбер</span><span class="sxs-lookup"><span data-stu-id="4c7f4-126">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c7f4-127">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c7f4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-129">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="4c7f4-129">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="4c7f4-130">Номер индекса диска, содержащего этот раздел.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-130">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="4c7f4-131">Изготовитель</span><span class="sxs-lookup"><span data-stu-id="4c7f4-131">Manufacturer</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c7f4-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c7f4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-134">Квалификаторы: Вмидатаид (10), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="4c7f4-134">Qualifiers: WmiDataId(10), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="4c7f4-135">Имя изготовителя диска.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-135">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="4c7f4-136">сксилун</span><span class="sxs-lookup"><span data-stu-id="4c7f4-136">SCSILun</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c7f4-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c7f4-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-139">Квалификаторы: Вмидатаид (9)</span><span class="sxs-lookup"><span data-stu-id="4c7f4-139">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="4c7f4-140">Логический номер устройства (LUN) SCSI адаптера SCSI.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-140">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4c7f4-141">сксипас</span><span class="sxs-lookup"><span data-stu-id="4c7f4-141">SCSIPath</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c7f4-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c7f4-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-144">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="4c7f4-144">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="4c7f4-145">Номер шины SCSI адаптера SCSI.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-145">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4c7f4-146">SCSIPort</span><span class="sxs-lookup"><span data-stu-id="4c7f4-146">SCSIPort</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c7f4-147">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c7f4-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-149">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="4c7f4-149">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="4c7f4-150">Номер SCSI адаптера SCSI.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-150">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4c7f4-151">скситаржет</span><span class="sxs-lookup"><span data-stu-id="4c7f4-151">SCSITarget</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c7f4-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c7f4-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-154">Квалификаторы: Вмидатаид (8)</span><span class="sxs-lookup"><span data-stu-id="4c7f4-154">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="4c7f4-155">Содержит номер целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-155">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="4c7f4-156">секторспертракк</span><span class="sxs-lookup"><span data-stu-id="4c7f4-156">SectorsPerTrack</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c7f4-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c7f4-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-159">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="4c7f4-159">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="4c7f4-160">Количество секторов в каждой дорожке для этого физического диска.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-160">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="4c7f4-161">TracksPerCylinder</span><span class="sxs-lookup"><span data-stu-id="4c7f4-161">TracksPerCylinder</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c7f4-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c7f4-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c7f4-164">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="4c7f4-164">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="4c7f4-165">Количество дорожек в каждом цилиндре на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-165">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="4c7f4-166">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-166">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="4c7f4-167">Значение может быть неточным, если диск использует схему перевода для поддержки размера дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-167">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="4c7f4-168">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-168">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c7f4-169">Требования</span><span class="sxs-lookup"><span data-stu-id="4c7f4-169">Requirements</span></span>



| <span data-ttu-id="4c7f4-170">Требование</span><span class="sxs-lookup"><span data-stu-id="4c7f4-170">Requirement</span></span> | <span data-ttu-id="4c7f4-171">Значение</span><span class="sxs-lookup"><span data-stu-id="4c7f4-171">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="4c7f4-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c7f4-172">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7f4-173">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4c7f4-173">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4c7f4-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c7f4-174">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7f4-175">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4c7f4-175">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="4c7f4-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c7f4-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c7f4-177">**хвконфиг**</span><span class="sxs-lookup"><span data-stu-id="4c7f4-177">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




