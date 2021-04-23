---
title: Создание файлов ASF с помощью сторонних кодеков
description: Создание файлов ASF с помощью сторонних кодеков
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- Windows Media Format SDK, создание файлов ASF
- Пакет SDK для Windows Media Format, сторонние кодеки
- Расширенный системный формат (ASF), создание файлов
- ASF (Расширенный системный формат), создание файлов
- Расширенный системный формат (ASF), сторонние кодеки
- ASF (Расширенный системный формат), сторонние кодеки
- сторонние кодеки
- кодеки, сторонние
- кодеки, создание файлов ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6c057f1785ed50e328ac6094ff7dbe078e98fc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336636"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a><span data-ttu-id="40893-112">Создание файлов ASF с помощью сторонних кодеков</span><span class="sxs-lookup"><span data-stu-id="40893-112">To Create ASF Files Using Third-Party Codecs</span></span>

<span data-ttu-id="40893-113">Пакет Windows Media Format SDK можно использовать для создания файлов ASF, которые содержат цифровые файлы мультимедиа, закодированные с помощью любого выбранного вами кодека.</span><span class="sxs-lookup"><span data-stu-id="40893-113">You can use the Windows Media Format SDK to create ASF files that contain digital media encoded with any codec you choose.</span></span> <span data-ttu-id="40893-114">При использовании кодека, не входящего в состав этого пакета SDK, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="40893-114">When using a codec other than one included with this SDK, you must perform the following steps.</span></span>

