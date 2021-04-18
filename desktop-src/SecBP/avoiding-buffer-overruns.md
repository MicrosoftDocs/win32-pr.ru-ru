---
description: Краткое введение в несколько типов ситуаций переполнения буфера и предлагает некоторые идеи и ресурсы, которые помогут избежать создания новых рисков и устранения проблем с существующими.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Предотвращение переполнения буфера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663951"
---
# <a name="avoiding-buffer-overruns"></a><span data-ttu-id="bf63e-103">Предотвращение переполнения буфера</span><span class="sxs-lookup"><span data-stu-id="bf63e-103">Avoiding Buffer Overruns</span></span>

<span data-ttu-id="bf63e-104">Переполнение буфера — один из наиболее распространенных источников угрозы безопасности.</span><span class="sxs-lookup"><span data-stu-id="bf63e-104">A buffer overrun is one of the most common sources of security risk.</span></span> <span data-ttu-id="bf63e-105">Переполнение буфера по сути вызывается путем обработки непроверенных внешних входных данных в качестве надежных.</span><span class="sxs-lookup"><span data-stu-id="bf63e-105">A buffer overrun is essentially caused by treating unchecked, external input as trustworthy data.</span></span> <span data-ttu-id="bf63e-106">Процесс копирования этих данных с помощью таких операций, как [**копимемори**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** или **wcscpy**, может создавать непредвиденные результаты, что позволяет повредить систему.</span><span class="sxs-lookup"><span data-stu-id="bf63e-106">The act of copying this data, using operations such as [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy**, or **wcscpy**, can create unanticipated results, which allows for system corruption.</span></span> <span data-ttu-id="bf63e-107">В лучших случаях приложение будет прерываться с помощью основного дампа, сбоя сегментации или нарушения прав доступа.</span><span class="sxs-lookup"><span data-stu-id="bf63e-107">In the best of cases, your application will abort with a core dump, segmentation fault, or access violation.</span></span> <span data-ttu-id="bf63e-108">В худшем случае злоумышленник может воспользоваться переполнением буфера, поставляя и выполняя другой вредоносный код в процессе.</span><span class="sxs-lookup"><span data-stu-id="bf63e-108">In the worst of cases, an attacker can exploit the buffer overrun by introducing and executing other malicious code in your process.</span></span> <span data-ttu-id="bf63e-109">Копирование непроверенных входных данных в буфер на основе стека является наиболее распространенной причиной уязвимых ошибок.</span><span class="sxs-lookup"><span data-stu-id="bf63e-109">Copying unchecked, input data into a stack-based buffer is the most common cause of exploitable faults.</span></span>

<span data-ttu-id="bf63e-110">Переполнение буфера может происходить различными способами.</span><span class="sxs-lookup"><span data-stu-id="bf63e-110">Buffer overruns can occur in a variety of ways.</span></span> <span data-ttu-id="bf63e-111">Ниже приведен краткий обзор нескольких типов ситуаций переполнения буфера, а также некоторые идеи и ресурсы, помогающие избежать создания новых рисков и устранения проблем с существующими элементами.</span><span class="sxs-lookup"><span data-stu-id="bf63e-111">The following list provides a brief introduction to a few types of buffer overrun situations and offers some ideas and resources to help you avoid creating new risks and mitigate existing ones:</span></span>

<dl> <dt>

<span data-ttu-id="bf63e-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Переполнение статических буферов</span><span class="sxs-lookup"><span data-stu-id="bf63e-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Static buffer overruns</span></span>
</dt> <dd>

<span data-ttu-id="bf63e-113">Статическое переполнение буфера возникает, когда буфер, который был объявлен в стеке, записывается в с большим объемом данных, чем он был выделен для хранения.</span><span class="sxs-lookup"><span data-stu-id="bf63e-113">A static buffer overrun occurs when a buffer, which has been declared on the stack, is written to with more data than it was allocated to hold.</span></span> <span data-ttu-id="bf63e-114">Менее очевидные версии этой ошибки возникают, когда непроверенные входные данные пользователя копируются непосредственно в статическую переменную, что приводит к потенциальному повреждению стека.</span><span class="sxs-lookup"><span data-stu-id="bf63e-114">The less apparent versions of this error occur when unverified user input data is copied directly to a static variable, causing potential stack corruption.</span></span>

</dd> <dt>

<span data-ttu-id="bf63e-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Переполнение кучи</span><span class="sxs-lookup"><span data-stu-id="bf63e-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Heap overruns</span></span>
</dt> <dd>

<span data-ttu-id="bf63e-116">Переполнение кучи, как и переполнение статических буферов, может привести к повреждению памяти и стека.</span><span class="sxs-lookup"><span data-stu-id="bf63e-116">Heap overruns, like static buffer overruns, can lead to memory and stack corruption.</span></span> <span data-ttu-id="bf63e-117">Так как переполнение кучи происходит в памяти кучи, а не в стеке, некоторые пользователи считают, что они менее способны вызвать серьезные проблемы. Тем не менее, для переполнения кучи требуется реальное программирование, а также возможность разрешения системных рисков в случае переполнения статических буферов.</span><span class="sxs-lookup"><span data-stu-id="bf63e-117">Because heap overruns occur in heap memory rather than on the stack, some people consider them to be less able to cause serious problems; nevertheless, heap overruns require real programming care and are just as able to allow system risks as static buffer overruns.</span></span>

</dd> <dt>

<span data-ttu-id="bf63e-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Ошибки индексации массива</span><span class="sxs-lookup"><span data-stu-id="bf63e-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Array indexing errors</span></span>
</dt> <dd>

<span data-ttu-id="bf63e-119">Ошибки индексирования массива также представляют собой источник переполнения памяти.</span><span class="sxs-lookup"><span data-stu-id="bf63e-119">Array indexing errors also are a source of memory overruns.</span></span> <span data-ttu-id="bf63e-120">Тщательная проверка границ и управление индексами помогут предотвратить такой тип переполнения памяти.</span><span class="sxs-lookup"><span data-stu-id="bf63e-120">Careful bounds checking and index management will help prevent this type of memory overrun.</span></span>

</dd> </dl>

<span data-ttu-id="bf63e-121">Предотвращение переполнения буфера в основном заключается в написании хорошего кода.</span><span class="sxs-lookup"><span data-stu-id="bf63e-121">Preventing buffer overruns is primarily about writing good code.</span></span> <span data-ttu-id="bf63e-122">Всегда проверяйте все входные данные и при необходимости корректно завершаются.</span><span class="sxs-lookup"><span data-stu-id="bf63e-122">Always validate all your inputs and fail gracefully when necessary.</span></span> <span data-ttu-id="bf63e-123">Дополнительные сведения о создании безопасного кода см. в следующих ресурсах:</span><span class="sxs-lookup"><span data-stu-id="bf63e-123">For more information about writing secure code, see the following resources:</span></span>

-   <span data-ttu-id="bf63e-124">Магуире, Стив \[ 1993 \] , *написание твердого кода*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Вашингтон.</span><span class="sxs-lookup"><span data-stu-id="bf63e-124">Maguire, Steve \[1993\], *Writing Solid Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span></span>
-   <span data-ttu-id="bf63e-125">Говард, Майкл и Леблана, Дэвид \[ 2003 \] , *написание безопасного кода*, 2d ED, ISBN 0-7356-1722-8, Microsoft Press, Redmond, Вашингтон.</span><span class="sxs-lookup"><span data-stu-id="bf63e-125">Howard, Michael and LeBlanc, David \[2003\], *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span></span>

> [!Note]  
> <span data-ttu-id="bf63e-126">Эти ресурсы могут быть недоступны в некоторых языках и странах.</span><span class="sxs-lookup"><span data-stu-id="bf63e-126">These resources may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="bf63e-127">Безопасная обработка строк — это долгосрочная проблема, которая, по-своему, должна быть решена как в следующих эффективных методиках программирования, так и часто с помощью и модернизация существующих систем с защищенными функциями обработки строк.</span><span class="sxs-lookup"><span data-stu-id="bf63e-127">Safe string handling is a long-standing issue that continues to be addressed both by following good programming practices and often by using and retrofitting existing systems with secure, string-handling functions.</span></span> <span data-ttu-id="bf63e-128">Пример такого набора функций для оболочки Windows начинается с [**стрингкбкат**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span><span class="sxs-lookup"><span data-stu-id="bf63e-128">An example of such a set of functions for the Windows shell starts with [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span></span>

 

 
