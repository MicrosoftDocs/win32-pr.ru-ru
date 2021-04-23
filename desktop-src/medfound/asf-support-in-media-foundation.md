---
description: Поддержка ASF в Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Поддержка ASF в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703455"
---
# <a name="asf-support-in-media-foundation"></a><span data-ttu-id="b005a-103">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b005a-103">ASF Support in Media Foundation</span></span>

<span data-ttu-id="b005a-104">Media Foundation поддерживает файлы мультимедиа в формате ASF:</span><span class="sxs-lookup"><span data-stu-id="b005a-104">Media Foundation supports media files in the Advanced Systems Format (ASF):</span></span>

-   <span data-ttu-id="b005a-105">Видео Windows Media (WMV-файлы)</span><span class="sxs-lookup"><span data-stu-id="b005a-105">Windows Media Video (WMV files)</span></span>
-   <span data-ttu-id="b005a-106">Windows Media Audio (WMA-файлы)</span><span class="sxs-lookup"><span data-stu-id="b005a-106">Windows Media Audio (WMA files)</span></span>

<span data-ttu-id="b005a-107">Media Foundation предоставляет несколько объектов для чтения и записи файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="b005a-107">Media Foundation provides several objects for reading and writing ASF files.</span></span> <span data-ttu-id="b005a-108">Эти объекты предоставляются на двух разных архитектурных уровнях.</span><span class="sxs-lookup"><span data-stu-id="b005a-108">These objects are provided in two different architectural layers.</span></span>

<span data-ttu-id="b005a-109">Во-первых, уровень *конвейера* содержит объекты, которые работают внутри [конвейера Media Foundation](media-foundation-pipeline.md) и соответствуют интерфейсам API, определенным в конвейере.</span><span class="sxs-lookup"><span data-stu-id="b005a-109">First, the *pipeline* layer contains objects that work inside the [Media Foundation pipeline](media-foundation-pipeline.md) and conform to the APIs defined by the pipeline.</span></span> <span data-ttu-id="b005a-110">Слой конвейера ASF содержит:</span><span class="sxs-lookup"><span data-stu-id="b005a-110">The ASF pipeline layer contains:</span></span>

-   <span data-ttu-id="b005a-111">[Источник носителя ASF](asf-media-source.md): АНАЛИЗИРУЕТ файлы ASF и доставляет пакеты аудио-и видеоданных.</span><span class="sxs-lookup"><span data-stu-id="b005a-111">[ASF Media Source](asf-media-source.md): Parses ASF files and delivers the audio/video data packets.</span></span>
-   <span data-ttu-id="b005a-112">[Кодеки Windows Media](windows-media-codecs.md): декодирование или кодирование потоков аудио или видео Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b005a-112">[Windows Media Codecs](windows-media-codecs.md): Decode or encode Windows Media audio or video streams.</span></span>
-   <span data-ttu-id="b005a-113">[Приемник мультимедиа ASF](asf-media-sinks.md): получает пакеты данных и записывает файл ASF.</span><span class="sxs-lookup"><span data-stu-id="b005a-113">[ASF Media Sink](asf-media-sinks.md): Receives data packets and writes an ASF file.</span></span>

<span data-ttu-id="b005a-114">Во-вторых, уровень контейнера WM обеспечивает низкоуровневый контроль над синтаксическим анализом и записью файла ASF.</span><span class="sxs-lookup"><span data-stu-id="b005a-114">Second, the WM Container layer provides low-level control over parsing and writing an ASF file.</span></span> <span data-ttu-id="b005a-115">Уровень конвейера использует Вмконтаинер внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="b005a-115">The pipeline layer uses WMContainer internally.</span></span> <span data-ttu-id="b005a-116">Приложения также могут использовать Вмконтаинер для анализа и записи в формате ASF низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="b005a-116">Applications can also use WMContainer for low-level ASF parsing and writing.</span></span>

![Диаграмма, на которой показаны элементы уровня конвейера и контейнера WM](images/asf-components.png)

## <a name="in-this-section"></a><span data-ttu-id="b005a-118">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b005a-118">In this section</span></span>



| <span data-ttu-id="b005a-119">Раздел</span><span class="sxs-lookup"><span data-stu-id="b005a-119">Topic</span></span>                                                                         | <span data-ttu-id="b005a-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b005a-120">Description</span></span>                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b005a-121">Структура файла ASF</span><span class="sxs-lookup"><span data-stu-id="b005a-121">ASF File Structure</span></span>](asf-file-structure.md)<br/>                       | <span data-ttu-id="b005a-122">Общие сведения о структуре файлов ASF и объектах, предоставляемых Media Foundation для работы с файлами ASF.</span><span class="sxs-lookup"><span data-stu-id="b005a-122">Overview of the ASF file structure and the objects provided by Media Foundation to work with ASF files.</span></span><br/> |
| [<span data-ttu-id="b005a-123">Компоненты ASF уровня конвейера</span><span class="sxs-lookup"><span data-stu-id="b005a-123">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)<br/> | <span data-ttu-id="b005a-124">Описывает, как анализировать и создавать файлы ASF с помощью уровня конвейера.</span><span class="sxs-lookup"><span data-stu-id="b005a-124">Describes how to parse and author ASF files using the pipeline layer.</span></span><br/>                                   |
| [<span data-ttu-id="b005a-125">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="b005a-125">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)<br/>       | <span data-ttu-id="b005a-126">Описывает, как анализировать и создавать файлы ASF с помощью слоя Вмконтаинер.</span><span class="sxs-lookup"><span data-stu-id="b005a-126">Describes how to parse and author ASF files using the WMContainer layer.</span></span><br/>                                |



 

<span data-ttu-id="b005a-127">Подробные сведения о структуре файла ASF см. в спецификации ASF, которую можно загрузить с [веб-сайта Майкрософт](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="b005a-127">For detailed information about the structure of an ASF file, see the ASF specification, which can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b005a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b005a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b005a-129">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="b005a-129">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




