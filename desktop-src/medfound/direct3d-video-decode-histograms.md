---
description: Эта статья содержит рекомендации по созданию гистограмм при декодировании видео с помощью API-интерфейсов Direct3D 11 или 12.
ms.assetid: ''
title: Гистограммы для расшифровки видео Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 6e25abd39ba95b669c2d76ced5f825ea80c4e3c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719266"
---
# <a name="direct3d-video-decode-histograms"></a><span data-ttu-id="e355e-103">Гистограммы для расшифровки видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="e355e-103">Direct3D video decode histograms</span></span>

<span data-ttu-id="e355e-104">Эта статья содержит рекомендации по созданию гистограмм при декодировании видео с помощью API-интерфейсов Direct3D 11 или 12.</span><span class="sxs-lookup"><span data-stu-id="e355e-104">This article contains guidance for generating histograms while decoding video using Direct3D 11 or 12 video APIs.</span></span>

## <a name="checking-the-video-device-for-histogram-capabilities"></a><span data-ttu-id="e355e-105">Проверка видеоустройства на наличие возможностей гистограммы</span><span class="sxs-lookup"><span data-stu-id="e355e-105">Checking the video device for histogram capabilities</span></span>

<span data-ttu-id="e355e-106">Перед созданием гистограмм необходимо проверить, поддерживает ли текущее видеоустройство функцию гистограммы для декодирования видео.</span><span class="sxs-lookup"><span data-stu-id="e355e-106">Before attempting to generated histograms, you must check to see if the current video device supports the video decode histogram feature.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="e355e-107">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e355e-107">Direct3D 12</span></span>

<span data-ttu-id="e355e-108">Вызовите [ID3D12VideoDevice:: чеккфеатуресуппорт](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , чтобы проверить сведения о поддержке для операций декодирования видео Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e355e-108">Call [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) to check for the support details for Direct3D 12 video decoding operations.</span></span> <span data-ttu-id="e355e-109">Передайте значение **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** из перечисления [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) , чтобы указать, что вы запрашиваете поддержку для гистограмм для расшифровки видео.</span><span class="sxs-lookup"><span data-stu-id="e355e-109">Pass the **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** value from the [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify that you are requesting support for video decode histograms.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="e355e-110">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e355e-110">Direct3D 11</span></span>

<span data-ttu-id="e355e-111">Вызовите [ID3D11VideoDevice2:: чеккфеатуресуппорт](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) и передайте значение **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) , чтобы определить, поддерживаются ли гистограммы для текущего устройства.</span><span class="sxs-lookup"><span data-stu-id="e355e-111">Call [ID3D11VideoDevice2::CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) and pass in the **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** value of the [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) to determine if histograms are supported for the current device.</span></span>

## <a name="enabling-histogram-during-decode"></a><span data-ttu-id="e355e-112">Включение гистограммы во время декодирования</span><span class="sxs-lookup"><span data-stu-id="e355e-112">Enabling histogram during decode</span></span>

<span data-ttu-id="e355e-113">Коллекция данных гистограммы включает вызывающий объект, предоставляющий буферы, в которых хранятся данные гистограммы.</span><span class="sxs-lookup"><span data-stu-id="e355e-113">The collection of histogram data is enabled by the caller providing the buffers in which the histogram data is stored.</span></span>  <span data-ttu-id="e355e-114">Пустой выходной буфер гистограммы для данного компонента указывает на то, что коллекция гистограмм отключена.</span><span class="sxs-lookup"><span data-stu-id="e355e-114">A null histogram output buffer for a given component indicates that histogram collection is disabled.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="e355e-115">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e355e-115">Direct3D 12</span></span>

<span data-ttu-id="e355e-116">Чтобы предоставить буферы вывода для получения данных гистограммы с помощью Direct3D 12, необходимо создать список команд декодирования с помощью метода [ID3D12VideoDecodeCommandList1::D ecodeframe1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) .</span><span class="sxs-lookup"><span data-stu-id="e355e-116">In order to provide output buffers to receive histogram data using Direct3D 12, you should create your decode command list using the [ID3D12VideoDecodeCommandList1::DecodeFrame1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) method.</span></span> <span data-ttu-id="e355e-117">Этот метод принимает в качестве аргумента структуру [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) .</span><span class="sxs-lookup"><span data-stu-id="e355e-117">This method takes a [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) structure as an argument.</span></span> <span data-ttu-id="e355e-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** имеет поле типа [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), которое позволяет указать [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) , в который выводятся данные гистограммы.</span><span class="sxs-lookup"><span data-stu-id="e355e-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** has a field of type [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), which allows you to specify an [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) into which histogram data is output.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="e355e-119">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e355e-119">Direct3D 11</span></span>

