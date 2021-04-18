---
description: Для быстрого восстановления можно использовать переносимые теневые копии.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Быстрое восстановление с помощью переносимых теневых скопированных томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693644"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="8d055-103">Быстрое восстановление с помощью переносимых теневых скопированных томов</span><span class="sxs-lookup"><span data-stu-id="8d055-103">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

<span data-ttu-id="8d055-104">Для *быстрого восстановления* можно использовать [*переносимые теневые копии*](vssgloss-t.md) .</span><span class="sxs-lookup"><span data-stu-id="8d055-104">[*Transportable shadow copies*](vssgloss-t.md) can be used to facilitate a *fast recovery*.</span></span>

<span data-ttu-id="8d055-105">Быстрое восстановление можно использовать для быстрого возврата к более ранней теневой копии.</span><span class="sxs-lookup"><span data-stu-id="8d055-105">Fast recovery can be used to quickly revert to an earlier shadow copy.</span></span> <span data-ttu-id="8d055-106">Ниже приведены необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="8d055-106">The steps involved are:</span></span>

1.  <span data-ttu-id="8d055-107">Создайте транспортную теневую копию соответствующих LUN.</span><span class="sxs-lookup"><span data-stu-id="8d055-107">Create the transportable shadow copy of the appropriate LUNs.</span></span> <span data-ttu-id="8d055-108">Теневая копия может быть либо [*постоянной*](vssgloss-p.md) , либо неустойчивой.</span><span class="sxs-lookup"><span data-stu-id="8d055-108">The shadow copy can be either [*persistent*](vssgloss-p.md) or nonpersistent.</span></span>
2.  <span data-ttu-id="8d055-109">Удаление исходных LUN</span><span class="sxs-lookup"><span data-stu-id="8d055-109">Remove the original LUNs</span></span>
    1.  <span data-ttu-id="8d055-110">Если компьютер находится в кластере, пометьте затронутые дисковые ресурсы как автономные или включите [режим обслуживания](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) для этих дисковых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d055-110">If the computer is inside a cluster, mark the affected disk resources as offline, or enable the [maintenance mode](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) for these disk resources.</span></span>
    2.  <span data-ttu-id="8d055-111">Маскирование затронутых LUN с этого компьютера (и всех остальных узлов, если компьютер находится в кластере).</span><span class="sxs-lookup"><span data-stu-id="8d055-111">Mask the affected LUNs from this computer (and all other nodes if the computer is in a cluster).</span></span>
3.  <span data-ttu-id="8d055-112">Импортируйте теневую копию с помощью метода [**ивссбаккупкомпонентс:: импортснапшотс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) .</span><span class="sxs-lookup"><span data-stu-id="8d055-112">Import the shadow copy using the [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) method.</span></span>
4.  <span data-ttu-id="8d055-113">Разбейте теневую копию с помощью метода [**ивссбаккупкомпонентс:: бреакснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .</span><span class="sxs-lookup"><span data-stu-id="8d055-113">Break the shadow copy using the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>
5.  <span data-ttu-id="8d055-114">Пометьте новые тома теневых копий как доступные для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8d055-114">Mark the new shadow copy volumes as read/write.</span></span>
6.  <span data-ttu-id="8d055-115">Если компьютер находится в кластере, предоставьте новые номера LUN теневого копирования в качестве исходных.</span><span class="sxs-lookup"><span data-stu-id="8d055-115">If the computer is in a cluster, expose the new shadow copy LUNs as the original LUNs.</span></span>
    1.  <span data-ttu-id="8d055-116">Снимите маску LUN теневой копии на другие узлы в кластере.</span><span class="sxs-lookup"><span data-stu-id="8d055-116">Unmask the shadow copy LUNs to the other nodes in the cluster.</span></span>
    2.  <span data-ttu-id="8d055-117">Пометьте ресурсы, которые ранее были помечены как подключенные к сети, или отключите режим обслуживания для этих дисковых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d055-117">Mark the resources that were previously marked as offline as online, or disable the maintenance mode for those disk resources.</span></span>

> [!Note]  
> <span data-ttu-id="8d055-118">Перепереносимые теневые копии в кластере не поддерживаются до Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8d055-118">Transportable shadow copies in a cluster are not supported before Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="8d055-119">Эта поддержка поддерживается только с соответствующими номерами LUN, у которых есть по крайней мере одна страница данных продукта (VPD) 0x83 с \_ идентификаторами хранилища 1, 2 или 8 и сопоставление 0, а LUN должны поддерживать базовый диск с разделением MBR.</span><span class="sxs-lookup"><span data-stu-id="8d055-119">This is only supported with compliant LUNs, which have at least one SCSI Vital Product Data (VPD) page 0x83 STORAGE\_IDENTIFIER of type 1,2, or 8, and association 0, and the LUNs must maintain a basic disk with MBR partitioning.</span></span>

 

 

 
