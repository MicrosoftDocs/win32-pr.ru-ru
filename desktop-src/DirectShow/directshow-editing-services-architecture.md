---
description: Архитектура служб редактирования DirectShow
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Архитектура служб редактирования DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105650424"
---
# <a name="directshow-editing-services-architecture"></a><span data-ttu-id="b3ad1-103">Архитектура служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3ad1-103">DirectShow Editing Services Architecture</span></span>

<span data-ttu-id="b3ad1-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="b3ad1-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b3ad1-105">На следующем рисунке показана архитектура [служб редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="b3ad1-105">The following illustration shows the architecture of [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

![Архитектура служб редактирования DirectShow](images/architecture.png)

-   <span data-ttu-id="b3ad1-107">Временная шкала — это рабочее видео в виде коллекции исходных клипов, переходов и эффектов, организованных в набор вложенных дорожек.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-107">Timeline: Represents a video production as a collection of source clips, transitions, and effects, organized into a set of nested tracks.</span></span> <span data-ttu-id="b3ad1-108">Дополнительные сведения см. [в разделе Модель временной шкалы](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="b3ad1-108">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>
-   <span data-ttu-id="b3ad1-109">Средство синтаксического анализа XML: анализирует временную шкалу и создает выходной файл или считывает входной файл и создает временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-109">XML Parser: Parses the timeline and generates an output file, or reads an input file and generates a timeline.</span></span> <span data-ttu-id="b3ad1-110">DES поддерживает формат сохраняемости на основе XML.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-110">DES supports an XML-based persistence format.</span></span>
-   <span data-ttu-id="b3ad1-111">Модуль визуализации: преобразует временную шкалу в форму, которая может быть подготовлена к просмотру в виде потокового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-111">Render engine: Translates the timeline into a form that can be rendered as streaming media.</span></span> <span data-ttu-id="b3ad1-112">По умолчанию модуль подготовки отчетов создает граф фильтра DirectShow (см. следующий раздел).</span><span class="sxs-lookup"><span data-stu-id="b3ad1-112">By default, the render engine produces a DirectShow filter graph (see next section).</span></span>
-   <span data-ttu-id="b3ad1-113">Указатель мультимедиа. поддерживает кэш расположений элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-113">Media locator: Maintains a cache of locations of media elements.</span></span> <span data-ttu-id="b3ad1-114">При неудачной попытке открыть элемент мультимедиа DES использует кэш для обнаружения элемента на основе журнала успешных открытий.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-114">When an attempt to open a media element fails, DES uses the cache to locate the element, based on a history of successful opens.</span></span>

<span data-ttu-id="b3ad1-115">Временная шкала является абстрактным описанием проекта редактирования видео.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-115">The timeline is an abstract description of a video editing project.</span></span> <span data-ttu-id="b3ad1-116">Он задает исходные клипы, используемые в проекте, время начала и окончания, эффекты и переходы, а также т. д.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-116">It specifies the source clips used in the project, start and stop times, effects and transitions, and so forth.</span></span> <span data-ttu-id="b3ad1-117">Однако временная шкала не отображает видеопотокы и звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-117">The timeline does not render the video and audio streams, however.</span></span> <span data-ttu-id="b3ad1-118">Вместо этого механизм визуализации преобразует временную шкалу в граф фильтра для предварительного просмотра или вывода файла.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-118">Instead, the render engine translates the timeline into a filter graph, for either preview or file output.</span></span> <span data-ttu-id="b3ad1-119">Приложение обрабатывает временную шкалу, а не напрямую манипулирует графом фильтров, что может быть громоздким и подверженным ошибкам.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-119">An application manipulates the timeline rather than directly manipulating the filter graph, which would be cumbersome and error prone.</span></span>

<span data-ttu-id="b3ad1-120">В следующей таблице перечислены основные задачи, выполняемые обычным приложением для редактирования видео, а также интерфейсы, поддерживающие каждую задачу.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-120">The following table lists the main tasks that a typical video editing application performs, along with the interfaces that support each task.</span></span> <span data-ttu-id="b3ad1-121">В последующих разделах более подробно описаны эти задачи и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-121">Later sections describe these tasks and the interfaces in more detail.</span></span>



