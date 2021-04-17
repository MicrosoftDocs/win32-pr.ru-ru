---
description: Для файловых очередей используются следующие функции.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Функции очереди файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663784"
---
# <a name="file-queue-functions"></a><span data-ttu-id="65ebb-103">Функции очереди файлов</span><span class="sxs-lookup"><span data-stu-id="65ebb-103">File Queue Functions</span></span>

<span data-ttu-id="65ebb-104">Для файловых очередей используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="65ebb-104">The following functions are used with file queues.</span></span>



| <span data-ttu-id="65ebb-105">Функция</span><span class="sxs-lookup"><span data-stu-id="65ebb-105">Function</span></span>                                                             | <span data-ttu-id="65ebb-106">Описание</span><span class="sxs-lookup"><span data-stu-id="65ebb-106">Description</span></span>                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65ebb-107">**сетупклосефилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="65ebb-107">**SetupCloseFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | <span data-ttu-id="65ebb-108">Завершает очередь.</span><span class="sxs-lookup"><span data-stu-id="65ebb-108">Terminates the queue.</span></span> <span data-ttu-id="65ebb-109">Все оставшиеся транзакции не фиксируются.</span><span class="sxs-lookup"><span data-stu-id="65ebb-109">Any remaining transactions are not committed.</span></span>                                   |
| [<span data-ttu-id="65ebb-110">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="65ebb-110">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | <span data-ttu-id="65ebb-111">Фиксирует все транзакции в очереди.</span><span class="sxs-lookup"><span data-stu-id="65ebb-111">Commits all queued transactions.</span></span>                                                                      |
| [<span data-ttu-id="65ebb-112">**сетупопенфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="65ebb-112">**SetupOpenFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | <span data-ttu-id="65ebb-113">Инициализирует и возвращает маркер в файловую очередь.</span><span class="sxs-lookup"><span data-stu-id="65ebb-113">Initializes and returns a handle to the file queue.</span></span>                                                   |
| [<span data-ttu-id="65ebb-114">**сетуппромптребут**</span><span class="sxs-lookup"><span data-stu-id="65ebb-114">**SetupPromptReboot**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | <span data-ttu-id="65ebb-115">При необходимости предлагает пользователю перезагрузить свой компьютер.</span><span class="sxs-lookup"><span data-stu-id="65ebb-115">Prompts the user to reboot his or her computer, if necessary.</span></span>                                         |
| [<span data-ttu-id="65ebb-116">**сетупкуеуекопи**</span><span class="sxs-lookup"><span data-stu-id="65ebb-116">**SetupQueueCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | <span data-ttu-id="65ebb-117">Ставит в очередь копию файла.</span><span class="sxs-lookup"><span data-stu-id="65ebb-117">Queues a file copy.</span></span>                                                                                   |
| [<span data-ttu-id="65ebb-118">**сетупкуеуекописектион**</span><span class="sxs-lookup"><span data-stu-id="65ebb-118">**SetupQueueCopySection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | <span data-ttu-id="65ebb-119">Ставит в очередь файлы в разделе файлы копирования INF.</span><span class="sxs-lookup"><span data-stu-id="65ebb-119">Queues the files in an INF Copy Files section.</span></span>                                                        |
| [<span data-ttu-id="65ebb-120">**сетупкуеуедефаулткопи**</span><span class="sxs-lookup"><span data-stu-id="65ebb-120">**SetupQueueDefaultCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | <span data-ttu-id="65ebb-121">Ставит в очередь файлы в разделе INF-файлов копирования, используя сведения по умолчанию, указанные в INF-файле.</span><span class="sxs-lookup"><span data-stu-id="65ebb-121">Queues the files in an INF Copy Files section using the default information specified in an INF file.</span></span> |
| [<span data-ttu-id="65ebb-122">**сетупкуеуеделете**</span><span class="sxs-lookup"><span data-stu-id="65ebb-122">**SetupQueueDelete**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | <span data-ttu-id="65ebb-123">Ставит в очередь удаление файлов.</span><span class="sxs-lookup"><span data-stu-id="65ebb-123">Queues a file deletion.</span></span>                                                                               |
| [<span data-ttu-id="65ebb-124">**сетупкуеуеделетесектион**</span><span class="sxs-lookup"><span data-stu-id="65ebb-124">**SetupQueueDeleteSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | <span data-ttu-id="65ebb-125">Ставит в очередь файлы в разделе Удаление файлов INF.</span><span class="sxs-lookup"><span data-stu-id="65ebb-125">Queues the files in an INF Delete Files section.</span></span>                                                      |
| [<span data-ttu-id="65ebb-126">**сетупкуеуеренаме**</span><span class="sxs-lookup"><span data-stu-id="65ebb-126">**SetupQueueRename**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | <span data-ttu-id="65ebb-127">Ставит в очередь переименование файлов.</span><span class="sxs-lookup"><span data-stu-id="65ebb-127">Queues a file rename.</span></span>                                                                                 |
| [<span data-ttu-id="65ebb-128">**сетупкуеуеренамесектион**</span><span class="sxs-lookup"><span data-stu-id="65ebb-128">**SetupQueueRenameSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | <span data-ttu-id="65ebb-129">Ставит в очередь файлы в разделе "переименованные файлы" INF.</span><span class="sxs-lookup"><span data-stu-id="65ebb-129">Queues the files in an INF Rename Files section.</span></span>                                                      |
| [<span data-ttu-id="65ebb-130">**сетупсканфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="65ebb-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | <span data-ttu-id="65ebb-131">Сканирует очередь файлов.</span><span class="sxs-lookup"><span data-stu-id="65ebb-131">Scans the file queue.</span></span>                                                                                 |
| [<span data-ttu-id="65ebb-132">**сетупсетплатформпасоверриде**</span><span class="sxs-lookup"><span data-stu-id="65ebb-132">**SetupSetPlatformPathOverride**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | <span data-ttu-id="65ebb-133">Задает переопределение пути платформы.</span><span class="sxs-lookup"><span data-stu-id="65ebb-133">Sets the platform path override.</span></span>                                                                      |



 

 

 



