---
description: 'Дополнительные сведения: <span id=vhd.vhd_functions></span> функции виртуального диска'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Функции виртуального диска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f31af2b24a55baa3c64bfe5bd9e09e0b9e2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692325"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span data-ttu-id="26f5f-103"><span id="vhd.vhd_functions"></span>Функции виртуального диска</span><span class="sxs-lookup"><span data-stu-id="26f5f-103"><span id="vhd.vhd_functions"></span>Virtual Disk Functions</span></span>

<span data-ttu-id="26f5f-104">В виртуальных дисках используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="26f5f-104">The following functions are used in Virtual Disks:</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="26f5f-105"><span id="in_this_section"></span>В этом разделе</span><span class="sxs-lookup"><span data-stu-id="26f5f-105"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26f5f-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="26f5f-106">Topic</span></span></th>
<th><span data-ttu-id="26f5f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="26f5f-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>апплиснапшотвхдсет</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-109">Применение моментального снимка текущего виртуального диска для файлов набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="26f5f-109">Applies a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>аддвиртуалдискпарент</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-111">Присоединяет родительский объект к виртуальному диску, открытому с флагом <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</span><span class="sxs-lookup"><span data-stu-id="26f5f-111">Attaches a parent to a virtual disk opened with the <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>аттачвиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-113">Подключает виртуальный жесткий диск (VHD) или файл образа диска DVD (ISO), находя соответствующий поставщик VHD для выполнения вложения.</span><span class="sxs-lookup"><span data-stu-id="26f5f-113">Attaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate VHD provider to accomplish the attachment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>бреакмиррорвиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-115">Прерывает ранее инициированную операцию зеркального отображения и устанавливает зеркальное отображение в качестве активного виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="26f5f-115">Breaks a previously initiated mirror operation and sets the mirror to be the active virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>компактвиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-117">Уменьшает размер файла резервного хранилища виртуального жесткого диска (VHD).</span><span class="sxs-lookup"><span data-stu-id="26f5f-117">Reduces the size of a virtual hard disk (VHD) backing store file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>креатевиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-119">Создает файл образа виртуального жесткого диска (VHD) либо с помощью параметров по умолчанию, либо с помощью существующего виртуального диска или физического диска.</span><span class="sxs-lookup"><span data-stu-id="26f5f-119">Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing virtual disk or physical disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>делетеснапшотвхдсет</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-121">Удаляет моментальный снимок из файла набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="26f5f-121">Deletes a snapshot from a VHD Set file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>делетевиртуалдискметадата</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-123">Удаляет метаданные с виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="26f5f-123">Deletes metadata from a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>детачвиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-125">Отсоединяет виртуальный жесткий диск (VHD) или файл образа компакт-диска или DVD, находя соответствующий поставщик виртуальных дисков для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="26f5f-125">Detaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate virtual disk provider to accomplish the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>енумератевиртуалдискметадата</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-127">Перечисляет метаданные, связанные с виртуальным диском.</span><span class="sxs-lookup"><span data-stu-id="26f5f-127">Enumerates the metadata associated with a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>експандвиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-129">Увеличивает размер фиксированного или динамически расширяемого виртуального жесткого диска (VHD).</span><span class="sxs-lookup"><span data-stu-id="26f5f-129">Increases the size of a fixed or dynamically expandable virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>жетсторажедепенденциинформатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-131">Возвращает связи между виртуальными жесткими дисками (VHD) или файлом образа компакт-диска или диска DVD (ISO) или томами, содержащимися на этих дисках, и их родительским диском или томом.</span><span class="sxs-lookup"><span data-stu-id="26f5f-131">Returns the relationships between virtual hard disks (VHDs) or CD or DVD image file (ISO) or the volumes contained within those disks and their parent disk or volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>жетвиртуалдискинформатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-133">Извлекает сведения о виртуальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="26f5f-133">Retrieves information about a VHD.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>жетвиртуалдискметадата</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-135">Извлекает указанные метаданные из виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="26f5f-135">Retrieves the specified metadata from the virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>жетвиртуалдископератионпрогресс</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-137">Проверяет ход выполнения асинхронной операции виртуального жесткого диска (VHD).</span><span class="sxs-lookup"><span data-stu-id="26f5f-137">Checks the progress of an asynchronous virtual hard disk (VHD) operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>жетвиртуалдискфисикалпас</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-139">Извлекает путь к объекту физического устройства, который содержит виртуальный жесткий диск (VHD) или файл образа компакт-диска или диска DVD (ISO).</span><span class="sxs-lookup"><span data-stu-id="26f5f-139">Retrieves the path to the physical device object that contains a virtual hard disk (VHD) or CD or DVD image file (ISO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>мержевиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-141">Слияние дочернего виртуального жесткого диска (VHD) в цепочке разностного с одним или несколькими родительскими виртуальными дисками в цепочке.</span><span class="sxs-lookup"><span data-stu-id="26f5f-141">Merges a child virtual hard disk (VHD) in a differencing chain with one or more parent virtual disks in the chain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>миррорвиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-143">Инициирует операцию зеркального отображения для виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="26f5f-143">Initiates a mirror operation for a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>модифивхдсет</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-145">Изменяет внутреннее содержимое файла виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="26f5f-145">Modifies the internal contents of a virtual disk file.</span></span> <span data-ttu-id="26f5f-146">Можно использовать для установки активного листа или для исправления записей моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="26f5f-146">Can be used to set the active leaf, or to fix up snapshot entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>опенвиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-148">Открывает виртуальный жесткий диск (VHD) или файл образа компакт-диска или диска DVD (ISO) для использования.</span><span class="sxs-lookup"><span data-stu-id="26f5f-148">Opens a virtual hard disk (VHD) or CD or DVD image file (ISO) for use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>куеричанжесвиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-150">Извлекает сведения об изменениях в указанных областях виртуального жесткого диска (VHD), которые отслеживаются с помощью отказоустойчивого отслеживания изменений (RCT).</span><span class="sxs-lookup"><span data-stu-id="26f5f-150">Retrieves information about changes to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>равсксивиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-152">Выдает встроенный SCSI-запрос непосредственно на виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="26f5f-152">Issues an embedded SCSI request directly to a virtual hard disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ресизевиртуалдиск</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-154">Изменяет размер виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="26f5f-154">Resizes a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>сетвиртуалдискинформатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-156">Задает сведения о виртуальном жестком диске (VHD).</span><span class="sxs-lookup"><span data-stu-id="26f5f-156">Sets information about a virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f5f-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>сетвиртуалдискметадата</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-158">Задает элемент метаданных для виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="26f5f-158">Sets a metadata item for a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f5f-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>такеснапшотвхдсет</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f5f-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="26f5f-160">Создает моментальный снимок текущего виртуального диска для файлов набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="26f5f-160">Creates a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 
