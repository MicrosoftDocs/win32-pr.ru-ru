---
description: Microsoft Windows Search использует фильтры для извлечения содержимого элементов, включаемых в полнотекстовый индекс.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Рекомендации по использованию обработчиков фильтров в поиске Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544992e252d9ec0e3a7c402d1c348d3e3bfa9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540743"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a><span data-ttu-id="bd5d0-103">Рекомендации по созданию обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="bd5d0-103">Best Practices for Creating Filter Handlers in Windows Search</span></span>

<span data-ttu-id="bd5d0-104">Microsoft Windows Search использует фильтры для извлечения содержимого элементов, включаемых в полнотекстовый индекс.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="bd5d0-105">Можно расширить поиск Windows для индексации новых или собственных типов файлов, создав обработчики фильтров для извлечения содержимого и обработчиков свойств для извлечения свойств файлов.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-105">You can extend Windows Search to index new or proprietary file types by writing filter handlers to extract the content, and property handlers to extract the properties of files.</span></span> <span data-ttu-id="bd5d0-106">Фильтры связаны с типами файлов, как отмечены расширениями имен файлов, типами MIME или идентификаторами классов (CLSID).</span><span class="sxs-lookup"><span data-stu-id="bd5d0-106">Filters are associated with file types, as denoted by file name extensions, MIME types or class identifiers (CLSIDs).</span></span> <span data-ttu-id="bd5d0-107">Хотя один фильтр может работать с несколькими типами файлов, каждый тип работает только с одним фильтром.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-107">While one filter can handle multiple file types, each type works with only one filter.</span></span>

