---
description: Модуль записи Active Directory не требует специальных действий во время операций резервного копирования.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Резервное копирование и восстановление VSS для Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541746"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a><span data-ttu-id="f29d8-103">Резервное копирование и восстановление VSS для Active Directory</span><span class="sxs-lookup"><span data-stu-id="f29d8-103">VSS Backup and Restore of the Active Directory</span></span>

<span data-ttu-id="f29d8-104">Модуль записи Active Directory не требует специальных действий во время операций резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f29d8-104">The Active Directory writer requires no special actions during backup operations.</span></span> <span data-ttu-id="f29d8-105">Модуль записи предоставит инициатору запроса сведения о компоненте и наборе файлов, а инициатор запроса использует эти сведения, чтобы решить, какие файлы следует копировать на носитель резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f29d8-105">The writer will provide the requester with component and file set information, and the requester uses that information to decide which files to copy to backup media.</span></span> <span data-ttu-id="f29d8-106">Для резервного копирования Active Directory нет необходимости использовать специальные API-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f29d8-106">There is no need to use any special APIs to back up the Active Directory.</span></span>

<span data-ttu-id="f29d8-107">Способ выполнения восстановления зависит от того, восстанавливается ли Active Directory в ходе аварийного восстановления или если восстановление выполняется в систему, в которой выполняется Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f29d8-107">How a restore is performed depends on whether the Active Directory is be restored as part of a disaster recovery operation, or if the restore is to a system on which the Active Directory is running.</span></span> <span data-ttu-id="f29d8-108">Кроме того, возраст резервной копии состояния Active Directory может быть проблемой из-за Active Directory захоронений.</span><span class="sxs-lookup"><span data-stu-id="f29d8-108">In addition, the age of the backup copy of the Active Directory state may be an issue because of Active Directory tombstones.</span></span>

## <a name="active-directory-restoration-following-disaster-recovery"></a><span data-ttu-id="f29d8-109">Восстановление Active Directory после аварийного восстановления</span><span class="sxs-lookup"><span data-stu-id="f29d8-109">Active Directory Restoration following Disaster Recovery</span></span>

<span data-ttu-id="f29d8-110">После сбоя, нуждающегося в аварийном восстановлении, Active Directory можно восстановить в ходе восстановления состояния операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f29d8-110">Following a crash requiring disaster recovery, the Active Directory can be restored as part of the restoration of the operating system state.</span></span>

<span data-ttu-id="f29d8-111">Эта операция восстановления, по сути, является восстановлением, не предназначенным для записи.</span><span class="sxs-lookup"><span data-stu-id="f29d8-111">This restore operation is essentially a writerless restore.</span></span>

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a><span data-ttu-id="f29d8-112">Active Directory восстановление в системе, где она работает</span><span class="sxs-lookup"><span data-stu-id="f29d8-112">Active Directory Restoration on the System where It Is Running</span></span>

<span data-ttu-id="f29d8-113">Если в данный момент на сервере выполняется Active Directory, система должна быть перезагружена в режиме восстановления служб каталогов.</span><span class="sxs-lookup"><span data-stu-id="f29d8-113">The system must be rebooted in Directory Services Restore mode if the Active Directory is currently running on the server.</span></span>

<span data-ttu-id="f29d8-114">После этого операционная система будет работать без Active Directory, и проверка всех пользователей выполняется через диспетчер учетных записей безопасности (SAM) в реестре.</span><span class="sxs-lookup"><span data-stu-id="f29d8-114">The operating system will then be running without the Active Directory, and all user validation occurs through the Security Accounts Manager (SAM) in the registry.</span></span> <span data-ttu-id="f29d8-115">Только администратор имеет разрешение на восстановление Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f29d8-115">Only the administrator has permission to recover the Active Directory.</span></span>

<span data-ttu-id="f29d8-116">В режиме восстановления службы каталогов восстановление VSS может выполняться обычным образом.</span><span class="sxs-lookup"><span data-stu-id="f29d8-116">Once in Directory Service Restore mode, a VSS restore can proceed normally.</span></span> <span data-ttu-id="f29d8-117">Нет причин использовать интерфейсы API Win32 Active Directory, не связанные с VSS, для восстановления состояния Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f29d8-117">There is no reason to use non-VSS Win32 Active Directory APIs to restore the Active Directory state.</span></span>

## <a name="active-directory-restores-and-active-directory-tombstones"></a><span data-ttu-id="f29d8-118">Active Directory восстановления и Active Directory захоронений</span><span class="sxs-lookup"><span data-stu-id="f29d8-118">Active Directory Restores and Active Directory Tombstones</span></span>

<span data-ttu-id="f29d8-119">Любой план восстановления должен гарантировать, что возраст резервной копии не должен превышать время жизни захоронения Active Directory (по умолчанию — 60 дней).</span><span class="sxs-lookup"><span data-stu-id="f29d8-119">Any recovery plan should ensure that the age of the backup should not exceed the Active Directory Tombstone Lifetime (default is 60 days).</span></span>

<span data-ttu-id="f29d8-120">Восстановление резервной копии старше, чем захоронение, приведет к тому, что контроллер домена будет иметь объекты, которые не реплицируются на другие серверы.</span><span class="sxs-lookup"><span data-stu-id="f29d8-120">Restoration of a backup older than the tombstone will cause a domain controller to have objects that are not replicated to the other servers.</span></span>

<span data-ttu-id="f29d8-121">Эти объекты, которые не реплицируются, не будут автоматически удалены на этом (восстановленном) контроллере домена, так как объекты-захоронения этих объектов на других репликах уже были удалены.</span><span class="sxs-lookup"><span data-stu-id="f29d8-121">Those objects that are not replicated will not be deleted automatically on that (restored) domain controller because the tombstones of those objects on the other replicas have already been deleted.</span></span>

<span data-ttu-id="f29d8-122">Администратору придется вручную удалить каждый из объектов на восстановленном контроллере домена, который не реплицируется.</span><span class="sxs-lookup"><span data-stu-id="f29d8-122">An administrator will have to manually delete each of the objects on the restored domain controller that are not replicated.</span></span> <span data-ttu-id="f29d8-123">Добавочное резервное копирование Active Directory не поддерживается; требуется полная резервная копия.</span><span class="sxs-lookup"><span data-stu-id="f29d8-123">Incremental backups of the Active Directory are not supported; a full backup is required.</span></span>

 

 



