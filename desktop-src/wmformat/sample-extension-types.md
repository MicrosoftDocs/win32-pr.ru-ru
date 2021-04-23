---
title: Примеры типов расширений
description: Примеры типов расширений
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Media Format SDK, примеры расширений
- Расширенный формат систем (ASF), примеры расширений
- ASF (Расширенный системный формат), примеры расширений
- Windows Media Format SDK, расширения модулей данных
- Расширенный системный формат (ASF), расширения модулей данных
- ASF (Расширенный системный формат), расширения модулей данных
- Windows Media Format SDK, свойства буфера
- Расширенный системный формат (ASF), свойства буфера
- ASF (Расширенный системный формат), свойства буфера
- Примеры расширений, типы
- расширения модулей данных, типы
- свойства буфера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "105710255"
---
# <a name="sample-extension-types"></a><span data-ttu-id="04d2f-115">Примеры типов расширений</span><span class="sxs-lookup"><span data-stu-id="04d2f-115">Sample Extension Types</span></span>

<span data-ttu-id="04d2f-116">Примеры расширений, также называемые модулями обработки данных (или свойствами буфера), — это элементы данных, которые присоединяются к примерам мультимедиа в разделе данных ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="04d2f-116">Sample extensions, also called data unit extensions (DUEs) or buffer properties, are items of data that are attached to the media samples in the data section of the ASF file.</span></span> <span data-ttu-id="04d2f-117">Несколько типов примеров расширений определяются в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="04d2f-117">Several types of sample extensions are defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="04d2f-118">Вы также можете создавать собственные типы расширений.</span><span class="sxs-lookup"><span data-stu-id="04d2f-118">You can also create your own extension types.</span></span>

<span data-ttu-id="04d2f-119">Чтобы использовать образцы расширений, необходимо указать тип расширения в данных конфигурации потока профиля.</span><span class="sxs-lookup"><span data-stu-id="04d2f-119">To use sample extensions, you must identify the extension type in the stream configuration data of the profile.</span></span> <span data-ttu-id="04d2f-120">Вызовите метод [**IWMStreamConfig2:: адддатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) , чтобы настроить поток для приема образцов с расширенными данными.</span><span class="sxs-lookup"><span data-stu-id="04d2f-120">Call the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method to configure a stream to accept samples with extended data.</span></span>

