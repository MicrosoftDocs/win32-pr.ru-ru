---
description: Кодирование постоянной скорости потока
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Кодирование постоянной скорости потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990839"
---
# <a name="constant-bit-rate-encoding"></a><span data-ttu-id="7c86d-103">Кодирование постоянной скорости потока</span><span class="sxs-lookup"><span data-stu-id="7c86d-103">Constant Bit Rate Encoding</span></span>

<span data-ttu-id="7c86d-104">При кодировании с постоянной скоростью (CBR) кодировщик знает скорость потока примеров выходного носителя и окно буфера (параметры утечки) перед началом сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="7c86d-104">In constant bit rate (CBR) encoding, the encoder knows the bit rate of the output media samples and the buffer window (leaky bucket parameters) before the encoding session begins.</span></span> <span data-ttu-id="7c86d-105">Кодировщик использует одинаковое количество битов для кодирования каждой секунды в течение файла, чтобы достичь целевой скорости потока.</span><span class="sxs-lookup"><span data-stu-id="7c86d-105">The encoder uses the same number of bits to encode each second of sample throughout the duration of the file to achieve the target bit rate for a stream.</span></span> <span data-ttu-id="7c86d-106">Это ограничивает изменение размера образцов потока.</span><span class="sxs-lookup"><span data-stu-id="7c86d-106">This limits the variation in the size of the stream samples.</span></span> <span data-ttu-id="7c86d-107">Кроме того, во время сеанса кодирования скорость потока не совпадает с заданным значением, но остается близкой к целевой скорости.</span><span class="sxs-lookup"><span data-stu-id="7c86d-107">Also, during the encoding session the bit rate is not exactly at the specified value but remains close to the target bit rate.</span></span>

<span data-ttu-id="7c86d-108">Кодирование CBR полезно, если вам нужно узнать битрейт или примерную длительность файла, не анализируя весь файл.</span><span class="sxs-lookup"><span data-stu-id="7c86d-108">CBR encoding is useful when you want to know the bit rate or approximate duration of a file without parsing the entire file.</span></span> <span data-ttu-id="7c86d-109">Это необходимо в сценариях потоковой передачи, когда содержимое мультимедиа должно передаваться с прогнозируемым битрейтом и постоянной пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="7c86d-109">This is required in live streaming scenarios where the media content needs to be streamed at a predictable bit rate and with consistent bandwidth usage.</span></span>

<span data-ttu-id="7c86d-110">Недостаток кодировки CBR заключается в том, что качество закодированного содержимого не будет постоянным.</span><span class="sxs-lookup"><span data-stu-id="7c86d-110">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="7c86d-111">Поскольку часть содержимого сложнее сжимать, части потока CBR будут иметь более низкую качество, чем другие.</span><span class="sxs-lookup"><span data-stu-id="7c86d-111">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="7c86d-112">Например, типичный фильм содержит несколько сцен, которые довольно статичны, и некоторые сцены, которые являются полными действиями.</span><span class="sxs-lookup"><span data-stu-id="7c86d-112">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="7c86d-113">При кодировании фильма с помощью CBR сцены, которые являются статическими и, следовательно, легко кодируются эффективно, будут иметь более высокое качество, чем сцены действий, для которых требуется более высокие размеры выборки, чтобы обеспечить одинаковое качество.</span><span class="sxs-lookup"><span data-stu-id="7c86d-113">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which would have required higher sample sizes to maintain the same quality.</span></span>

<span data-ttu-id="7c86d-114">Как правило, вариации в качестве файла CBR более производятся с более низкими скоростями.</span><span class="sxs-lookup"><span data-stu-id="7c86d-114">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="7c86d-115">При более высоких скоростях качество файла с CBR по-прежнему будет отличаться, но проблемы с качеством будут менее заметны для пользователя.</span><span class="sxs-lookup"><span data-stu-id="7c86d-115">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="7c86d-116">При использовании кодировки CBR следует задать высокую пропускную способность так, как это разрешено в сценарии доставки.</span><span class="sxs-lookup"><span data-stu-id="7c86d-116">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

