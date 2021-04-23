---
description: В следующем списке перечислены дополнения и изменения в интерфейсе служба теневого копирования томов в Windows Server 2003 с пакетом обновления 1 (SP1).
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Новые возможности VSS в Windows Server 2003 с пакетом обновления 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497517"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a><span data-ttu-id="63664-103">Новые возможности VSS в Windows Server 2003 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="63664-103">What's New in VSS in Windows Server 2003 SP1</span></span>

<span data-ttu-id="63664-104">В следующем списке перечислены дополнения и изменения в интерфейсе служба теневого копирования томов в Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="63664-104">The following list indicates additions and changes to the Volume Shadow Copy Service interface in Windows Server 2003 with Service Pack 1 (SP1):</span></span>

## <a name="auto-recovery"></a><span data-ttu-id="63664-105">Автоматическое восстановление</span><span class="sxs-lookup"><span data-stu-id="63664-105">Auto-recovery</span></span>

<span data-ttu-id="63664-106">[*Автоматическое восстановление*](vssgloss-a.md) позволяет записывающим компонентом времени обновлять компоненты в теневой копии, прежде чем теневая копия будет окончательно изменена на доступ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63664-106">[*Auto-recovery*](vssgloss-a.md) allows writers a time to update components in a shadow copy before the shadow copy is permanently changed to read-only.</span></span> <span data-ttu-id="63664-107">Например, базе данных может потребоваться откатить все незавершенные транзакции для всех теневых копий (модуль записи базы данных установил флаг **\_ \_ \_ восстановления резервной копии VSS CF** для компонентов базы данных).</span><span class="sxs-lookup"><span data-stu-id="63664-107">For example, a database may need to rollback any incomplete transactions for all shadow copies (the database writer would set the **VSS\_CF\_BACKUP\_RECOVERY** flag for the database components).</span></span> <span data-ttu-id="63664-108">Автоматическое восстановление, инициированное инициатором запроса, позволяет выполнять детализированное восстановление (например, восстановление одной таблицы в базе данных или одной папки на почтовом сервере) или откат для поддержки интеллектуального анализа данных для анализа, который будет слишком замедляться для рабочего сервера (инициатор запроса добавляет к контексту теневого копирования **\_ \_ инструкцию VSS VOLSNAP attr \_ ROLLBACK \_ Recovery** ). Автоматическое восстановление несовместимо с транспортными теневыми копиями, но эти же функции поддерживаются с помощью [быстрого восстановления с помощью переносимых теневых скопированных томов](fast-recovery-using-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="63664-108">Auto-recovery initiated by the requester allows both fine-grained restore (for example restoring one table in a database or one folder on a mail server), or the rollback to support data mining to perform analysis that would be too slow for a production server (the requester would add **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** to the shadow copy context.) Auto-recovery is not compatible with transportable shadow copies, but the same functionality is supported by using [Fast Recovery Using Transportable Shadow Copied Volumes](fast-recovery-using-transportable-shadow-copied-volumes.md).</span></span>

<span data-ttu-id="63664-109">Следующие элементы программирования имеют изменения для поддержки автоматического восстановления:</span><span class="sxs-lookup"><span data-stu-id="63664-109">The following programming elements have changes to support auto-recovery:</span></span>

<span data-ttu-id="63664-110">Методы класса</span><span class="sxs-lookup"><span data-stu-id="63664-110">Class methods</span></span>

-   [<span data-ttu-id="63664-111">**Квссвритер:: Жетснапшотдевиценаме**</span><span class="sxs-lookup"><span data-stu-id="63664-111">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [<span data-ttu-id="63664-112">**Квссвритер:: Онпостснапшот**</span><span class="sxs-lookup"><span data-stu-id="63664-112">**CVssWriter::OnPostSnapshot**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

<span data-ttu-id="63664-113">Перечисления</span><span class="sxs-lookup"><span data-stu-id="63664-113">Enumerations</span></span>

-   [<span data-ttu-id="63664-114">**\_ \_ Флаги компонента VSS**</span><span class="sxs-lookup"><span data-stu-id="63664-114">**VSS\_COMPONENT\_FLAGS**</span></span>](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [<span data-ttu-id="63664-115">**\_\_ \_ атрибуты моментального снимка тома VSS \_**</span><span class="sxs-lookup"><span data-stu-id="63664-115">**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

<span data-ttu-id="63664-116">Методы интерфейса</span><span class="sxs-lookup"><span data-stu-id="63664-116">Interface methods</span></span>

-   [<span data-ttu-id="63664-117">**Ивсспровидеркреатеснапшотсет::P Рефиналкоммитснапшотс**</span><span class="sxs-lookup"><span data-stu-id="63664-117">**IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [<span data-ttu-id="63664-118">**Ивсспровидеркреатеснапшотсет::P Остфиналкоммитснапшотс**</span><span class="sxs-lookup"><span data-stu-id="63664-118">**IVssProviderCreateSnapshotSet::PostFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a><span data-ttu-id="63664-119">Полная поддержка переносимых теневых копий</span><span class="sxs-lookup"><span data-stu-id="63664-119">Full Support for Transportable Shadow Copies</span></span>

<span data-ttu-id="63664-120">Транспортные теневые копии поддерживаются во всех выпусках Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="63664-120">Transportable shadow copies are supported in all editions of Windows Server 2003 with SP1.</span></span> <span data-ttu-id="63664-121">Дополнительные сведения см. в разделе [Импорт переносимых теневых скопированных томов](importing-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="63664-121">For more information, see [Importing Transportable Shadow Copied Volumes](importing-transportable-shadow-copied-volumes.md).</span></span>

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="63664-122">Быстрое восстановление с помощью переносимых теневых скопированных томов</span><span class="sxs-lookup"><span data-stu-id="63664-122">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

[<span data-ttu-id="63664-123">Быстрое восстановление с помощью переносимых теневых скопированных томов</span><span class="sxs-lookup"><span data-stu-id="63664-123">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a><span data-ttu-id="63664-124">Управление областью хранения теневых копий</span><span class="sxs-lookup"><span data-stu-id="63664-124">Shadow copy storage area management</span></span>

[<span data-ttu-id="63664-125">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="63664-125">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



