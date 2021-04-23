---
description: С помощью локального хранилища потоков (TLS) можно предоставить уникальные данные для каждого потока, к которому процесс может получить доступ с помощью глобального индекса. Один поток выделяет индекс, который может использоваться другими потоками для получения уникальных данных, связанных с индексом.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: локальное хранилище потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "104557665"
---
# <a name="thread-local-storage"></a><span data-ttu-id="be420-104">локальное хранилище потока</span><span class="sxs-lookup"><span data-stu-id="be420-104">Thread Local Storage</span></span>

<span data-ttu-id="be420-105">Все потоки процесса используют общий диапазон виртуальных адресов.</span><span class="sxs-lookup"><span data-stu-id="be420-105">All threads of a process share its virtual address space.</span></span> <span data-ttu-id="be420-106">Локальные переменные функции уникальны для каждого потока, который выполняет функцию.</span><span class="sxs-lookup"><span data-stu-id="be420-106">The local variables of a function are unique to each thread that runs the function.</span></span> <span data-ttu-id="be420-107">Однако статические и глобальные переменные совместно используются всеми потоками в процессе.</span><span class="sxs-lookup"><span data-stu-id="be420-107">However, the static and global variables are shared by all threads in the process.</span></span> <span data-ttu-id="be420-108">С помощью *локального хранилища потоков* (TLS) можно предоставить уникальные данные для каждого потока, к которому процесс может получить доступ с помощью глобального индекса.</span><span class="sxs-lookup"><span data-stu-id="be420-108">With *thread local storage* (TLS), you can provide unique data for each thread that the process can access using a global index.</span></span> <span data-ttu-id="be420-109">Один поток выделяет индекс, который может использоваться другими потоками для получения уникальных данных, связанных с индексом.</span><span class="sxs-lookup"><span data-stu-id="be420-109">One thread allocates the index, which can be used by the other threads to retrieve the unique data associated with the index.</span></span>

<span data-ttu-id="be420-110">\_Минимальная \_ величина постоянного TLS определяет минимальное количество ИНДЕКСов TLS, доступных в каждом процессе.</span><span class="sxs-lookup"><span data-stu-id="be420-110">The constant TLS\_MINIMUM\_AVAILABLE defines the minimum number of TLS indexes available in each process.</span></span> <span data-ttu-id="be420-111">Этот минимум гарантированно должен быть не менее 64 для всех систем.</span><span class="sxs-lookup"><span data-stu-id="be420-111">This minimum is guaranteed to be at least 64 for all systems.</span></span> <span data-ttu-id="be420-112">Максимальное количество индексов на процесс — 1 088.</span><span class="sxs-lookup"><span data-stu-id="be420-112">The maximum number of indexes per process is 1,088.</span></span>

<span data-ttu-id="be420-113">При создании потоков система выделяет массив значений **лпвоид** для TLS, которые ИНИЦИАЛИЗИРУЮТСЯ значением NULL.</span><span class="sxs-lookup"><span data-stu-id="be420-113">When the threads are created, the system allocates an array of **LPVOID** values for TLS, which are initialized to NULL.</span></span> <span data-ttu-id="be420-114">Прежде чем индекс можно будет использовать, он должен быть выделен одним из потоков.</span><span class="sxs-lookup"><span data-stu-id="be420-114">Before an index can be used, it must be allocated by one of the threads.</span></span> <span data-ttu-id="be420-115">Каждый поток хранит свои данные для индекса TLS в *слоте TLS* в массиве.</span><span class="sxs-lookup"><span data-stu-id="be420-115">Each thread stores its data for a TLS index in a *TLS slot* in the array.</span></span> <span data-ttu-id="be420-116">Если данные, связанные с индексом, будут помещаться в значение **лпвоид** , данные можно хранить непосредственно в слоте TLS.</span><span class="sxs-lookup"><span data-stu-id="be420-116">If the data associated with an index will fit in an **LPVOID** value, you can store the data directly in the TLS slot.</span></span> <span data-ttu-id="be420-117">Однако, если используется большое количество индексов таким образом, лучше выделить отдельное хранилище, консолидировать данные и свести к минимальному количеству используемых слотов TLS.</span><span class="sxs-lookup"><span data-stu-id="be420-117">However, if you are using a large number of indexes in this way, it is better to allocate separate storage, consolidate the data, and minimize the number of TLS slots in use.</span></span>

<span data-ttu-id="be420-118">На следующей схеме показано, как работает TLS.</span><span class="sxs-lookup"><span data-stu-id="be420-118">The following diagram illustrates how TLS works.</span></span> <span data-ttu-id="be420-119">Пример кода, иллюстрирующий использование локального хранилища потока, см. в разделе [использование локального хранилища потока](using-thread-local-storage.md).</span><span class="sxs-lookup"><span data-stu-id="be420-119">For a code example illustrating the use of thread local storage, see [Using Thread Local Storage](using-thread-local-storage.md).</span></span>

![Схема, на которой показано, как работает процесс T L S.](images/tls.png)

<span data-ttu-id="be420-121">Процесс имеет два потока: поток 1 и поток 2.</span><span class="sxs-lookup"><span data-stu-id="be420-121">The process has two threads, Thread 1 and Thread 2.</span></span> <span data-ttu-id="be420-122">Он выделяет два индекса для использования с TLS, gdwTlsIndex1 и gdwTlsIndex2.</span><span class="sxs-lookup"><span data-stu-id="be420-122">It allocates two indexes for use with TLS, gdwTlsIndex1 and gdwTlsIndex2.</span></span> <span data-ttu-id="be420-123">Каждый поток выделяет два блока памяти (по одному для каждого индекса), в которых хранятся данные, и сохраняет указатели на эти блоки памяти в соответствующих слотах TLS.</span><span class="sxs-lookup"><span data-stu-id="be420-123">Each thread allocates two memory blocks (one for each index) in which to store the data, and stores the pointers to these memory blocks in the corresponding TLS slots.</span></span> <span data-ttu-id="be420-124">Для доступа к данным, связанным с индексом, поток получает указатель на блок памяти из слота TLS и сохраняет его в локальной переменной Лпвдата.</span><span class="sxs-lookup"><span data-stu-id="be420-124">To access the data associated with an index, the thread retrieves the pointer to the memory block from the TLS slot and stores it in the lpvData local variable.</span></span>

<span data-ttu-id="be420-125">Лучше использовать TLS в библиотеке динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="be420-125">It is ideal to use TLS in a dynamic-link library (DLL).</span></span> <span data-ttu-id="be420-126">Пример см. в разделе [использование локального хранилища потоков в библиотеке динамической компоновки](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span><span class="sxs-lookup"><span data-stu-id="be420-126">For an example, see [Using Thread Local Storage in a Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="be420-127">См. также</span><span class="sxs-lookup"><span data-stu-id="be420-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be420-128">Локальное хранилище потока (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="be420-128">Thread Local Storage (Visual C++)</span></span>](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="be420-129">Использование локального хранилища потоков</span><span class="sxs-lookup"><span data-stu-id="be420-129">Using Thread Local Storage</span></span>](using-thread-local-storage.md)
</dt> <dt>

[<span data-ttu-id="be420-130">Использование локального хранилища потока в библиотеке динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="be420-130">Using Thread Local Storage in a Dynamic Link Library</span></span>](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
