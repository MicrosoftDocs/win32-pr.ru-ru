---
description: Кодировщик преобразует несжатые аудио или видео в сжатые пакеты в формате, указанном приложением. Для преобразования файлов мультимедиа в формат ASF можно использовать видеокодеки Windows Media Audio и Video.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Кодировщики Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693832"
---
# <a name="windows-media-encoders"></a><span data-ttu-id="cf876-104">Кодировщики Windows Media</span><span class="sxs-lookup"><span data-stu-id="cf876-104">Windows Media Encoders</span></span>

<span data-ttu-id="cf876-105">Кодировщик преобразует несжатые аудио или видео в сжатые пакеты в формате, указанном приложением.</span><span class="sxs-lookup"><span data-stu-id="cf876-105">An encoder converts uncompressed audio or video into compressed packets in the format specified by the application.</span></span> <span data-ttu-id="cf876-106">Для преобразования файлов мультимедиа в формат ASF можно использовать видеокодеки Windows Media Audio и Video.</span><span class="sxs-lookup"><span data-stu-id="cf876-106">For converting media files into ASF format, you can use the Windows Media audio and video codecs.</span></span>

<span data-ttu-id="cf876-107">Кодировщик идентифицируется по идентификатору GUID, который представляет категорию: аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="cf876-107">An encoder is identified by the GUID that represents the category: audio or video.</span></span> <span data-ttu-id="cf876-108">Тип выходных данных кодировщика представлен основным типом и идентификатором GUID подтипа.</span><span class="sxs-lookup"><span data-stu-id="cf876-108">The encoder's output type is represented by a media type's major and the sub type GUID.</span></span>

-   <span data-ttu-id="cf876-109">Аудиокодеки Windows Media</span><span class="sxs-lookup"><span data-stu-id="cf876-109">Windows Media audio codecs</span></span>

    <span data-ttu-id="cf876-110">Категория: **\_ \_ звуковая \_ кодировщик категории MFT**</span><span class="sxs-lookup"><span data-stu-id="cf876-110">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="cf876-111">Основной тип: Мфмедиатипе \_ Audio</span><span class="sxs-lookup"><span data-stu-id="cf876-111">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="cf876-112">Подтип: Мфаудиоформат \_ WMAudioV9, мфаудиоформат \_ WMAudioV8, мфаудиоформат \_ вмаудио \_ без потерь, мфаудиоформат \_ вмаспдиф</span><span class="sxs-lookup"><span data-stu-id="cf876-112">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="cf876-113">Видеокодеки видео Windows Media</span><span class="sxs-lookup"><span data-stu-id="cf876-113">Windows Media video codecs</span></span>

    <span data-ttu-id="cf876-114">Категория: **\_ \_ \_ видеокодировщик категории MFT**</span><span class="sxs-lookup"><span data-stu-id="cf876-114">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="cf876-115">Основной тип: \_ видео мфмедиатипе</span><span class="sxs-lookup"><span data-stu-id="cf876-115">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="cf876-116">Подтип: Мфвидеоформат \_ WVC1, мфвидеоформат \_ WMV3, мфвидеоформат \_ WMV2, мфвидеоформат \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="cf876-116">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="cf876-117">Эти кодировщики реализуются как [Media Foundation преобразования](media-foundation-transforms.md) (MFT), и Media Foundation предоставляет доступ к приложению через интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cf876-117">These encoders are implemented as [Media Foundation transform](media-foundation-transforms.md) (MFT) and Media Foundation provides access to the application through the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the encoder.</span></span> <span data-ttu-id="cf876-118">Если для кодирования ASF используются компоненты уровня конвейера, MFT кодировщика вставляется в конвейер в виде узла преобразования, так как он отвечает за преобразование данных мультимедиа, которые проходят через источник к приемнику.</span><span class="sxs-lookup"><span data-stu-id="cf876-118">If you are using pipeline layer components for ASF encoding, the encoder MFT is inserted into the pipeline as a transform node because it is responsible for transforming media data that flows through the source to the sink.</span></span> <span data-ttu-id="cf876-119">Если источником является сжатый тип, то конвейер добавляет необходимые декодеры для преобразования источника в несжатый тип.</span><span class="sxs-lookup"><span data-stu-id="cf876-119">If the source is a compressed type, then the pipeline adds the required decoders to convert the source into an uncompressed type.</span></span> <span data-ttu-id="cf876-120">Кодировщик имеет один входной поток и один выходной поток.</span><span class="sxs-lookup"><span data-stu-id="cf876-120">An encoder has one input stream and one output stream.</span></span> <span data-ttu-id="cf876-121">Кодировщик получает входные данные и создает закодированные данные в соответствии с конфигурацией и форматом, заданным приложением до сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="cf876-121">The encoder receives input data and produces encoded data according to the configuration and format set by the application prior to the encoding session.</span></span> <span data-ttu-id="cf876-122">Формат выходного потока описывается типом носителя.</span><span class="sxs-lookup"><span data-stu-id="cf876-122">The format of the output stream is described by a media type.</span></span>

