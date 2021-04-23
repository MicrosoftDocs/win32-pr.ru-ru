---
title: Функции резервного копирования каталога
description: Следующие функции используются с операциями резервного копирования и восстановления в службах домен Active Directory.
ms.assetid: 6683240e-d324-43b9-b673-dda03c89612c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7e3d8b05095cea26276dfebaddf95fb9e4e8e2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987347"
---
# <a name="directory-backup-functions"></a><span data-ttu-id="044c6-103">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="044c6-103">Directory Backup Functions</span></span>

<span data-ttu-id="044c6-104">\[Эти функции доступны для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="044c6-104">\[These functions are available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="044c6-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="044c6-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="044c6-106">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="044c6-106">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="044c6-107">Следующие функции используются с операциями резервного копирования и восстановления в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="044c6-107">The following functions are used with the backup and restore operations in Active Directory Domain Services:</span></span>

-   [<span data-ttu-id="044c6-108">**дсбаккупклосе**</span><span class="sxs-lookup"><span data-stu-id="044c6-108">**DsBackupClose**</span></span>](dsbackupclose.md)
-   [<span data-ttu-id="044c6-109">**дсбаккупенд**</span><span class="sxs-lookup"><span data-stu-id="044c6-109">**DsBackupEnd**</span></span>](dsbackupend.md)
-   [<span data-ttu-id="044c6-110">**дсбаккупфри**</span><span class="sxs-lookup"><span data-stu-id="044c6-110">**DsBackupFree**</span></span>](dsbackupfree.md)
-   [<span data-ttu-id="044c6-111">**дсбаккупжетбаккуплогс**</span><span class="sxs-lookup"><span data-stu-id="044c6-111">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
-   [<span data-ttu-id="044c6-112">**дсбаккупжетдатабасенамес**</span><span class="sxs-lookup"><span data-stu-id="044c6-112">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
-   [<span data-ttu-id="044c6-113">**дсбаккупопенфиле**</span><span class="sxs-lookup"><span data-stu-id="044c6-113">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
-   [<span data-ttu-id="044c6-114">**дсбаккуппрепаре**</span><span class="sxs-lookup"><span data-stu-id="044c6-114">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
-   [<span data-ttu-id="044c6-115">**дсбаккупреад**</span><span class="sxs-lookup"><span data-stu-id="044c6-115">**DsBackupRead**</span></span>](dsbackupread.md)
-   [<span data-ttu-id="044c6-116">**дсбаккуптрункателогс**</span><span class="sxs-lookup"><span data-stu-id="044c6-116">**DsBackupTruncateLogs**</span></span>](dsbackuptruncatelogs.md)
-   [<span data-ttu-id="044c6-117">**дсиснтдсонлине**</span><span class="sxs-lookup"><span data-stu-id="044c6-117">**DsIsNTDSOnline**</span></span>](dsisntdsonline.md)
-   [<span data-ttu-id="044c6-118">**дсресторинд**</span><span class="sxs-lookup"><span data-stu-id="044c6-118">**DsRestoreEnd**</span></span>](dsrestoreend.md)
-   [<span data-ttu-id="044c6-119">**дсресторежетдатабаселокатионс**</span><span class="sxs-lookup"><span data-stu-id="044c6-119">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
-   [<span data-ttu-id="044c6-120">**дсресторепрепаре**</span><span class="sxs-lookup"><span data-stu-id="044c6-120">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
-   [<span data-ttu-id="044c6-121">**дсресторерегистер**</span><span class="sxs-lookup"><span data-stu-id="044c6-121">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
-   [<span data-ttu-id="044c6-122">**дсресторерегистеркомплете**</span><span class="sxs-lookup"><span data-stu-id="044c6-122">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
-   [<span data-ttu-id="044c6-123">**дссетаусидентити**</span><span class="sxs-lookup"><span data-stu-id="044c6-123">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
-   [<span data-ttu-id="044c6-124">**дссеткуррентбаккуплог**</span><span class="sxs-lookup"><span data-stu-id="044c6-124">**DsSetCurrentBackupLog**</span></span>](dssetcurrentbackuplog.md)

 

 