<span data-ttu-id="bd5d0-108">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="bd5d0-109">Машинный код</span><span class="sxs-lookup"><span data-stu-id="bd5d0-109">Native Code</span></span>](#native-code)
-   [<span data-ttu-id="bd5d0-110">Методики безопасного кодирования для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="bd5d0-110">Secure Code Practices for Windows Search</span></span>](#secure-code-practices-for-windows-search)
-   [<span data-ttu-id="bd5d0-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bd5d0-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="bd5d0-112">См. также</span><span class="sxs-lookup"><span data-stu-id="bd5d0-112">Related topics</span></span>](#related-topics)

## <a name="native-code"></a><span data-ttu-id="bd5d0-113">Машинный код</span><span class="sxs-lookup"><span data-stu-id="bd5d0-113">Native Code</span></span>

<span data-ttu-id="bd5d0-114">В Windows 7 и более поздних версиях фильтры, написанные в управляемом коде, явным образом блокируются.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-114">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="bd5d0-115">Фильтры должны быть написаны в машинном коде из-за потенциальных проблем с управлением версиями среды CLR в процессе выполнения нескольких надстроек.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-115">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

## <a name="secure-code-practices-for-windows-search"></a><span data-ttu-id="bd5d0-116">Методики безопасного кодирования для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="bd5d0-116">Secure Code Practices for Windows Search</span></span>

<span data-ttu-id="bd5d0-117">Ниже приведены рекомендации по написанию защищенных приложений для использования с поиском Windows.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-117">The following are practices for writing secure applications for use with Windows Search.</span></span>

<span data-ttu-id="bd5d0-118">**Для приложений запросов:**</span><span class="sxs-lookup"><span data-stu-id="bd5d0-118">**For query applications:**</span></span>

-   <span data-ttu-id="bd5d0-119">При написании клиентов поиска следует выбрать API, который выполняется в контексте безопасности, который позволяет пользователю иметь минимальные привилегии.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-119">When writing search clients, you should choose the API that runs in a security context that allows the user the least privilege.</span></span> <span data-ttu-id="bd5d0-120">Например, страницы ASP могут использовать объект запроса ИКСССО, который выполняется как пользовательский процесс.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-120">For example, ASP pages can use the IXSSO query object, which runs as a user process.</span></span>

<span data-ttu-id="bd5d0-121">**Для IFilter и языковых ресурсов:**</span><span class="sxs-lookup"><span data-stu-id="bd5d0-121">**For IFilters and Language Resources:**</span></span>

-   <span data-ttu-id="bd5d0-122">Если новый обработчик фильтра для типа файла устанавливается в качестве замены для существующей регистрации фильтра, установщик должен сохранить текущую регистрацию и восстановить ее при удалении нового обработчика фильтра.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-122">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="bd5d0-123">Механизм фильтрации цепочек отсутствует.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-123">There is no mechanism to chain filters.</span></span> <span data-ttu-id="bd5d0-124">Таким образом, новый обработчик фильтра отвечает за репликацию всех необходимых функций старого фильтра.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-124">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>
-   <span data-ttu-id="bd5d0-125">Фильтры IFilter, средство разбиения по словам и парадигматические модули для службы поиска Windows выполняются в локальном контексте безопасности.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-125">IFilters, word breakers, and stemmers for Windows Search run in the Local Security context.</span></span> <span data-ttu-id="bd5d0-126">Они должны быть написаны для корректного управления буферами и их правильного стека.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-126">They should be written to manage buffers and to stack correctly.</span></span> <span data-ttu-id="bd5d0-127">Все копии строк должны иметь явные проверки для защиты от переполнения буфера.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-127">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="bd5d0-128">Следует всегда проверять выделенный размер буфера и проверять размер данных в соответствии с размером буфера.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-128">You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.</span></span> <span data-ttu-id="bd5d0-129">Переполнение буфера — это распространенная методика использования кода, который не обеспечивает ограничения размера буфера.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-129">Buffer overruns are a common technique for exploiting code that does not enforce buffer size restrictions.</span></span>
-   <span data-ttu-id="bd5d0-130">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), средство разбиения по словам и компоненты парадигматические модули никогда не должны вызывать функцию [ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) или аналогичный API, который завершает процесс и все его потоки.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-130">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), word breaker and stemmer components should never call the [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function or similar API that terminates a process and all its threads.</span></span>
-   <span data-ttu-id="bd5d0-131">Не выделяйте и не освобождайте ресурсы в точке входа DllMain.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-131">Do not allocate or free resources in the DllMain entry point.</span></span> <span data-ttu-id="bd5d0-132">Это может привести к сбоям при нехватке нагрузочных тестов.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-132">This can lead to failures during low-resource stress tests.</span></span>
-   <span data-ttu-id="bd5d0-133">Код все объекты должны быть потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-133">Code all objects to be thread-safe.</span></span> <span data-ttu-id="bd5d0-134">Windows Search вызывает в одном потоке один экземпляр средств разбиения по словам или парадигматические модули, но может одновременно вызывать несколько экземпляров в нескольких потоках.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-134">Windows Search calls any one instance of a word breaker or stemmer in one thread at a time, but it may call multiple instances at the same time across multiple threads.</span></span>
-   <span data-ttu-id="bd5d0-135">Избегайте создания временных файлов или записи в реестр.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-135">Avoid creating temporary files or writing to the registry.</span></span>
-   <span data-ttu-id="bd5d0-136">При использовании компилятора Microsoft Visual C++ Убедитесь, что приложение компилируется с параметром **/GS** .</span><span class="sxs-lookup"><span data-stu-id="bd5d0-136">If you use the Microsoft Visual C++ compiler, ensure that you compile your application using the **/GS** option.</span></span> <span data-ttu-id="bd5d0-137">Параметр **/GS** используется для обнаружения переполнений буфера.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-137">The **/GS** option is used to detect buffer overruns.</span></span> <span data-ttu-id="bd5d0-138">Параметр/GS помещает проверки безопасности в скомпилированный код.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-138">The /GS option places security checks into the compiled code.</span></span> <span data-ttu-id="bd5d0-139">Дополнительные сведения см. в разделе [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (проверка безопасности буфера) раздела Visual C++ параметров компилятора в пакете SDK платформы.</span><span class="sxs-lookup"><span data-stu-id="bd5d0-139">For more information, see [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) /**GS** (Buffer Security Check) in the Visual C++ Compiler Options section of the Platform SDK.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd5d0-140">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bd5d0-140">Additional Resources</span></span>

-   <span data-ttu-id="bd5d0-141">В примере [ифилтерсампле](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) показано, как создать базовый класс IFilter для реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="bd5d0-141">The [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
-   <span data-ttu-id="bd5d0-142">Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bd5d0-142">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="bd5d0-143">Общие сведения о типах файлов см. в разделе [типы файлов](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="bd5d0-143">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
-   <span data-ttu-id="bd5d0-144">Сведения о запросе атрибутов сопоставления файлов для типа файлов см. в разделе [перцеиведтипес, системфилеассоЦиатионс и регистрация приложения](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bd5d0-144">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd5d0-145">См. также</span><span class="sxs-lookup"><span data-stu-id="bd5d0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd5d0-146">Разработка обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="bd5d0-146">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
</dt> <dt>

[<span data-ttu-id="bd5d0-147">О обработчиках фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="bd5d0-147">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
</dt> <dt>

[<span data-ttu-id="bd5d0-148">Возвращение свойств из обработчика фильтра</span><span class="sxs-lookup"><span data-stu-id="bd5d0-148">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
</dt> <dt>

[<span data-ttu-id="bd5d0-149">Обработчики фильтров, поставляемые с Windows</span><span class="sxs-lookup"><span data-stu-id="bd5d0-149">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
</dt> <dt>

[<span data-ttu-id="bd5d0-150">Реализация обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="bd5d0-150">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
</dt> <dt>

[<span data-ttu-id="bd5d0-151">Регистрация обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="bd5d0-151">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="bd5d0-152">Тестирование обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="bd5d0-152">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
