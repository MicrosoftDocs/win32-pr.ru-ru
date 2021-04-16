---
description: Допустимые типы разделов, используемые драйверами дисков.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Типы разделов диска (Виниоктл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664279"
---
# <a name="disk-partition-types"></a><span data-ttu-id="88e77-103">Типы разделов диска</span><span class="sxs-lookup"><span data-stu-id="88e77-103">Disk Partition Types</span></span>

<span data-ttu-id="88e77-104">В следующей таблице указаны допустимые типы разделов, используемые драйверами дисков.</span><span class="sxs-lookup"><span data-stu-id="88e77-104">The following table identifies the valid partition types that are used by disk drivers.</span></span>



| <span data-ttu-id="88e77-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="88e77-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="88e77-106">Описание</span><span class="sxs-lookup"><span data-stu-id="88e77-106">Description</span></span>                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <span data-ttu-id="88e77-107"><dt>**Раздел \_ \_Неиспользуемая запись**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="88e77-107"><dt>**PARTITION\_ENTRY\_UNUSED**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="88e77-108">Неиспользуемая Секция записи.</span><span class="sxs-lookup"><span data-stu-id="88e77-108">An unused entry partition.</span></span><br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <span data-ttu-id="88e77-109"><dt>**Раздел \_ Расширенные**</dt> <dt>0x05</dt></span><span class="sxs-lookup"><span data-stu-id="88e77-109"><dt>**PARTITION\_EXTENDED**</dt> <dt>0x05</dt></span></span> </dl>              | <span data-ttu-id="88e77-110">Дополнительный раздел.</span><span class="sxs-lookup"><span data-stu-id="88e77-110">An extended partition.</span></span><br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <span data-ttu-id="88e77-111"><dt>**Раздел \_ FAT \_ 12**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="88e77-111"><dt>**PARTITION\_FAT\_12**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="88e77-112">Раздел FAT12 файловой системы.</span><span class="sxs-lookup"><span data-stu-id="88e77-112">A FAT12 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <span data-ttu-id="88e77-113"><dt>**Раздел \_ 0x04 FAT \_ 16**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="88e77-113"><dt>**PARTITION\_FAT\_16**</dt> <dt>0x04</dt></span></span> </dl>                   | <span data-ttu-id="88e77-114">Раздел файловой системы FAT16.</span><span class="sxs-lookup"><span data-stu-id="88e77-114">A FAT16 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <span data-ttu-id="88e77-115"><dt>**Раздел \_**</dt> <dt>0x0B</dt> FAT32</span><span class="sxs-lookup"><span data-stu-id="88e77-115"><dt>**PARTITION\_FAT32**</dt> <dt>0x0B</dt></span></span> </dl>                       | <span data-ttu-id="88e77-116">Раздел файловой системы FAT32.</span><span class="sxs-lookup"><span data-stu-id="88e77-116">A FAT32 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <span data-ttu-id="88e77-117"><dt>**Раздел \_**</dt> <dt>0x07</dt> IFS</span><span class="sxs-lookup"><span data-stu-id="88e77-117"><dt>**PARTITION\_IFS**</dt> <dt>0x07</dt></span></span> </dl>                             | <span data-ttu-id="88e77-118">Раздел IFS.</span><span class="sxs-lookup"><span data-stu-id="88e77-118">An IFS partition.</span></span><br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <span data-ttu-id="88e77-119"><dt>**Раздел \_**</dt> <dt>0x42</dt> LDM</span><span class="sxs-lookup"><span data-stu-id="88e77-119"><dt>**PARTITION\_LDM**</dt> <dt>0x42</dt></span></span> </dl>                             | <span data-ttu-id="88e77-120">Раздел диспетчера логических дисков (LDM).</span><span class="sxs-lookup"><span data-stu-id="88e77-120">A logical disk manager (LDM) partition.</span></span><br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <span data-ttu-id="88e77-121"><dt>**Раздел \_ НТФТ**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="88e77-121"><dt>**PARTITION\_NTFT**</dt> <dt>0x80</dt></span></span> </dl>                          | <span data-ttu-id="88e77-122">Секция НТФТ.</span><span class="sxs-lookup"><span data-stu-id="88e77-122">An NTFT partition.</span></span><br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <span data-ttu-id="88e77-123"><dt>**Допустимое \_ НТФТ**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="88e77-123"><dt>**VALID\_NTFT**</dt> <dt>0xC0</dt></span></span> </dl>                                      | <span data-ttu-id="88e77-124">Допустимая Секция НТФТ.</span><span class="sxs-lookup"><span data-stu-id="88e77-124">A valid NTFT partition.</span></span><br/> <span data-ttu-id="88e77-125">Старший бит кода типа секции указывает на то, что Секция является частью зеркального или чередующегося массива НТФТ.</span><span class="sxs-lookup"><span data-stu-id="88e77-125">The high bit of a partition type code indicates that a partition is part of an NTFT mirror or striped array.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="88e77-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88e77-126">Remarks</span></span>

<span data-ttu-id="88e77-127">Существует несколько макросов, которые могут помочь при обнаружении типа раздела: **исконтаинерпартитион**, **исфтпартитион** и **исрекогнизедпартитион**.</span><span class="sxs-lookup"><span data-stu-id="88e77-127">There are several macros that can help you detect the partition type: **IsContainerPartition**, **IsFTPartition**, and **IsRecognizedPartition**.</span></span> <span data-ttu-id="88e77-128">Дополнительные сведения см. в разделе Виниоктл. h.</span><span class="sxs-lookup"><span data-stu-id="88e77-128">For more information, see WinIoCtl.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e77-129">Требования</span><span class="sxs-lookup"><span data-stu-id="88e77-129">Requirements</span></span>



| <span data-ttu-id="88e77-130">Требование</span><span class="sxs-lookup"><span data-stu-id="88e77-130">Requirement</span></span> | <span data-ttu-id="88e77-131">Значение</span><span class="sxs-lookup"><span data-stu-id="88e77-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88e77-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88e77-132">Minimum supported client</span></span><br/> | <span data-ttu-id="88e77-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="88e77-133">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="88e77-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88e77-134">Minimum supported server</span></span><br/> | <span data-ttu-id="88e77-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="88e77-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="88e77-136">Header</span><span class="sxs-lookup"><span data-stu-id="88e77-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="88e77-137"><dt>Виниоктл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88e77-137"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88e77-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88e77-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e77-139">**\_сведения о разделах, \_ например**</span><span class="sxs-lookup"><span data-stu-id="88e77-139">**PARTITION\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[<span data-ttu-id="88e77-140">**\_ \_ Основная загрузочная запись о разделах**</span><span class="sxs-lookup"><span data-stu-id="88e77-140">**PARTITION\_INFORMATION\_MBR**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[<span data-ttu-id="88e77-141">**Задание \_ \_ сведений о секции**</span><span class="sxs-lookup"><span data-stu-id="88e77-141">**SET\_PARTITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