-   [<span data-ttu-id="7c86d-117">Параметры конфигурации CBR</span><span class="sxs-lookup"><span data-stu-id="7c86d-117">CBR Configuration Settings</span></span>](#cbr-configuration-settings)
-   [<span data-ttu-id="7c86d-118">Параметры неутечек сегментов</span><span class="sxs-lookup"><span data-stu-id="7c86d-118">Leaky Bucket Settings</span></span>](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a><span data-ttu-id="7c86d-119">Параметры конфигурации CBR</span><span class="sxs-lookup"><span data-stu-id="7c86d-119">CBR Configuration Settings</span></span>

<span data-ttu-id="7c86d-120">Необходимо настроить кодировщик, указав тип кодировки и различные параметры конкретного потока перед сеансом кодирования.</span><span class="sxs-lookup"><span data-stu-id="7c86d-120">You must configure an encoder by specifying the type of encoding and the various stream specific settings before the encoding session.</span></span>

<span data-ttu-id="7c86d-121">**Настройка кодировщика для кодирования CBR**</span><span class="sxs-lookup"><span data-stu-id="7c86d-121">**To configure the encoder for CBR encoding**</span></span>

1.  <span data-ttu-id="7c86d-122">Укажите режим кодирования CBR.</span><span class="sxs-lookup"><span data-stu-id="7c86d-122">Specify the CBR encoding mode.</span></span>

    <span data-ttu-id="7c86d-123">По умолчанию кодировщик настроен на использование кодировки CBR.</span><span class="sxs-lookup"><span data-stu-id="7c86d-123">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="7c86d-124">Конфигурация кодировщика задается с помощью значений свойств.</span><span class="sxs-lookup"><span data-stu-id="7c86d-124">Encoder configuration is set through property values.</span></span> <span data-ttu-id="7c86d-125">Эти свойства определены в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="7c86d-125">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="7c86d-126">Этот режим можно задать явным образом, задав для свойства [**мфпкэй \_ ВБРЕНАБЛЕД**](mfpkey-vbrenabledproperty.md) значение Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="7c86d-126">You can explicitly specify this mode by setting the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to VARIANT\_FALSE.</span></span> <span data-ttu-id="7c86d-127">Дополнительные сведения о настройке свойств кодировщиков см. в разделе [Настройка кодировщика](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="7c86d-127">For information about how to set properties on encoders, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

2.  <span data-ttu-id="7c86d-128">Выберите скорость кодирования.</span><span class="sxs-lookup"><span data-stu-id="7c86d-128">Choose the encoding bit rate.</span></span>

    <span data-ttu-id="7c86d-129">Для кодировки CBR необходимо знание скорости потока, с которой необходимо кодировать поток перед началом сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="7c86d-129">For CBR encoding, you must know the bit rate at which you want to encode the stream before the encoding session begins.</span></span> <span data-ttu-id="7c86d-130">Скорость потока во время настройки кодировщика должна быть задана.</span><span class="sxs-lookup"><span data-stu-id="7c86d-130">You must set the bit rate during while you are configuring the encoder.</span></span> <span data-ttu-id="7c86d-131">Для этого во время согласования типа мультимедиа проверьте атрибут " [**\_ \_ \_ Среднее \_ число байт \_ в \_ секунду MF-MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) " (для звуковых потоков) или атрибут " [**\_ \_ Средняя \_ скорость" MF-MT**](mf-mt-avg-bitrate-attribute.md) (для видеопотоков) доступных типов выходных данных и выберите тип выходного носителя с средней скоростью, ближайшей к целевой скорости, которую вы хотите достичь.</span><span class="sxs-lookup"><span data-stu-id="7c86d-131">To do this, while you are performing media type negotiation, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the target bit rate you want to achieve.</span></span> <span data-ttu-id="7c86d-132">Дополнительные сведения см. [в разделе Согласование типа носителя в кодировщике](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="7c86d-132">For more information, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="7c86d-133">В следующем примере кода показана реализация для Сетенкодингпропертиес.</span><span class="sxs-lookup"><span data-stu-id="7c86d-133">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="7c86d-134">Эта функция задает свойства кодирования на уровне потока для CBR и VBR.</span><span class="sxs-lookup"><span data-stu-id="7c86d-134">This function sets stream level encoding properties for CBR and VBR.</span></span>


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a><span data-ttu-id="7c86d-135">Параметры неутечек сегментов</span><span class="sxs-lookup"><span data-stu-id="7c86d-135">Leaky Bucket Settings</span></span>

<span data-ttu-id="7c86d-136">Для кодировки CBR среднее и максимальное значения сегмента утечки для потока одинаковы.</span><span class="sxs-lookup"><span data-stu-id="7c86d-136">For CBR encoding, the average and the maximum leaky bucket values for the stream are the same.</span></span> <span data-ttu-id="7c86d-137">Дополнительные сведения об этих параметрах см. [в разделе Модель буфера для сегмента утечки](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="7c86d-137">For more information about these parameters, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="7c86d-138">Чтобы CBR звуковые потоки, необходимо задать значения сегментов утечки после согласования типа выходного носителя в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="7c86d-138">To CBR-encode audio streams, you need to set the leaky bucket values after negotiating the output media type on the encoder.</span></span> <span data-ttu-id="7c86d-139">Кодировщик вычисляет окно буфера внутренне на основе средней скорости, заданной для выходного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="7c86d-139">The encoder calculates the buffer window internally based on the average bit rate set on the output media type.</span></span>

<span data-ttu-id="7c86d-140">Чтобы задать значения сегментов с утечкой, создайте массив значений типа DWORD. в [**мфпкэй \_ асфстреамсинк \_ Исправлено свойство \_ леакибуккет**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) в хранилище свойств приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7c86d-140">To set leaky bucket values create an array of DWORDs can set the following values in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property in the media sink's property store.</span></span> <span data-ttu-id="7c86d-141">Дополнительные сведения см. [в разделе Установка свойств в приемнике файла](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="7c86d-141">For more information, see [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

-   <span data-ttu-id="7c86d-142">Средняя скорость потока: Возвращает среднюю скорость потока из типа выходного носителя, выбранного во время согласования типа носителя.</span><span class="sxs-lookup"><span data-stu-id="7c86d-142">Average bit rate: Get the average bit rate from the output media type that is selected during media type negotiation.</span></span> <span data-ttu-id="7c86d-143">Используйте атрибут [**" \_ \_ \_ Среднее \_ число байтов со \_ \_ звуком MF в секунду**](mf-mt-audio-avg-bytes-per-second-attribute.md) ".</span><span class="sxs-lookup"><span data-stu-id="7c86d-143">Use the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute.</span></span>
-   <span data-ttu-id="7c86d-144">Окно буфера. запросите кодировщик для интерфейса [**ивмкодеклеакибуккет**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) , а затем вызовите [**Ивмкодеклеакибуккет:: жетбуфферсизебитс**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (вмкодеЦифацес. h, вмкодекдспууид. lib).</span><span class="sxs-lookup"><span data-stu-id="7c86d-144">Buffer window: Query the encoder for the [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) interface and then call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib).</span></span>
-   <span data-ttu-id="7c86d-145">Начальный размер буфера: значение 0.</span><span class="sxs-lookup"><span data-stu-id="7c86d-145">Initial buffer size: Set to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c86d-146">См. также</span><span class="sxs-lookup"><span data-stu-id="7c86d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c86d-147">Типы кодирования ASF</span><span class="sxs-lookup"><span data-stu-id="7c86d-147">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="7c86d-148">Учебник. 1. Передача кодирования мультимедиа Windows</span><span class="sxs-lookup"><span data-stu-id="7c86d-148">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="7c86d-149">Руководство. запись файла WMA с помощью CBR Encoding</span><span class="sxs-lookup"><span data-stu-id="7c86d-149">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
