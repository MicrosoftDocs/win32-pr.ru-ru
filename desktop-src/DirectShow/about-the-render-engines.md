---
description: Сведения о механизмах подготовки отчетов
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Сведения о механизмах подготовки отчетов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537829"
---
# <a name="about-the-render-engines"></a><span data-ttu-id="94c0c-103">Сведения о механизмах подготовки отчетов</span><span class="sxs-lookup"><span data-stu-id="94c0c-103">About the Render Engines</span></span>

<span data-ttu-id="94c0c-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="94c0c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="94c0c-105">В этой статье описывается визуализация проекта редактирования видео с помощью [служб редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="94c0c-105">This article describes how [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project.</span></span>

<span data-ttu-id="94c0c-106">В DES проект представлен в виде временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="94c0c-106">In DES, a project is represented as a timeline.</span></span> <span data-ttu-id="94c0c-107">Временная шкала полезна, так как она упрощает наиболее распространенные задачи редактирования видео, такие как изменение расположения исходных клипов и Добавление видеоэффектов.</span><span class="sxs-lookup"><span data-stu-id="94c0c-107">The timeline is useful because it simplifies the most common tasks in video editing, such as rearranging source clips and adding video effects.</span></span> <span data-ttu-id="94c0c-108">Для архитектуры потока DirectShow, с другой стороны, требуется граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="94c0c-108">The DirectShow stream architecture, on the other hand, requires a filter graph.</span></span> <span data-ttu-id="94c0c-109">Таким же для подготовки проекта к просмотру необходимо преобразовать временную шкалу в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="94c0c-109">Thus, to render your project, you must translate a timeline into a filter graph.</span></span> <span data-ttu-id="94c0c-110">Компонент, выполняющий это, называется *подсистемой визуализации*.</span><span class="sxs-lookup"><span data-stu-id="94c0c-110">The component that does this is called a *render engine*.</span></span> <span data-ttu-id="94c0c-111">DirectShow предоставляет два обработчика визуализации:</span><span class="sxs-lookup"><span data-stu-id="94c0c-111">DirectShow provides two render engines:</span></span>

-   <span data-ttu-id="94c0c-112">Базовая подсистема визуализации: создает граф фильтра, который доставляет несжатые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="94c0c-112">Basic render engine: Builds a filter graph that delivers uncompressed output.</span></span>
-   <span data-ttu-id="94c0c-113">Интеллектуальный модуль визуализации: создает граф фильтра, который доставляет сжатые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="94c0c-113">Smart render engine: Builds a filter graph that delivers compressed output.</span></span>

<span data-ttu-id="94c0c-114">Интеллектуальный механизм визуализации использует интеллектуальное повторное сжатие для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="94c0c-114">The smart render engine uses smart recompression to improve performance.</span></span> <span data-ttu-id="94c0c-115">При смарт-сжатии исходные файлы пересжимаются только в том случае, если исходный формат файла отличается от конечного формата.</span><span class="sxs-lookup"><span data-stu-id="94c0c-115">With smart recompression, source files are recompressed only when the original file format differs from the final output format.</span></span> <span data-ttu-id="94c0c-116">Если форматы совпадают, источник никогда не распаковывается.</span><span class="sxs-lookup"><span data-stu-id="94c0c-116">If the formats match, the source is never decompressed.</span></span> <span data-ttu-id="94c0c-117">Интеллектуальное сжатие поддерживается только для сжатия видео, а не для сжатия звука.</span><span class="sxs-lookup"><span data-stu-id="94c0c-117">Smart recompression is supported only for video compression, not for audio compression.</span></span>

<span data-ttu-id="94c0c-118">Для предварительной версии используйте базовый механизм визуализации.</span><span class="sxs-lookup"><span data-stu-id="94c0c-118">For preview, use the basic render engine.</span></span> <span data-ttu-id="94c0c-119">Модуль интеллектуального просмотра также может быть предварительно доступен для предварительного просмотра, но менее эффективно, поскольку он должен распаковать сжатый поток.</span><span class="sxs-lookup"><span data-stu-id="94c0c-119">The smart render engine can also preview, but less efficiently because it has to decompress the compressed stream.</span></span> <span data-ttu-id="94c0c-120">Для записи файлов используйте интеллектуальный модуль визуализации, если требуется выполнить интеллектуальное сжатие.</span><span class="sxs-lookup"><span data-stu-id="94c0c-120">For writing files, use the smart render engine if you want smart recompression.</span></span> <span data-ttu-id="94c0c-121">В противном случае используйте базовый механизм визуализации.</span><span class="sxs-lookup"><span data-stu-id="94c0c-121">Otherwise, use the basic render engine.</span></span> <span data-ttu-id="94c0c-122">Интеллектуальное повторное сжатие может значительно сократить время, затрачиваемое на запись файла.</span><span class="sxs-lookup"><span data-stu-id="94c0c-122">Smart recompression can greatly reduce the time it takes to write the file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94c0c-123">Не используйте интеллектуальный модуль визуализации для чтения или записи файлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="94c0c-123">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="94c0c-124">Оба модуля подготовки отчетов создают невидимое окно, обрабатывающее сообщения.</span><span class="sxs-lookup"><span data-stu-id="94c0c-124">Both render engines create an invisible window that processes messages.</span></span> <span data-ttu-id="94c0c-125">Поток, создающий подсистему отрисовки, должен иметь цикл обработки сообщений для отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="94c0c-125">The thread that creates the render engine must have a message loop, to dispatch messages.</span></span> <span data-ttu-id="94c0c-126">Кроме того, этот поток не должен выходить из системы до тех пор, пока не будет освобожден механизм визуализации и диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="94c0c-126">Also, that thread must not exit until the Render Engine and the Filter Graph Manager are released.</span></span> <span data-ttu-id="94c0c-127">В противном случае приложение может привести к взаимоблокировке.</span><span class="sxs-lookup"><span data-stu-id="94c0c-127">Otherwise, the application might deadlock.</span></span>

 

<span data-ttu-id="94c0c-128">Создание графа фильтра</span><span class="sxs-lookup"><span data-stu-id="94c0c-128">Constructing the Filter Graph</span></span>

<span data-ttu-id="94c0c-129">Граф фильтра строится в два этапа.</span><span class="sxs-lookup"><span data-stu-id="94c0c-129">The filter graph is built in two stages.</span></span> <span data-ttu-id="94c0c-130">На первом этапе механизм визуализации создает «внешний интерфейс», который является графом частичного фильтра.</span><span class="sxs-lookup"><span data-stu-id="94c0c-130">In the first stage, the render engine constructs a "front end," which is a partial filter graph.</span></span> <span data-ttu-id="94c0c-131">На следующей схеме показан типичный внешний интерфейс:</span><span class="sxs-lookup"><span data-stu-id="94c0c-131">The following diagram illustrates a typical front end:</span></span>

![внешний интерфейс фильтра графа](images/rendeng1.png)

<span data-ttu-id="94c0c-133">Подсистемы содержат различные специализированные фильтры, которые механизм визуализации собирает автоматически.</span><span class="sxs-lookup"><span data-stu-id="94c0c-133">The subsystems contain various specialized filters, which the render engine assembles automatically.</span></span> <span data-ttu-id="94c0c-134">Внешний интерфейс содержит один выходной ПИН-код для каждой группы на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="94c0c-134">The front end contains one output pin for each group in the timeline.</span></span> <span data-ttu-id="94c0c-135">Выходные данные доставляют несжатых данных, если используется базовый механизм рендеринга, или сжатые данные, если используется модуль интеллектуального просмотра.</span><span class="sxs-lookup"><span data-stu-id="94c0c-135">The output pins deliver uncompressed data if you use the basic render engine, or compressed data if you use the smart render engine.</span></span>

<span data-ttu-id="94c0c-136">На втором шаге выходные контакты подключены к фильтрам подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="94c0c-136">In the second step, the output pins are connected to rendering filters.</span></span> <span data-ttu-id="94c0c-137">Для предварительной версии фильтры подготовки отчетов — это видеоролики видео и аудио.</span><span class="sxs-lookup"><span data-stu-id="94c0c-137">For preview, the rendering filters are video and audio renderers.</span></span> <span data-ttu-id="94c0c-138">Для записи файлов фильтры отрисовки — это фильтры мультиплексора (мультиплексор) и фильтры записи файлов.</span><span class="sxs-lookup"><span data-stu-id="94c0c-138">For file writing, the rendering filters are multiplexer (mux) filters and file-writer filters.</span></span>

![завершение графа фильтра](images/rendeng2.png)

## <a name="related-topics"></a><span data-ttu-id="94c0c-140">См. также</span><span class="sxs-lookup"><span data-stu-id="94c0c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94c0c-141">Предварительный просмотр проекта</span><span class="sxs-lookup"><span data-stu-id="94c0c-141">Previewing a Project</span></span>](previewing-a-project.md)
</dt> <dt>

[<span data-ttu-id="94c0c-142">Запись проекта в файл</span><span class="sxs-lookup"><span data-stu-id="94c0c-142">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



