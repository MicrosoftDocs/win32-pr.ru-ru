---
description: Инициатору запроса необходимо четко определить сведения о состоянии модуля записи, который участвует в процессе создания теневого копирования, а также во время операций резервного копирования и восстановления.
ms.assetid: 676d5cff-bd28-43f0-a402-d184c96f0061
title: Определение состояния модуля записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719322a18808748e92d412c48c7b7628fdac9d51
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273379"
---
# <a name="determining-writer-status"></a><span data-ttu-id="2f26c-103">Определение состояния модуля записи</span><span class="sxs-lookup"><span data-stu-id="2f26c-103">Determining Writer Status</span></span>

<span data-ttu-id="2f26c-104">Инициатору запроса необходимо четко определить сведения о состоянии модуля записи, который участвует в процессе создания теневого копирования, а также во время операций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="2f26c-104">A requester needs to have a well-defined understanding about the status of the writer that participates with it during shadow copy creation, and during backup and restore operations.</span></span> <span data-ttu-id="2f26c-105">Для этого рекомендуется:</span><span class="sxs-lookup"><span data-stu-id="2f26c-105">To do so, it is recommended:</span></span>

-   <span data-ttu-id="2f26c-106">Запрашивающие стороны используют [**ивссбаккупкомпонентс:: гасервритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**Ивссбаккупкомпонентс:: жетвритерстатускаунт**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)и [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).</span><span class="sxs-lookup"><span data-stu-id="2f26c-106">Requesters use [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents::GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount), and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).</span></span>
-   <span data-ttu-id="2f26c-107">Как описано в статье [Общие сведения об обработке резервной копии в VSS](overview-of-processing-a-backup-under-vss.md) и [Общие сведения об обработке восстановления в VSS](overview-of-processing-a-restore-under-vss.md), эти методы наиболее полезны при вызове в четко определенной последовательности резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="2f26c-107">As described in [Overview of Processing a Backup Under VSS](overview-of-processing-a-backup-under-vss.md) and [Overview of Processing a Restore Under VSS](overview-of-processing-a-restore-under-vss.md), these methods are most useful when called in a well-defined backup or restore sequence.</span></span> <span data-ttu-id="2f26c-108">Как правило, это означает, что записи должны быть запрошены после того, как инициатор запроса завершил одну из своих задач и создал событие VSS.</span><span class="sxs-lookup"><span data-stu-id="2f26c-108">Typically, this means that the writers should be queried after a requester has completed one of its tasks and generated a VSS event.</span></span>

    <span data-ttu-id="2f26c-109">При обработке резервной копии инициатор запроса должен запрашивать модуль записи после завершения следующих методов.</span><span class="sxs-lookup"><span data-stu-id="2f26c-109">When processing a backup, a requester should query a writer following the completion of the following methods.</span></span> <span data-ttu-id="2f26c-110">Запрашивающие стороны должны вызвать [**гасервритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) после вызова [**баккупкомплете**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , чтобы задать для сеанса модуля записи завершенное состояние.</span><span class="sxs-lookup"><span data-stu-id="2f26c-110">Requesters must call [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) after calling [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) to cause the writer session to be set to a completed state.</span></span>

    > [!Note]  
    > <span data-ttu-id="2f26c-111">Это необходимо только в Windows Server 2008 с пакетом обновления 2 (SP2) и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="2f26c-111">This is only necessary on Windows Server 2008 with Service Pack 2 (SP2) and earlier.</span></span>

     

    <dl> <dt>

[<span data-ttu-id="2f26c-112">**Ивссбаккупкомпонентс::P Репарефорбаккуп**</span><span class="sxs-lookup"><span data-stu-id="2f26c-112">**IVssBackupComponents::PrepareForBackup**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[<span data-ttu-id="2f26c-113">**Ивссбаккупкомпонентс::D Оснапшотсет**</span><span class="sxs-lookup"><span data-stu-id="2f26c-113">**IVssBackupComponents::DoSnapshotSet**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[<span data-ttu-id="2f26c-114">**Ивссбаккупкомпонентс:: Баккупкомплете**</span><span class="sxs-lookup"><span data-stu-id="2f26c-114">**IVssBackupComponents::BackupComplete**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

<span data-ttu-id="2f26c-115">Во время операций восстановления инициатор запроса должен запрашивать модуль записи после завершения следующих методов:</span><span class="sxs-lookup"><span data-stu-id="2f26c-115">During restore operations, a requester should query a writer after completion of these methods:</span></span>
<dl> <dt>

[<span data-ttu-id="2f26c-116">**Ивссбаккупкомпонентс::P восстановить**</span><span class="sxs-lookup"><span data-stu-id="2f26c-116">**IVssBackupComponents::PreRestore**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[<span data-ttu-id="2f26c-117">**Ивссбаккупкомпонентс::P Остресторе**</span><span class="sxs-lookup"><span data-stu-id="2f26c-117">**IVssBackupComponents::PostRestore**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   <span data-ttu-id="2f26c-118">Вызовы [**ивссбаккупкомпонентс:: гасервритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) , которые не являются частью четко определенной последовательности резервного копирования или восстановления, не предоставляют надежной картины состояния модуля записи, так как они могут отражать условия, не указывающие на сбой в текущей операции, например:</span><span class="sxs-lookup"><span data-stu-id="2f26c-118">Calls to [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) that are not part of a well-defined backup or restore sequence do not provide a reliable picture of writer status, because they might reflect conditions that do not indicate failure in the current operation, such as:</span></span>
    -   <span data-ttu-id="2f26c-119">Сбой предыдущего создания теневой копии</span><span class="sxs-lookup"><span data-stu-id="2f26c-119">A failure of a previous shadow copy creation</span></span>
    -   <span data-ttu-id="2f26c-120">Ошибка при выполнении раннего резервного копирования или восстановления</span><span class="sxs-lookup"><span data-stu-id="2f26c-120">An error in an early backup or restore operation</span></span>
    -   <span data-ttu-id="2f26c-121">Модуль записи, который сейчас обрабатывает событие, не отвечает</span><span class="sxs-lookup"><span data-stu-id="2f26c-121">An unresponsive writer currently processing an event</span></span>

<span data-ttu-id="2f26c-122">Таким образом, разработчики не должны полагаться на состояние модуля записи, возвращаемое процессами, которые затем инициатор запроса или пытается отслеживать ход выполнения одного экземпляра интерфейса [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) с другим (возможно, в отдельном потоке).</span><span class="sxs-lookup"><span data-stu-id="2f26c-122">Therefore, developers should not rely on writer status returned by processes other then the requester or attempt to monitor the progress of one instance of the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface with another (possibly in a separate thread).</span></span>

<span data-ttu-id="2f26c-123">Обратите внимание, что для операций резервного копирования, где необходимо проверять документы метаданных модуля записи Writer, не требуется вызывать [**ивссбаккупкомпонентс:: гасервритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) и [**Ивссбаккупкомпонентс:: жетвритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) после создания и обработки события [*Identify*](vssgloss-i.md) , вызванного [**ивссбаккупкомпонентс:: GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).</span><span class="sxs-lookup"><span data-stu-id="2f26c-123">Note that for backup operations, where it is necessary to examine writers' Writer Metadata Documents, there is no need for a requester call to [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) following the generation and handling of the [*Identify*](vssgloss-i.md) event caused by [**IVssBackupComponents::GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).</span></span>

<span data-ttu-id="2f26c-124">[**Ивссбаккупкомпонентс:: жетвритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) сообщает только о состоянии тех модулей записи, метаданные которых были предоставлены в VSS с [](vssgloss-i.md) помощью средств записи, [**квссвритер:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (и возвращаются инициатору запроса [**ивссбаккупкомпонентс:: жетвритерметадатакаунт**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) и [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).</span><span class="sxs-lookup"><span data-stu-id="2f26c-124">[**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) reports only the status of those writers whose metadata was provided to VSS by writers' [*Identify*](vssgloss-i.md) event handlers, [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (and returned to the requester by [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) and [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).</span></span>

<span data-ttu-id="2f26c-125">Если реализация модуля записи [**квссвритер:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) завершается ошибкой, метаданные этого модуля записи не будут входить в список документов метаданных модуля записи, предоставляемых VSS, сведения о состоянии будут недоступны, а вызов будет избыточным.</span><span class="sxs-lookup"><span data-stu-id="2f26c-125">If a writer's implementation of [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) fails, that writer's metadata will not be part of the list of Writer Metadata Documents provided to VSS, no status information will be available, and the call would be redundant.</span></span>

<span data-ttu-id="2f26c-126">Для операций восстановления, где инициатору запроса не нужно изучать документы метаданных модуля записи исполняемых модулей записи, вызов [**ивссбаккупкомпонентс:: гасервритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) и [**Ивссбаккупкомпонентс:: жетвритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) может быть более эффективным способом определения того, какие модули записи выполняются.</span><span class="sxs-lookup"><span data-stu-id="2f26c-126">For restore operations, where the requester does not need to examine Writer Metadata Documents of executing writers, calling [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) may be a more efficient way to determine which writers are executing.</span></span>

 

 