| <span data-ttu-id="b3ad1-122">Задача</span><span class="sxs-lookup"><span data-stu-id="b3ad1-122">Task</span></span>                                     | <span data-ttu-id="b3ad1-123">Интерфейс (ы)</span><span class="sxs-lookup"><span data-stu-id="b3ad1-123">Interface(s)</span></span>                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ad1-124">Создание или изменение временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-124">Construct or modify a timeline.</span></span>          | <span data-ttu-id="b3ad1-125">[**Иамтимелине**](iamtimeline.md) и другие интерфейсы **иамтимелинекскскскс**</span><span class="sxs-lookup"><span data-stu-id="b3ad1-125">[**IAMTimeline**](iamtimeline.md) and the other **IAMTimelineXXXX** interfaces</span></span>          |
| <span data-ttu-id="b3ad1-126">Сохранение и загрузка файлов проекта.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-126">Save and load project files.</span></span>             | [<span data-ttu-id="b3ad1-127">**IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="b3ad1-127">**IXml2Dex**</span></span>](ixml2dex.md)                                                             |
| <span data-ttu-id="b3ad1-128">Предварительный просмотр проекта или запись в файл.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-128">Preview a project or write it to a file.</span></span> | <span data-ttu-id="b3ad1-129">[**Ирендеренгине**](irenderengine.md), [ **исмартрендеренгине**](ismartrenderengine.md)</span><span class="sxs-lookup"><span data-stu-id="b3ad1-129">[**IRenderEngine**](irenderengine.md), [**ISmartRenderEngine**](ismartrenderengine.md)</span></span> |



 

<span data-ttu-id="b3ad1-130">Кроме того, приложение может выполнять некоторые или все следующие вторичные задачи.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-130">In addition, an application might perform some or all of the following secondary tasks.</span></span>



| <span data-ttu-id="b3ad1-131">Задача</span><span class="sxs-lookup"><span data-stu-id="b3ad1-131">Task</span></span>                                                                                           | <span data-ttu-id="b3ad1-132">Интерфейс (ы)</span><span class="sxs-lookup"><span data-stu-id="b3ad1-132">Interface(s)</span></span>                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b3ad1-133">Получение сведений о файлах мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-133">Obtain information about media files.</span></span> <span data-ttu-id="b3ad1-134">(Количество потоков; формат и длительность каждого потока.)</span><span class="sxs-lookup"><span data-stu-id="b3ad1-134">(Number of streams; format and duration of each stream.)</span></span> | [<span data-ttu-id="b3ad1-135">**имедиадет**</span><span class="sxs-lookup"><span data-stu-id="b3ad1-135">**IMediaDet**</span></span>](imediadet.md)                                               |
| <span data-ttu-id="b3ad1-136">Задание свойств для переходов и эффектов.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-136">Set properties on transitions and effects.</span></span>                                                     | [<span data-ttu-id="b3ad1-137">**ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="b3ad1-137">**IPropertySetter**</span></span>](ipropertysetter.md)                                   |
| <span data-ttu-id="b3ad1-138">Получение уведомлений при возникновении ошибок во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-138">Receive notification when errors occur during rendering.</span></span>                                       | <span data-ttu-id="b3ad1-139">[**Иамсетеррорлог**](iamseterrorlog.md), [ **иамеррорлог**](iamerrorlog.md)</span><span class="sxs-lookup"><span data-stu-id="b3ad1-139">[**IAMSetErrorLog**](iamseterrorlog.md), [**IAMErrorLog**](iamerrorlog.md)</span></span> |
| <span data-ttu-id="b3ad1-140">Получение кадров афиши.</span><span class="sxs-lookup"><span data-stu-id="b3ad1-140">Retrieve poster frames.</span></span>                                                                        | <span data-ttu-id="b3ad1-141">[**Имедиадет**](imediadet.md), [ **исамплеграббер**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="b3ad1-141">[**IMediaDet**](imediadet.md), [**ISampleGrabber**](isamplegrabber.md)</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="b3ad1-142">См. также</span><span class="sxs-lookup"><span data-stu-id="b3ad1-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3ad1-143">начало работы с помощью служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3ad1-143">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