<span data-ttu-id="cf876-123">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="cf876-123">This section contains the following topics.</span></span>



| <span data-ttu-id="cf876-124">Раздел</span><span class="sxs-lookup"><span data-stu-id="cf876-124">Topic</span></span>                                                                              | <span data-ttu-id="cf876-125">Описание</span><span class="sxs-lookup"><span data-stu-id="cf876-125">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf876-126">Создание экземпляра MFT для кодировщика</span><span class="sxs-lookup"><span data-stu-id="cf876-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)                  | <span data-ttu-id="cf876-127">Объясняется, как создать кодировщик.</span><span class="sxs-lookup"><span data-stu-id="cf876-127">Explains how to create the encoder.</span></span>                                                         |
| [<span data-ttu-id="cf876-128">Свойства кодировки</span><span class="sxs-lookup"><span data-stu-id="cf876-128">Encoding Properties</span></span>](configuring-the-encoder.md)                                 | <span data-ttu-id="cf876-129">Объясняется, как настроить кодировщик, задав соответствующие свойства в файле MFT кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cf876-129">Explains how to configure the encoder by setting appropriate properties on the encoder MFT.</span></span> |
| [<span data-ttu-id="cf876-130">Согласование типов мультимедиа в кодировщике</span><span class="sxs-lookup"><span data-stu-id="cf876-130">Media Type Negotiation on the Encoder</span></span>](media-type-negotiation-on-the-encoder.md) | <span data-ttu-id="cf876-131">Объясняет, как задать входные и выходные типы мультимедиа для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cf876-131">Explains how to set input and output media types on the encoder.</span></span>                            |
| [<span data-ttu-id="cf876-132">Настройка кодировщика WMV</span><span class="sxs-lookup"><span data-stu-id="cf876-132">Configuring a WMV Encoder</span></span>](configuring-a-wmv-encoder.md)                         | <span data-ttu-id="cf876-133">Описание настройки кодировщика Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="cf876-133">Explains how to configure a Windows Media Video (WMV) encoder.</span></span>                              |
| [<span data-ttu-id="cf876-134">Задание типа выходных данных для кодировщика WMA</span><span class="sxs-lookup"><span data-stu-id="cf876-134">Setting an Output Type for a WMA Encoder</span></span>](configuring-a-wma-encoder.md)          | <span data-ttu-id="cf876-135">Объясняет, как задать тип выходных данных для кодировщика Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="cf876-135">Explains how to set an output type on a Windows Media Audio (WMA) encoder.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="cf876-136">См. также</span><span class="sxs-lookup"><span data-stu-id="cf876-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf876-137">Компоненты ASF уровня конвейера</span><span class="sxs-lookup"><span data-stu-id="cf876-137">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