<span data-ttu-id="e355e-120">Интерфейс [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) предоставляет метод [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) , который позволяет предоставить один или несколько интерфейсов [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) , в которые будут выводиться данные гистограммы.</span><span class="sxs-lookup"><span data-stu-id="e355e-120">The [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) interface provides the [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) method, which allows you to provide one or more [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) interfaces into which the histogram data will be output.</span></span> <span data-ttu-id="e355e-121">[D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) для указания компонентов, для которых необходимо создавать данные гистограммы.</span><span class="sxs-lookup"><span data-stu-id="e355e-121">The [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) to specify the components for which you want histogram data to be generated.</span></span>


## <a name="buffer-format"></a><span data-ttu-id="e355e-122">Формат буфера</span><span class="sxs-lookup"><span data-stu-id="e355e-122">Buffer format</span></span>

<span data-ttu-id="e355e-123">Выходные данные гистограммы записываются в буфер в виде целочисленного счетчика на каждый компонент.</span><span class="sxs-lookup"><span data-stu-id="e355e-123">The decode histogram output is written to a buffer as an integer counter per component.</span></span>  <span data-ttu-id="e355e-124">Формат буфера — это 32-битное значение для каждой ячейки.</span><span class="sxs-lookup"><span data-stu-id="e355e-124">The buffer format is a 32-bit value per bin.</span></span>  <span data-ttu-id="e355e-125">Устройство может использовать битовую глубину целочисленного счетчика, размер которой меньше 32 бит, но должен иметь длину 16, 24 или 32 бит.</span><span class="sxs-lookup"><span data-stu-id="e355e-125">A device may use an integer counter bit depth that is smaller than 32 bits, but must be 16, 24, or 32 bits.</span></span>  <span data-ttu-id="e355e-126">Если да, значение счетчика сохраняется в младших битах, а верхние неиспользуемые биты равны нулю.</span><span class="sxs-lookup"><span data-stu-id="e355e-126">If so, the counter value is stored in the lower bits and the upper unused bits are zero.</span></span>  <span data-ttu-id="e355e-127">Когда количество для ячейки превысит максимальное значение, устройство задает вместо этого максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="e355e-127">When the count for a bin would exceed the max value, the device sets the max value instead.</span></span> <span data-ttu-id="e355e-128">Устройства сообщают о количестве поддерживаемых ячеек, которое должно быть степенью числа 2.</span><span class="sxs-lookup"><span data-stu-id="e355e-128">Devices report the number of bins supported, which must be a value that is a power of 2.</span></span>  <span data-ttu-id="e355e-129">Минимальное число ячеек, необходимых для устройств, поддерживающих эту функцию, — 64.</span><span class="sxs-lookup"><span data-stu-id="e355e-129">The minimum number of bins required for devices that support this feature is 64.</span></span> 

<span data-ttu-id="e355e-130">Необходимо предоставить буфер с согласованным смещением в 256 байт и размером, который является поддерживаемым числом ячеек, умноженным на размер ячейки (4 байта) для каждого запрошенного компонента.</span><span class="sxs-lookup"><span data-stu-id="e355e-130">You must supply a buffer with a 256-byte aligned offset and a size that is the supported number of bins multiplied by the bin size (4 bytes) for each component requested.</span></span>  <span data-ttu-id="e355e-131">Расположение ячейки определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e355e-131">Bin placement is determined by:</span></span>

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


<span data-ttu-id="e355e-132">Если формат определяет полезные биты компонента, меньший, чем число битов хранилища (например, P010 использует 10 верхних бит из 16 бит хранилища компонентов), учитываются только полезные биты (P010 обрабатывается как 10-разрядное значение).</span><span class="sxs-lookup"><span data-stu-id="e355e-132">When a format defines the useful bits of a component as less than the number of storage bits (for example, P010 uses the top 10 bits of 16 bits of component storage), only the useful bits are considered (P010 is treated as a 10 bit value).</span></span> 

<span data-ttu-id="e355e-133">Видеоустройство сообщает о том, какие компоненты поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e355e-133">The video device reports which components are supported.</span></span>  <span data-ttu-id="e355e-134">Если для вызывающего объекта не требуется гистограмма для данного компонента, они указывают nullptr.</span><span class="sxs-lookup"><span data-stu-id="e355e-134">If the caller does not want a histogram for a given component, they specify nullptr.</span></span>  <span data-ttu-id="e355e-135">Если драйвер не поддерживает гистограмму для данного компонента, то буфер гистограммы этого компонента должен быть nullptr.</span><span class="sxs-lookup"><span data-stu-id="e355e-135">If the driver does not support a histogram for a given component, that component's histogram buffer must be nullptr.</span></span>

