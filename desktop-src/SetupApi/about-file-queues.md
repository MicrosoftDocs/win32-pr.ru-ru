---
description: Очередь файлов — это список файловых операций, обрабатываемых за один раз. Операции с файлами в очереди могут быть операциями копирования, переименования или удаления. Файловая очередь организует операции с файлами по типу, создавая копии, переименовывать и удалять подочереди.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: О файловых очередях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662340"
---
# <a name="about-file-queues"></a><span data-ttu-id="e8fde-105">О файловых очередях</span><span class="sxs-lookup"><span data-stu-id="e8fde-105">About File Queues</span></span>

<span data-ttu-id="e8fde-106">Очередь файлов — это список файловых операций, обрабатываемых за один раз.</span><span class="sxs-lookup"><span data-stu-id="e8fde-106">A file queue is a list of file operations that are processed at one time.</span></span> <span data-ttu-id="e8fde-107">Операции с файлами в очереди могут быть операциями копирования, переименования или удаления.</span><span class="sxs-lookup"><span data-stu-id="e8fde-107">The file operations in the queue may be copy, rename, or delete operations.</span></span> <span data-ttu-id="e8fde-108">Файловая очередь организует операции с файлами по типу, создавая копии, переименовывать и удалять подочереди.</span><span class="sxs-lookup"><span data-stu-id="e8fde-108">The file queue organizes file operations by type, creating copy, rename, and delete subqueues.</span></span>

<span data-ttu-id="e8fde-109">Эти операции могут быть отправлены в очередь в любом порядке, а процесс постановку не должен быть непрерывным.</span><span class="sxs-lookup"><span data-stu-id="e8fde-109">These operations may be sent to the queue in any order, and the enqueuing process need not be contiguous.</span></span> <span data-ttu-id="e8fde-110">При фиксации очереди функция [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) выполняет файловые операции в порядке, определенном типом операции.</span><span class="sxs-lookup"><span data-stu-id="e8fde-110">When the queue is committed, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function performs file operations in order of the operation type.</span></span>

<span data-ttu-id="e8fde-111">Как правило, все операции с файлами, необходимые для всей установки, помещаются в очередь файлов, а затем обрабатываются в одном пакете при фиксации очереди.</span><span class="sxs-lookup"><span data-stu-id="e8fde-111">Typically, all of the file operations necessary for an entire installation are queued to the file queue, and then processed in a single batch when the queue is committed.</span></span>

<span data-ttu-id="e8fde-112">Одним из преимуществ операций с файлами в очереди, посвященных установке файлов в разделе из INF-файла, является возможность упростить процесс установки.</span><span class="sxs-lookup"><span data-stu-id="e8fde-112">One advantage of queuing file operations over installing files section-by-section from an INF file is that you can streamline the installation process.</span></span> <span data-ttu-id="e8fde-113">Вместо того чтобы получать сведения от пользователя для каждого устанавливаемого раздела, можно получить сведения об установке от пользователя для всех файлов, которые будут установлены во время создания очереди.</span><span class="sxs-lookup"><span data-stu-id="e8fde-113">Instead of having to obtain information from the user for each section to be installed, you can obtain installation information from the user for all the files to be installed while building the queue.</span></span> <span data-ttu-id="e8fde-114">Это освобождает пользователя от выполнения других действий, в то время как операции копирования, требующие много времени, обрабатываются функцией [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) .</span><span class="sxs-lookup"><span data-stu-id="e8fde-114">This frees the user to pursue other activities while the time-intensive copy operations are processed by the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function.</span></span>

<span data-ttu-id="e8fde-115">Другое преимущество файловых очередей заключается в том, что можно отслеживать ход выполнения установки в целом.</span><span class="sxs-lookup"><span data-stu-id="e8fde-115">Another advantage of file queues is that you can track the progress of the installation as a whole.</span></span> <span data-ttu-id="e8fde-116">При установке раздела по разделам из INF-файла индикаторы выполнения, такие как индикатор выполнения, могут отслеживать только текущий раздел INF.</span><span class="sxs-lookup"><span data-stu-id="e8fde-116">When installing section-by-section from an INF file, progress indicators such as progress bars can track only the current INF section.</span></span> <span data-ttu-id="e8fde-117">При установке следующего раздела индикатор выполнения начинается заново.</span><span class="sxs-lookup"><span data-stu-id="e8fde-117">When the next section is installed, the progress bar starts over.</span></span> <span data-ttu-id="e8fde-118">При использовании очереди общее число файлов, которые будут обрабатываться во время всей установки, известно до фиксации очереди, и поэтому можно создать индикатор выполнения для отслеживания всей установки.</span><span class="sxs-lookup"><span data-stu-id="e8fde-118">With a queue, the total number of files to be processed during the entire installation is known before the queue is committed, and thus, a progress bar can be generated to track the entire installation.</span></span>

<span data-ttu-id="e8fde-119">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="e8fde-119">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e8fde-120">Порядок обязательств по очереди</span><span class="sxs-lookup"><span data-stu-id="e8fde-120">Order of Queue Commitment</span></span>](order-of-queue-commitment.md)
-   [<span data-ttu-id="e8fde-121">Уведомления в очереди</span><span class="sxs-lookup"><span data-stu-id="e8fde-121">Queue Notifications</span></span>](queue-notifications.md)

 

 



