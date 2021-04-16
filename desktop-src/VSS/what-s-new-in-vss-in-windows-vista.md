---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Новые возможности VSS в Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122caa350ede984d5b05eb7eedd6039d82a76f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692344"
---
# <a name="whats-new-in-vss-in-windows-vista"></a><span data-ttu-id="feb94-103">Новые возможности VSS в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb94-103">What's New in VSS in Windows Vista</span></span>

<span data-ttu-id="feb94-104">В Windows Vista появились следующие изменения в служба теневого копирования томов.</span><span class="sxs-lookup"><span data-stu-id="feb94-104">Windows Vista introduces the following changes to the Volume Shadow Copy Service.</span></span>

<span data-ttu-id="feb94-105">Обратите внимание, что все изменения для Windows Vista также относятся к Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="feb94-105">Note that all changes for Windows Vista also apply to Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="feb94-106">Новые интерфейсы VSS</span><span class="sxs-lookup"><span data-stu-id="feb94-106">New VSS Interfaces</span></span>

[<span data-ttu-id="feb94-107">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="feb94-107">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[<span data-ttu-id="feb94-108">**ивсскомпонентекс**</span><span class="sxs-lookup"><span data-stu-id="feb94-108">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[<span data-ttu-id="feb94-109">**ивсскреатевритерметадатаекс**</span><span class="sxs-lookup"><span data-stu-id="feb94-109">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[<span data-ttu-id="feb94-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="feb94-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[<span data-ttu-id="feb94-111">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="feb94-111">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a><span data-ttu-id="feb94-112">Новые классы VSS</span><span class="sxs-lookup"><span data-stu-id="feb94-112">New VSS Classes</span></span>

[<span data-ttu-id="feb94-113">**квссвритерекс**</span><span class="sxs-lookup"><span data-stu-id="feb94-113">**CVssWriterEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a><span data-ttu-id="feb94-114">Новые перечисления VSS</span><span class="sxs-lookup"><span data-stu-id="feb94-114">New VSS Enumerations</span></span>

[<span data-ttu-id="feb94-115">**\_тип НАКАТУ \_ VSS**</span><span class="sxs-lookup"><span data-stu-id="feb94-115">**VSS\_ROLLFORWARD\_TYPE**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="feb94-116">Существующие изменения перечисления VSS</span><span class="sxs-lookup"><span data-stu-id="feb94-116">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="feb94-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ схемы резервного копирования**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span><span class="sxs-lookup"><span data-stu-id="feb94-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="feb94-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:</span><span class="sxs-lookup"><span data-stu-id="feb94-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="feb94-119">\_ \_ полномочное \_ восстановление в VSS</span><span class="sxs-lookup"><span data-stu-id="feb94-119">VSS\_BS\_AUTHORITATIVE\_RESTORE</span></span>

<span data-ttu-id="feb94-120">\_ \_ независимое \_ состояние системы "BS \_ " VSS</span><span class="sxs-lookup"><span data-stu-id="feb94-120">VSS\_BS\_INDEPENDENT\_SYSTEM\_STATE</span></span>

<span data-ttu-id="feb94-121">\_ \_ Переименование восстанавливаемого восстановления VSS \_</span><span class="sxs-lookup"><span data-stu-id="feb94-121">VSS\_BS\_RESTORE\_RENAME</span></span>

<span data-ttu-id="feb94-122">\_ \_ Восстановление накатуа BS VSS \_</span><span class="sxs-lookup"><span data-stu-id="feb94-122">VSS\_BS\_ROLLFORWARD\_RESTORE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="feb94-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ флагов компонентов**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span><span class="sxs-lookup"><span data-stu-id="feb94-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="feb94-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:</span><span class="sxs-lookup"><span data-stu-id="feb94-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="feb94-125">VSS \_ CF \_ не \_ является \_ состоянием системы</span><span class="sxs-lookup"><span data-stu-id="feb94-125">VSS\_CF\_NOT\_SYSTEM\_STATE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="feb94-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Перечисление [**\_ \_ \_ \_ атрибутов моментальных снимков тома VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="feb94-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="feb94-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:</span><span class="sxs-lookup"><span data-stu-id="feb94-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="feb94-128">Служба VSS \_ VOLSNAP \_ attr \_ без \_ автовосстановления</span><span class="sxs-lookup"><span data-stu-id="feb94-128">VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY</span></span>

<span data-ttu-id="feb94-129">Служба VSS \_ VOLSNAP \_ attr \_ не \_ транзакционная</span><span class="sxs-lookup"><span data-stu-id="feb94-129">VSS\_VOLSNAP\_ATTR\_NOT\_TRANSACTED</span></span>

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="feb94-130">Трассировка и ведение журнала событий VSS</span><span class="sxs-lookup"><span data-stu-id="feb94-130">VSS Event Tracing and Logging</span></span>

-   <span data-ttu-id="feb94-131">Теперь файл трассировки VSS можно найти на любом локальном томе.</span><span class="sxs-lookup"><span data-stu-id="feb94-131">The VSS trace file can now be located on any local volume.</span></span> <span data-ttu-id="feb94-132">В версиях Windows, предшествовавших Windows Vista, файл трассировки VSS не удалось найти на томе, который был в наборе теневых копий.</span><span class="sxs-lookup"><span data-stu-id="feb94-132">On versions of Windows prior to Windows Vista, the VSS trace file could not be located on a volume that was in the shadow copy set.</span></span>
-   <span data-ttu-id="feb94-133">Многие записи в журнале событий были изменены, чтобы сделать их более четкими.</span><span class="sxs-lookup"><span data-stu-id="feb94-133">Many event log entries have been reworded to make them clearer.</span></span>
-   <span data-ttu-id="feb94-134">Все записи журнала событий VSS теперь содержат сведения о контексте.</span><span class="sxs-lookup"><span data-stu-id="feb94-134">All VSS event log entries now contain context information.</span></span>

## <a name="vss-error-reporting"></a><span data-ttu-id="feb94-135">Отчеты об ошибках VSS</span><span class="sxs-lookup"><span data-stu-id="feb94-135">VSS Error Reporting</span></span>

-   <span data-ttu-id="feb94-136">Описания всех кодов ошибок VSS теперь можно получить, вызвав функцию [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) с \_ сообщением Format \_ из \_ флага хмодуле, указанного в параметре *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="feb94-136">Descriptions of all VSS error codes can now be retrieved by calling the [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_HMODULE flag specified in the *dwFlags* parameter.</span></span>
-   <span data-ttu-id="feb94-137">Сообщения с кодом ошибки VSS содержатся в vsstrace.dll.</span><span class="sxs-lookup"><span data-stu-id="feb94-137">The VSS error code messages are contained in vsstrace.dll.</span></span> <span data-ttu-id="feb94-138">В параметре *лпсаурце* должен быть указан обработчик для этого модуля.</span><span class="sxs-lookup"><span data-stu-id="feb94-138">A handle to this module must be specified in the *lpSource* parameter.</span></span>

## <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="feb94-139">Исключение файлов из теневых копий</span><span class="sxs-lookup"><span data-stu-id="feb94-139">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="feb94-140">Приложения или службы могут использовать раздел реестра Филесноттоснапшот, чтобы указать файлы, которые будут удалены из вновь создаваемых теневых копий.</span><span class="sxs-lookup"><span data-stu-id="feb94-140">Applications or services can use the FilesNotToSnapshot registry key to specify files to be deleted from newly created shadow copies.</span></span> <span data-ttu-id="feb94-141">Дополнительные сведения см. в разделе [исключение файлов из теневых копий](excluding-files-from-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="feb94-141">For more information, see [Excluding Files from Shadow Copies](excluding-files-from-shadow-copies.md).</span></span>

## <a name="backup-and-restore-application-compatibility"></a><span data-ttu-id="feb94-142">Резервное копирование и восстановление совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="feb94-142">Backup and Restore Application Compatibility</span></span>

<span data-ttu-id="feb94-143">Разработчикам приложений для резервного копирования и восстановления необходимо знать о некоторых новых возможностях Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="feb94-143">Developers of backup and restore applications need to be aware of certain new features in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="feb94-144">Контрольный список совместимости приложений см. в разделе [совместимость приложений для резервного копирования и восстановления](application-compatibility-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="feb94-144">For an application compatibility checklist, see [Application Compatibility for Backup and Restore](application-compatibility-for-backup-and-restore.md).</span></span>

 

 
