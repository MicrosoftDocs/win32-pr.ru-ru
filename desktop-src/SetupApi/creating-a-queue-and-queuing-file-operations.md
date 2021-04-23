---
description: Очередь файловых операций полезна, так как позволяет обрабатывать установку в целом, а не в разделе INF.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Создание операций с очередью и файлами в очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663564"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a><span data-ttu-id="bc6e0-103">Создание операций с очередью и файлами в очереди</span><span class="sxs-lookup"><span data-stu-id="bc6e0-103">Creating a Queue and Queuing File Operations</span></span>

<span data-ttu-id="bc6e0-104">Очередь файловых операций полезна, так как позволяет обрабатывать установку в целом, а не в разделе INF.</span><span class="sxs-lookup"><span data-stu-id="bc6e0-104">Queuing the file operations is useful because it enables you to process the installation as a whole, instead of by INF section.</span></span>

<span data-ttu-id="bc6e0-105">Чтобы создать очередь файлов, объявите переменную для хранения маркера очереди, а затем вызовите функцию [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) .</span><span class="sxs-lookup"><span data-stu-id="bc6e0-105">To create a file queue, declare a variable to store the queue handle, then call the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function.</span></span> <span data-ttu-id="bc6e0-106">После создания очереди можно ставить в очередь операции копирования, переименования и удаления, а также сканировать очередь файлов для проверки операций, поставленных в очередь.</span><span class="sxs-lookup"><span data-stu-id="bc6e0-106">After the queue is created, you can queue copy, rename, and delete operations, as well as scan the file queue to verify enqueued operations.</span></span>

<span data-ttu-id="bc6e0-107">Чтобы добавить операции с отдельными файлами в очередь, используйте функции [**сетупкуеуекопи**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**сетупкуеуеренаме**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)и [**сетупкуеуеделете**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) .</span><span class="sxs-lookup"><span data-stu-id="bc6e0-107">To add single file operations to the queue, use the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea), and [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) functions.</span></span>

<span data-ttu-id="bc6e0-108">Все операции с файлами, перечисленные в разделе **копирование файлов**, **Удаление файлов** или **Переименование файлов** , можно добавить в очередь с помощью [**сетупкуеуекописектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**сетупкуеуеделетесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)или [**сетупкуеуеренамесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)соответственно.</span><span class="sxs-lookup"><span data-stu-id="bc6e0-108">All the file operations listed in a **Copy Files**, **Delete Files**, or **Rename Files** section can be added to the queue by using [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona), or [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectively.</span></span>

<span data-ttu-id="bc6e0-109">Другой способ поставить в очередь все файлы в разделах " **копирование файлов** ", перечисленных в разделе " **Установка** " INF-файла, — использовать функцию [**сетупинсталлфилесфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span><span class="sxs-lookup"><span data-stu-id="bc6e0-109">Another way to queue all the files in the **Copy Files** sections listed in an **Install** section of an INF is to use the function, [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span></span>

<span data-ttu-id="bc6e0-110">В следующем примере функция [**сетупкуеуекописектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) используется для постановки в очередь операций копирования для всех файлов, перечисленных в разделе " **копирование файлов** " INF-файла.</span><span class="sxs-lookup"><span data-stu-id="bc6e0-110">The following example uses the [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) function to enqueue copy operations for all the files listed in a **Copy Files** section of an INF file.</span></span>

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

<span data-ttu-id="bc6e0-111">В этом примере MyQueue — это очередь, в которую добавляются операции копирования, "A: \\ " указывает путь к источнику, а минф — маркер открытого INF-файла.</span><span class="sxs-lookup"><span data-stu-id="bc6e0-111">In the example, MyQueue is the queue to add copy operations to, "A:\\" specifies the path to the source, and MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="bc6e0-112">Параметр *листинфхандле* имеет значение **null**, указывающее, что раздел для копирования находится в минф.</span><span class="sxs-lookup"><span data-stu-id="bc6e0-112">The parameter *ListInfHandle* is set to **NULL**, indicating that the section for copying is in MyInf.</span></span> <span data-ttu-id="bc6e0-113">Мисектион — это раздел в Минф, содержащий файлы, которые нужно поместить в очередь для копирования.</span><span class="sxs-lookup"><span data-stu-id="bc6e0-113">MySection is the section in MyInf containing the files to queue for copying.</span></span>

<span data-ttu-id="bc6e0-114">Флаги SP \_ Copy \_ unskip и SP \_ Copy \_ OnBrowse были объединены с помощью оператора или, чтобы указать, что пользователю не следует предлагать варианты пропуска или поиска файлов при возникновении ошибок.</span><span class="sxs-lookup"><span data-stu-id="bc6e0-114">The flags SP\_COPY\_NOSKIP and SP\_COPY\_NOBROWSE have been combined using an OR operator to indicate that the user should not be offered options to skip or browse for files if errors occur.</span></span>

 

 



