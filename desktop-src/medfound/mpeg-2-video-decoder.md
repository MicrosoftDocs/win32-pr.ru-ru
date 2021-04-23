---
description: Видеодекодер MPEG-2 — это Media Foundation преобразование, которое декодирует видео MPEG-1 и MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Видеодекодер MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543895"
---
# <a name="mpeg-2-video-decoder"></a><span data-ttu-id="7c8bc-103">Видеодекодер MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7c8bc-103">MPEG-2 Video Decoder</span></span>

<span data-ttu-id="7c8bc-104">Видеодекодер MPEG-2 — это [Media Foundation преобразование](media-foundation-transforms.md) , которое ДЕКОДИРУЕТ видео MPEG-1 и MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-104">The MPEG-2 Video Decoder is a [Media Foundation transform](media-foundation-transforms.md) that decodes MPEG-1 and MPEG-2 video.</span></span> <span data-ttu-id="7c8bc-105">Декодер поддерживает простой и основной профиль MPEG-2 (H. 262, ISO/IEC 13818-2) и видео MPEG-1 (ISO/IEC 11172-2).</span><span class="sxs-lookup"><span data-stu-id="7c8bc-105">The decoder supports MPEG-2 Simple and Main profile video (H.262, ISO/IEC 13818-2) and MPEG-1 video (ISO/IEC 11172-2).</span></span>

## <a name="input-types"></a><span data-ttu-id="7c8bc-106">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="7c8bc-106">Input Types</span></span>

<span data-ttu-id="7c8bc-107">Декодер поддерживает следующие входные типы носителей.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-107">The decoder supports the following input media types.</span></span>

