---
description: Запрашивающие стороны управляют функциями теневой копии, задавая ее контекст. Этот контекст указывает, будет ли теневая копия содержаться в текущей операции, а также степенью координации модуля записи и поставщика.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Конфигурации контекста теневого копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544954"
---
# <a name="shadow-copy-context-configurations"></a><span data-ttu-id="5ee69-104">Конфигурации контекста теневого копирования</span><span class="sxs-lookup"><span data-stu-id="5ee69-104">Shadow Copy Context Configurations</span></span>

<span data-ttu-id="5ee69-105">Запрашивающие стороны управляют функциями теневой копии, задавая ее контекст.</span><span class="sxs-lookup"><span data-stu-id="5ee69-105">Requesters control a shadow copy's features by setting its context.</span></span> <span data-ttu-id="5ee69-106">Этот контекст указывает, будет ли теневая копия содержаться в текущей операции, а также степенью координации модуля записи и поставщика.</span><span class="sxs-lookup"><span data-stu-id="5ee69-106">This context indicates whether the shadow copy will survive the current operation, and the degree of writer/provider coordination.</span></span>

## <a name="persistence-and-shadow-copy-context"></a><span data-ttu-id="5ee69-107">Контекст сохраняемости и теневого копирования</span><span class="sxs-lookup"><span data-stu-id="5ee69-107">Persistence and Shadow Copy Context</span></span>

