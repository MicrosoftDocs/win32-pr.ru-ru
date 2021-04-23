---
description: Windows Server 2008 R2.
ms.assetid: 4ab37529-8d56-47a3-ad3d-0197cabd4f87
title: Новые возможности службы виртуальных дисков в Windows Server 2008 R2 и Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4ab0054697457dd67028df2b888b1ea68784427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674455"
---
# <a name="whats-new-in-vds-in-windows-server-2008-r2-and-windows-7"></a><span data-ttu-id="64ede-103">Новые возможности службы виртуальных дисков в Windows Server 2008 R2 и Windows 7</span><span class="sxs-lookup"><span data-stu-id="64ede-103">What's New in VDS in Windows Server 2008 R2 and Windows 7</span></span>

<span data-ttu-id="64ede-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="64ede-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="64ede-105">В Windows Server 2008 R2 и Windows 7 внесены следующие изменения в службу виртуальных дисков (VDS):</span><span class="sxs-lookup"><span data-stu-id="64ede-105">Windows Server 2008 R2 and Windows 7 introduce the following changes to the Virtual Disk Service (VDS):</span></span>

- [<span data-ttu-id="64ede-106">Новые интерфейсы VDS</span><span class="sxs-lookup"><span data-stu-id="64ede-106">New VDS Interfaces</span></span>](#new-vds-interfaces)
- [<span data-ttu-id="64ede-107">Новые перечисления VDS</span><span class="sxs-lookup"><span data-stu-id="64ede-107">New VDS Enumerations</span></span>](#new-vds-enumerations)
- [<span data-ttu-id="64ede-108">Новые структуры VDS</span><span class="sxs-lookup"><span data-stu-id="64ede-108">New VDS Structures</span></span>](#new-vds-structures)
- [<span data-ttu-id="64ede-109">Изменения в существующих перечислениях VDS</span><span class="sxs-lookup"><span data-stu-id="64ede-109">Modifications to Existing VDS Enumerations</span></span>](#modifications-to-existing-vds-enumerations)
- [<span data-ttu-id="64ede-110">Изменения в существующих структурах VDS</span><span class="sxs-lookup"><span data-stu-id="64ede-110">Modifications to Existing VDS Structures</span></span>](#modifications-to-existing-vds-structures)

## <a name="new-vds-interfaces"></a><span data-ttu-id="64ede-111">Новые интерфейсы VDS</span><span class="sxs-lookup"><span data-stu-id="64ede-111">New VDS Interfaces</span></span>

<dl>

[<span data-ttu-id="64ede-112">**IVdsDisk3**</span><span class="sxs-lookup"><span data-stu-id="64ede-112">**IVdsDisk3**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk3)  
[<span data-ttu-id="64ede-113">**IVdsDiskPartitionMF2**</span><span class="sxs-lookup"><span data-stu-id="64ede-113">**IVdsDiskPartitionMF2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)  
[<span data-ttu-id="64ede-114">**IVdsDrive2**</span><span class="sxs-lookup"><span data-stu-id="64ede-114">**IVdsDrive2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdrive2)  
[<span data-ttu-id="64ede-115">**ивдшвпровидерсторажепулс**</span><span class="sxs-lookup"><span data-stu-id="64ede-115">**IVdsHwProviderStoragePools**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)  
[<span data-ttu-id="64ede-116">**IVdsLun2**</span><span class="sxs-lookup"><span data-stu-id="64ede-116">**IVdsLun2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslun2)  
[<span data-ttu-id="64ede-117">**ивдслуннумбер**</span><span class="sxs-lookup"><span data-stu-id="64ede-117">**IVdsLunNumber**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)  
[<span data-ttu-id="64ede-118">**ивдсопенвдиск**</span><span class="sxs-lookup"><span data-stu-id="64ede-118">**IVdsOpenVDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsopenvdisk)  
[<span data-ttu-id="64ede-119">**ивдссторажепул**</span><span class="sxs-lookup"><span data-stu-id="64ede-119">**IVdsStoragePool**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)  
[<span data-ttu-id="64ede-120">**IVdsSubSystem2**</span><span class="sxs-lookup"><span data-stu-id="64ede-120">**IVdsSubSystem2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdssubsystem2)  
[<span data-ttu-id="64ede-121">**ивдссубсистеминтерконнект**</span><span class="sxs-lookup"><span data-stu-id="64ede-121">**IVdsSubSystemInterconnect**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdssubsysteminterconnect)  
[<span data-ttu-id="64ede-122">**ивдсвдиск**</span><span class="sxs-lookup"><span data-stu-id="64ede-122">**IVdsVDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvdisk)  
[<span data-ttu-id="64ede-123">**ивдсвдпровидер**</span><span class="sxs-lookup"><span data-stu-id="64ede-123">**IVdsVdProvider**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvdprovider)  
[<span data-ttu-id="64ede-124">**IVdsVolume2**</span><span class="sxs-lookup"><span data-stu-id="64ede-124">**IVdsVolume2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvolume2)  
[<span data-ttu-id="64ede-125">**IVdsVolumeMF3**</span><span class="sxs-lookup"><span data-stu-id="64ede-125">**IVdsVolumeMF3**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf3)  


## <a name="new-vds-enumerations"></a><span data-ttu-id="64ede-126">Новые перечисления VDS</span><span class="sxs-lookup"><span data-stu-id="64ede-126">New VDS Enumerations</span></span>

<dl>

[<span data-ttu-id="64ede-127">**VDS_DISK_OFFLINE_REASON**</span><span class="sxs-lookup"><span data-stu-id="64ede-127">**VDS_DISK_OFFLINE_REASON**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_disk_offline_reason)  
[<span data-ttu-id="64ede-128">**VDS_FORMAT_OPTION_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="64ede-128">**VDS_FORMAT_OPTION_FLAGS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_format_option_flags)  
[<span data-ttu-id="64ede-129">**VDS_INTERCONNECT_FLAG**</span><span class="sxs-lookup"><span data-stu-id="64ede-129">**VDS_INTERCONNECT_FLAG**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_interconnect_flag)  
[<span data-ttu-id="64ede-130">**VDS_RAID_TYPE**</span><span class="sxs-lookup"><span data-stu-id="64ede-130">**VDS_RAID_TYPE**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_raid_type)  
[<span data-ttu-id="64ede-131">**VDS_STORAGE_POOL_STATUS**</span><span class="sxs-lookup"><span data-stu-id="64ede-131">**VDS_STORAGE_POOL_STATUS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)  
[<span data-ttu-id="64ede-132">**VDS_STORAGE_POOL_TYPE**</span><span class="sxs-lookup"><span data-stu-id="64ede-132">**VDS_STORAGE_POOL_TYPE**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type)  
[<span data-ttu-id="64ede-133">**VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG**</span><span class="sxs-lookup"><span data-stu-id="64ede-133">**VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_sub_system_supported_raid_type_flag)  
[<span data-ttu-id="64ede-134">**VDS_VDISK_STATE**</span><span class="sxs-lookup"><span data-stu-id="64ede-134">**VDS_VDISK_STATE**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_vdisk_state)  


## <a name="new-vds-structures"></a><span data-ttu-id="64ede-135">Новые структуры VDS</span><span class="sxs-lookup"><span data-stu-id="64ede-135">New VDS Structures</span></span>

<dl>

[<span data-ttu-id="64ede-136">**VDS_CREATE_VDISK_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="64ede-136">**VDS_CREATE_VDISK_PARAMETERS**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_create_vdisk_parameters)  
[<span data-ttu-id="64ede-137">**VDS_DISK_FREE_EXTENT**</span><span class="sxs-lookup"><span data-stu-id="64ede-137">**VDS_DISK_FREE_EXTENT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_disk_free_extent)  
[<span data-ttu-id="64ede-138">**VDS_DISK_PROP2**</span><span class="sxs-lookup"><span data-stu-id="64ede-138">**VDS_DISK_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_disk_prop2)  
[<span data-ttu-id="64ede-139">**VDS_DRIVE_PROP2**</span><span class="sxs-lookup"><span data-stu-id="64ede-139">**VDS_DRIVE_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_drive_prop2)  
[<span data-ttu-id="64ede-140">**VDS_HINTS2**</span><span class="sxs-lookup"><span data-stu-id="64ede-140">**VDS_HINTS2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_hints2)  
[<span data-ttu-id="64ede-141">**VDS_POOL_ATTRIBUTES**</span><span class="sxs-lookup"><span data-stu-id="64ede-141">**VDS_POOL_ATTRIBUTES**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes)  
[<span data-ttu-id="64ede-142">**VDS_POOL_CUSTOM_ATTRIBUTES**</span><span class="sxs-lookup"><span data-stu-id="64ede-142">**VDS_POOL_CUSTOM_ATTRIBUTES**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes)  
[<span data-ttu-id="64ede-143">**VDS_STORAGE_POOL_DRIVE_EXTENT**</span><span class="sxs-lookup"><span data-stu-id="64ede-143">**VDS_STORAGE_POOL_DRIVE_EXTENT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)  
[<span data-ttu-id="64ede-144">**VDS_STORAGE_POOL_PROP**</span><span class="sxs-lookup"><span data-stu-id="64ede-144">**VDS_STORAGE_POOL_PROP**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop)  
[<span data-ttu-id="64ede-145">**VDS_SUB_SYSTEM_PROP2**</span><span class="sxs-lookup"><span data-stu-id="64ede-145">**VDS_SUB_SYSTEM_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop2)  
[<span data-ttu-id="64ede-146">**VDS_VDISK_PROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="64ede-146">**VDS_VDISK_PROPERTIES**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_vdisk_properties)  
[<span data-ttu-id="64ede-147">**VDS_VOLUME_PROP2**</span><span class="sxs-lookup"><span data-stu-id="64ede-147">**VDS_VOLUME_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_volume_prop)  


## <a name="modifications-to-existing-vds-enumerations"></a><span data-ttu-id="64ede-148">Изменения в существующих перечислениях VDS</span><span class="sxs-lookup"><span data-stu-id="64ede-148">Modifications to Existing VDS Enumerations</span></span>

<span data-ttu-id="64ede-149">[**VDS_ASYNC_OUTPUT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_async_output_type) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-149">[**VDS_ASYNC_OUTPUT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_async_output_type) enumeration added values:</span></span>

 <span data-ttu-id="64ede-150">**VDS_ASYNCOUT_CREATE_VDISK**</span><span class="sxs-lookup"><span data-stu-id="64ede-150">**VDS_ASYNCOUT_CREATE_VDISK**</span></span>  
<span data-ttu-id="64ede-151">**VDS_ASYNCOUT_ATTACH_VDISK**</span><span class="sxs-lookup"><span data-stu-id="64ede-151">**VDS_ASYNCOUT_ATTACH_VDISK**</span></span>  
<span data-ttu-id="64ede-152">**VDS_ASYNCOUT_COMPACT_VDISK**</span><span class="sxs-lookup"><span data-stu-id="64ede-152">**VDS_ASYNCOUT_COMPACT_VDISK**</span></span>  
<span data-ttu-id="64ede-153">**VDS_ASYNCOUT_MERGE_VDISK**</span><span class="sxs-lookup"><span data-stu-id="64ede-153">**VDS_ASYNCOUT_MERGE_VDISK**</span></span>  
<span data-ttu-id="64ede-154">**VDS_ASYNCOUT_EXPAND_VDISK**</span><span class="sxs-lookup"><span data-stu-id="64ede-154">**VDS_ASYNCOUT_EXPAND_VDISK**</span></span>  


<span data-ttu-id="64ede-155">[**VDS_CONTROLLER_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status) добавлено значение перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-155">[**VDS_CONTROLLER_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status) enumeration added value:</span></span>

<span data-ttu-id="64ede-156">**VDS_CS_REMOVED**</span><span class="sxs-lookup"><span data-stu-id="64ede-156">**VDS_CS_REMOVED**</span></span>  


<span data-ttu-id="64ede-157">[**VDS_DISK_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) добавлено значение перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-157">[**VDS_DISK_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) enumeration added value:</span></span>

<span data-ttu-id="64ede-158">**VDS_DF_BOOT_FROM_DISK**</span><span class="sxs-lookup"><span data-stu-id="64ede-158">**VDS_DF_BOOT_FROM_DISK**</span></span>  
<span data-ttu-id="64ede-159">**VDS_DF_CURRENT_READ_ONLY**</span><span class="sxs-lookup"><span data-stu-id="64ede-159">**VDS_DF_CURRENT_READ_ONLY**</span></span>  


<span data-ttu-id="64ede-160">[**VDS_DRIVE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-160">[**VDS_DRIVE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) enumeration added values:</span></span>

<span data-ttu-id="64ede-161">**VDS_DRF_ASSIGNED**</span><span class="sxs-lookup"><span data-stu-id="64ede-161">**VDS_DRF_ASSIGNED**</span></span>  
<span data-ttu-id="64ede-162">**VDS_DRF_UNASSIGNED**</span><span class="sxs-lookup"><span data-stu-id="64ede-162">**VDS_DRF_UNASSIGNED**</span></span>  
<span data-ttu-id="64ede-163">**VDS_DRF_HOTSPARE_IN_USE**</span><span class="sxs-lookup"><span data-stu-id="64ede-163">**VDS_DRF_HOTSPARE_IN_USE**</span></span>  
<span data-ttu-id="64ede-164">**VDS_DRF_HOTSPARE_STANDBY**</span><span class="sxs-lookup"><span data-stu-id="64ede-164">**VDS_DRF_HOTSPARE_STANDBY**</span></span>  


<span data-ttu-id="64ede-165">[**VDS_DRIVE_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status) добавлено значение перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-165">[**VDS_DRIVE_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status) enumeration added value:</span></span>

<span data-ttu-id="64ede-166">**VDS_DRS_REMOVED**</span><span class="sxs-lookup"><span data-stu-id="64ede-166">**VDS_DRS_REMOVED**</span></span>  


<span data-ttu-id="64ede-167">[**VDS_FILE_SYSTEM_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_file_system_type) добавлено значение перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-167">[**VDS_FILE_SYSTEM_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_file_system_type) enumeration added value:</span></span>

<span data-ttu-id="64ede-168">**VDS_FST_EXFAT**</span><span class="sxs-lookup"><span data-stu-id="64ede-168">**VDS_FST_EXFAT**</span></span>  


<span data-ttu-id="64ede-169">[**VDS_HEALTH**](/windows/desktop/api/Vds/ne-vds-vds_health) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-169">[**VDS_HEALTH**](/windows/desktop/api/Vds/ne-vds-vds_health) enumeration added values:</span></span>

<span data-ttu-id="64ede-170">**VDS_H_REPLACED**</span><span class="sxs-lookup"><span data-stu-id="64ede-170">**VDS_H_REPLACED**</span></span>  
<span data-ttu-id="64ede-171">**VDS_H_PENDING_FAILURE**</span><span class="sxs-lookup"><span data-stu-id="64ede-171">**VDS_H_PENDING_FAILURE**</span></span>  
<span data-ttu-id="64ede-172">**VDS_H_DEGRADED**</span><span class="sxs-lookup"><span data-stu-id="64ede-172">**VDS_H_DEGRADED**</span></span>  


<span data-ttu-id="64ede-173">[**VDS_HWPROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hwprovider_type) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-173">[**VDS_HWPROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hwprovider_type) enumeration added values:</span></span>

<span data-ttu-id="64ede-174">**VDS_HWT_SAS**</span><span class="sxs-lookup"><span data-stu-id="64ede-174">**VDS_HWT_SAS**</span></span>  
<span data-ttu-id="64ede-175">**VDS_HWT_HYBRID**</span><span class="sxs-lookup"><span data-stu-id="64ede-175">**VDS_HWT_HYBRID**</span></span>  


<span data-ttu-id="64ede-176">[**VDS_LUN_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-176">[**VDS_LUN_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) enumeration added values:</span></span>

<span data-ttu-id="64ede-177">**VDS_LF_READ_CACHE_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="64ede-177">**VDS_LF_READ_CACHE_ENABLED**</span></span>  
<span data-ttu-id="64ede-178">**VDS_LF_WRITE_CACHE_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="64ede-178">**VDS_LF_WRITE_CACHE_ENABLED**</span></span>  
<span data-ttu-id="64ede-179">**VDS_LF_MEDIA_SCAN_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="64ede-179">**VDS_LF_MEDIA_SCAN_ENABLED**</span></span>  
<span data-ttu-id="64ede-180">**VDS_LF_CONSISTENCY_CHECK_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="64ede-180">**VDS_LF_CONSISTENCY_CHECK_ENABLED**</span></span>  
<span data-ttu-id="64ede-181">**VDS_LF_SNAPSHOT**</span><span class="sxs-lookup"><span data-stu-id="64ede-181">**VDS_LF_SNAPSHOT**</span></span>  


<span data-ttu-id="64ede-182">[**VDS_LUN_PLEX_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-182">[**VDS_LUN_PLEX_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type) enumeration added values:</span></span>

<span data-ttu-id="64ede-183">**VDS_LPT_RAID2**</span><span class="sxs-lookup"><span data-stu-id="64ede-183">**VDS_LPT_RAID2**</span></span>  
<span data-ttu-id="64ede-184">**VDS_LPT_RAID3**</span><span class="sxs-lookup"><span data-stu-id="64ede-184">**VDS_LPT_RAID3**</span></span>  
<span data-ttu-id="64ede-185">**VDS_LPT_RAID4**</span><span class="sxs-lookup"><span data-stu-id="64ede-185">**VDS_LPT_RAID4**</span></span>  
<span data-ttu-id="64ede-186">**VDS_LPT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="64ede-186">**VDS_LPT_RAID5**</span></span>  
<span data-ttu-id="64ede-187">**VDS_LPT_RAID6**</span><span class="sxs-lookup"><span data-stu-id="64ede-187">**VDS_LPT_RAID6**</span></span>  
<span data-ttu-id="64ede-188">**VDS_LPT_RAID03**</span><span class="sxs-lookup"><span data-stu-id="64ede-188">**VDS_LPT_RAID03**</span></span>  
<span data-ttu-id="64ede-189">**VDS_LPT_RAID05**</span><span class="sxs-lookup"><span data-stu-id="64ede-189">**VDS_LPT_RAID05**</span></span>  
<span data-ttu-id="64ede-190">**VDS_LPT_RAID10**</span><span class="sxs-lookup"><span data-stu-id="64ede-190">**VDS_LPT_RAID10**</span></span>  
<span data-ttu-id="64ede-191">**VDS_LPT_RAID15**</span><span class="sxs-lookup"><span data-stu-id="64ede-191">**VDS_LPT_RAID15**</span></span>  
<span data-ttu-id="64ede-192">**VDS_LPT_RAID30**</span><span class="sxs-lookup"><span data-stu-id="64ede-192">**VDS_LPT_RAID30**</span></span>  
<span data-ttu-id="64ede-193">**VDS_LPT_RAID50**</span><span class="sxs-lookup"><span data-stu-id="64ede-193">**VDS_LPT_RAID50**</span></span>  
<span data-ttu-id="64ede-194">**VDS_LPT_RAID53**</span><span class="sxs-lookup"><span data-stu-id="64ede-194">**VDS_LPT_RAID53**</span></span>  
<span data-ttu-id="64ede-195">**VDS_LPT_RAID60**</span><span class="sxs-lookup"><span data-stu-id="64ede-195">**VDS_LPT_RAID60**</span></span>  


<span data-ttu-id="64ede-196">[**VDS_LUN_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_type) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-196">[**VDS_LUN_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_type) enumeration added values:</span></span>

<span data-ttu-id="64ede-197">**VDS_LT_RAID2**</span><span class="sxs-lookup"><span data-stu-id="64ede-197">**VDS_LT_RAID2**</span></span>  
<span data-ttu-id="64ede-198">**VDS_LT_RAID3**</span><span class="sxs-lookup"><span data-stu-id="64ede-198">**VDS_LT_RAID3**</span></span>  
<span data-ttu-id="64ede-199">**VDS_LT_RAID4**</span><span class="sxs-lookup"><span data-stu-id="64ede-199">**VDS_LT_RAID4**</span></span>  
<span data-ttu-id="64ede-200">**VDS_LT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="64ede-200">**VDS_LT_RAID5**</span></span>  
<span data-ttu-id="64ede-201">**VDS_LT_RAID6**</span><span class="sxs-lookup"><span data-stu-id="64ede-201">**VDS_LT_RAID6**</span></span>  
<span data-ttu-id="64ede-202">**VDS_LT_RAID01**</span><span class="sxs-lookup"><span data-stu-id="64ede-202">**VDS_LT_RAID01**</span></span>  
<span data-ttu-id="64ede-203">**VDS_LT_RAID03**</span><span class="sxs-lookup"><span data-stu-id="64ede-203">**VDS_LT_RAID03**</span></span>  
<span data-ttu-id="64ede-204">**VDS_LT_RAID05**</span><span class="sxs-lookup"><span data-stu-id="64ede-204">**VDS_LT_RAID05**</span></span>  
<span data-ttu-id="64ede-205">**VDS_LT_RAID10**</span><span class="sxs-lookup"><span data-stu-id="64ede-205">**VDS_LT_RAID10**</span></span>  
<span data-ttu-id="64ede-206">**VDS_LT_RAID15**</span><span class="sxs-lookup"><span data-stu-id="64ede-206">**VDS_LT_RAID15**</span></span>  
<span data-ttu-id="64ede-207">**VDS_LT_RAID30**</span><span class="sxs-lookup"><span data-stu-id="64ede-207">**VDS_LT_RAID30**</span></span>  
<span data-ttu-id="64ede-208">**VDS_LT_RAID50**</span><span class="sxs-lookup"><span data-stu-id="64ede-208">**VDS_LT_RAID50**</span></span>  
<span data-ttu-id="64ede-209">**VDS_LT_RAID51**</span><span class="sxs-lookup"><span data-stu-id="64ede-209">**VDS_LT_RAID51**</span></span>  
<span data-ttu-id="64ede-210">**VDS_LT_RAID53**</span><span class="sxs-lookup"><span data-stu-id="64ede-210">**VDS_LT_RAID53**</span></span>  
<span data-ttu-id="64ede-211">**VDS_LT_RAID60**</span><span class="sxs-lookup"><span data-stu-id="64ede-211">**VDS_LT_RAID60**</span></span>  
<span data-ttu-id="64ede-212">**VDS_LT_RAID61**</span><span class="sxs-lookup"><span data-stu-id="64ede-212">**VDS_LT_RAID61**</span></span>  


<span data-ttu-id="64ede-213">[**VDS_OBJECT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_object_type) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-213">[**VDS_OBJECT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_object_type) enumeration added values:</span></span>

<span data-ttu-id="64ede-214">**VDS_OT_STORAGE_POOL**</span><span class="sxs-lookup"><span data-stu-id="64ede-214">**VDS_OT_STORAGE_POOL**</span></span>  
<span data-ttu-id="64ede-215">**VDS_OT_VDISK**</span><span class="sxs-lookup"><span data-stu-id="64ede-215">**VDS_OT_VDISK**</span></span>  
<span data-ttu-id="64ede-216">**VDS_OT_OPEN_VDISK**</span><span class="sxs-lookup"><span data-stu-id="64ede-216">**VDS_OT_OPEN_VDISK**</span></span>  


<span data-ttu-id="64ede-217">[**VDS_PORT_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_port_status) добавлено значение перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-217">[**VDS_PORT_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_port_status) enumeration added value:</span></span>

<span data-ttu-id="64ede-218">**VDS_DRS_REMOVED**</span><span class="sxs-lookup"><span data-stu-id="64ede-218">**VDS_DRS_REMOVED**</span></span>  


<span data-ttu-id="64ede-219">[**VDS_PROVIDER_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-219">[**VDS_PROVIDER_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag) enumeration added values:</span></span>

<span data-ttu-id="64ede-220">**VDS_PF_SUPPORT_MIRROR**</span><span class="sxs-lookup"><span data-stu-id="64ede-220">**VDS_PF_SUPPORT_MIRROR**</span></span>  
<span data-ttu-id="64ede-221">**VDS_PF_SUPPORT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="64ede-221">**VDS_PF_SUPPORT_RAID5**</span></span>  


<span data-ttu-id="64ede-222">[**VDS_PROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_provider_type) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-222">[**VDS_PROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_provider_type) enumeration added values:</span></span>

<span data-ttu-id="64ede-223">**VDS_PT_VIRTUALDISK**</span><span class="sxs-lookup"><span data-stu-id="64ede-223">**VDS_PT_VIRTUALDISK**</span></span>  
<span data-ttu-id="64ede-224">**VDS_PT_MAX**</span><span class="sxs-lookup"><span data-stu-id="64ede-224">**VDS_PT_MAX**</span></span>  


<span data-ttu-id="64ede-225">[**VDS_SERVICE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_service_flag) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-225">[**VDS_SERVICE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_service_flag) enumeration added values:</span></span>

<span data-ttu-id="64ede-226">**VDS_SVF_SUPPORT_MIRROR**</span><span class="sxs-lookup"><span data-stu-id="64ede-226">**VDS_SVF_SUPPORT_MIRROR**</span></span>  
<span data-ttu-id="64ede-227">**VDS_SVF_SUPPORT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="64ede-227">**VDS_SVF_SUPPORT_RAID5**</span></span>  


<span data-ttu-id="64ede-228">[**VDS_SUB_SYSTEM_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-228">[**VDS_SUB_SYSTEM_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) enumeration added values:</span></span>

<span data-ttu-id="64ede-229">**VDS_SF_SUPPORTS_LUN_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="64ede-229">**VDS_SF_SUPPORTS_LUN_NUMBER**</span></span>  
<span data-ttu-id="64ede-230">**VDS_SF_SUPPORTS_MIRRORED_CACHE**</span><span class="sxs-lookup"><span data-stu-id="64ede-230">**VDS_SF_SUPPORTS_MIRRORED_CACHE**</span></span>  
<span data-ttu-id="64ede-231">**VDS_SF_READ_CACHING_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="64ede-231">**VDS_SF_READ_CACHING_CAPABLE**</span></span>  
<span data-ttu-id="64ede-232">**VDS_SF_WRITE_CACHING_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="64ede-232">**VDS_SF_WRITE_CACHING_CAPABLE**</span></span>  
<span data-ttu-id="64ede-233">**VDS_SF_MEDIA_SCAN_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="64ede-233">**VDS_SF_MEDIA_SCAN_CAPABLE**</span></span>  
<span data-ttu-id="64ede-234">**VDS_SF_CONSISTENCY_CHECK_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="64ede-234">**VDS_SF_CONSISTENCY_CHECK_CAPABLE**</span></span>  


<span data-ttu-id="64ede-235">[**VDS_TRANSITION_STATE**](/windows/desktop/api/Vds/ne-vds-vds_transition_state) добавлено значение перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-235">[**VDS_TRANSITION_STATE**](/windows/desktop/api/Vds/ne-vds-vds_transition_state) enumeration added value:</span></span>

<span data-ttu-id="64ede-236">**VDS_TS_RESTRIPING**</span><span class="sxs-lookup"><span data-stu-id="64ede-236">**VDS_TS_RESTRIPING**</span></span>  


<span data-ttu-id="64ede-237">[**VDS_VERSION_SUPPORT_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_version_support_flag) добавлены значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-237">[**VDS_VERSION_SUPPORT_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_version_support_flag) enumeration added values:</span></span>

<span data-ttu-id="64ede-238">**VDS_VSF_2_0**</span><span class="sxs-lookup"><span data-stu-id="64ede-238">**VDS_VSF_2_0**</span></span>  
<span data-ttu-id="64ede-239">**VDS_VSF_2_1**</span><span class="sxs-lookup"><span data-stu-id="64ede-239">**VDS_VSF_2_1**</span></span>  
<span data-ttu-id="64ede-240">**VDS_VSF_3_0**</span><span class="sxs-lookup"><span data-stu-id="64ede-240">**VDS_VSF_3_0**</span></span>  


<span data-ttu-id="64ede-241">[**VDS_VOLUME_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_volume_status) добавлено значение перечисления:</span><span class="sxs-lookup"><span data-stu-id="64ede-241">[**VDS_VOLUME_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_volume_status) enumeration added value:</span></span>

<span data-ttu-id="64ede-242">**VDS_VS_OFFLINE**</span><span class="sxs-lookup"><span data-stu-id="64ede-242">**VDS_VS_OFFLINE**</span></span>  


## <a name="modifications-to-existing-vds-structures"></a><span data-ttu-id="64ede-243">Изменения в существующих структурах VDS</span><span class="sxs-lookup"><span data-stu-id="64ede-243">Modifications to Existing VDS Structures</span></span>

<span data-ttu-id="64ede-244">[**VDS_CONTROLLER_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification) структура добавлены значения **улевент** :</span><span class="sxs-lookup"><span data-stu-id="64ede-244">[**VDS_CONTROLLER_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification) structure added **ulEvent** values:</span></span>

<span data-ttu-id="64ede-245">VDS_NF_CONTROLLER_MODIFY</span><span class="sxs-lookup"><span data-stu-id="64ede-245">VDS_NF_CONTROLLER_MODIFY</span></span>  
<span data-ttu-id="64ede-246">VDS_NF_CONTROLLER_REMOVED</span><span class="sxs-lookup"><span data-stu-id="64ede-246">VDS_NF_CONTROLLER_REMOVED</span></span>  


<span data-ttu-id="64ede-247">[**VDS_DRIVE_NOTIFICATIONная**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification) структура добавила значение **улевент** :</span><span class="sxs-lookup"><span data-stu-id="64ede-247">[**VDS_DRIVE_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification) structure added **ulEvent** value:</span></span>

<span data-ttu-id="64ede-248">VDS_NF_DRIVE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="64ede-248">VDS_NF_DRIVE_REMOVED</span></span>  


<span data-ttu-id="64ede-249">[**VDS_PORT_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) структура добавлены значения **улевент** :</span><span class="sxs-lookup"><span data-stu-id="64ede-249">[**VDS_PORT_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) structure added **ulEvent** values:</span></span>

<span data-ttu-id="64ede-250">VDS_NF_PORT_MODIFY</span><span class="sxs-lookup"><span data-stu-id="64ede-250">VDS_NF_PORT_MODIFY</span></span>  
<span data-ttu-id="64ede-251">VDS_NF_PORT_REMOVED</span><span class="sxs-lookup"><span data-stu-id="64ede-251">VDS_NF_PORT_REMOVED</span></span>  


 

 
