---
title: Перечисление форматов кодеков
description: Перечисление форматов кодеков
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- потоки, перечисление форматов кодеков
- кодеки, перечисления
- потоки, форматы кодеков
- кодеки, форматы
- кодеки, интерфейс ИвмкодеЦинфо
- ИвмкодеЦинфо, форматы кодеков
- кодеки, интерфейс IWMCodecInfo3
- IWMCodecInfo3, форматы кодеков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a00c9afdbeba5a187be4b992a19d4c9bdb138e1
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444785"
---
# <a name="to-enumerate-codec-formats"></a><span data-ttu-id="e1d0c-111">Перечисление форматов кодеков</span><span class="sxs-lookup"><span data-stu-id="e1d0c-111">To Enumerate Codec Formats</span></span>

<span data-ttu-id="e1d0c-112">Формат кодека — это объект конфигурации потока, заполненный данными из кодека.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-112">A codec format is a stream configuration object populated with data from a codec.</span></span> <span data-ttu-id="e1d0c-113">Каждый формат кодека содержит конфигурацию носителя, поддерживаемую кодеком.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-113">Each codec format contains a media configuration supported by the codec.</span></span> <span data-ttu-id="e1d0c-114">Большинство аудиокодеков поддерживают конечное число форматов, каждое из которых перечислено кодеком, и доступ к нему можно получить с помощью методов [**ивмкодеЦинфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span><span class="sxs-lookup"><span data-stu-id="e1d0c-114">Most audio codecs support a finite number of formats, each of which is enumerated by the codec and can be accessed using the methods of [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span></span> <span data-ttu-id="e1d0c-115">Видеокодеки, с другой стороны, предоставляют только один формат.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-115">Video codecs, on the other hand, provide only a single format.</span></span> <span data-ttu-id="e1d0c-116">Это обусловлено тем, что видеопотоки имеют переменные, такие как размер кадра, которые являются более гибкими по сравнению с параметрами аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-116">This is because video streams have variables, like frame size, that are more flexible than the settings of an audio stream.</span></span> <span data-ttu-id="e1d0c-117">В потоке видео необходимо заполнить некоторые значения конфигурации потока. конфигурации аудиопотока следует изменять только для присвоения имени, имени соединения и номера потока.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-117">With a video stream, you must fill in some of the stream configuration values; audio stream configurations should only be edited to assign a name, connection name, and stream number.</span></span> <span data-ttu-id="e1d0c-118">Дополнительные сведения см. [в разделе Общая конфигурация для всех потоков](configuration-common-to-all-streams.md).</span><span class="sxs-lookup"><span data-stu-id="e1d0c-118">For more information, see [Configuration Common to All Streams](configuration-common-to-all-streams.md).</span></span>

<span data-ttu-id="e1d0c-119">Перечисленные форматы кодеков зависят от текущих параметров перечисления кодеков, которые задаются с помощью [**IWMCodecInfo3:: сеткодеценумератионсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span><span class="sxs-lookup"><span data-stu-id="e1d0c-119">The codec formats enumerated depend upon the current codec enumeration settings, which are set using [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span></span> <span data-ttu-id="e1d0c-120">В настоящее время поддерживаются только два свойства кодека: g \_ всзнумпассес, который указывает количество проходов кодирования, которые будет выполнять кодек, и g \_ всзвбренаблед, который указывает, будет ли кодек использовать кодирование переменной скорости.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-120">Currently, only two codec properties are supported: g\_wszNumPasses, which specifies the number of encoding passes that the codec will perform, and g\_wszVBREnabled, which specifies whether the codec will use variable bit rate encoding.</span></span> <span data-ttu-id="e1d0c-121">Максимальное число проходов по кодировке, поддерживаемое любыми кодеками, равно двум, поэтому существуют четыре отдельные конфигурации, для которых можно получить кодеки, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-121">The maximum number of encoding passes supported by any of the codecs is two, so there are four distinct configurations for which you can retrieve codecs, as shown in the following table.</span></span>



|    &nbsp;    | <span data-ttu-id="e1d0c-122">Поток постоянной скорости (CBR)</span><span class="sxs-lookup"><span data-stu-id="e1d0c-122">Constant bit rate (CBR) stream</span></span> | <span data-ttu-id="e1d0c-123">2. Передача потока CBR</span><span class="sxs-lookup"><span data-stu-id="e1d0c-123">2-pass CBR stream</span></span> | <span data-ttu-id="e1d0c-124">Потоковая частота с переменной скоростью (VBR) на основе качества</span><span class="sxs-lookup"><span data-stu-id="e1d0c-124">Quality-based variable bit rate (VBR) stream</span></span> | <span data-ttu-id="e1d0c-125">Поток VBR на основе битов (с ограничением или неограниченным доступом)</span><span class="sxs-lookup"><span data-stu-id="e1d0c-125">Bit-rate-based VBR stream (constrained or unconstrained)</span></span> |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="e1d0c-126">g \_ всзвбренаблед</span><span class="sxs-lookup"><span data-stu-id="e1d0c-126">g\_wszVBREnabled</span></span> | <span data-ttu-id="e1d0c-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="e1d0c-127">FALSE</span></span>                          | <span data-ttu-id="e1d0c-128">FALSE</span><span class="sxs-lookup"><span data-stu-id="e1d0c-128">FALSE</span></span>             | <span data-ttu-id="e1d0c-129">TRUE</span><span class="sxs-lookup"><span data-stu-id="e1d0c-129">TRUE</span></span>                                         | <span data-ttu-id="e1d0c-130">TRUE</span><span class="sxs-lookup"><span data-stu-id="e1d0c-130">TRUE</span></span>                                                     |
| <span data-ttu-id="e1d0c-131">g \_ всзнумпассес</span><span class="sxs-lookup"><span data-stu-id="e1d0c-131">g\_wszNumPasses</span></span>  | <span data-ttu-id="e1d0c-132">1</span><span class="sxs-lookup"><span data-stu-id="e1d0c-132">1</span></span>                              | <span data-ttu-id="e1d0c-133">2</span><span class="sxs-lookup"><span data-stu-id="e1d0c-133">2</span></span>                 | <span data-ttu-id="e1d0c-134">1</span><span class="sxs-lookup"><span data-stu-id="e1d0c-134">1</span></span>                                            | <span data-ttu-id="e1d0c-135">2</span><span class="sxs-lookup"><span data-stu-id="e1d0c-135">2</span></span>                                                        |



 

<span data-ttu-id="e1d0c-136">Чтобы перечислить форматы, поддерживаемые кодеком, используйте [**ивмкодеЦинфо:: жеткодекформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) для поиска количества поддерживаемых кодеков.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-136">To enumerate the formats supported for a codec, use [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) to find the number of supported codecs.</span></span> <span data-ttu-id="e1d0c-137">Затем вызовите [**ивмкодеЦинфо:: жеткодекформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-137">Then call [**IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) for each format.</span></span> <span data-ttu-id="e1d0c-138">Индексы формата в диапазоне от нуля до одного меньше общего числа поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-138">The format indexes range from zero, to one less than the total number of supported formats.</span></span> <span data-ttu-id="e1d0c-139">Вы можете получить описание формата, вызвав [**IWMCodecInfo2:: жеткодекформатдеск**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span><span class="sxs-lookup"><span data-stu-id="e1d0c-139">You can retrieve a description of the format by calling [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span></span> <span data-ttu-id="e1d0c-140">При использовании **жеткодекформатдеск** не нужно использовать **жеткодекформат**, так как объект конфигурации потока извлекается обоими методами.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-140">When using **GetCodecFormatDesc**, you do not need to use **GetCodecFormat**, because the stream configuration object is retrieved by both methods.</span></span> <span data-ttu-id="e1d0c-141">Форматы видеокодеков не включают описание.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-141">Video codec formats do not include a description.</span></span> <span data-ttu-id="e1d0c-142">Каждый видеокодек имеет только один формат, используемый для всех потоков этого типа.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-142">Each video codec has only one format that is used for all streams of that type.</span></span>

<span data-ttu-id="e1d0c-143">При извлечении формата кодека вы получаете интерфейс [**ивмстреамконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) объекта конфигурации потока, который содержит параметры формата.</span><span class="sxs-lookup"><span data-stu-id="e1d0c-143">When you retrieve a codec format, you get the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface of a stream configuration object containing the format settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1d0c-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e1d0c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1d0c-145">**Получение сведений о конфигурации потока из кодеков**</span><span class="sxs-lookup"><span data-stu-id="e1d0c-145">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




