---
description: Чтобы включить перенос файлов приложения, COMREPL автоматически управляет набором папок файловой системы на исходном и целевом компьютере. Все эти папки COMREPL находятся в каталоге% системдир% \\ COM- \\ репликации.
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Управление файлами (службы компонентов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538723"
---
# <a name="file-management"></a><span data-ttu-id="3a50f-104">Управление файлами</span><span class="sxs-lookup"><span data-stu-id="3a50f-104">File Management</span></span>

<span data-ttu-id="3a50f-105">Чтобы включить перенос файлов приложения, COMREPL автоматически управляет набором папок файловой системы на исходном и целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="3a50f-105">To enable the transfer of application files, COMREPL automatically manages sets of file system folders on the source and target.</span></span> <span data-ttu-id="3a50f-106">Все эти папки COMREPL находятся в каталоге% системдир% \\ COM- \\ репликации.</span><span class="sxs-lookup"><span data-stu-id="3a50f-106">These COMREPL folders are all rooted in %systemdir%\\com\\replication.</span></span>

## <a name="source-folders"></a><span data-ttu-id="3a50f-107">Исходные папки</span><span class="sxs-lookup"><span data-stu-id="3a50f-107">Source folders</span></span>



| <span data-ttu-id="3a50f-108">Папка</span><span class="sxs-lookup"><span data-stu-id="3a50f-108">Folder</span></span>                   | <span data-ttu-id="3a50f-109">Назначение</span><span class="sxs-lookup"><span data-stu-id="3a50f-109">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a50f-110">репликасаурце</span><span class="sxs-lookup"><span data-stu-id="3a50f-110">ReplicaSource</span></span><br/> | <span data-ttu-id="3a50f-111">Приложения, экспортированные на этапе подготовки, хранятся здесь.</span><span class="sxs-lookup"><span data-stu-id="3a50f-111">Applications exported during the prepare phase are stored here.</span></span><br/> <span data-ttu-id="3a50f-112">Эта папка перезаписывается каждый раз при выполнении этапа подготовки к данному исходному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="3a50f-112">This folder is overwritten each time the prepare phase is executed against a given source computer.</span></span> <span data-ttu-id="3a50f-113">Эта папка никогда не удаляется явно, поэтому репликация на целевые объекты может быть выполнена в любое время после подготовки источника.</span><span class="sxs-lookup"><span data-stu-id="3a50f-113">This folder is never explicitly deleted, so replication to targets can take place at any time after the source is prepared.</span></span><br/> <span data-ttu-id="3a50f-114">Каждое приложение хранится в собственной вложенной папке с именем <appName> + <appID> .</span><span class="sxs-lookup"><span data-stu-id="3a50f-114">Each application is stored in its own subfolder named <appName>+<appID>.</span></span><br/> |



 

## <a name="target-folders"></a><span data-ttu-id="3a50f-115">Папки назначения</span><span class="sxs-lookup"><span data-stu-id="3a50f-115">Target folders</span></span>



| <span data-ttu-id="3a50f-116">Папка</span><span class="sxs-lookup"><span data-stu-id="3a50f-116">Folder</span></span>                    | <span data-ttu-id="3a50f-117">Назначение</span><span class="sxs-lookup"><span data-stu-id="3a50f-117">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a50f-118">репликанев</span><span class="sxs-lookup"><span data-stu-id="3a50f-118">ReplicaNew</span></span><br/>     | <span data-ttu-id="3a50f-119">Фаза копирования копирует все файлы и вложенные папки из Репликасаурце в источнике в Репликанев на целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="3a50f-119">The copy phase copies all files and subfolders from ReplicaSource on the source to ReplicaNew on the target.</span></span> <span data-ttu-id="3a50f-120">Любое предыдущее содержимое Репликанев удаляется каждый раз при выполнении этапа копирования для заданного целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="3a50f-120">Any previous contents of ReplicaNew are deleted each time the copy phase is run against a given target.</span></span><br/> <span data-ttu-id="3a50f-121">Эта папка существует, только пока выполняется процесс репликации.</span><span class="sxs-lookup"><span data-stu-id="3a50f-121">This folder exists only while the replication process is running.</span></span> <span data-ttu-id="3a50f-122">(См. Репликакуррент.)</span><span class="sxs-lookup"><span data-stu-id="3a50f-122">(See ReplicaCurrent.)</span></span><br/>           |
| <span data-ttu-id="3a50f-123">репликакуррент</span><span class="sxs-lookup"><span data-stu-id="3a50f-123">ReplicaCurrent</span></span><br/> | <span data-ttu-id="3a50f-124">Реплицированные приложения, установленные на целевом объекте, хранятся здесь.</span><span class="sxs-lookup"><span data-stu-id="3a50f-124">The replicated applications currently installed on the target are stored here.</span></span><br/> <span data-ttu-id="3a50f-125">После запуска фазы установки папка Репликанев переименовывается в Репликакуррент.</span><span class="sxs-lookup"><span data-stu-id="3a50f-125">When the install phase is started, the ReplicaNew folder is renamed to ReplicaCurrent.</span></span> <span data-ttu-id="3a50f-126">Если существует папка Репликакуррент, она переименовывается в Репликаолд.</span><span class="sxs-lookup"><span data-stu-id="3a50f-126">If there is an existing ReplicaCurrent folder, it is renamed to ReplicaOld.</span></span> <span data-ttu-id="3a50f-127">При наличии существующей папки Репликаолд ее содержимое удаляется.</span><span class="sxs-lookup"><span data-stu-id="3a50f-127">If there is an existing ReplicaOld folder, its contents are deleted.</span></span><br/> |
| <span data-ttu-id="3a50f-128">репликаолд</span><span class="sxs-lookup"><span data-stu-id="3a50f-128">ReplicaOld</span></span><br/>     | <span data-ttu-id="3a50f-129">Сохраняет файлы приложения, установленные во время следующей репликации.</span><span class="sxs-lookup"><span data-stu-id="3a50f-129">Saves the application files installed during the next to last replication.</span></span> <span data-ttu-id="3a50f-130">Эти файлы сохраняются только в целях резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="3a50f-130">These files are saved for backup purposes only.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="3a50f-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3a50f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a50f-132">Ведение журнала и отчеты об ошибках</span><span class="sxs-lookup"><span data-stu-id="3a50f-132">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="3a50f-133">Этапы репликации</span><span class="sxs-lookup"><span data-stu-id="3a50f-133">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="3a50f-134">Использование COMREPL</span><span class="sxs-lookup"><span data-stu-id="3a50f-134">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="3a50f-135">Что реплицируется</span><span class="sxs-lookup"><span data-stu-id="3a50f-135">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 




