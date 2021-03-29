---
description: После того как все требуемые операции с файлами были поставлены в очередь, очередь должна быть зафиксирована. Это приводит к обработке операций с файлами в очереди.
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: Фиксация очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818080"
---
# <a name="committing-a-queue"></a><span data-ttu-id="477b0-104">Фиксация очереди</span><span class="sxs-lookup"><span data-stu-id="477b0-104">Committing a Queue</span></span>

<span data-ttu-id="477b0-105">После того как все требуемые операции с файлами были поставлены в очередь, очередь должна быть зафиксирована.</span><span class="sxs-lookup"><span data-stu-id="477b0-105">After all the desired file operations have been queued, the queue must be committed.</span></span> <span data-ttu-id="477b0-106">Это приводит к обработке операций с файлами в очереди.</span><span class="sxs-lookup"><span data-stu-id="477b0-106">This causes the enqueued file operations to be processed.</span></span>

<span data-ttu-id="477b0-107">Невозможно повторно использовать очередь файлов после ее фиксации.</span><span class="sxs-lookup"><span data-stu-id="477b0-107">A file queue cannot be reused after it has been committed.</span></span> <span data-ttu-id="477b0-108">Рекомендуется составить все необходимые файловые операции для очереди файлов и зафиксировать очередь только один раз.</span><span class="sxs-lookup"><span data-stu-id="477b0-108">The best practice is to collect all the required file operations for the file queue and commit the queue only once.</span></span> <span data-ttu-id="477b0-109">Если требуется дополнительная обработка очереди после ее фиксации, необходимо закрыть обработчик очереди и создать новую файловую очередь.</span><span class="sxs-lookup"><span data-stu-id="477b0-109">If additional processing of the queue is required after it has been committed, the handle to the queue should be closed and a new file queue created.</span></span> <span data-ttu-id="477b0-110">Чтобы зафиксировать очередь файлов, вызовите функцию [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , указав подпрограммы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="477b0-110">To commit the file queue, call the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function, specifying a callback routine.</span></span> <span data-ttu-id="477b0-111">Подпрограммы обратного вызова будут получать уведомления от **сетупкоммитфилекуеуе** при обработке файловых операций.</span><span class="sxs-lookup"><span data-stu-id="477b0-111">The callback routine will receive notifications from **SetupCommitFileQueue** as the file operations are processed.</span></span> <span data-ttu-id="477b0-112">Если вы хотите использовать подпрограммы обратного вызова очереди по умолчанию, необходимо сначала инициализировать необходимый контекст, вызвав либо [**сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) , либо [**сетупинитдефаулткуеуекаллбаккекс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="477b0-112">If you want to use the default queue callback routine, you must first initialize the necessary context by calling either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span> <span data-ttu-id="477b0-113">Дополнительные сведения о подпрограммы обратного вызова очереди по умолчанию см. в разделе [подпрограммы обратного вызова очереди по умолчанию](default-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="477b0-113">For more information about the default queue callback routine, see [Default Queue Callback Routine](default-queue-callback-routine.md).</span></span>

> [!Note]  
> <span data-ttu-id="477b0-114">[**Сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) следует вызывать до закрытия очереди.</span><span class="sxs-lookup"><span data-stu-id="477b0-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) should be called before the queue is closed.</span></span> <span data-ttu-id="477b0-115">Любые операции, которые не зафиксированы при вызове [**сетупклосефилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) , выполняться не будут.</span><span class="sxs-lookup"><span data-stu-id="477b0-115">Any operations that are uncommitted when [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) is called will not be performed.</span></span>

 

 

 



