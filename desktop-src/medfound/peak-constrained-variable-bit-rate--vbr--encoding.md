---
description: 'В частоте переменной пиковой скорости (VBR) содержимое кодируется на заданную скорость и пиковые значения: Пиковая скорость потока и пиковое окно буфера.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Peak-Constrained кодирование переменной скорости
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711419"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a><span data-ttu-id="d02a2-103">Peak-Constrained кодирование переменной скорости</span><span class="sxs-lookup"><span data-stu-id="d02a2-103">Peak-Constrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="d02a2-104">В частоте переменной пиковой скорости (VBR) содержимое кодируется на заданную скорость и *пиковые значения*: Пиковая скорость потока и пиковое окно буфера.</span><span class="sxs-lookup"><span data-stu-id="d02a2-104">In the peak-constrained variable bit rate (VBR), the content is encoded to a specified bit rate and *peak values*: a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="d02a2-105">Эти пиковые значения также называются *значениями пиковой утечки*.</span><span class="sxs-lookup"><span data-stu-id="d02a2-105">These peak values are also called the *peak leaky bucket values*.</span></span> <span data-ttu-id="d02a2-106">Файл кодируется в соответствии с буфером, описанным в значениях пиковой нагрузки, так что общая средняя скорость потока равна указанному значению среднего значения скорости или меньше него.</span><span class="sxs-lookup"><span data-stu-id="d02a2-106">The file is encoded to conform to a buffer described by the peak values, such that the overall average bit rate of the stream is equal to or less than the average bit rate value you specified.</span></span>

<span data-ttu-id="d02a2-107">Как правило, Пиковая скорость очень высока.</span><span class="sxs-lookup"><span data-stu-id="d02a2-107">Typically, the peak bit rate is quite high.</span></span> <span data-ttu-id="d02a2-108">Кодировщик гарантирует, что указанное среднее значение скорости работы будет поддерживаться в течение потока (средняя скорость передачи >= (общий размер потока в битах/длительности потока в секундах)).</span><span class="sxs-lookup"><span data-stu-id="d02a2-108">The encoder ensures that the average bit rate value specified is maintained over the duration of the stream (average bit rate >= (total stream size in bits / stream duration in seconds)).</span></span> <span data-ttu-id="d02a2-109">Рассмотрим следующий пример: вы настраиваете поток с средним битом скорости в 16 000 бит/с, пиковой скоростью в 48 000 бит/с и пиковым окном буфера в 3 000 (3 секунды).</span><span class="sxs-lookup"><span data-stu-id="d02a2-109">Consider the following example: You configure a stream with an average bit rate of 16,000 bits per second, a peak bit rate of 48,000 bits per second, and a peak buffer window of 3,000 (3 seconds).</span></span> <span data-ttu-id="d02a2-110">Размер буфера, используемого для потока, составляет 144 000 бит (48 000 бит в секунду \* 3 секунды), определяемый значениями пиковой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d02a2-110">The size of the buffer used for the stream is 144,000 bits (48,000 bits per second \* 3 seconds) as determined by the peak values.</span></span> <span data-ttu-id="d02a2-111">Кодировщик сжимает данные, чтобы они соответствовали этому буферу.</span><span class="sxs-lookup"><span data-stu-id="d02a2-111">The encoder compresses the data to conform to that buffer.</span></span> <span data-ttu-id="d02a2-112">Кроме того, средняя скорость потока должна составлять 16 000 или меньше.</span><span class="sxs-lookup"><span data-stu-id="d02a2-112">Additionally, the average bit rate of the stream must be 16,000 or less.</span></span> <span data-ttu-id="d02a2-113">Если кодировщику необходимо создать крупные образцы для работы с сложным сегментом содержимого, можно воспользоваться большим размером буфера.</span><span class="sxs-lookup"><span data-stu-id="d02a2-113">If the encoder must create large samples to handle a complex segment of content, it can take advantage of the large buffer size.</span></span> <span data-ttu-id="d02a2-114">Однако другие части потока должны быть закодированы с более низкой скоростью, чтобы сократить среднее до указанного уровня.</span><span class="sxs-lookup"><span data-stu-id="d02a2-114">But other parts of the stream must be encoded at a lower bit rate to bring the average down to the specified level.</span></span> <span data-ttu-id="d02a2-115">Скорость кодирования с ограничением в пиковую пользу полезна для устройств воспроизведения с ограничением емкости буфера и ограничениями на скорость передачи данных.</span><span class="sxs-lookup"><span data-stu-id="d02a2-115">Peak-constrained VBR encoding is useful for playback devices with a finite buffer capacity and data rate constraints.</span></span> <span data-ttu-id="d02a2-116">Распространенный пример — это кодировка, используемая для DVD-дисков при декодировании с помощью микросхемы устройства, где существуют ограничения по оборудованию, которые необходимо учитывать.</span><span class="sxs-lookup"><span data-stu-id="d02a2-116">A common example of this is the encoding used for DVDs when decoding is performed by a chip in a device, where there are hardware limitations that must be considered.</span></span>

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a><span data-ttu-id="d02a2-117">Настройка кодировщика для Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="d02a2-117">Configuring the Encoder for Peak-Constrained VBR</span></span>

