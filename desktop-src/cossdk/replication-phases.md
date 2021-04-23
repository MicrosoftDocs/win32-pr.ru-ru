---
description: COMREPL выполняет свою работу в три этапа.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Этапы репликации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710791"
---
# <a name="replication-phases"></a><span data-ttu-id="7500f-103">Этапы репликации</span><span class="sxs-lookup"><span data-stu-id="7500f-103">Replication Phases</span></span>

<span data-ttu-id="7500f-104">COMREPL выполняет свою работу в три этапа.</span><span class="sxs-lookup"><span data-stu-id="7500f-104">COMREPL does its work in three phases.</span></span> <span data-ttu-id="7500f-105">Процесс репликации делится на отдельные этапы по следующим двум причинам.</span><span class="sxs-lookup"><span data-stu-id="7500f-105">The replication process is divided into distinct phases for the following two reasons:</span></span>

-   <span data-ttu-id="7500f-106">Разделение работы для подготовки источника от работы, выполненной на каждом целевом объекте</span><span class="sxs-lookup"><span data-stu-id="7500f-106">To separate work done to prepare the source from work that is done on each target</span></span>
-   <span data-ttu-id="7500f-107">Задержка изменения целевого объекта до получения всех данных из источника</span><span class="sxs-lookup"><span data-stu-id="7500f-107">To delay modification of the target until all data has been acquired from the source</span></span>

<span data-ttu-id="7500f-108">Этапы репликации приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="7500f-108">The replication phases are as follows.</span></span>



| <span data-ttu-id="7500f-109">Этап</span><span class="sxs-lookup"><span data-stu-id="7500f-109">Phase</span></span>         | <span data-ttu-id="7500f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7500f-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7500f-111">Фаза подготовки</span><span class="sxs-lookup"><span data-stu-id="7500f-111">Prepare phase</span></span> | <span data-ttu-id="7500f-112">Экспортирует все установленные приложения локально на исходном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7500f-112">Exports all the installed applications locally on the source computer.</span></span> <span data-ttu-id="7500f-113">Этот этап не затрагивает настройку целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="7500f-113">This phase does not touch the configuration of any targets.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7500f-114">Стадия копирования</span><span class="sxs-lookup"><span data-stu-id="7500f-114">Copy phase</span></span>    | <span data-ttu-id="7500f-115">Копирует данные на конечный компьютер.</span><span class="sxs-lookup"><span data-stu-id="7500f-115">Copies data to a target computer.</span></span> <span data-ttu-id="7500f-116">Все приложения, экспортированные в источнике, копируются в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="7500f-116">All applications exported on the source are copied to the target.</span></span> <span data-ttu-id="7500f-117">Это операция копирования файлов.</span><span class="sxs-lookup"><span data-stu-id="7500f-117">This is a file copy operation.</span></span> <span data-ttu-id="7500f-118">(См. раздел [Управление файлами](file-management.md).) На этом шаге также запрашиваются некоторые данные с исходного компьютера, которые не инкапсулированы в экспортированных файлах приложения (например, удостоверения приложений).</span><span class="sxs-lookup"><span data-stu-id="7500f-118">(See [File Management](file-management.md).) This step also acquires some data from the source computer that is not encapsulated within exported application files (for example, application identities).</span></span> <span data-ttu-id="7500f-119">Эти данные хранятся в памяти в COMREPL.</span><span class="sxs-lookup"><span data-stu-id="7500f-119">This data is held in memory within COMREPL.</span></span> <span data-ttu-id="7500f-120">Этот этап не затрагивает настройку конечных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="7500f-120">This phase does not touch the configuration of any target computers.</span></span>                                                                               |
| <span data-ttu-id="7500f-121">Этап установки</span><span class="sxs-lookup"><span data-stu-id="7500f-121">Install phase</span></span> | <span data-ttu-id="7500f-122">Устанавливает исходный каталог на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="7500f-122">Installs source catalog on a target computer.</span></span> <span data-ttu-id="7500f-123">При запуске этого шага все данные, необходимые для перенастройки целевого объекта, находятся в файлах приложения в целевой файловой системе или хранятся как данные экземпляра в COMREPL.</span><span class="sxs-lookup"><span data-stu-id="7500f-123">When this step is initiated, all data required to reconfigure the target is within application files in the target's file system or is held as instance data within COMREPL.</span></span> <span data-ttu-id="7500f-124">На этом этапе будут удалены все установленные приложения на целевом компьютере (за исключением приложений, описанных в разделе [что реплицируется](what-gets-replicated.md)) перед установкой приложений, скопированных из источника.</span><span class="sxs-lookup"><span data-stu-id="7500f-124">This phase will delete all the installed applications on the target (except the applications described in [What Gets Replicated](what-gets-replicated.md)) prior to installing the applications copied from the source.</span></span> <span data-ttu-id="7500f-125">COMREPL устанавливается параллельно с несколькими целевыми объектами с помощью потока установки для каждого целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="7500f-125">COMREPL installs on multiple targets concurrently by using an install thread per target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7500f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7500f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7500f-127">Управление файлами</span><span class="sxs-lookup"><span data-stu-id="7500f-127">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="7500f-128">Ведение журнала и отчеты об ошибках</span><span class="sxs-lookup"><span data-stu-id="7500f-128">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="7500f-129">Использование COMREPL</span><span class="sxs-lookup"><span data-stu-id="7500f-129">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="7500f-130">Что реплицируется</span><span class="sxs-lookup"><span data-stu-id="7500f-130">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