| <span data-ttu-id="7c8bc-108">attribute</span><span class="sxs-lookup"><span data-stu-id="7c8bc-108">Attribute</span></span>                                                 | <span data-ttu-id="7c8bc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7c8bc-109">Description</span></span>                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="7c8bc-110">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-110">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="7c8bc-111">**\_Видео мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-111">**MFMediaType\_Video**</span></span>                                                  |
| [<span data-ttu-id="7c8bc-112">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="7c8bc-113">**Мфвидеоформат \_ MPEG1**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-113">**MFVideoFormat\_MPEG1**</span></span><br/> <span data-ttu-id="7c8bc-114">**Мфвидеоформат \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-114">**MFVideoFormat\_MPEG2**</span></span><br/> |



 

## <a name="output-types"></a><span data-ttu-id="7c8bc-115">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="7c8bc-115">Output Types</span></span>

<span data-ttu-id="7c8bc-116">Декодер поддерживает следующие типы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-116">The decoder supports the following output types.</span></span>

| <span data-ttu-id="7c8bc-117">attribute</span><span class="sxs-lookup"><span data-stu-id="7c8bc-117">Attribute</span></span>                                                 | <span data-ttu-id="7c8bc-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7c8bc-118">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c8bc-119">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-119">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="7c8bc-120">**\_Видео мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-120">**MFMediaType\_Video**</span></span>                                                                                                                                                         |
| [<span data-ttu-id="7c8bc-121">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-121">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="7c8bc-122">**Мфвидеоформат \_ I420**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-122">**MFVideoFormat\_I420**</span></span><br/> <span data-ttu-id="7c8bc-123">**Мфвидеоформат \_ ийув**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-123">**MFVideoFormat\_IYUV**</span></span><br/> <span data-ttu-id="7c8bc-124">**Мфвидеоформат \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-124">**MFVideoFormat\_NV12**</span></span><br/> <span data-ttu-id="7c8bc-125">**Мфвидеоформат \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-125">**MFVideoFormat\_YUY2**</span></span><br/> <span data-ttu-id="7c8bc-126">**Мфвидеоформат \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-126">**MFVideoFormat\_YV12**</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c8bc-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c8bc-127">Remarks</span></span>

<span data-ttu-id="7c8bc-128">Видеодекодер MPEG-2 предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="7c8bc-128">The MPEG-2 video decoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="7c8bc-129">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-129">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="7c8bc-130">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-130">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="7c8bc-131">**имфкуалитядвисе**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-131">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="7c8bc-132">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-132">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="7c8bc-133">**имфратеконтрол**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-133">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="7c8bc-134">**имфратесуппорт**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-134">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="7c8bc-135">**имфреалтимеклиент**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-135">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="7c8bc-136">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-136">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="7c8bc-137">Входные данные для декодера должны представлять собой простейший поток.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-137">The input to the decoder must be an elementary stream.</span></span> <span data-ttu-id="7c8bc-138">Максимальное поддерживаемое разрешение — 1920 × 1088 пикселей.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-138">The maximum supported resolution is 1920 × 1088 pixels.</span></span>

<span data-ttu-id="7c8bc-139">Декодер поддерживает ускорение видео DirectX (ДКСВА) с помощью Microsoft Direct3D 9 или Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-139">The decoder supports DirectX Video Acceleration (DXVA) using either Microsoft Direct3D 9 or Microsoft Direct3D 11.</span></span>

### <a name="special-decoding-modes"></a><span data-ttu-id="7c8bc-140">Специальные режимы декодирования</span><span class="sxs-lookup"><span data-stu-id="7c8bc-140">Special Decoding Modes</span></span>

-   <span data-ttu-id="7c8bc-141">**Режим с низкой задержкой.**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-141">**Low latency mode.**</span></span> <span data-ttu-id="7c8bc-142">Этот режим подходит для таких сценариев, как обмен данными в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-142">This mode is appropriate for scenarios such as real-time communications.</span></span> <span data-ttu-id="7c8bc-143">Это сокращает задержку запуска, поэтому декодер создает первый выходной пример быстрее.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-143">It reduces start-up latency, so the decoder produces the first output sample sooner.</span></span> <span data-ttu-id="7c8bc-144">Однако в этом режиме в буфере декодера меньше выборок, что потенциально может привести к сбоям, поскольку декодер не декодирует столько кадров заранее.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-144">However, the decoder buffers fewer samples in this mode, which can potentially lead to glitches, because the decoder does not decode as many frames in advance.</span></span> <span data-ttu-id="7c8bc-145">Чтобы включить режим с низкой задержкой, установите атрибут [кодекапи \_ авловлатенцимоде](codecapi-avlowlatencymode.md) .</span><span class="sxs-lookup"><span data-stu-id="7c8bc-145">To enable low latency mode, set the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) attribute.</span></span>
-   <span data-ttu-id="7c8bc-146">**Нужна.**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-146">**Seeking.**</span></span> <span data-ttu-id="7c8bc-147">Для точного поиска вызовите метод [**имфтрансформ:: сетаутпутбаундс**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) .</span><span class="sxs-lookup"><span data-stu-id="7c8bc-147">For precise seeking, call the [**IMFTransform::SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) method.</span></span> <span data-ttu-id="7c8bc-148">При вызове этого метода декодер выводит только кадры, которые попадают в диапазон меток времени, заданный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-148">When this method is called, the decoder outputs only frames that fall within the range of time stamps specified by the caller.</span></span>
-   <span data-ttu-id="7c8bc-149">**Режим создания эскиза**.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-149">**Thumbnail generation mode**.</span></span> <span data-ttu-id="7c8bc-150">Этот режим предназначен для быстрого создания эскизов изображений.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-150">This mode is intended for quick generation of thumbnail images.</span></span> <span data-ttu-id="7c8bc-151">В этом режиме Декодер изначально декодировать только кадры I.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-151">In this mode, the decoder initially decodes only I frames.</span></span> <span data-ttu-id="7c8bc-152">Если в определенном числе кадров нет кадра I, декодер начинает декодировать кадры P и выводит кадры, не являющиеся кадрами, с фиксированным интервалом (по одному на *N* изображений) до тех пор, пока не будет достигнута рамка i.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-152">If no I frame is found within a certain number of frames, the decoder starts decoding P frames and outputs non–I frames at a fixed interval (one per *N* pictures) until an I frame is reached.</span></span> <span data-ttu-id="7c8bc-153">Чтобы включить режим формирования эскизов, задайте свойство [кодекапи \_ авдеквидеосумбнаилженератионмоде](../directshow/avdecvideothumbnailgenerationmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="7c8bc-153">To enable thumbnail generation mode, set the [CODECAPI\_AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) property.</span></span>
-   <span data-ttu-id="7c8bc-154">**Игра.**</span><span class="sxs-lookup"><span data-stu-id="7c8bc-154">**Trick play.**</span></span> <span data-ttu-id="7c8bc-155">Декодер может выполнять декодирование по тарифам быстрее, чем в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-155">The decoder can decode at rates faster than real time.</span></span> <span data-ttu-id="7c8bc-156">При более высоком темпе воспроизведения декодер переключается на декодирование только кадров, которые я использую.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-156">At higher playback rates, the decoder will switch to decoding only I frames.</span></span> <span data-ttu-id="7c8bc-157">В случае с обратным воспроизведением декодированы только кадры I.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-157">For reverse playback, only I frames are decoded.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="7c8bc-158">Свойства кодека</span><span class="sxs-lookup"><span data-stu-id="7c8bc-158">Codec Properties</span></span>

<span data-ttu-id="7c8bc-159">Декодер поддерживает следующие свойства с помощью метода [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="7c8bc-159">The decoder supports the following properties through the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span>



| <span data-ttu-id="7c8bc-160">Свойство</span><span class="sxs-lookup"><span data-stu-id="7c8bc-160">Property</span></span>                                                                                                      | <span data-ttu-id="7c8bc-161">Описание</span><span class="sxs-lookup"><span data-stu-id="7c8bc-161">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c8bc-162">КОДЕКАПИ \_ авдеквидеосумбнаилженератионмоде</span><span class="sxs-lookup"><span data-stu-id="7c8bc-162">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)               | <span data-ttu-id="7c8bc-163">Включает или отключает режим формирования эскизов.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-163">Enables or disables thumbnail generation mode.</span></span>                                                             |
| [<span data-ttu-id="7c8bc-164">КОДЕКАПИ \_ авдеквидеоакцелератион \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="7c8bc-164">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | <span data-ttu-id="7c8bc-165">Включает или отключает аппаратно ускоренное декодирование.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-165">Enables or disables hardware accelerated decoding.</span></span>                                                         |
| [<span data-ttu-id="7c8bc-166">КОДЕКАПИ \_ авловлатенцимоде</span><span class="sxs-lookup"><span data-stu-id="7c8bc-166">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="7c8bc-167">Включает или отключает режим низкой задержки.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-167">Enables or disables low-latency mode.</span></span>                                                                      |
| [<span data-ttu-id="7c8bc-168">\_декодер MFT \_ предоставляют \_ типы выходных данных \_ \_ в \_ собственном \_ порядке</span><span class="sxs-lookup"><span data-stu-id="7c8bc-168">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="7c8bc-169">Указывает, предоставляет ли декодер выходные типы, которые подходят для перекодирования перед другими форматами.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-169">Specifies whether the decoder exposes output types that are suitable for transcoding before other formats.</span></span> |



 

<span data-ttu-id="7c8bc-170">Из этих свойств можно также установить следующие параметры через интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) :</span><span class="sxs-lookup"><span data-stu-id="7c8bc-170">Of these properties, the following can also be set through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface:</span></span>

-   [<span data-ttu-id="7c8bc-171">КОДЕКАПИ \_ авдеквидеосумбнаилженератионмоде</span><span class="sxs-lookup"><span data-stu-id="7c8bc-171">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="7c8bc-172">КОДЕКАПИ \_ авдеквидеоакцелератион \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="7c8bc-172">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [<span data-ttu-id="7c8bc-173">КОДЕКАПИ \_ авловлатенцимоде</span><span class="sxs-lookup"><span data-stu-id="7c8bc-173">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

### <a name="limitations"></a><span data-ttu-id="7c8bc-174">Ограничения</span><span class="sxs-lookup"><span data-stu-id="7c8bc-174">Limitations</span></span>

-   <span data-ttu-id="7c8bc-175">Декодер не поддерживается на платформах на базе IA-64.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-175">The decoder is not supported on IA-64–based platforms.</span></span>
-   <span data-ttu-id="7c8bc-176">Декодер не поддерживает расшифровку CSS или воспроизведение зашифрованных DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="7c8bc-176">The decoder does not support CSS decryption or playback of encrypted DVDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c8bc-177">Требования</span><span class="sxs-lookup"><span data-stu-id="7c8bc-177">Requirements</span></span>



| <span data-ttu-id="7c8bc-178">Требование</span><span class="sxs-lookup"><span data-stu-id="7c8bc-178">Requirement</span></span> | <span data-ttu-id="7c8bc-179">Значение</span><span class="sxs-lookup"><span data-stu-id="7c8bc-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c8bc-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c8bc-180">Minimum supported client</span></span><br/> | <span data-ttu-id="7c8bc-181">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7c8bc-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7c8bc-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c8bc-182">Minimum supported server</span></span><br/> | <span data-ttu-id="7c8bc-183">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7c8bc-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7c8bc-184">DLL</span><span class="sxs-lookup"><span data-stu-id="7c8bc-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c8bc-185"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c8bc-185"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c8bc-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c8bc-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c8bc-187">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="7c8bc-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
