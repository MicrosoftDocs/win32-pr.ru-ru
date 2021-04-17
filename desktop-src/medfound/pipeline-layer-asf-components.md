---
description: В модели конвейера Media Foundation источник мультимедиа подключен к преобразованию, которое затем подключается к приемнику мультимедиа.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Компоненты ASF уровня конвейера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711417"
---
# <a name="pipeline-layer-asf-components"></a><span data-ttu-id="f1344-103">Компоненты ASF уровня конвейера</span><span class="sxs-lookup"><span data-stu-id="f1344-103">Pipeline Layer ASF Components</span></span>

<span data-ttu-id="f1344-104">В модели конвейера Media Foundation источник мультимедиа подключен к преобразованию, которое затем подключается к приемнику мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f1344-104">In Media Foundation's pipeline model, a media source is connected to a transform which is further connected to a media sink.</span></span> <span data-ttu-id="f1344-105">Данные, содержащиеся в источнике, проходят через преобразование и формируют примеры выходных носителей в приемнике для воспроизведения или кодирования.</span><span class="sxs-lookup"><span data-stu-id="f1344-105">The data contained in the source flows through the transform and generates output media samples in the sink for the purpose of playback or encoding.</span></span> <span data-ttu-id="f1344-106">В зависимости от того, желает ли приложение воспроизводить содержимое ASF или кодировать в ASF-файл, приложение должно по-разному строить конвейер.</span><span class="sxs-lookup"><span data-stu-id="f1344-106">Depending on whether the application wants to playback ASF content or encode to an ASF file, the application must build the pipeline differently.</span></span>

<span data-ttu-id="f1344-107">В следующих разделах содержатся сведения о компонентах уровня конвейера.</span><span class="sxs-lookup"><span data-stu-id="f1344-107">The following topics contain information about the pipeline layer components.</span></span>

-   [<span data-ttu-id="f1344-108">Источник носителя ASF</span><span class="sxs-lookup"><span data-stu-id="f1344-108">ASF Media Source</span></span>](asf-media-source.md)
-   [<span data-ttu-id="f1344-109">Кодировщики Windows Media</span><span class="sxs-lookup"><span data-stu-id="f1344-109">Windows Media Encoders</span></span>](windows-media-encoders.md)
-   [<span data-ttu-id="f1344-110">Приемники мультимедиа ASF</span><span class="sxs-lookup"><span data-stu-id="f1344-110">ASF Media Sinks</span></span>](asf-media-sinks.md)

<span data-ttu-id="f1344-111">Ниже приведены три основных компонента конвейера ASF для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f1344-111">The three main components of an ASF pipeline for playback are as follows:</span></span>

-   <span data-ttu-id="f1344-112">Источник ASF Media предоставляется Media Foundation, который представляет ASF-файл.</span><span class="sxs-lookup"><span data-stu-id="f1344-112">ASF media source is provided by Media Foundation that represents an ASF file.</span></span>
-   <span data-ttu-id="f1344-113">Звуковые рересизерсы, видео-изображения и т. д. (преобразование)</span><span class="sxs-lookup"><span data-stu-id="f1344-113">Audio resamplers, video image resizers, etc., (transform)</span></span>
-   <span data-ttu-id="f1344-114">Модуль подготовки звука и видео (приемники)</span><span class="sxs-lookup"><span data-stu-id="f1344-114">Audio and Video renderer (sinks)</span></span>