<span data-ttu-id="d02a2-118">Пиковая частота VBR похожа на " [неограниченное число VBR](unconstrained-variable-bit-rate--vbr--encoding.md) ", так как она ограничена средним битом скорости в течение потока.</span><span class="sxs-lookup"><span data-stu-id="d02a2-118">Peak-constrained VBR is like [unconstrained VBR](unconstrained-variable-bit-rate--vbr--encoding.md) in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="d02a2-119">Кроме того, Пиковая нагрузка соответствует пиковому буферу.</span><span class="sxs-lookup"><span data-stu-id="d02a2-119">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="d02a2-120">Этот буфер описывается с помощью пиковой скорости и пикового окна буфера.</span><span class="sxs-lookup"><span data-stu-id="d02a2-120">This buffer is described using a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="d02a2-121">В этом режиме используется два прохода кодирования и обеспечивается гибкость кодировщика при кодировании отдельных выборок с соблюдением пиковых ограничений.</span><span class="sxs-lookup"><span data-stu-id="d02a2-121">This mode uses two encoding passes and gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span>

<span data-ttu-id="d02a2-122">Конфигурация кодировщика задается с помощью значений свойств.</span><span class="sxs-lookup"><span data-stu-id="d02a2-122">Encoder configuration is set through property values.</span></span> <span data-ttu-id="d02a2-123">Эти свойства определены в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="d02a2-123">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="d02a2-124">Перед согласованием типа выходного носителя необходимо установить свойства конфигурации в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="d02a2-124">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="d02a2-125">Дополнительные сведения о настройке свойств кодировщика см. в разделе [Настройка кодировщика](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="d02a2-125">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="d02a2-126">На основе указанных значений свойств можно перечислить Поддерживаемые типы выходных данных VBR и выбрать требуемый тип на кодировщике [Media Foundation преобразование](media-foundation-transforms.md) (MFT) на основе средней скорости.</span><span class="sxs-lookup"><span data-stu-id="d02a2-126">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="d02a2-127">Для этого типа кодировки необходимо задать следующую пропертиесфор:</span><span class="sxs-lookup"><span data-stu-id="d02a2-127">You must set the following propertiesfor this type of encoding:</span></span>

-   <span data-ttu-id="d02a2-128">Укажите режим кодирования VBR, задав \_ для свойства мфпкэй вбренаблед значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="d02a2-128">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="d02a2-129">Присвойте параметру пассесусед МФПКЭЙ значение \_ 2, так как в режиме пиковой скорости используется два прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="d02a2-129">Set the MFPKEY\_PASSESUSED to 2 because peak-constrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="d02a2-130">Задайте МФПКЭЙ \_ рмакс, чтобы указать пиковую скорость, и установите мфпкэй \_ бмакс, чтобы указать пиковое окно буфера.</span><span class="sxs-lookup"><span data-stu-id="d02a2-130">Set MFPKEY\_RMAX to specify the peak bit rate and set MFPKEY\_BMAX to specify the peak buffer window.</span></span>
-   <span data-ttu-id="d02a2-131">При перечислении типа выходного носителя установите флажок [**\_ \_ \_ Среднее \_ число байт \_ в \_ секунду MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) (для звуковых потоков) или атрибут [**с \_ \_ средним \_ значением скорости MF MT**](mf-mt-avg-bitrate-attribute.md) (для видеопотоков) доступных типов выходных носителей и выберите тип выходного носителя с средней скоростью потока, ближайшей к требуемой средней скорости, которую должен поддерживать кодировщик в закодированном содержимом.</span><span class="sxs-lookup"><span data-stu-id="d02a2-131">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="d02a2-132">Дополнительные сведения о выборе типа выходного носителя см. в разделе [Согласование типа носителя в кодировщике](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="d02a2-132">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="d02a2-133">Рекомендуется установить пиковую скорость по крайней мере вдвое в два раза выше средней скорости.</span><span class="sxs-lookup"><span data-stu-id="d02a2-133">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="d02a2-134">Если задать для пиковой скорости более низкое значение, кодировщик может закодировать содержимое как CBR, а не Пиковое ограничение VBR.</span><span class="sxs-lookup"><span data-stu-id="d02a2-134">Setting the peak rate to a lower value may cause the encoder to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

<span data-ttu-id="d02a2-135">Чтобы получить значение окна буфера, заданное кодировщиком, вызовите **ивмкодеклеакибуккет:: жетбуфферсизебитс**, определенный в вмкодеЦифацес. h, вмкодекдспууид. lib, после сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="d02a2-135">To get the buffer window value set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h, wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="d02a2-136">Чтобы добавить поддержку неограниченных VBR для потоков, необходимо задать это значение в атрибуте [**MF \_ асфстреамконфиг \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (значения пиковой утечки) в объекте конфигурации потока при настройке профиля ASF.</span><span class="sxs-lookup"><span data-stu-id="d02a2-136">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) attribute (peak leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="d02a2-137">В следующем примере кода изменяется метод Сетенкодингтипе класса Sample Ценкодер для настройки режима с пиковым ограничением VBR.</span><span class="sxs-lookup"><span data-stu-id="d02a2-137">The following code sample modifies the SetEncodingType method of the sample class CEncoder to set up the peak-constrained VBR mode.</span></span> <span data-ttu-id="d02a2-138">Сведения об этом классе см. в разделе [пример кода кодировщика](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="d02a2-138">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="d02a2-139">Сведения о вспомогательных макросах, используемых в этом примере, см. в разделе Использование Media Foundation примеров кода.</span><span class="sxs-lookup"><span data-stu-id="d02a2-139">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="d02a2-140">См. также</span><span class="sxs-lookup"><span data-stu-id="d02a2-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d02a2-141">Типы кодирования ASF</span><span class="sxs-lookup"><span data-stu-id="d02a2-141">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="d02a2-142">Модель буфера для контейнера утечки</span><span class="sxs-lookup"><span data-stu-id="d02a2-142">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="d02a2-143">Создание топологии для Two-Pass кодирования Windows Media</span><span class="sxs-lookup"><span data-stu-id="d02a2-143">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



