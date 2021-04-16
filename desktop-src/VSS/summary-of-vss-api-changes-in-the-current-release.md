---
description: Сводка изменений API VSS в Windows Server 2003
ms.assetid: 35572fc6-9147-4726-ae7a-d78292683ba0
title: Сводка изменений API VSS в Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9154da0ac67dd7a599064ed3b5cf1dc7285b0fb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692870"
---
# <a name="summary-of-vss-api-changes-in-windows-server-2003"></a><span data-ttu-id="e76ac-103">Сводка изменений API VSS в Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e76ac-103">Summary of VSS API Changes in Windows Server 2003</span></span>

## <a name="changes-in-the-vss-service"></a><span data-ttu-id="e76ac-104">Изменения в службе VSS</span><span class="sxs-lookup"><span data-stu-id="e76ac-104">Changes in the VSS Service</span></span>

<dl> <dt>

<span data-ttu-id="e76ac-105"><span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Добавлено событий:</span><span class="sxs-lookup"><span data-stu-id="e76ac-105"><span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Events added:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-106">*баккупшутдовн*</span><span class="sxs-lookup"><span data-stu-id="e76ac-106">*BackupShutdown*</span></span>](vssgloss-b.md)

</dd> </dl>

## <a name="changes-in-vss-functionality"></a><span data-ttu-id="e76ac-107">Изменения в функциональных возможностях VSS</span><span class="sxs-lookup"><span data-stu-id="e76ac-107">Changes in VSS Functionality</span></span>

<dl> <dt>

<span data-ttu-id="e76ac-108"><span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Дополнительные функции:</span><span class="sxs-lookup"><span data-stu-id="e76ac-108"><span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Additional functionality:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-109">*Частичная поддержка файлов*</span><span class="sxs-lookup"><span data-stu-id="e76ac-109">*partial file support*</span></span>](vssgloss-p.md)

[<span data-ttu-id="e76ac-110">*направлено нацеливание*</span><span class="sxs-lookup"><span data-stu-id="e76ac-110">*directed targeting*</span></span>](vssgloss-d.md)

</dd> </dl>

## <a name="new-vss-interfaces"></a><span data-ttu-id="e76ac-111">Новые интерфейсы VSS</span><span class="sxs-lookup"><span data-stu-id="e76ac-111">New VSS Interfaces</span></span>

