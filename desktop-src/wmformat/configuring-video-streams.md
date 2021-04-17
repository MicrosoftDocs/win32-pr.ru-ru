---
title: Настройка потоков видео
description: Настройка потоков видео
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- потоки, Настройка потоков видео
- кодеки, Настройка потоков видео
- видеопотоки, Настройка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691439"
---
# <a name="configuring-video-streams"></a><span data-ttu-id="df542-106">Настройка потоков видео</span><span class="sxs-lookup"><span data-stu-id="df542-106">Configuring Video Streams</span></span>

<span data-ttu-id="df542-107">Потоки видео являются более гибкими в своей конфигурации, чем звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="df542-107">Video streams are more flexible in their configuration than audio streams.</span></span> <span data-ttu-id="df542-108">Это связано с тем, что свойства кадров, составляющих видео, могут сильно варьироваться от одного файла до следующего.</span><span class="sxs-lookup"><span data-stu-id="df542-108">This is because the properties of the frames that make up the video can vary widely from one file to the next.</span></span> <span data-ttu-id="df542-109">При извлечении формата кодека для используемого кодека необходимо задать следующие значения для объектов конфигурации видеопотока.</span><span class="sxs-lookup"><span data-stu-id="df542-109">When you retrieve the codec format for the codec you are using, you must set the following values for video stream configuration objects.</span></span>



| <span data-ttu-id="df542-110">Значение</span><span class="sxs-lookup"><span data-stu-id="df542-110">Value</span></span>                                 | <span data-ttu-id="df542-111">Описание</span><span class="sxs-lookup"><span data-stu-id="df542-111">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df542-112">Скорость потока</span><span class="sxs-lookup"><span data-stu-id="df542-112">Bit rate</span></span>                              | <span data-ttu-id="df542-113">Вызовите [**ивмстреамконфиг:: сетбитрате**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) , чтобы задать нужное значение.</span><span class="sxs-lookup"><span data-stu-id="df542-113">Call [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) to set to the desired value.</span></span> <span data-ttu-id="df542-114">Видеокодек попытается сжать носитель в соответствии со своими спецификациями.</span><span class="sxs-lookup"><span data-stu-id="df542-114">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="df542-115">Если значения слишком низкие, полученное сжатое видео будет иметь низкую производительность.</span><span class="sxs-lookup"><span data-stu-id="df542-115">If your values are too low, the resulting compressed video will be very degraded.</span></span>           |
| <span data-ttu-id="df542-116">Окно буфера</span><span class="sxs-lookup"><span data-stu-id="df542-116">Buffer window</span></span>                         | <span data-ttu-id="df542-117">Вызовите [**ивмстреамконфиг:: сетбуффервиндов**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) , чтобы задать нужное значение.</span><span class="sxs-lookup"><span data-stu-id="df542-117">Call [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) to set to the desired value.</span></span> <span data-ttu-id="df542-118">Видеокодек попытается сжать носитель в соответствии со своими спецификациями.</span><span class="sxs-lookup"><span data-stu-id="df542-118">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="df542-119">Если значения слишком низкие, полученное сжатое видео будет иметь низкую производительность.</span><span class="sxs-lookup"><span data-stu-id="df542-119">If your values are too low, the resulting compressed video will be very degraded.</span></span> |
| <span data-ttu-id="df542-120">**ВМВИДЕОИНФОХЕАДЕР. Рксаурце**</span><span class="sxs-lookup"><span data-stu-id="df542-120">**WMVIDEOINFOHEADER.rcSource**</span></span>        | <span data-ttu-id="df542-121">Верхний левый угол должен иметь значение 0, 0.</span><span class="sxs-lookup"><span data-stu-id="df542-121">The upper left corner must be set to 0,0.</span></span> <span data-ttu-id="df542-122">В нижнем правом углу должны быть установлены размеры рамки.</span><span class="sxs-lookup"><span data-stu-id="df542-122">The lower right corner must be set to the frame dimensions.</span></span> <span data-ttu-id="df542-123">Например, в потоке 640x480 эти параметры будут иметь значение 0, 0640480.</span><span class="sxs-lookup"><span data-stu-id="df542-123">For example, in a 640x480 stream, these settings would be 0,0,640,480.</span></span>                                                                                                |
| <span data-ttu-id="df542-124">**ВМВИДЕОИНФОХЕАДЕР. Рктаржет**</span><span class="sxs-lookup"><span data-stu-id="df542-124">**WMVIDEOINFOHEADER.rcTarget**</span></span>        | <span data-ttu-id="df542-125">Должен соответствовать **рксаурце**.</span><span class="sxs-lookup"><span data-stu-id="df542-125">Must match **rcSource**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="df542-126">**ВМВИДЕОИНФОХЕАДЕР. Двбитрате**</span><span class="sxs-lookup"><span data-stu-id="df542-126">**WMVIDEOINFOHEADER.dwBitRate**</span></span>       | <span data-ttu-id="df542-127">Параметр должен соответствовать скорости, заданной для потока.</span><span class="sxs-lookup"><span data-stu-id="df542-127">Must match the bit rate set for the stream.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="df542-128">**ВМВИДЕОИНФОХЕАДЕР. авгтимеперфраме**</span><span class="sxs-lookup"><span data-stu-id="df542-128">**WMVIDEOINFOHEADER.AvgTimePerFrame**</span></span> | <span data-ttu-id="df542-129">Задайте приблизительное время для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="df542-129">Set to the approximate time per frame.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="df542-130">**БИТМАПИНФОХЕАДЕР. Бивидс**</span><span class="sxs-lookup"><span data-stu-id="df542-130">**BITMAPINFOHEADER.biWidth**</span></span>          | <span data-ttu-id="df542-131">Задайте ширину (в пикселях) требуемого размера кадра.</span><span class="sxs-lookup"><span data-stu-id="df542-131">Set to the width, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="df542-132">**БИТМАПИНФОХЕАДЕР. Бихеигхт**</span><span class="sxs-lookup"><span data-stu-id="df542-132">**BITMAPINFOHEADER.biHeight**</span></span>         | <span data-ttu-id="df542-133">Задайте высоту (в пикселях) требуемого размера кадра.</span><span class="sxs-lookup"><span data-stu-id="df542-133">Set to the height, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                    |



 