1.  <span data-ttu-id="40893-115">Кодирование содержимого с помощью нужного кодека.</span><span class="sxs-lookup"><span data-stu-id="40893-115">Encode the content with the desired codec.</span></span>
2.  <span data-ttu-id="40893-116">Найдите или создайте значение идентификатора GUID для определения содержимого, закодированного кодеком, который используется на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="40893-116">Find or create a GUID value to identify content encoded with the codec used in step 1.</span></span>
3.  <span data-ttu-id="40893-117">Создайте новый профиль или измените существующий профиль для использования с закодированным содержимым.</span><span class="sxs-lookup"><span data-stu-id="40893-117">Create a new profile, or modify an existing profile for use with the encoded content.</span></span>
    -   <span data-ttu-id="40893-118">Создайте поток для закодированного содержимого с соответствующим основным типом.</span><span class="sxs-lookup"><span data-stu-id="40893-118">Create a stream for the encoded content with the appropriate major type.</span></span> <span data-ttu-id="40893-119">Дополнительные сведения о основных типах носителей см. в разделе [типы носителей](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="40893-119">For more information about major media types, see [Media Types](media-types.md).</span></span> <span data-ttu-id="40893-120">Используйте идентификатор GUID, указанный в шаге 2, в качестве подтипа носителя.</span><span class="sxs-lookup"><span data-stu-id="40893-120">Use the GUID identified in step 2 as the media subtype.</span></span>
    -   <span data-ttu-id="40893-121">Задайте для потока значения скорость и буфер, которые не будут приводить к переполнению буфера.</span><span class="sxs-lookup"><span data-stu-id="40893-121">Set the bit rate and buffer window for the stream to values that will not result in buffer overflow.</span></span> <span data-ttu-id="40893-122">Эти значения можно получить из кодека во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="40893-122">You should be able to obtain these values from the codec at the time of encoding.</span></span> <span data-ttu-id="40893-123">Компоненты среды выполнения пакета SDK проверяют значения скорости и окна буфера и удаляют образцы, если это необходимо, чтобы обеспечить соответствие заданным значениям.</span><span class="sxs-lookup"><span data-stu-id="40893-123">The SDK runtime components check the bitrate/buffer window values and drop samples if necessary to make the given data fit in with these values.</span></span> <span data-ttu-id="40893-124">Если значения заданы неправильно, то файл не будет правильно работать в потоке, что приведет к плохому воспроизведению.</span><span class="sxs-lookup"><span data-stu-id="40893-124">If you set the values incorrectly, the file will not stream properly, resulting in poor playback.</span></span>
    -   <span data-ttu-id="40893-125">Для видеопотоков необходимо установить элемент **бикомпрессион** структуры **битмапинфохеадер** , содержащейся в структуре [**ВМВИДЕОИНФОХЕАДЕР**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) , в соответствующее значение FOURCC для содержимого.</span><span class="sxs-lookup"><span data-stu-id="40893-125">For video streams, you must set the **biCompression** member of the **BITMAPINFOHEADER** structure contained in the [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure to the appropriate FOURCC value for the content.</span></span> <span data-ttu-id="40893-126">Это значение должно быть равно первым четырем байтам в GUID подтипа.</span><span class="sxs-lookup"><span data-stu-id="40893-126">This value must be equal to the first four bytes of the subtype GUID.</span></span> <span data-ttu-id="40893-127">Например, если **бикомпрессион** имеет значение Макефауркк ('t ', ' E ', ', ') = 0x54455354, то идентификатор GUID подтипа будет начинаться следующим образом: 54455354-XXXX-XXXX-XXXX-XXXXXXXXXXXX.</span><span class="sxs-lookup"><span data-stu-id="40893-127">For example, if **biCompression** is MAKEFOURCC('T','E','S','T')=0x54455354, then the subtype GUID will begin like this: 54455354-XXXX-XXXX-XXXX-XXXXXXXXXXXX.</span></span>
4.  <span data-ttu-id="40893-128">Создайте объект модуля записи и загрузите профиль, созданный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="40893-128">Create a writer object and load the profile created in the previous step.</span></span> <span data-ttu-id="40893-129">Дополнительные сведения о записи файлов см. в разделе [запись файлов ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="40893-129">For more information about writing files, see [Writing ASF Files](writing-asf-files.md).</span></span>
5.  <span data-ttu-id="40893-130">Пройдите по входным данным файла и присвойте входные свойства, как обычно.</span><span class="sxs-lookup"><span data-stu-id="40893-130">Loop through the inputs of the file and assign input properties for each as you normally would.</span></span> <span data-ttu-id="40893-131">Дополнительные сведения о входных данных см. [в разделе Работа с входными](working-with-inputs.md)данными.</span><span class="sxs-lookup"><span data-stu-id="40893-131">For more information about inputs, see [Working with Inputs](working-with-inputs.md).</span></span> <span data-ttu-id="40893-132">Для потока, закодированного с помощью стороннего кодека, установите указатель интерфейса [**ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) в **значение NULL** перед вызовом [**ивмвритер:: бегинвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="40893-132">For the stream encoded with a third-party codec, set the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface pointer to **NULL** before calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>
6.  <span data-ttu-id="40893-133">Используйте новый профиль, созданный на предыдущем шаге, для записи файла.</span><span class="sxs-lookup"><span data-stu-id="40893-133">Use the new profile created in the previous step to write the file.</span></span> <span data-ttu-id="40893-134">Передайте сжатые образцы с помощью [**ивмвритерадванцед:: вритестреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) вместо [**Ивмвритер:: вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span><span class="sxs-lookup"><span data-stu-id="40893-134">Pass the compressed samples using [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) instead of [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span> <span data-ttu-id="40893-135">Для видео необходимо указать, какие примеры являются ключевыми кадрами, передав WM \_ SF \_ клеанпоинт в качестве параметра *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="40893-135">For video, you must specify which samples are key frames by passing WM\_SF\_CLEANPOINT as the *dwFlags* parameter.</span></span>

<span data-ttu-id="40893-136">Чтобы обработать и распаковать поток, закодированный сторонним кодеком, необходимо ознакомиться со сжатыми примерами потока.</span><span class="sxs-lookup"><span data-stu-id="40893-136">To process and decompress the stream encoded with a third-party codec, you must read compressed stream samples.</span></span> <span data-ttu-id="40893-137">Приложение для чтения должно также выполнять распаковку выборки для потока.</span><span class="sxs-lookup"><span data-stu-id="40893-137">Your reading application must handle sample decompression for the stream as well.</span></span>

## <a name="putting-mpeg-2-streams-into-asf"></a><span data-ttu-id="40893-138">Размещение потоков MPEG-2 в формате ASF</span><span class="sxs-lookup"><span data-stu-id="40893-138">Putting MPEG-2 streams into ASF</span></span>

> [!Note]  
> <span data-ttu-id="40893-139">Эта статья относится к приложениям, использующим пакет SDK Windows Media Format для помещения MPEG-2 (или других форматов сжатия, использующих кадры B) в контейнер файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="40893-139">This topic applies to applications that use the Windows Media Format SDK to put MPEG-2 (or other compression formats that use B frames) into the ASF file container.</span></span>

 

<span data-ttu-id="40893-140">Объект модуля записи требует, чтобы все входные образцы имели штампы времени, и предполагается, что каждый входной пример имеет время презентации позже, чем предшествующее ему.</span><span class="sxs-lookup"><span data-stu-id="40893-140">The writer object requires that all input samples have time stamps, and it assumes that each input sample has a presentation time later than the one that preceded it.</span></span> <span data-ttu-id="40893-141">Хотя практически все несжатые видео и даже некоторые сжатые видеопотоки соответствуют этим условиям, потоки MPEG-2 не имеют.</span><span class="sxs-lookup"><span data-stu-id="40893-141">While virtually all uncompressed video and even some compressed video streams meet these conditions, MPEG-2 streams do not.</span></span> <span data-ttu-id="40893-142">В формате MPEG-2 не все образцы имеют отметку времени, а при наличии кадров B, порядок декодирования примеров не совпадает с порядком отрисовки.</span><span class="sxs-lookup"><span data-stu-id="40893-142">In MPEG-2, not all samples are time stamped, and when B frames are present, the sample decoding order is not the same as the rendering order.</span></span> <span data-ttu-id="40893-143">Когда объект модуля записи обнаруживает неупорядоченные образцы, он перемещает их в правильный порядок.</span><span class="sxs-lookup"><span data-stu-id="40893-143">When the writer object encounters out-of-order samples, it rearranges them into the "correct" order.</span></span> <span data-ttu-id="40893-144">Таким образом, чтобы хранить потоки MPEG-2 в собственном (не декодированном) потоке в контейнере ASF, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="40893-144">Therefore, to store MPEG-2 streams natively (not decoded) in an ASF container, you must perform the following steps:</span></span>

<span data-ttu-id="40893-145">При записи файла:</span><span class="sxs-lookup"><span data-stu-id="40893-145">When writing the file:</span></span>

1.  <span data-ttu-id="40893-146">Добавьте расширение единицы данных фиксированного размера (из-за) к каждому входному примеру, который будет содержать структуру, содержащую фактические значения времени начала и времени остановки для образца.</span><span class="sxs-lookup"><span data-stu-id="40893-146">Add a fixed-size data unit extension (DUE) to each input sample that will hold a structure that contains the actual MPEG time-stamp start-time and stop-time values for the sample.</span></span> <span data-ttu-id="40893-147">Используйте значение-1 для этих значений, если у образца нет метки времени.</span><span class="sxs-lookup"><span data-stu-id="40893-147">Use -1 for these values if the sample has no time stamp.</span></span>
2.  <span data-ttu-id="40893-148">Предоставьте объекту модуля записи "фиктивные" метки времени, которые всегда увеличиваются, чтобы они записывали образцы в файл в том же порядке, в котором они были получены.</span><span class="sxs-lookup"><span data-stu-id="40893-148">Give the writer object "dummy" input time stamps that are always increasing so that it will write the samples to the file in exactly the same order as they are received.</span></span> <span data-ttu-id="40893-149">Штампы времени фиктивных данных должны соответствовать реальному времени показа, как усреднено по времени.</span><span class="sxs-lookup"><span data-stu-id="40893-149">The dummy time stamps should correspond approximately to the actual presentation times, as averaged over time.</span></span> <span data-ttu-id="40893-150">Временные метки времени формируют временную шкалу, поэтому если они расходятся относительно меток реального времени, операции поиска в файле приведут к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="40893-150">The dummy time stamps will form the seeking timeline, so if they diverge relative to the real time stamps, seek operations on the file will produce unexpected results.</span></span> <span data-ttu-id="40893-151">Однако ограниченное количество колебаний между временами выборки не повлияет на операции поиска.</span><span class="sxs-lookup"><span data-stu-id="40893-151">However, a limited amount of jitter between the sample times will not seriously affect seek operations.</span></span>

<span data-ttu-id="40893-152">При чтении файла:</span><span class="sxs-lookup"><span data-stu-id="40893-152">When reading the file:</span></span>

-   <span data-ttu-id="40893-153">Для каждого примера, считанного из файла, следует изучить значение по причине.</span><span class="sxs-lookup"><span data-stu-id="40893-153">For each sample read from the file, examine the DUE.</span></span> <span data-ttu-id="40893-154">Если оно содержит время начала, которое больше или равно нулю, скопируйте это значение в отметку времени для образца выходных данных перед его доставкой в декодер.</span><span class="sxs-lookup"><span data-stu-id="40893-154">If it contains a start time that is greater than or equal to zero, copy that value to the time stamp for the output sample before it is delivered to the decoder.</span></span> <span data-ttu-id="40893-155">Задайте для всех других меток времени в выходных образцах **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="40893-155">Set all other time stamps on the output samples to **NULL**.</span></span> <span data-ttu-id="40893-156">В DirectShow это делается путем вызова **имедиасампле:: setTime**(**null**,**null**).</span><span class="sxs-lookup"><span data-stu-id="40893-156">In DirectShow, this is done by calling **IMediaSample::SetTime**(**NULL**,**NULL**).</span></span>

## <a name="related-topics"></a><span data-ttu-id="40893-157">См. также</span><span class="sxs-lookup"><span data-stu-id="40893-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40893-158">**Буферизация содержимого**</span><span class="sxs-lookup"><span data-stu-id="40893-158">**Buffering Content**</span></span>](buffering-content.md)
</dt> <dt>

[<span data-ttu-id="40893-159">**Интерфейс Ивмвритер**</span><span class="sxs-lookup"><span data-stu-id="40893-159">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="40893-160">**Интерфейс Ивмвритерадванцед**</span><span class="sxs-lookup"><span data-stu-id="40893-160">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="40893-161">**Доставка сжатых образцов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="40893-161">**To Deliver Compressed Samples with the Asynchronous Reader**</span></span>](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="40893-162">**Получение примеров Stream с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="40893-162">**To Retrieve Stream Samples with the Synchronous Reader**</span></span>](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="40893-163">**вмвидеоинфохеадер**</span><span class="sxs-lookup"><span data-stu-id="40893-163">**WMVIDEOINFOHEADER**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[<span data-ttu-id="40893-164">**Работа с профилями**</span><span class="sxs-lookup"><span data-stu-id="40893-164">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> <dt>

[<span data-ttu-id="40893-165">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="40893-165">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




