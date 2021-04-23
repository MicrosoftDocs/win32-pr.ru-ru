---
description: Кодирование переменной скорости с неограниченным битом
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: Кодирование переменной скорости с неограниченным битом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692772"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a><span data-ttu-id="0ce37-103">Кодирование переменной скорости с неограниченным битом</span><span class="sxs-lookup"><span data-stu-id="0ce37-103">Unconstrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="0ce37-104">В режиме кодирования с переменной скоростью без ограничений (VBR) содержимое кодируется на максимально возможное качество, сохраняя при этом указанную скорость.</span><span class="sxs-lookup"><span data-stu-id="0ce37-104">In unconstrained variable bit rate (VBR) encoding mode, the content is encoded to the highest possible quality while maintaining a specified bit rate.</span></span>

<span data-ttu-id="0ce37-105">Для кодирования с неограниченной VBR используется два прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="0ce37-105">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="0ce37-106">При использовании кодирования с неограниченным числом VBR необходимо указать скорость потока, как в случае с [постоянной кодировкой битовой скорости](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="0ce37-106">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="0ce37-107">Однако кодировщик использует это значение только в качестве средней скорости потока и кодирует, чтобы качество по мере возможности максимально велико при сохранении среднего значения.</span><span class="sxs-lookup"><span data-stu-id="0ce37-107">However, the encoder uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="0ce37-108">Отдельные выборки, созданные кодировщиком, зависят от размера без явных ограничений буфера.</span><span class="sxs-lookup"><span data-stu-id="0ce37-108">Individual samples produced by the encoder varies in size without any explicit buffer limits.</span></span> <span data-ttu-id="0ce37-109">Однако средняя скорость потока в течение сеанса кодирования и длительность потоковой передачи не должны превышать значение, указанное вами.</span><span class="sxs-lookup"><span data-stu-id="0ce37-109">However, the average bit rate during the encoding session and the duration of the stream must be no more than the value specified by you.</span></span> <span data-ttu-id="0ce37-110">Реальная скорость потока в любой момент в закодированном потоке может сильно отличаться от среднего значения.</span><span class="sxs-lookup"><span data-stu-id="0ce37-110">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span> <span data-ttu-id="0ce37-111">Не задается окно буфера для кодирования с неограниченными VBR.</span><span class="sxs-lookup"><span data-stu-id="0ce37-111">You do not set a buffer window for unconstrained VBR encoding.</span></span> <span data-ttu-id="0ce37-112">Вместо этого кодировщик вычислит размер требуемого окна буфера на основе требований закодированных образцов.</span><span class="sxs-lookup"><span data-stu-id="0ce37-112">Instead, the encoder computes the size of the required buffer window based on the requirements of the encoded samples.</span></span> <span data-ttu-id="0ce37-113">Это означает, что ограничение размера отдельных выборок в потоке не ограничено, если средняя скорость потока меньше или равна заданному значению.</span><span class="sxs-lookup"><span data-stu-id="0ce37-113">This means that there is no limit to the size of individual samples in the stream, as long as the average bit rate is less than or equal to the value you set.</span></span>

<span data-ttu-id="0ce37-114">Преимуществом кодирования с неограниченным числом VBR является то, что сжатый поток имеет наивысшее возможное качество, сохраняя при этом прогнозируемую среднюю пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="0ce37-114">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span> <span data-ttu-id="0ce37-115">Используйте этот параметр, если необходимо указать пропускную способность, но колебания, окружающие указанную пропускную способность, приемлемы. Например, для локальных файлов или только для загрузки.</span><span class="sxs-lookup"><span data-stu-id="0ce37-115">Use this when you need to specify a bandwidth but fluctuations around the specified bandwidth are acceptable; for example, for local files or downloading only.</span></span>

<span data-ttu-id="0ce37-116">Недостаток этого режима кодирования заключается в том, что кодировщик может установить окно буфера в любое значение, необходимое после кодирования, что дает вам контроль над размером буфера.</span><span class="sxs-lookup"><span data-stu-id="0ce37-116">The disadvantage of this mode of encoding is that the encoder can set the buffer window to whatever value is required after encoding, giving you no control over the buffer size.</span></span> <span data-ttu-id="0ce37-117">В большинстве случаев, если нет опасений относительно размера буфера или согласованности использования пропускной способности, следует использовать [кодирование с переменной скоростью с переменным качеством](quality-based-variable-bit-rate--vbr--encoding.md) .</span><span class="sxs-lookup"><span data-stu-id="0ce37-117">In most cases, if you are not concerned about the size of the buffer or the consistency of bandwidth usage, you should use [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md)</span></span>

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a><span data-ttu-id="0ce37-118">Настройка кодировщика для неограниченных VBR</span><span class="sxs-lookup"><span data-stu-id="0ce37-118">Configuring the Encoder for Unconstrained VBR</span></span>

<span data-ttu-id="0ce37-119">Конфигурация кодировщика задается с помощью значений свойств.</span><span class="sxs-lookup"><span data-stu-id="0ce37-119">Encoder configuration is set through property values.</span></span> <span data-ttu-id="0ce37-120">Эти свойства определены в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="0ce37-120">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="0ce37-121">Перед согласованием типа выходного носителя необходимо установить свойства конфигурации в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="0ce37-121">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="0ce37-122">Дополнительные сведения о настройке свойств кодировщика см. в разделе [Настройка кодировщика](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="0ce37-122">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="0ce37-123">На основе указанных значений свойств можно перечислить Поддерживаемые типы выходных данных VBR и выбрать требуемый тип на кодировщике [Media Foundation преобразование](media-foundation-transforms.md) (MFT) на основе средней скорости.</span><span class="sxs-lookup"><span data-stu-id="0ce37-123">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation Transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="0ce37-124">В следующем списке перечислены свойства, которые необходимо задать для этого типа кодирования.</span><span class="sxs-lookup"><span data-stu-id="0ce37-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="0ce37-125">Укажите режим кодирования VBR, задав \_ для свойства мфпкэй вбренаблед значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="0ce37-125">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="0ce37-126">Присвойте параметру пассесусед МФПКЭЙ значение \_ 2, так как в режиме неограниченных VBR используется два прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="0ce37-126">Set the MFPKEY\_PASSESUSED to 2 because unconstrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="0ce37-127">При перечислении типа выходного носителя проверьте атрибут [**" \_ \_ \_ Среднее \_ число байт \_ в \_ секунду MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) " (для звуковых потоков) или атрибут с [**\_ \_ средним \_ скоростью MF MT**](mf-mt-avg-bitrate-attribute.md) (для видеопотоков) доступных типов выходного носителя.</span><span class="sxs-lookup"><span data-stu-id="0ce37-127">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types.</span></span> <span data-ttu-id="0ce37-128">Выберите тип выходного носителя с средней скоростью, ближайшей к требуемой средней скорости, которую должен поддерживать кодировщик в закодированном содержимом.</span><span class="sxs-lookup"><span data-stu-id="0ce37-128">Choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="0ce37-129">Дополнительные сведения о выборе типа выходного носителя см. в разделе [Согласование типа носителя в кодировщике](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="0ce37-129">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="0ce37-130">Чтобы получить значение окна буфера, заданное кодировщиком, вызовите **ивмкодеклеакибуккет:: жетбуфферсизебитс**, определенный в вмкодеЦифацес. h и вмкодекдспууид. lib, после сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="0ce37-130">To get the buffer window value is set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h and wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="0ce37-131">Чтобы добавить поддержку неограниченных VBR для потоков, необходимо задать это значение в атрибуте [**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (среднее значение сегмента утечки) в объекте конфигурации потока при настройке профиля ASF.</span><span class="sxs-lookup"><span data-stu-id="0ce37-131">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute (average leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="0ce37-132">В следующем примере метод Сетенкодингтипе класса Sample Ценкодер изменяется для настройки режима с неограниченным числом VBR.</span><span class="sxs-lookup"><span data-stu-id="0ce37-132">The following modifies the SetEncodingType method of the sample class CEncoder to set up the unconstrained VBR mode.</span></span> <span data-ttu-id="0ce37-133">Сведения об этом классе см. в разделе [пример кода кодировщика](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="0ce37-133">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="0ce37-134">Сведения о вспомогательных макросах, используемых в этом примере, см. в разделе Использование Media Foundation примеров кода.</span><span class="sxs-lookup"><span data-stu-id="0ce37-134">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
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

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="0ce37-135">См. также</span><span class="sxs-lookup"><span data-stu-id="0ce37-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ce37-136">Типы кодирования ASF</span><span class="sxs-lookup"><span data-stu-id="0ce37-136">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="0ce37-137">Модель буфера для контейнера утечки</span><span class="sxs-lookup"><span data-stu-id="0ce37-137">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="0ce37-138">Создание топологии для Two-Pass кодирования Windows Media</span><span class="sxs-lookup"><span data-stu-id="0ce37-138">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



