---
description: 'Когда функция Сетупкоммитфилекуеуе фиксирует очередь файлов, она обрабатывает операции с файлами в следующем порядке: операции удаления файлов, операции переименования файлов и, наконец, операции копирования файлов.'
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Порядок обязательств по очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910335"
---
# <a name="order-of-queue-commitment"></a><span data-ttu-id="76882-103">Порядок обязательств по очереди</span><span class="sxs-lookup"><span data-stu-id="76882-103">Order of Queue Commitment</span></span>

<span data-ttu-id="76882-104">Когда функция [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) фиксирует очередь файлов, она обрабатывает операции с файлами в следующем порядке: операции удаления файлов, операции переименования файлов и, наконец, операции копирования файлов.</span><span class="sxs-lookup"><span data-stu-id="76882-104">When the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function commits the file queue, it processes the file operations in the following order: file deletion operations, then file renaming operations, and finally, file copying operations.</span></span> <span data-ttu-id="76882-105">В следующей структуре показан жизненный цикл процесса фиксации очереди.</span><span class="sxs-lookup"><span data-stu-id="76882-105">The following outline illustrates the life cycle of a queue's commitment process.</span></span>

 

-   <span data-ttu-id="76882-106">Запуск вложенной очереди удаления</span><span class="sxs-lookup"><span data-stu-id="76882-106">start the delete subqueue</span></span>
    -   <span data-ttu-id="76882-107">Запуск операции удаления файла <--REPEAT для каждого</span><span class="sxs-lookup"><span data-stu-id="76882-107">start a file delete operation <-- repeat for each</span></span>
    -   <span data-ttu-id="76882-108">завершение операции удаления файла <--удаление из очереди файла</span><span class="sxs-lookup"><span data-stu-id="76882-108">finish a file delete operation <-- queued file delete</span></span>
-   <span data-ttu-id="76882-109">завершение вложенной очереди удаления</span><span class="sxs-lookup"><span data-stu-id="76882-109">finish the delete subqueue</span></span>

<!-- -->

-   <span data-ttu-id="76882-110">запустить вложенную очередь переименования</span><span class="sxs-lookup"><span data-stu-id="76882-110">start the rename subqueue</span></span>
    -   <span data-ttu-id="76882-111">Запуск операции переименования файла <--REPEAT для каждого</span><span class="sxs-lookup"><span data-stu-id="76882-111">start a file rename operation <-- repeat for each</span></span>
    -   <span data-ttu-id="76882-112">завершение операции удаления файла <--переименование файла в очереди</span><span class="sxs-lookup"><span data-stu-id="76882-112">finish a file delete operation <-- queued file rename</span></span>
-   <span data-ttu-id="76882-113">завершить вложенную очередь переименования</span><span class="sxs-lookup"><span data-stu-id="76882-113">finish the rename subqueue</span></span>

<!-- -->

-   <span data-ttu-id="76882-114">Запуск субкуе копирования</span><span class="sxs-lookup"><span data-stu-id="76882-114">start the copy subque</span></span>
    -   <span data-ttu-id="76882-115">Запуск операции копирования файла <--REPEAT для каждого</span><span class="sxs-lookup"><span data-stu-id="76882-115">start a file copy operation <-- repeat for each</span></span>
    -   <span data-ttu-id="76882-116">завершение операции копирования файла <--копирование файлов в очереди</span><span class="sxs-lookup"><span data-stu-id="76882-116">finish a file copy operation <-- queued file copy</span></span>
    -   <span data-ttu-id="76882-117">завершение вложенной очереди копирования</span><span class="sxs-lookup"><span data-stu-id="76882-117">finish the copy subqueue</span></span>
-   <span data-ttu-id="76882-118">завершение очереди</span><span class="sxs-lookup"><span data-stu-id="76882-118">finish the queue</span></span>

 

<span data-ttu-id="76882-119">На каждом шаге или при возникновении ошибки функция [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) отправляет уведомление в подпрограммы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="76882-119">At each step, or if an error occurs, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function sends a notification to the callback routine.</span></span> <span data-ttu-id="76882-120">Подпрограмма обратного вызова может использовать информацию, отправленную очередью, для отслеживания хода установки и, при необходимости, взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="76882-120">The callback routine can use the information sent by the queue to track the installation progress and, if necessary, interact with the user.</span></span>

<span data-ttu-id="76882-121">Например, если операции копирования файлов требуется исходный файл, который был недоступен по текущему пути, [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) отправит уведомление о спфиленотифи \_ нидмедиа в подпрограммы обратного вызова, а также сведения о файлах и носителях.</span><span class="sxs-lookup"><span data-stu-id="76882-121">For example, if a file copy operation needed a source file that was not available at the current path, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) would send a SPFILENOTIFY\_NEEDMEDIA notification to the callback routine, along with information about the file and media required.</span></span> <span data-ttu-id="76882-122">Подпрограмма обратного вызова может использовать эти сведения для создания диалогового окна, предлагающего пользователю вставить следующий диск путем вызова [ **сетуппромптфордиск**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span><span class="sxs-lookup"><span data-stu-id="76882-122">The callback routine could use this information to generate a dialog box that prompts the user to insert the next disk by calling [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span></span>

<span data-ttu-id="76882-123">Подпрограмма обратного вызова очереди по умолчанию, [**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), включена в API установки.</span><span class="sxs-lookup"><span data-stu-id="76882-123">A default queue callback routine, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), is included with the Setup API.</span></span> <span data-ttu-id="76882-124">Эта подпрограммы обрабатывает уведомления очереди и создает для установки диалоговые окна ошибок и индикаторы выполнения.</span><span class="sxs-lookup"><span data-stu-id="76882-124">This routine handles queue notifications and generates error dialog boxes and progress bars for the installation.</span></span> <span data-ttu-id="76882-125">Вы можете использовать подпрограммы обратного вызова очереди по умолчанию, если она есть, или написать подпрограммы обратного вызова фильтра для выполнения подмножества уведомлений и передачи других параметров в подпрограммы обратного вызова очереди по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76882-125">You can use the default queue callback routine as it is, or write a filter callback routine to handle a subset of the notifications and pass the others on to the default queue callback routine.</span></span>

<span data-ttu-id="76882-126">Если ни одна из функций подпрограммы обратного вызова не подходит для ваших нужд, можно написать автономную подпрограммы обратного вызова, которая не вызывает подпрограммы обратного вызова очереди по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76882-126">If none of the functionality of the callback routine suits your needs, you can write a self-contained custom callback routine that does not call the default queue callback routine.</span></span>

<span data-ttu-id="76882-127">Дополнительные сведения о подфункциях обратного вызова очереди см. в разделе подпрограммы [обратного вызова очереди по умолчанию](default-queue-callback-routine.md)и [создании подпрограммы обратного вызова пользовательской очереди](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="76882-127">For more information about queue callback routines, see [Default Queue Callback Routine](default-queue-callback-routine.md), and [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