<span data-ttu-id="5ee69-108">Теневая копия может быть [*постоянной*](vssgloss-p.md), т. е. теневая копия не удаляется после завершения операции резервного копирования или выпуска объекта [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .</span><span class="sxs-lookup"><span data-stu-id="5ee69-108">A shadow copy may be [*persistent*](vssgloss-p.md)—that is, the shadow copy is not deleted following the termination of a backup operation or the release of an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object.</span></span>

<span data-ttu-id="5ee69-109">Для постоянных теневых копий требуются [**\_ \_ \_ контексты контекста моментальных снимков**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) VSS **\_ CTX \_ клиента \_ VSS**, **\_ \_ \_ откат приложения VSS CTX** или **\_ \_ \_ откат VSS CTX NAS**.</span><span class="sxs-lookup"><span data-stu-id="5ee69-109">Persistent shadow copies require [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) contexts of **VSS\_CTX\_CLIENT\_ACCESSIBLE**, **VSS\_CTX\_APP\_ROLLBACK**, or **VSS\_CTX\_NAS\_ROLLBACK**.</span></span> <span data-ttu-id="5ee69-110">Постоянные теневые копии можно создавать только для томов NTFS.</span><span class="sxs-lookup"><span data-stu-id="5ee69-110">Persistent shadow copies can be made only for NTFS volumes.</span></span>

<span data-ttu-id="5ee69-111">Непостоянные теневые копии создаются с использованием контекстов **\_ \_ резервного копирования VSS CTX** или **VSS \_ CTX \_ файлового \_ ресурса \_**.</span><span class="sxs-lookup"><span data-stu-id="5ee69-111">Nonpersistent shadow copies are created with contexts of **VSS\_CTX\_BACKUP** or **VSS\_CTX\_FILE\_SHARE\_BACKUP**.</span></span> <span data-ttu-id="5ee69-112">Для NTFS и томов, отличных от NTFS, можно создавать непостоянные теневые копии.</span><span class="sxs-lookup"><span data-stu-id="5ee69-112">Nonpersistent shadow copies can be made for NTFS and non-NTFS volumes.</span></span>

## <a name="writer-participation-and-shadow-copies"></a><span data-ttu-id="5ee69-113">Участие в записи и теневые копии</span><span class="sxs-lookup"><span data-stu-id="5ee69-113">Writer Participation and Shadow Copies</span></span>

<span data-ttu-id="5ee69-114">Контекст теневой копии может классифицироваться либо с участием модулей записи, либо без участия в модулях записи.</span><span class="sxs-lookup"><span data-stu-id="5ee69-114">A shadow copy context can be classified as either involving writers or not involving writers.</span></span>

<span data-ttu-id="5ee69-115">Контексты теневого копирования, которые включают в себя записи для создания, включают:</span><span class="sxs-lookup"><span data-stu-id="5ee69-115">Shadow copy contexts that involve writers in their creation include:</span></span>

-   <span data-ttu-id="5ee69-116">**\_ \_ откат приложения CTX \_ VSS**</span><span class="sxs-lookup"><span data-stu-id="5ee69-116">**VSS\_CTX\_APP\_ROLLBACK**</span></span>
-   <span data-ttu-id="5ee69-117">**\_ \_ резервное копирование CTX VSS**</span><span class="sxs-lookup"><span data-stu-id="5ee69-117">**VSS\_CTX\_BACKUP**</span></span>
-   <span data-ttu-id="5ee69-118">**\_ \_ \_ модули записи, доступные \_ клиенту VSS CTX**</span><span class="sxs-lookup"><span data-stu-id="5ee69-118">**VSS\_CTX\_CLIENT\_ACCESSIBLE\_WRITERS**</span></span>

<span data-ttu-id="5ee69-119">Те, которые не включают в себя модули записи при их создании, включают:</span><span class="sxs-lookup"><span data-stu-id="5ee69-119">Those that do not involve writers in their creation include:</span></span>

-   <span data-ttu-id="5ee69-120">**\_доступ к \_ клиенту \_ CTX VSS**</span><span class="sxs-lookup"><span data-stu-id="5ee69-120">**VSS\_CTX\_CLIENT\_ACCESSIBLE**</span></span>
-   <span data-ttu-id="5ee69-121">**\_ \_ \_ резервное копирование файлового ресурса CTX VSS \_**</span><span class="sxs-lookup"><span data-stu-id="5ee69-121">**VSS\_CTX\_FILE\_SHARE\_BACKUP**</span></span>
-   <span data-ttu-id="5ee69-122">**\_откат CTX \_ NAS \_ VSS**</span><span class="sxs-lookup"><span data-stu-id="5ee69-122">**VSS\_CTX\_NAS\_ROLLBACK**</span></span>

<span data-ttu-id="5ee69-123">Один контекст может использоваться с обоими типами теневых копий, но не может использоваться при создании теневой копии:</span><span class="sxs-lookup"><span data-stu-id="5ee69-123">One context can be used with both types of shadow copies, but cannot be used in creating a shadow copy:</span></span>

-   <span data-ttu-id="5ee69-124">**VSS \_ CTX \_ все**</span><span class="sxs-lookup"><span data-stu-id="5ee69-124">**VSS\_CTX\_ALL**</span></span>

<span data-ttu-id="5ee69-125">Создание теневой копии с помощью контекста **VSS \_ CTX \_ ALL** (с использованием [**Ивссбаккупкомпонентс:: Стартснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) и [**ивссбаккупкомпонентс::D оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5ee69-125">Creating a shadow copy with a context of **VSS\_CTX\_ALL** (using [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) and [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) is not supported.</span></span>

<span data-ttu-id="5ee69-126">Операции, поддерживающие контекст **VSS \_ CTX \_ ALL** , — это административные операции [**ивссбаккупкомпонентс:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**ивссбаккупкомпонентс::D Елетеснапшотс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**ивссбаккупкомпонентс:: бреакснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)и [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="5ee69-126">Operations that support a context of **VSS\_CTX\_ALL** are the administrative operations [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::DeleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset), and [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span></span>

## <a name="obtaining-shadow-copy-information"></a><span data-ttu-id="5ee69-127">Получение сведений о теневой копии</span><span class="sxs-lookup"><span data-stu-id="5ee69-127">Obtaining Shadow Copy Information</span></span>

<span data-ttu-id="5ee69-128">Если инициатор запроса знает идентификационный идентификатор GUID теневой копии (ее **\_ идентификатор VSS**), он может получить сведения о контексте определенной теневой копии (определяется ее **\_ идентификатором VSS**) путем распаковки структуры свойства " [**\_ \_ prop" моментального снимка VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) , возвращенной вызовом метода [**ивссбаккупкомпонентс:: жетснапшотпропертиес**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span><span class="sxs-lookup"><span data-stu-id="5ee69-128">If a requester knows the identifying GUID of a shadow copy (its **VSS\_ID**), it can obtain information about the context of a specific shadow copy (identified by its **VSS\_ID**) by unpacking the [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure returned by a call to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="5ee69-129">Чтобы получить контекстные сведения обо всех теневых копиях в системе, инициатор запроса изучает **член m \_ Лснапшотаттрибутес** элемента **obj. Snap** в [**\_ \_ свойстве-объекте Prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) . Snapin (структура [**\_ снимка VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ), полученном с помощью [**ивссенумобжект**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) , для прохода по списку объектов, возвращенных вызовом [**ивссбаккупкомпонентс:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="5ee69-129">To obtain context information about all shadow copies on a system, a requester examines the **m\_lSnapshotAttributes** member of the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) structure obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

 

 