<span data-ttu-id="04d2f-121">Отдельные образцы расширений необходимо добавить во входные образцы, вызвав метод [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="04d2f-121">Individual sample extensions must be added to the input samples by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="04d2f-122">При чтении образцов можно вызвать метод [**INSSBuffer3:: Property**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) для получения данных расширения.</span><span class="sxs-lookup"><span data-stu-id="04d2f-122">When reading samples, you can call the [**INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) method to retrieve the extension data.</span></span> <span data-ttu-id="04d2f-123">Можно также использовать методы интерфейса [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) для перечисления расширений модулей данных, присоединенных к примеру.</span><span class="sxs-lookup"><span data-stu-id="04d2f-123">You can also use the methods of the [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) interface to enumerate the data unit extensions attached to a sample.</span></span>

<span data-ttu-id="04d2f-124">В следующей таблице перечислены предопределенные идентификаторы расширений единиц данных, а также приводятся данные, присоединяемые к образцам для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="04d2f-124">The following table lists the predefined data unit extension identifiers, and describes the data that is attached to samples for each.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04d2f-125">Пример GUID расширения</span><span class="sxs-lookup"><span data-stu-id="04d2f-125">Sample extension GUID</span></span></th>
<th><span data-ttu-id="04d2f-126">Описание</span><span class="sxs-lookup"><span data-stu-id="04d2f-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04d2f-127">WM_SampleExtensionGUID_OutputCleanPoint</span><span class="sxs-lookup"><span data-stu-id="04d2f-127">WM_SampleExtensionGUID_OutputCleanPoint</span></span></td>
<td><span data-ttu-id="04d2f-128">Данные указывают, является ли образец <a href="wmformat-glossary.md"><em>клеанпоинт</em></a>.</span><span class="sxs-lookup"><span data-stu-id="04d2f-128">The data indicates whether the sample is a <a href="wmformat-glossary.md"><em>cleanpoint</em></a>.</span></span> <span data-ttu-id="04d2f-129">Нулевое значение указывает, что образец не является клеанпоинт.</span><span class="sxs-lookup"><span data-stu-id="04d2f-129">A value of zero indicates that the sample is not a cleanpoint.</span></span> <span data-ttu-id="04d2f-130">Ненулевое значение указывает, что это клеанпоинт.</span><span class="sxs-lookup"><span data-stu-id="04d2f-130">A non-zero value indicates that it is a cleanpoint.</span></span> <span data-ttu-id="04d2f-131">Этот образец типа расширения единицы данных (тип) используется для мониторинга клеанпоинтс при записи предварительно сжатых потоков мультимедиа, закодированных с помощью кодеков сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="04d2f-131">This sample data unit extension (DUE) type is used to keep track of cleanpoints when writing precompressed media streams that were encoded with third-party codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04d2f-132">WM_SampleExtensionGUID_Timecode</span><span class="sxs-lookup"><span data-stu-id="04d2f-132">WM_SampleExtensionGUID_Timecode</span></span></td>
<td><span data-ttu-id="04d2f-133">Данные представляют собой структуру <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> , содержащую данные кода времени SMPTE, связанные с образцом. Размер этого WM_SampleExtension_Timecode_Size всегда равен 14 байтам.</span><span class="sxs-lookup"><span data-stu-id="04d2f-133">The data is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> structure containing SMPTE time code data associated with the sample.The size for this DUE is always WM_SampleExtension_Timecode_Size, which is 14 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04d2f-134">WM_SampleExtensionGUID_FileName</span><span class="sxs-lookup"><span data-stu-id="04d2f-134">WM_SampleExtensionGUID_FileName</span></span></td>
<td><span data-ttu-id="04d2f-135">Этот тип примера расширения используется для файловых потоков.</span><span class="sxs-lookup"><span data-stu-id="04d2f-135">This type of sample extension is used for file streams.</span></span> <span data-ttu-id="04d2f-136">Данные в примере файлового потока являются частью файла данных.</span><span class="sxs-lookup"><span data-stu-id="04d2f-136">The data in a file stream sample is a piece of a data file.</span></span> <span data-ttu-id="04d2f-137">Данные в примере расширения указывают имя файла, из которого было получено содержимое в образце. Имя файла представляет собой строку расширенных символов, содержащую имя файла в формате name. extension без сведений о пути.</span><span class="sxs-lookup"><span data-stu-id="04d2f-137">The data in the sample extension specifies the name of the file from which the content in the sample was taken.The file name is a wide-character string containing the file name in name.extension format without any path information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04d2f-138">WM_SampleExtensionGUID_ContentType</span><span class="sxs-lookup"><span data-stu-id="04d2f-138">WM_SampleExtensionGUID_ContentType</span></span></td>
<td><span data-ttu-id="04d2f-139">Данные определяют тип содержимого, которое содержит образец.</span><span class="sxs-lookup"><span data-stu-id="04d2f-139">The data identifies the type of content that the sample contains.</span></span> <span data-ttu-id="04d2f-140">Этот тип примера расширения используется с потоками видео с чередованием. Все содержимое с чередованием использует флаг WM_CT_INTERLACED в сочетании с побитовой <strong>или</strong> с помощью WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST или WM_CT_REPEAT_FIRST_FIELD.</span><span class="sxs-lookup"><span data-stu-id="04d2f-140">This type of sample extension is used with interlaced video streams.All interlaced content uses the WM_CT_INTERLACED flag combined by a bitwise <strong>OR</strong> with either WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST, or WM_CT_REPEAT_FIRST_FIELD.</span></span><br/> <span data-ttu-id="04d2f-141">Порядок полей не используется в процессе кодирования, но сохраняется с использованием сжатых образцов, чтобы его можно было передать в оборудование для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="04d2f-141">The field order is not used in the encoding process, but is maintained with the compressed samples so that it can be passed to the rendering hardware.</span></span> <span data-ttu-id="04d2f-142">Воспроизведение содержимого с чередованием с неправильным порядком полей вводит в видео такие артефакты, как нарушение движения.</span><span class="sxs-lookup"><span data-stu-id="04d2f-142">Playing interlaced content with the incorrect field order introduces artifacts such as motion jitter in the video.</span></span><br/> <span data-ttu-id="04d2f-143">Размер этого срока всегда WM_SampleExtension_ContentType_Size.</span><span class="sxs-lookup"><span data-stu-id="04d2f-143">The size for this DUE is always WM_SampleExtension_ContentType_Size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04d2f-144">WM_SampleExtensionGUID_PixelAspectRatio</span><span class="sxs-lookup"><span data-stu-id="04d2f-144">WM_SampleExtensionGUID_PixelAspectRatio</span></span></td>
<td><span data-ttu-id="04d2f-145">Данные обозначают пропорцию содержимого в образце пикселя.</span><span class="sxs-lookup"><span data-stu-id="04d2f-145">The data indicates the pixel aspect ratio of the content in the sample.</span></span> <span data-ttu-id="04d2f-146">Это относится только к видео. Этот тип расширения используется для обнаружения пропорций неквадратных пикселей.</span><span class="sxs-lookup"><span data-stu-id="04d2f-146">This applies only to video.This extension type is used to identify the aspect ratio of non-square pixels.</span></span> <span data-ttu-id="04d2f-147">Дополнительные сведения см. <a href="to-read-and-write-video-streams-with-non-square-pixels.md">в разделе чтение и запись видеопотоков с неквадратными пикселями</a>.</span><span class="sxs-lookup"><span data-stu-id="04d2f-147">For more information, see <a href="to-read-and-write-video-streams-with-non-square-pixels.md">To Read and Write Video Streams with Non-Square Pixels</a>.</span></span><br/> <span data-ttu-id="04d2f-148">Значения пропорций хранятся в виде слова, младший байт которого равен X, а старший байт — это значение Y.</span><span class="sxs-lookup"><span data-stu-id="04d2f-148">Aspect ratio values are stored as a word whose low byte is the X aspect and whose high byte is the Y aspect.</span></span> <span data-ttu-id="04d2f-149">Например, 16:9 хранится в виде 0x0910.</span><span class="sxs-lookup"><span data-stu-id="04d2f-149">For example, 16:9 is stored as 0x0910.</span></span><br/> <span data-ttu-id="04d2f-150">Размер этого срока всегда WM_SampleExtension_PixelAspectRatio_Size, что составляет 2 байта.</span><span class="sxs-lookup"><span data-stu-id="04d2f-150">The size for this DUE is always WM_SampleExtension_PixelAspectRatio_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04d2f-151">WM_SampleExtensionGUID_SampleDuration</span><span class="sxs-lookup"><span data-stu-id="04d2f-151">WM_SampleExtensionGUID_SampleDuration</span></span></td>
<td><span data-ttu-id="04d2f-152">Данные указывают длительность (в миллисекундах) образца, содержащегося в объекте buffer.</span><span class="sxs-lookup"><span data-stu-id="04d2f-152">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span> <span data-ttu-id="04d2f-153">При воспроизведении, если это так, объект модуля чтения будет использовать его для перезаписи существующего значения длительности выборки. Это СВЯЗАНО с тем, что компоненты времени выполнения пакета SDK устанавливаются автоматически в видеопотоках с частотой в 100 Кбит/с и выше, в которой издержки из-за этих данных не существенны.</span><span class="sxs-lookup"><span data-stu-id="04d2f-153">On playback, if this DUE is set the reader object will use it to overwrite the existing sample duration value.This DUE is set automatically by the SDK run-time components on video streams with bit rates of 100 kbps or greater, where the overhead of the DUE information is not significant.</span></span> <span data-ttu-id="04d2f-154">Он не задается для потоков с частотой битов в 100 Кбит/с.</span><span class="sxs-lookup"><span data-stu-id="04d2f-154">It is not set for streams with bit rates under 100 kbps.</span></span> <span data-ttu-id="04d2f-155">Приложения не должны устанавливать это по следующим причинам, так как модуль записи (в потоках с большим числом битов) перезапишет значение собственными данными.</span><span class="sxs-lookup"><span data-stu-id="04d2f-155">Applications should not set this DUE manually because the writer (on high-bit-rate streams) will overwrite the value with its own data.</span></span><br/> <span data-ttu-id="04d2f-156">Размер этого срока всегда WM_SampleExtension_SampleDuration_Size, что составляет 2 байта.</span><span class="sxs-lookup"><span data-stu-id="04d2f-156">The size for this DUE is always WM_SampleExtension_SampleDuration_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04d2f-157">WM_SampleExtensionGUID_ChromaLocation</span><span class="sxs-lookup"><span data-stu-id="04d2f-157">WM_SampleExtensionGUID_ChromaLocation</span></span></td>
<td><span data-ttu-id="04d2f-158">Данные указывают тип подвыборки чрома, используемый в видеоформате I420. Значение этого расширения задается одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="04d2f-158">The data indicates the type of chroma subsampling used in the I420 video format.The value of this extension is set to one of the follow values:</span></span><br/>
<ul>
<li><span data-ttu-id="04d2f-159">WM_CL_INTERLACED420</span><span class="sxs-lookup"><span data-stu-id="04d2f-159">WM_CL_INTERLACED420</span></span></li>
<li><span data-ttu-id="04d2f-160">WM_CL_PROGRESSIVE420</span><span class="sxs-lookup"><span data-stu-id="04d2f-160">WM_CL_PROGRESSIVE420</span></span></li>
</ul>
<span data-ttu-id="04d2f-161">Это расширение единицы данных не настроено в профиле.</span><span class="sxs-lookup"><span data-stu-id="04d2f-161">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="04d2f-162">Он включается в выходные данные выборки из декодера.</span><span class="sxs-lookup"><span data-stu-id="04d2f-162">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="04d2f-163">Размер такой оплаты всегда WM_SampleExtension_ChromaLocation_Size, что составляет 1 байт.</span><span class="sxs-lookup"><span data-stu-id="04d2f-163">The size of this DUE is always WM_SampleExtension_ChromaLocation_Size, which is 1 byte.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04d2f-164">WM_SampleExtensionGUID_ColorSpaceInfo</span><span class="sxs-lookup"><span data-stu-id="04d2f-164">WM_SampleExtensionGUID_ColorSpaceInfo</span></span></td>
<td><span data-ttu-id="04d2f-165">Данные содержат сведения о цветовом пространстве, используемом для текущего кадра видео. Значение этого расширения является структурой <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="04d2f-165">The data provides information about the color space used for the current video frame.The value of this extension is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> structure.</span></span><br/> <span data-ttu-id="04d2f-166">Это расширение единицы данных не настроено в профиле.</span><span class="sxs-lookup"><span data-stu-id="04d2f-166">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="04d2f-167">Он включается в выходные данные выборки из декодера.</span><span class="sxs-lookup"><span data-stu-id="04d2f-167">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="04d2f-168">Размер этого объекта всегда WM_SampleExtension_ColorSpaceInfo_Size, что составляет 3 байта.</span><span class="sxs-lookup"><span data-stu-id="04d2f-168">The size of this DUE is always WM_SampleExtension_ColorSpaceInfo_Size, which is 3 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04d2f-169">WM_SampleExtensionGUID_UserDataInfo</span><span class="sxs-lookup"><span data-stu-id="04d2f-169">WM_SampleExtensionGUID_UserDataInfo</span></span></td>
<td><span data-ttu-id="04d2f-170">Данные являются пользовательскими данными пользователя. Первые четыре байта данных содержат размер пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="04d2f-170">The data is custom user data.The first four bytes of the data contain the size of the custom data.</span></span><br/> <span data-ttu-id="04d2f-171">Следующий байт содержит тип пользовательских данных, предоставленных в примере расширения.</span><span class="sxs-lookup"><span data-stu-id="04d2f-171">The next byte contains the type of user data provided in the sample extension.</span></span> <span data-ttu-id="04d2f-172">Поддерживаются такие типы:</span><span class="sxs-lookup"><span data-stu-id="04d2f-172">The following types are supported:</span></span><br/>
<ul>
<li><span data-ttu-id="04d2f-173">0x1F — данные пользователя уровня последовательности</span><span class="sxs-lookup"><span data-stu-id="04d2f-173">0x1F - Sequence level user data</span></span></li>
<li><span data-ttu-id="04d2f-174">0x1E — данные пользователя на уровне входных точек</span><span class="sxs-lookup"><span data-stu-id="04d2f-174">0x1E - Entry-point level user data</span></span></li>
<li><span data-ttu-id="04d2f-175">0x1D-данные пользователя на уровне кадров</span><span class="sxs-lookup"><span data-stu-id="04d2f-175">0x1D - Frame level user data</span></span></li>
<li><span data-ttu-id="04d2f-176">данные пользователя уровня поля 0x1C</span><span class="sxs-lookup"><span data-stu-id="04d2f-176">0x1C - Field level user data</span></span></li>
<li><span data-ttu-id="04d2f-177">0x1B — данные пользователя уровня среза</span><span class="sxs-lookup"><span data-stu-id="04d2f-177">0x1B - Slice level user data</span></span></li>
</ul>
<span data-ttu-id="04d2f-178">Шестой и последующие байты содержат данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="04d2f-178">The sixth and subsequent bytes contain the user data.</span></span> <span data-ttu-id="04d2f-179">Число байтов данных пользователя, указанное в числе первых четырех байтов, равно количеству байт.</span><span class="sxs-lookup"><span data-stu-id="04d2f-179">There are as many bytes of user data as specified by the number in the first four bytes.</span></span><br/> <span data-ttu-id="04d2f-180">Это расширение единицы данных не настроено в профиле.</span><span class="sxs-lookup"><span data-stu-id="04d2f-180">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="04d2f-181">Он включается в образцы, выводимые из декодера.</span><span class="sxs-lookup"><span data-stu-id="04d2f-181">It is included in samples that are output from the decoder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04d2f-182">WM_SampleExtensionGUID_SampleProtectionSalt</span><span class="sxs-lookup"><span data-stu-id="04d2f-182">WM_SampleExtensionGUID_SampleProtectionSalt</span></span></td>
<td><span data-ttu-id="04d2f-183">Данные шифруются с помощью образца.</span><span class="sxs-lookup"><span data-stu-id="04d2f-183">The data is encrypted by sample.</span></span> <span data-ttu-id="04d2f-184">Этот пример типа расширения используется для содержимого, импортированного из формата файлов, отличного от ASF, и схемы защиты прав, отличной от Windows Media DRM. При импорте защищенного содержимого каждый пример должен включать уникальную соль.</span><span class="sxs-lookup"><span data-stu-id="04d2f-184">This sample extension type is used for content that is imported from a non-ASF file format and a rights protection scheme other than Windows Media DRM.When importing protected content, each sample must include a unique salt.</span></span> <span data-ttu-id="04d2f-185">Как правило, это значение является монотонно увеличивающимся счетчиком.</span><span class="sxs-lookup"><span data-stu-id="04d2f-185">Typically, this value is a monotonically increasing counter.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="04d2f-186">См. также</span><span class="sxs-lookup"><span data-stu-id="04d2f-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04d2f-187">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="04d2f-187">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 





