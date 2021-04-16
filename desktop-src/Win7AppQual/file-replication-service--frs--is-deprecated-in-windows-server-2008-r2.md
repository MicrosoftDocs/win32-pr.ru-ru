---
description: .
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Служба репликации файлов (FRS) является устаревшей в Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3acf7eb6310f2c296abfd5eb1db0f30c4b48dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712036"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a><span data-ttu-id="02852-103">Служба репликации файлов (FRS) является устаревшей в Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="02852-103">File Replication Service (FRS) Is Deprecated in Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="02852-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="02852-104">Platform</span></span>

 <span data-ttu-id="02852-105">**Серверы —** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="02852-105">**Servers -** Windows Server 2008 R2</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="02852-106">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="02852-106">Feature Impact</span></span>

 <span data-ttu-id="02852-107">**Уровень серьезности —** Высоком</span><span class="sxs-lookup"><span data-stu-id="02852-107">**Severity -** High</span></span>  
<span data-ttu-id="02852-108">**Частота —** Высоком</span><span class="sxs-lookup"><span data-stu-id="02852-108">**Frequency -** High</span></span>  


## <a name="description"></a><span data-ttu-id="02852-109">Описание</span><span class="sxs-lookup"><span data-stu-id="02852-109">Description</span></span>

<span data-ttu-id="02852-110">В Windows Server 2008 R2 служба репликации файлов (FRS) не может использоваться для репликации папок распределенная файловая система (DFS) или пользовательских (не являющихся SYSVOL) данных.</span><span class="sxs-lookup"><span data-stu-id="02852-110">In Windows Server 2008 R2, File Replication Service (FRS) cannot be used for replicating Distributed File System (DFS) folders or custom (non-SYSVOL) data.</span></span> <span data-ttu-id="02852-111">Контроллер домена Windows Server 2008 R2 по-прежнему может использовать службу FRS для репликации содержимого общего ресурса SYSVOL в домене, использующем службу FRS для репликации общего ресурса SYSVOL между контроллерами домена.</span><span class="sxs-lookup"><span data-stu-id="02852-111">A Windows Server 2008 R2 domain controller can still use FRS to replicate the contents of the SYSVOL share in a domain that uses FRS for replicating the SYSVOL share between domain controllers.</span></span> <span data-ttu-id="02852-112">Однако серверы Windows Server 2008 R2 не могут использовать службу FRS для репликации содержимого всех реплик, отличных от общего ресурса SYSVOL.</span><span class="sxs-lookup"><span data-stu-id="02852-112">However, Windows Server 2008 R2 servers cannot use FRS to replicate the contents of any replica set apart from the SYSVOL share.</span></span> <span data-ttu-id="02852-113">Служба репликация DFS является заменой FRS и может использоваться для репликации содержимого общей папки SYSVOL, папок DFS, а также других пользовательских данных (не являющихся SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="02852-113">The DFS Replication service is a replacement for FRS and can be used to replicate the contents of the SYSVOL share, DFS folders as well as other custom (non-SYSVOL) data.</span></span> <span data-ttu-id="02852-114">Перенесите все наборы реплик FRS, не относящиеся к SYSVOL, в репликация DFS.</span><span class="sxs-lookup"><span data-stu-id="02852-114">Migrate all non-SYSVOL FRS replica sets to DFS Replication.</span></span> <span data-ttu-id="02852-115">Также настоятельно рекомендуется перенести репликацию общей папки SYSVOL с FRS на репликация DFS так как репликация DFS является более надежным, масштабируемым и имеет лучшую производительность репликации по сравнению с FRS.</span><span class="sxs-lookup"><span data-stu-id="02852-115">We also highly recommend that you migrate replication of the SYSVOL share from FRS to DFS Replication because DFS Replication is more robust, scalable and has better replication performance than FRS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="02852-116">Проявление</span><span class="sxs-lookup"><span data-stu-id="02852-116">Manifestation</span></span>

<span data-ttu-id="02852-117">Репликация FRS пользовательских данных будет прерываться необратимо при обновлении на месте.</span><span class="sxs-lookup"><span data-stu-id="02852-117">FRS replication of custom data will break irreversibly upon in-place upgrade.</span></span> <span data-ttu-id="02852-118">Единственный способ восстановления из этой ситуации — переустановить более старую операционную систему на сервере и повторно инициализировать репликацию FRS.</span><span class="sxs-lookup"><span data-stu-id="02852-118">The only way to recover from this situation would be to reinstall an older operating system on the server and reinitialize FRS replication.</span></span> <span data-ttu-id="02852-119">Серверы, которые были обновлены до Windows Server 2008 R2, не могут участвовать в существующих группах репликации FRS.</span><span class="sxs-lookup"><span data-stu-id="02852-119">Servers that have been upgraded to Windows Server 2008 R2 are not allowed to participate in existing FRS replication groups.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="02852-120">Снижение влияния</span><span class="sxs-lookup"><span data-stu-id="02852-120">Mitigation of Impact</span></span>

<span data-ttu-id="02852-121">Чтобы предотвратить возникновение проблем, которые могут возникнуть в результате этих изменений, перенесите пользовательские наборы репликации FRS в репликация DFS.</span><span class="sxs-lookup"><span data-stu-id="02852-121">To prevent issues that might occur as a result of these changes, migrate custom FRS replication sets to DFS Replication.</span></span> <span data-ttu-id="02852-122">Служба репликация DFS имеет множество преимуществ по сравнению с FRS, в том числе улучшенные средства управления, повышенная производительность и делегированное управление.</span><span class="sxs-lookup"><span data-stu-id="02852-122">The DFS Replication service has many benefits over FRS, including improved management tools, higher performance, and delegated management.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="02852-123">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="02852-123">Links to Other Resources</span></span>

-   <span data-ttu-id="02852-124">[Обзор FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="02852-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span></span>
-   [<span data-ttu-id="02852-125">Репликация распределенной файловой системы (DFS): вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="02852-125">Distributed File System Replication: Frequently Asked Questions</span></span>](/windows-server/storage/dfs-replication/dfsr-faq)
-   [<span data-ttu-id="02852-126">Руководство по миграции репликации SYSVOL: FRS — репликация DFS</span><span class="sxs-lookup"><span data-stu-id="02852-126">SYSVOL Replication Migration Guide: FRS to DFS Replication</span></span>](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
