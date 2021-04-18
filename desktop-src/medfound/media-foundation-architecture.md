---
description: В этом разделе описывается общий дизайн Microsoft Media Foundation. Сведения об использовании Media Foundation для конкретных задач программирования см. в разделе Media Foundation Guide по программированию.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Архитектура Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720043"
---
# <a name="media-foundation-architecture"></a><span data-ttu-id="1d71f-104">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d71f-104">Media Foundation Architecture</span></span>

<span data-ttu-id="1d71f-105">В этом разделе описывается общий дизайн Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1d71f-105">This section describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="1d71f-106">Сведения об использовании Media Foundation для конкретных задач программирования см. в разделе [Media Foundation Guide по программированию](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="1d71f-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1d71f-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="1d71f-107">In this section</span></span>



| <span data-ttu-id="1d71f-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="1d71f-108">Topic</span></span>                                                                                                         | <span data-ttu-id="1d71f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1d71f-109">Description</span></span>                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d71f-110">Общие сведения об архитектуре Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d71f-110">Overview of the Media Foundation Architecture</span></span>](overview-of-the-media-foundation-architecture.md)<br/> | <span data-ttu-id="1d71f-111">Предоставляет высокоуровневый обзор архитектуры Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1d71f-111">Gives a high-level overview of the Media Foundation architecture.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="1d71f-112">Примитивы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d71f-112">Media Foundation Primitives</span></span>](media-foundation-primitives.md)<br/>                                     | <span data-ttu-id="1d71f-113">Описание некоторых основных интерфейсов, используемых в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1d71f-113">Describes some basic interfaces that are used throughout Media Foundation.</span></span><br/> <span data-ttu-id="1d71f-114">Почти все Media Foundation приложения будут использовать эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1d71f-114">Almost all Media Foundation applications will use these interfaces.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="1d71f-115">Media Foundation API платформы</span><span class="sxs-lookup"><span data-stu-id="1d71f-115">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)<br/>                               | <span data-ttu-id="1d71f-116">Описание основных функций Media Foundation, таких как асинхронные обратные вызовы и рабочие очереди.</span><span class="sxs-lookup"><span data-stu-id="1d71f-116">Describes core Media Foundation functions, such as asynchronous callbacks and work queues.</span></span><br/> <span data-ttu-id="1d71f-117">Некоторые приложения могут использовать интерфейсы уровня платформы.</span><span class="sxs-lookup"><span data-stu-id="1d71f-117">Some applications might use platform-level interfaces.</span></span> <span data-ttu-id="1d71f-118">Кроме того, Пользовательские подключаемые модули, такие как источники мультимедиа и МФТС, используют эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1d71f-118">Also, custom plug-ins, such as media sources and MFTs, use these interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="1d71f-119">Конвейер Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d71f-119">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)<br/>                                         | <span data-ttu-id="1d71f-120">Media Foundationный уровень конвейера состоит из источников мультимедиа, МФТС и приемников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1d71f-120">The Media Foundation pipeline layer consists of media sources, MFTs, and media sinks.</span></span> <span data-ttu-id="1d71f-121">Большинство приложений не вызывают методы непосредственно на уровне конвейера.</span><span class="sxs-lookup"><span data-stu-id="1d71f-121">Most applications do not call methods directly on the pipeline layer.</span></span> <span data-ttu-id="1d71f-122">Вместо этого приложения используют один из более высоких уровней, например сеанс мультимедиа или модуль чтения исходного кода и модуль записи приемника.</span><span class="sxs-lookup"><span data-stu-id="1d71f-122">Instead, applications use one of the higher layers, such as the Media Session or the Source Reader and Sink Writer.</span></span><br/> |
| [<span data-ttu-id="1d71f-123">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1d71f-123">Media Session</span></span>](media-session.md)<br/>                                                                 | <span data-ttu-id="1d71f-124">Сеанс мультимедиа управляет потоком данных в конвейере Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1d71f-124">The Media Session manages data flow in the Media Foundation pipeline.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="1d71f-125">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="1d71f-125">Source Reader</span></span>](source-reader.md)<br/>                                                                 | <span data-ttu-id="1d71f-126">Модуль чтения исходного кода позволяет приложению получать данные из источника мультимедиа без необходимости непосредственно вызывать API источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1d71f-126">The Source Reader enables an application to get data from a media source, without the applicating needing to call the media source APIs directly.</span></span> <span data-ttu-id="1d71f-127">Модуль чтения исходного кода может также выполнять декодирование сжатых потоков.</span><span class="sxs-lookup"><span data-stu-id="1d71f-127">The Source Reader can also perform decoding of compressed streams.</span></span><br/>                                                            |
| [<span data-ttu-id="1d71f-128">Путь к защищенному носителю</span><span class="sxs-lookup"><span data-stu-id="1d71f-128">Protected Media Path</span></span>](protected-media-path.md)<br/>                                                   | <span data-ttu-id="1d71f-129">Защищенный путь к носителю (PMP) предоставляет защищенную среду для воспроизведения видеоматериалов уровня "Премиум".</span><span class="sxs-lookup"><span data-stu-id="1d71f-129">The protected media path (PMP) provides a protected environment for playing premium video content.</span></span> <span data-ttu-id="1d71f-130">Необязательно использовать PMP при написании приложения Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1d71f-130">It is not necessary to use the PMP when writing a Media Foundation application.</span></span> <br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="1d71f-131">См. также</span><span class="sxs-lookup"><span data-stu-id="1d71f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d71f-132">О Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d71f-132">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="1d71f-133">Media Foundation: основные понятия</span><span class="sxs-lookup"><span data-stu-id="1d71f-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="1d71f-134">Media Foundation и COM</span><span class="sxs-lookup"><span data-stu-id="1d71f-134">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="1d71f-135">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="1d71f-135">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