<span data-ttu-id="f1344-115">Дополнительные сведения о создании конвейера воспроизведения см. в разделе [Создание топологий воспроизведения](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="f1344-115">For information about building a playback pipeline, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="f1344-116">Ниже приведены три основных компонента конвейера ASF для кодирования.</span><span class="sxs-lookup"><span data-stu-id="f1344-116">The three main components of an ASF pipeline for encoding are as follows:</span></span>

-   <span data-ttu-id="f1344-117">Источник мультимедиа, представляющий данные в формате, который необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="f1344-117">Media source representing the data in a format that needs to be converted.</span></span> <span data-ttu-id="f1344-118">Этот компонент может быть одним из источников мультимедиа по умолчанию, предоставляемых Media Foundation или пользовательским источником, предоставляющим интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="f1344-118">This component can be one of the default media sources provided by Media Foundation or a custom source that exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>
-   <span data-ttu-id="f1344-119">Кодировщики Windows Media (Transform), которые выполняют преобразование формата.</span><span class="sxs-lookup"><span data-stu-id="f1344-119">Windows Media encoders (transform) that perform the format conversion.</span></span>
-   <span data-ttu-id="f1344-120">Приемники мультимедиа ASF, предоставляемые Media Foundation, которые записывают объекты ASF и примеры мультимедиа в выходной файл, заданный приложением.</span><span class="sxs-lookup"><span data-stu-id="f1344-120">ASF media sinks provided by Media Foundation that write ASF objects and media samples in an output file specified by the application.</span></span>

<span data-ttu-id="f1344-121">Конвейер представлен в топологии, а каждый объект в конвейере представлен узлом топологии.</span><span class="sxs-lookup"><span data-stu-id="f1344-121">The pipeline is represented in a topology and each object in the pipeline is represented by a topology node.</span></span> <span data-ttu-id="f1344-122">Как для воспроизведения, так и для кодирования, все операции конвейера обрабатываются сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f1344-122">Both for playback and encoding, all of the pipeline operations are handled by the Media Session.</span></span> <span data-ttu-id="f1344-123">Одной из обязанностей сеанса мультимедиа является обеспечение того, что конвейер содержит все компоненты, необходимые для формирования выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f1344-123">One of responsibilities of the Media Session is to make sure that the pipeline has all the components required to generate output.</span></span> <span data-ttu-id="f1344-124">Например, в конвейере кодирования, если формат источника звука отличается от формата целевого объекта, сеанс мультимедиа вставляет дополнительные компоненты преобразования, такие как resamples, который выполняет соответствующие преобразования частоты выборки.</span><span class="sxs-lookup"><span data-stu-id="f1344-124">For example, in an encoding pipeline, if the audio source format is different than the target format, the Media Session inserts additional transform components such as the resampler that performs appropriate sample rate conversions.</span></span> <span data-ttu-id="f1344-125">Управление потоком данных через конвейер также управляется сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f1344-125">The data flow control through the pipeline is also managed by the Media Session.</span></span> <span data-ttu-id="f1344-126">В сценарии воспроизведения запуск сеанса мультимедиа отправляет образцы в САР и евр, которые визуализируются на выходном устройстве.</span><span class="sxs-lookup"><span data-stu-id="f1344-126">In a playback scenario, starting the Media Session the Media Session sends samples to SAR and EVR, which renders them on the output device.</span></span> <span data-ttu-id="f1344-127">Для кодирования запуск сеанса мультимедиа начнет процесс кодирования.</span><span class="sxs-lookup"><span data-stu-id="f1344-127">For encoding, starting the Media Session begins the encoding process.</span></span> <span data-ttu-id="f1344-128">Сеанс асинхронно уведомляет приложение о завершении кодирования.</span><span class="sxs-lookup"><span data-stu-id="f1344-128">The session asynchronously notifies the application when the encoding is complete.</span></span>

<span data-ttu-id="f1344-129">В следующем разделе содержатся пошаговые инструкции по использованию компонентов уровня конвейера для создания топологии кодирования.</span><span class="sxs-lookup"><span data-stu-id="f1344-129">The following topic contains step-by-step instructions about using the pipeline layer components to build an encoding topology.</span></span> <span data-ttu-id="f1344-130">компоненты для чтения и записи файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="f1344-130">components for reading and writing ASF files.</span></span>

-   [<span data-ttu-id="f1344-131">Учебник. 1. Передача кодирования мультимедиа Windows</span><span class="sxs-lookup"><span data-stu-id="f1344-131">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a><span data-ttu-id="f1344-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f1344-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1344-133">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1344-133">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