<span data-ttu-id="e355e-136">Если поддерживается несколько компонентов, приложение может запросить любое сочетание компонентов для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="e355e-136">When multiple components are supported, the application may request any combination of components per frame decode.</span></span>  <span data-ttu-id="e355e-137">Например, если в отчетах об оборудовании поддерживаются компоненты Y, U и V, то приложение может запросить гистограмму Y только для одного кадра, гистограммы U — только для двух кадров, а гистограмма — только для кадра 3.</span><span class="sxs-lookup"><span data-stu-id="e355e-137">For example,if the hardware reports support for Y, U, and V components, the application may request the Y histogram only for frame one, the U histogram only for frame two, and the V histogram only for frame 3.</span></span>  <span data-ttu-id="e355e-138">Они также могут запросить любое сочетание двух компонентов или всех трех компонентов.</span><span class="sxs-lookup"><span data-stu-id="e355e-138">They may also request any combination of two components or all three components.</span></span>

<span data-ttu-id="e355e-139">Приложения предоставляют отдельные смещение и указатель буфера или обработчика для каждого запрошенного компонента.</span><span class="sxs-lookup"><span data-stu-id="e355e-139">Applications supply a separate offset and buffer pointer/handle for each component requested.</span></span>  <span data-ttu-id="e355e-140">Этот указатель может указывать на тот же ресурс, что и другой компонент или отдельный ресурс.</span><span class="sxs-lookup"><span data-stu-id="e355e-140">This pointer may point to the same resource as another component or a separate resource.</span></span>  <span data-ttu-id="e355e-141">Смещение позволяет разместить несколько компонентов в одном буфере, но выходная область, заданная смещением и размером гистограммы, не должна пересекаться с другими выходными данными компонента гистограммы.</span><span class="sxs-lookup"><span data-stu-id="e355e-141">The offset allows placing multiple components in the same buffer, but the output region specified by the offset and the histogram size must not overlap another histogram component output.</span></span>  <span data-ttu-id="e355e-142">Гистограмма также может быть записана в тот же буфер, что и другое несвязанное содержимое, например при использовании в стратегии подраспределений ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e355e-142">The histogram may also be written to the same buffer as other unrelated content such as when being used in a resource sub-allocation strategy.</span></span>


<span data-ttu-id="e355e-143">Среда выполнения D3D проверяет, что вызывающие объекты включают только гистограмму для поддерживаемых компонентов, смещенное смещение буфера и размер буфера достаточно для сообщаемого количества ячеек.</span><span class="sxs-lookup"><span data-stu-id="e355e-143">The D3D runtime validates that callers only enable histogram for supported components, that the buffer offset is aligned, and that buffer size is sufficient for the reported number of bins.</span></span>


## <a name="protected-content"></a><span data-ttu-id="e355e-144">Защищенное содержимое</span><span class="sxs-lookup"><span data-stu-id="e355e-144">Protected content</span></span>

<span data-ttu-id="e355e-145">Буферы гистограммы должны иметь ту же защиту поверхности, что и область вывода декодирования.</span><span class="sxs-lookup"><span data-stu-id="e355e-145">The Histogram buffers are required to have the same surface protection as the decode output surface.</span></span> <span data-ttu-id="e355e-146">Если поверхность вывода декодирования не является защищенным ресурсом, буфер гистограммы не должен быть защищенным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="e355e-146">If the decode output surface is not a protected resource, the histogram buffer must not be a protected resource.</span></span> <span data-ttu-id="e355e-147">Если область вывода декодирования является защищенным ресурсом, то гистограмма должна быть защищенным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="e355e-147">If the decode output surface is protected resource, the histogram must be a protected resource.</span></span>








## <a name="related-topics"></a><span data-ttu-id="e355e-148">См. также</span><span class="sxs-lookup"><span data-stu-id="e355e-148">Related topics</span></span>

<dl> <span data-ttu-id="e355e-149"><dt>
[API-интерфейсы](direct3d-12-video-apis.md) 
 видео Direct3D 12 [Media Foundationое программное руководством](media-foundation-programming-guide.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="e355e-149"><dt>
[Direct3D 12 Video APIs](direct3d-12-video-apis.md)
[Media Foundation Programming Guide](media-foundation-programming-guide.md)
</dt> </span></span></dl>

 

 