[<span data-ttu-id="e76ac-112">**ивссвмдепенденци**</span><span class="sxs-lookup"><span data-stu-id="e76ac-112">**IVssWMDependency**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="e76ac-113">Существующие изменения интерфейса VSS</span><span class="sxs-lookup"><span data-stu-id="e76ac-113">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="e76ac-114"><span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>Интерфейс [**ивссасинк**](/windows/desktop/api/Vss/nn-vss-ivssasync)</span><span class="sxs-lookup"><span data-stu-id="e76ac-114"><span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>[**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-115"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Измененные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-115"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-116">**Ивссасинк:: wait**</span><span class="sxs-lookup"><span data-stu-id="e76ac-116">**IVssAsync::Wait**</span></span>](/windows/desktop/api/Vss/nf-vss-ivssasync-wait)

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-117"><span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>Интерфейс [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)</span><span class="sxs-lookup"><span data-stu-id="e76ac-117"><span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>[**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-118"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-118"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-119">**Ивссбаккупкомпонентс:: Аддневтаржет**</span><span class="sxs-lookup"><span data-stu-id="e76ac-119">**IVssBackupComponents::AddNewTarget**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

[<span data-ttu-id="e76ac-120">**Ивссбаккупкомпонентс:: Куериревертстатус**</span><span class="sxs-lookup"><span data-stu-id="e76ac-120">**IVssBackupComponents::QueryRevertStatus**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-queryrevertstatus)

[<span data-ttu-id="e76ac-121">**Ивссбаккупкомпонентс:: Реверттоснапшот**</span><span class="sxs-lookup"><span data-stu-id="e76ac-121">**IVssBackupComponents::RevertToSnapshot**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-reverttosnapshot)

[<span data-ttu-id="e76ac-122">**Ивссбаккупкомпонентс:: Сетранжесфилепас**</span><span class="sxs-lookup"><span data-stu-id="e76ac-122">**IVssBackupComponents::SetRangesFilePath**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)

[<span data-ttu-id="e76ac-123">**Ивссбаккупкомпонентс:: Сетресторестате**</span><span class="sxs-lookup"><span data-stu-id="e76ac-123">**IVssBackupComponents::SetRestoreState**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-124"><span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>Интерфейс [**ивсскреатевритерметадата**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)</span><span class="sxs-lookup"><span data-stu-id="e76ac-124"><span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>[**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-125"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-125"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-126">**Ивсскреатевритерметадата:: Аддкомпонентдепенденци**</span><span class="sxs-lookup"><span data-stu-id="e76ac-126">**IVssCreateWriterMetadata::AddComponentDependency**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)

[<span data-ttu-id="e76ac-127">**Ивсскреатевритерметадата:: Сетбаккупсчема**</span><span class="sxs-lookup"><span data-stu-id="e76ac-127">**IVssCreateWriterMetadata::SetBackupSchema**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)

</dd> <dt>

<span data-ttu-id="e76ac-128"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Измененные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-128"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-129">**Ивсскреатевритерметадата:: AddComponent**</span><span class="sxs-lookup"><span data-stu-id="e76ac-129">**IVssCreateWriterMetadata::AddComponent**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)

[<span data-ttu-id="e76ac-130">**Ивсскреатевритерметадата:: Адддатабасефилес**</span><span class="sxs-lookup"><span data-stu-id="e76ac-130">**IVssCreateWriterMetadata::AddDatabaseFiles**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)

[<span data-ttu-id="e76ac-131">**Ивсскреатевритерметадата:: Адддатабаселогфилес**</span><span class="sxs-lookup"><span data-stu-id="e76ac-131">**IVssCreateWriterMetadata::AddDatabaseLogFiles**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

[<span data-ttu-id="e76ac-132">**Ивсскреатевритерметадата:: Аддфилестофилеграуп**</span><span class="sxs-lookup"><span data-stu-id="e76ac-132">**IVssCreateWriterMetadata::AddFilesToFileGroup**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-133"><span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>Интерфейс [**ивссексаминевритерметадата**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)</span><span class="sxs-lookup"><span data-stu-id="e76ac-133"><span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>[**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-134"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-134"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-135">**Ивссексаминевритерметадата:: Жетбаккупсчема**</span><span class="sxs-lookup"><span data-stu-id="e76ac-135">**IVssExamineWriterMetadata::GetBackupSchema**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-136"><span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>Интерфейс [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)</span><span class="sxs-lookup"><span data-stu-id="e76ac-136"><span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-137"><span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Удаленные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-137"><span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Methods removed:</span></span>
</dt> <dd>

<span data-ttu-id="e76ac-138">**Ивсскомпонент:: Аддневтаржет**</span><span class="sxs-lookup"><span data-stu-id="e76ac-138">**IVssComponent::AddNewTarget**</span></span>

</dd> <dt>

<span data-ttu-id="e76ac-139"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-139"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-140">**Ивсскомпонент:: Адддифференцедфилесбиластмодифитиме**</span><span class="sxs-lookup"><span data-stu-id="e76ac-140">**IVssComponent::AddDifferencedFilesByLastModifyTime**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)

[<span data-ttu-id="e76ac-141">**Ивсскомпонент:: Жетдифференцедфиле**</span><span class="sxs-lookup"><span data-stu-id="e76ac-141">**IVssComponent::GetDifferencedFile**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

[<span data-ttu-id="e76ac-142">**Ивсскомпонент:: Жетдифференцедфилескаунт**</span><span class="sxs-lookup"><span data-stu-id="e76ac-142">**IVssComponent::GetDifferencedFilesCount**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)

</dd> <dt>

<span data-ttu-id="e76ac-143"><span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>Методы больше не зарезервированы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-143"><span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>Methods no longer reserved:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-144">**Ивсскомпонент:: Адддиректедтаржет**</span><span class="sxs-lookup"><span data-stu-id="e76ac-144">**IVssComponent::AddDirectedTarget**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)

[<span data-ttu-id="e76ac-145">**Ивсскомпонент:: Жетдиректедтаржет**</span><span class="sxs-lookup"><span data-stu-id="e76ac-145">**IVssComponent::GetDirectedTarget**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-146"><span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>Интерфейс [**ивссвмкомпонент**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)</span><span class="sxs-lookup"><span data-stu-id="e76ac-146"><span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>[**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-147"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-147"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-148">**Ивссвмкомпонент:: dependency**</span><span class="sxs-lookup"><span data-stu-id="e76ac-148">**IVssWMComponent::GetDependency**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-149"><span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>Интерфейс [**ивссвмфиледеск**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)</span><span class="sxs-lookup"><span data-stu-id="e76ac-149"><span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>[**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-150"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-150"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-151">**Ивссвмфиледеск:: Жетбаккуптипемаск**</span><span class="sxs-lookup"><span data-stu-id="e76ac-151">**IVssWMFiledesc::GetBackupTypeMask**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)

</dd> </dl> </dd> </dl>

## <a name="existing-vss-class-modifications"></a><span data-ttu-id="e76ac-152">Существующие изменения класса VSS</span><span class="sxs-lookup"><span data-stu-id="e76ac-152">Existing VSS Class Modifications</span></span>

<dl> <dt>

<span data-ttu-id="e76ac-153"><span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>Класс [**квссвритер**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter)</span><span class="sxs-lookup"><span data-stu-id="e76ac-153"><span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>[**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-154"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Измененные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-154"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-155">**Квссвритер:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="e76ac-155">**CVssWriter::Initialize**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)

</dd> <dt>

<span data-ttu-id="e76ac-156"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-156"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="e76ac-157">**Квссвритер:: SPContext**</span><span class="sxs-lookup"><span data-stu-id="e76ac-157">**CVssWriter::GetContext**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext)

[<span data-ttu-id="e76ac-158">**Квссвритер:: Жетресторетипе**</span><span class="sxs-lookup"><span data-stu-id="e76ac-158">**CVssWriter::GetRestoreType**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)

[<span data-ttu-id="e76ac-159">**Квссвритер:: Жетснапшотдевиценаме**</span><span class="sxs-lookup"><span data-stu-id="e76ac-159">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)

[<span data-ttu-id="e76ac-160">**Квссвритер:: Онбаккупшутдовн**</span><span class="sxs-lookup"><span data-stu-id="e76ac-160">**CVssWriter::OnBackupShutdown**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)

</dd> </dl> </dd> </dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="e76ac-161">Новые перечисления VSS</span><span class="sxs-lookup"><span data-stu-id="e76ac-161">New VSS Enumerations</span></span>

<dl> <dt>

<span data-ttu-id="e76ac-162"><span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**\_схема резервного копирования VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span><span class="sxs-lookup"><span data-stu-id="e76ac-162"><span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e76ac-163"><span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**\_ \_ Флаги компонента VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span><span class="sxs-lookup"><span data-stu-id="e76ac-163"><span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e76ac-164"><span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**\_ \_ \_ тип резервного копирования спецификации файла VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)</span><span class="sxs-lookup"><span data-stu-id="e76ac-164"><span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e76ac-165"><span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**\_тип восстановления \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)</span><span class="sxs-lookup"><span data-stu-id="e76ac-165"><span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**VSS\_RESTORE\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)</span></span>
<span data-ttu-id="e76ac-166"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e76ac-166"></dt> <dd></dd> </dl></span></span>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="e76ac-167">Существующие изменения перечисления VSS</span><span class="sxs-lookup"><span data-stu-id="e76ac-167">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="e76ac-168"><span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ типов резервных копий**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)</span><span class="sxs-lookup"><span data-stu-id="e76ac-168"><span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>[**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-169"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:</span><span class="sxs-lookup"><span data-stu-id="e76ac-169"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="e76ac-170">\_BT \_ Copy VSS</span><span class="sxs-lookup"><span data-stu-id="e76ac-170">VSS\_BT\_COPY</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-171"><span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ целевых объектов восстановления**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)</span><span class="sxs-lookup"><span data-stu-id="e76ac-171"><span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>[**VSS\_RESTORE\_TARGET**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-172"><span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Удаленные значения:</span><span class="sxs-lookup"><span data-stu-id="e76ac-172"><span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Removed values:</span></span>
</dt> <dd>

<span data-ttu-id="e76ac-173">\_Новый VSS RT \_</span><span class="sxs-lookup"><span data-stu-id="e76ac-173">VSS\_RT\_NEW</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-174"><span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ enum ресторемесод**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)</span><span class="sxs-lookup"><span data-stu-id="e76ac-174"><span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>[**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-175"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:</span><span class="sxs-lookup"><span data-stu-id="e76ac-175"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="e76ac-176">\_Восстановление рме VSS при \_ \_ \_ перезагрузке, \_ Если \_ не может \_ заменить</span><span class="sxs-lookup"><span data-stu-id="e76ac-176">VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-177"><span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ состояний моментальных снимков**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)</span><span class="sxs-lookup"><span data-stu-id="e76ac-177"><span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>[**VSS\_SNAPSHOT\_STATE**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-178"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:</span><span class="sxs-lookup"><span data-stu-id="e76ac-178"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="e76ac-179">обработка с применением VSS \_ SS \_ \_</span><span class="sxs-lookup"><span data-stu-id="e76ac-179">VSS\_SS\_PROCESSING\_POSTCOMMIT</span></span>

<span data-ttu-id="e76ac-180">\_ \_ ПРЕФИНАЛКОММИТ обработки VSS \_ SS</span><span class="sxs-lookup"><span data-stu-id="e76ac-180">VSS\_SS\_PROCESSING\_PREFINALCOMMIT</span></span>

<span data-ttu-id="e76ac-181">VSS \_ SS \_ префиналкоммиттед</span><span class="sxs-lookup"><span data-stu-id="e76ac-181">VSS\_SS\_PREFINALCOMMITTED</span></span>

<span data-ttu-id="e76ac-182">\_ \_ ПОСТФИНАЛКОММИТ обработки VSS \_ SS</span><span class="sxs-lookup"><span data-stu-id="e76ac-182">VSS\_SS\_PROCESSING\_POSTFINALCOMMIT</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-183"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Перечисление [**\_ \_ \_ \_ атрибутов моментальных снимков тома VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="e76ac-183"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-184"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:</span><span class="sxs-lookup"><span data-stu-id="e76ac-184"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="e76ac-185">автовосстановление в VSS \_ VOLSNAP \_ attr \_</span><span class="sxs-lookup"><span data-stu-id="e76ac-185">VSS\_VOLSNAP\_ATTR\_AUTORECOVER</span></span>

</dd> <dt>

<span data-ttu-id="e76ac-186"><span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>Зарезервированные значения теперь поддерживают:</span><span class="sxs-lookup"><span data-stu-id="e76ac-186"><span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>Reserved values now support:</span></span>
</dt> <dd>

<span data-ttu-id="e76ac-187">\_устройство с \_ \_ \_ поддержкой VSS VOLSNAP attr</span><span class="sxs-lookup"><span data-stu-id="e76ac-187">VSS\_VOLSNAP\_ATTR\_HARDWARE\_ASSISTED</span></span>

<span data-ttu-id="e76ac-188">Импорт атрибута VOLSNAP для VSS \_ \_ \_ импортирован</span><span class="sxs-lookup"><span data-stu-id="e76ac-188">VSS\_VOLSNAP\_ATTR\_IMPORTED</span></span>

<span data-ttu-id="e76ac-189">Служба VSS \_ VOLSNAP \_ attr \_ доступна \_ локально</span><span class="sxs-lookup"><span data-stu-id="e76ac-189">VSS\_VOLSNAP\_ATTR\_EXPOSED\_LOCALLY</span></span>

<span data-ttu-id="e76ac-190">\_удаленная служба VSS VOLSNAP \_ attr \_ доступна \_</span><span class="sxs-lookup"><span data-stu-id="e76ac-190">VSS\_VOLSNAP\_ATTR\_EXPOSED\_REMOTELY</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e76ac-191"><span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ состояния модуля записи**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)</span><span class="sxs-lookup"><span data-stu-id="e76ac-191"><span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>[**VSS\_WRITER\_STATE**](/windows/desktop/api/Vss/ne-vss-vss_writer_state) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-192"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:</span><span class="sxs-lookup"><span data-stu-id="e76ac-192"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="e76ac-193">\_сбой VSS \_ WS \_ в \_ баккупшутдовн</span><span class="sxs-lookup"><span data-stu-id="e76ac-193">VSS\_WS\_FAILED\_AT\_BACKUPSHUTDOWN</span></span>

</dd> </dl> </dd> </dl>

## <a name="changes-to-vss-structures"></a><span data-ttu-id="e76ac-194">Изменения в структурах VSS</span><span class="sxs-lookup"><span data-stu-id="e76ac-194">Changes to VSS Structures</span></span>

<dl> <dt>

<span data-ttu-id="e76ac-195"><span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>Служба [**VSS \_ Структура КОМПОНЕНТИНФО**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)</span><span class="sxs-lookup"><span data-stu-id="e76ac-195"><span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>[**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="e76ac-196"><span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Добавленные элементы:</span><span class="sxs-lookup"><span data-stu-id="e76ac-196"><span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Added members:</span></span>
</dt> <dd>

<span data-ttu-id="e76ac-197">**бселектаблефорресторе**</span><span class="sxs-lookup"><span data-stu-id="e76ac-197">**bSelectableForRestore**</span></span>

<span data-ttu-id="e76ac-198">**двкомпонентфлагс**</span><span class="sxs-lookup"><span data-stu-id="e76ac-198">**dwComponentFlags**</span></span>

<span data-ttu-id="e76ac-199">**кдепенденЦиес**</span><span class="sxs-lookup"><span data-stu-id="e76ac-199">**cDependencies**</span></span>

</dd> </dl> </dd> </dl>

 

 



