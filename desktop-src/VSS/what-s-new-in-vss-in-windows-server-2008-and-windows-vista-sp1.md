---
description: Windows Server 2008;
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Новые возможности VSS в Windows Server 2008 и Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f053e327a7a54a9597bc06836b37c00effc62f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145193"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="a3483-103">Новые возможности VSS в Windows Server 2008 и Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="a3483-103">What's New in VSS in Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="a3483-104">Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1) вносят следующие изменения в служба теневого копирования томов.</span><span class="sxs-lookup"><span data-stu-id="a3483-104">Windows Server 2008 and Windows Vista with Service Pack 1 (SP1) introduce the following changes to the Volume Shadow Copy Service.</span></span>

> [!Note]  
> <span data-ttu-id="a3483-105">Все изменения в Windows Vista относятся к Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a3483-105">All changes for Windows Vista apply to Windows Server 2008 and Windows Vista with SP1.</span></span> <span data-ttu-id="a3483-106">Дополнительные сведения об этих изменениях см. в статье [новые возможности VSS в Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="a3483-106">For details on those changes, see [What's New in VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span></span>

 

-   [<span data-ttu-id="a3483-107">Новые интерфейсы VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-107">New VSS Interfaces</span></span>](#new-vss-interfaces)
-   [<span data-ttu-id="a3483-108">Новые перечисления VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-108">New VSS Enumerations</span></span>](#new-vss-enumerations)
-   [<span data-ttu-id="a3483-109">Новые структуры VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-109">New VSS Structures</span></span>](#new-vss-structures)
-   [<span data-ttu-id="a3483-110">Существующие изменения перечисления VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-110">Existing VSS Enumeration Modifications</span></span>](#existing-vss-enumeration-modifications)
-   [<span data-ttu-id="a3483-111">Существующие изменения интерфейса VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-111">Existing VSS Interface Modifications</span></span>](#existing-vss-interface-modifications)
-   [<span data-ttu-id="a3483-112">Новые модули записи VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-112">New VSS Writers</span></span>](#new-vss-writers)

## <a name="new-vss-interfaces"></a><span data-ttu-id="a3483-113">Новые интерфейсы VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-113">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="a3483-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="a3483-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[<span data-ttu-id="a3483-115">**ивсшардвареснапшотпровидерекс**</span><span class="sxs-lookup"><span data-stu-id="a3483-115">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="a3483-116">Новые перечисления VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-116">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="a3483-117">**\_\_Параметры оборудования \_ VSS**</span><span class="sxs-lookup"><span data-stu-id="a3483-117">**\_VSS\_HARDWARE\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[<span data-ttu-id="a3483-118">**\_сбой защиты \_ VSS**</span><span class="sxs-lookup"><span data-stu-id="a3483-118">**VSS\_PROTECTION\_FAULT**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[<span data-ttu-id="a3483-119">**\_уровень защиты \_ VSS**</span><span class="sxs-lookup"><span data-stu-id="a3483-119">**VSS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a><span data-ttu-id="a3483-120">Новые структуры VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-120">New VSS Structures</span></span>

<dl>

[<span data-ttu-id="a3483-121">**\_ \_ сведения о защите томов VSS \_**</span><span class="sxs-lookup"><span data-stu-id="a3483-121">**VSS\_VOLUME\_PROTECTION\_INFO**</span></span>](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="a3483-122">Существующие изменения перечисления VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-122">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="a3483-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ схемы резервного копирования**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span><span class="sxs-lookup"><span data-stu-id="a3483-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="a3483-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Добавлено значение:</span><span class="sxs-lookup"><span data-stu-id="a3483-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Added value:</span></span>
</dt> <dd>

<span data-ttu-id="a3483-125">\_модуль записи BS в VSS \_ \_ поддерживает \_ параллельное \_ восстановление</span><span class="sxs-lookup"><span data-stu-id="a3483-125">VSS\_BS\_WRITER\_SUPPORTS\_PARALLEL\_RESTORES</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="a3483-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Перечисление [**\_ \_ \_ \_ атрибутов моментальных снимков тома VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="a3483-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="a3483-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:</span><span class="sxs-lookup"><span data-stu-id="a3483-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="a3483-128">\_ \_ \_ отложенный \_ моментальный снимок для службы VSS VOLSNAP attr</span><span class="sxs-lookup"><span data-stu-id="a3483-128">VSS\_VOLSNAP\_ATTR\_DELAYED\_POSTSNAPSHOT</span></span>

<span data-ttu-id="a3483-129">Восстановление из службы VSS \_ VOLSNAP \_ attr \_ TxF \_</span><span class="sxs-lookup"><span data-stu-id="a3483-129">VSS\_VOLSNAP\_ATTR\_TXF\_RECOVERY</span></span>

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="a3483-130">Существующие изменения интерфейса VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-130">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="a3483-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Интерфейс [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)</span><span class="sxs-lookup"><span data-stu-id="a3483-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="a3483-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Добавленный метод:</span><span class="sxs-lookup"><span data-stu-id="a3483-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Added method:</span></span>
</dt> <dd>

[<span data-ttu-id="a3483-133">**бреакснапшотсетекс**</span><span class="sxs-lookup"><span data-stu-id="a3483-133">**BreakSnapshotSetEx**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a><span data-ttu-id="a3483-134">Новые модули записи VSS</span><span class="sxs-lookup"><span data-stu-id="a3483-134">New VSS Writers</span></span>

<span data-ttu-id="a3483-135">В Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1) представлены следующие модули записи VSS:</span><span class="sxs-lookup"><span data-stu-id="a3483-135">Windows Server 2008 and Windows Vista with SP1 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="a3483-136">Модуль записи конфигурации IIS</span><span class="sxs-lookup"><span data-stu-id="a3483-136">IIS Configuration Writer</span></span>
-   <span data-ttu-id="a3483-137">Модуль записи метабазы IIS</span><span class="sxs-lookup"><span data-stu-id="a3483-137">IIS Metabase Writer</span></span>
-   <span data-ttu-id="a3483-138">Модуль записи VSS NPS</span><span class="sxs-lookup"><span data-stu-id="a3483-138">NPS VSS Writer</span></span>
-   <span data-ttu-id="a3483-139">Модуль записи VSS шлюза службы удаленных рабочих столов (службы терминалов)</span><span class="sxs-lookup"><span data-stu-id="a3483-139">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>
-   <span data-ttu-id="a3483-140">Модуль записи VSS лицензирования службы удаленных рабочих столов (службы терминалов)</span><span class="sxs-lookup"><span data-stu-id="a3483-140">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="a3483-141">Эти модули записи описаны в встроенных [модулях записи VSS](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="a3483-141">These writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 