<span data-ttu-id="df542-134">Видеосодержимое не воспроизводится правильно, если оно не закодировано до размера, кратного четырем для ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="df542-134">Video content does not play correctly unless it is encoded to a size that is a multiple of four for both width and height.</span></span> <span data-ttu-id="df542-135">Исключением является видео в формате [*RGB*](wmformat-glossary.md) без сжатия, которое может иметь любой размер.</span><span class="sxs-lookup"><span data-stu-id="df542-135">The exception is [*RGB*](wmformat-glossary.md) uncompressed video, which can be any size.</span></span> <span data-ttu-id="df542-136">Если вы попытаетесь задать размер, который не кратен четырем, модуль записи вернет одну из следующих ошибок:</span><span class="sxs-lookup"><span data-stu-id="df542-136">If you try to set a size that is not a multiple of four, one of the following errors will be returned by the writer:</span></span>

-   <span data-ttu-id="df542-137">\_ \_ Недопустимый \_ входной \_ Формат NS E</span><span class="sxs-lookup"><span data-stu-id="df542-137">NS\_E\_INVALID\_INPUT\_FORMAT</span></span>
-   <span data-ttu-id="df542-138">\_ \_ Недопустимый \_ выходной \_ Формат NS E</span><span class="sxs-lookup"><span data-stu-id="df542-138">NS\_E\_INVALID\_OUTPUT\_FORMAT</span></span>
-   <span data-ttu-id="df542-139">NS \_ E \_ инвалидпрофиле</span><span class="sxs-lookup"><span data-stu-id="df542-139">NS\_E\_INVALIDPROFILE</span></span>

<span data-ttu-id="df542-140">Если вы используете переменное кодирование с переменной скоростью, может потребоваться выполнить другие корректировки.</span><span class="sxs-lookup"><span data-stu-id="df542-140">If you are using variable bit rate encoding, you may need to make other adjustments.</span></span> <span data-ttu-id="df542-141">Дополнительные сведения см. в разделе [Настройка потоков VBR](configuring-vbr-streams.md).</span><span class="sxs-lookup"><span data-stu-id="df542-141">For more information, see [Configuring VBR Streams](configuring-vbr-streams.md).</span></span>

<span data-ttu-id="df542-142">Некоторые видеокодеки Windows Media поддерживают несколько уровней сложности.</span><span class="sxs-lookup"><span data-stu-id="df542-142">Some Windows Media Video codecs support multiple complexity levels.</span></span> <span data-ttu-id="df542-143">Уровни сложности определяют алгоритмы, которые кодек будет использовать при кодировании видеопотока.</span><span class="sxs-lookup"><span data-stu-id="df542-143">Complexity levels determine the algorithms that the codec will use when encoding a video stream.</span></span> <span data-ttu-id="df542-144">При использовании высокого уровня сложности потребуется больше вычислительной мощности для кодирования и декодирования.</span><span class="sxs-lookup"><span data-stu-id="df542-144">Using a high complexity level will require more processing power for encoding and decoding.</span></span>

<span data-ttu-id="df542-145">Каждый кодек, поддерживающий параметры сложности, предоставляет следующие параметры, которые можно извлечь с помощью метода [**IWMCodecInfo3:: жеткодекпроп**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) .</span><span class="sxs-lookup"><span data-stu-id="df542-145">Each codec that supports complexity settings exposes the following settings that you can retrieve with the [**IWMCodecInfo3::GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) method.</span></span>



| <span data-ttu-id="df542-146">Параметр</span><span class="sxs-lookup"><span data-stu-id="df542-146">Setting</span></span>                 | <span data-ttu-id="df542-147">Описание</span><span class="sxs-lookup"><span data-stu-id="df542-147">Description</span></span>                                         |
|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="df542-148">g \_ всзкомплекситимакс</span><span class="sxs-lookup"><span data-stu-id="df542-148">g\_wszComplexityMax</span></span>     | <span data-ttu-id="df542-149">Максимальный уровень качества, поддерживаемый кодеком.</span><span class="sxs-lookup"><span data-stu-id="df542-149">The maximum quality level supported by the codec.</span></span>   |
| <span data-ttu-id="df542-150">g \_ всзкомплекситйоффлине</span><span class="sxs-lookup"><span data-stu-id="df542-150">g\_wszComplexityOffline</span></span> | <span data-ttu-id="df542-151">Предлагаемый уровень качества для воспроизведения в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="df542-151">The suggested quality level for offline playback.</span></span>   |
| <span data-ttu-id="df542-152">g \_ всзкомплекситиливе</span><span class="sxs-lookup"><span data-stu-id="df542-152">g\_wszComplexityLive</span></span>    | <span data-ttu-id="df542-153">Предлагаемый уровень качества для воспроизведения потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="df542-153">The suggested quality level for streaming playback.</span></span> |



 

<span data-ttu-id="df542-154">Чтобы задать сложность потока видео в профиле, используйте метод [**ивмпропертиваулт:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) , используя свойство g \_ всзкомплексити.</span><span class="sxs-lookup"><span data-stu-id="df542-154">To set the complexity for a video stream in a profile, use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method using the property g\_wszComplexity.</span></span> <span data-ttu-id="df542-155">Заданное значение должно быть меньше или равно максимально поддерживаемой сложности для кодека.</span><span class="sxs-lookup"><span data-stu-id="df542-155">The value you set must be less than or equal to the maximum supported complexity for the codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df542-156">См. также</span><span class="sxs-lookup"><span data-stu-id="df542-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df542-157">**Общая конфигурация для всех потоков**</span><span class="sxs-lookup"><span data-stu-id="df542-157">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="df542-158">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="df542-158">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="df542-159">**Параметры сложности видео**</span><span class="sxs-lookup"><span data-stu-id="df542-159">**Video Complexity Settings**</span></span>](video-complexity-settings.md)
</dt> </dl>

 

 




