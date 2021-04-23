---
description: Quality-Based кодирование переменной скорости
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Quality-Based кодирование переменной скорости
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692585"
---
# <a name="quality-based-variable-bit-rate-encoding"></a><span data-ttu-id="a5102-103">Quality-Based кодирование переменной скорости</span><span class="sxs-lookup"><span data-stu-id="a5102-103">Quality-Based Variable Bit Rate Encoding</span></span>

<span data-ttu-id="a5102-104">В отличие от [кодирования с постоянной скоростью потока](constant-bit-rate-encoding.md) (CBR), когда кодировщик стремится поддерживать определенную скорость потока закодированного носителя, в режиме переменной скорости (VBR) кодировщик стремится достичь наилучшего возможного качества закодированного носителя.</span><span class="sxs-lookup"><span data-stu-id="a5102-104">Unlike [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR), where the encoder strives to maintain a particular bit rate of the encoded media, in the variable bit rate (VBR) mode, the encoder strives to achieve the best possible quality of the encoded media.</span></span> <span data-ttu-id="a5102-105">Основное различие между CBR и VBR — размер используемого окна буфера.</span><span class="sxs-lookup"><span data-stu-id="a5102-105">The primary difference between CBR and VBR is the size of the buffer window used.</span></span> <span data-ttu-id="a5102-106">Потоки с кодированием VBR обычно имеют большие окна буфера по сравнению с потоками, закодированными CBR.</span><span class="sxs-lookup"><span data-stu-id="a5102-106">VBR-encoded streams usually have large buffer windows compared to CBR-encoded streams.</span></span>

<span data-ttu-id="a5102-107">Качество закодированного содержимого определяется объемом данных, потерянных при сжатии содержимого.</span><span class="sxs-lookup"><span data-stu-id="a5102-107">The quality of encoded content is determined by the amount of data that is lost when the content is compressed.</span></span> <span data-ttu-id="a5102-108">На потери данных в процессе сжатия влияют многие факторы. но, как правило, чем сложнее исходные данные, тем выше степень сжатия, тем больше сведений теряется в процессе сжатия.</span><span class="sxs-lookup"><span data-stu-id="a5102-108">Many factors affect the loss of data in the compression process; but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="a5102-109">В режиме VBR на основе качества не следует определять скорость потока или окно буфера, которое должен выполнять кодировщик.</span><span class="sxs-lookup"><span data-stu-id="a5102-109">In quality-based VBR mode, you do not define a bit rate or a buffer window that the encoder must follow.</span></span> <span data-ttu-id="a5102-110">Вместо этого следует указать уровень качества для потока цифрового мультимедиа, а не скорость.</span><span class="sxs-lookup"><span data-stu-id="a5102-110">Instead, you specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="a5102-111">Кодировщик сжимает содержимое, чтобы все выборки были сравнимы по качеству. Это гарантирует, что качество будет согласовано на протяжении всего времени воспроизведения независимо от требований к буферу результирующего потока.</span><span class="sxs-lookup"><span data-stu-id="a5102-111">The encoder compresses the content so that all samples are of comparable quality; this ensures that quality is consistent throughout the playback duration, regardless of the buffer requirements of the resulting stream.</span></span>

<span data-ttu-id="a5102-112">Для кодирования VBR на основе качества обычно создаются большие сжатые потоки.</span><span class="sxs-lookup"><span data-stu-id="a5102-112">Quality-based VBR encoding tends to create large compressed streams.</span></span> <span data-ttu-id="a5102-113">Как правило, этот тип кодирования хорошо подходит для локального воспроизведения или для сетевых подключений с высокой пропускной способностью (или для загрузки и воспроизведения).</span><span class="sxs-lookup"><span data-stu-id="a5102-113">In general, this type of encoding is well suited for local playback or high bandwidth network connections (or download and play).</span></span> <span data-ttu-id="a5102-114">Например, можно написать приложение для копирования песен из компакт-диска в файлы ASF на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a5102-114">For example, you can write an application to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="a5102-115">Использование кодирования VBR на основе качества гарантирует, что все песни будут иметь одинаковое качество.</span><span class="sxs-lookup"><span data-stu-id="a5102-115">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span> <span data-ttu-id="a5102-116">В таких случаях последовательное качество обеспечит лучшую работу пользователей.</span><span class="sxs-lookup"><span data-stu-id="a5102-116">In those cases, the consistent quality will provide a better user experience.</span></span>

<span data-ttu-id="a5102-117">Недостатком кодирования VBR на основе качества является то, что на самом деле нет способа получить сведения о размере или пропускной способности закодированного носителя перед сеансом кодирования, так как кодировщик использует один проход кодирования.</span><span class="sxs-lookup"><span data-stu-id="a5102-117">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before the encoding session, because the encoder uses a single encoding pass.</span></span> <span data-ttu-id="a5102-118">Это может сделать файлы в кодировке с поддержкой VBR в случаях, когда ограничена память или пропускная способность, например воспроизведение содержимого на портативных проигрывателях мультимедиа или потоковая передача по сети с низкой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="a5102-118">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as playing content on portable media players or streaming over a low-bandwidth network.</span></span>

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a><span data-ttu-id="a5102-119">Настройка кодировщика для кодирования Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="a5102-119">Configuring the Encoder for Quality-Based VBR Encoding</span></span>

<span data-ttu-id="a5102-120">Конфигурация кодировщика задается с помощью значений свойств.</span><span class="sxs-lookup"><span data-stu-id="a5102-120">Encoder configuration is set through property values.</span></span> <span data-ttu-id="a5102-121">Эти свойства определены в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="a5102-121">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="a5102-122">Перед согласованием типа выходного носителя необходимо установить свойства конфигурации в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="a5102-122">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="a5102-123">Дополнительные сведения о настройке свойств кодировщика см. в разделе [Настройка кодировщика](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="a5102-123">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

<span data-ttu-id="a5102-124">В следующем списке перечислены свойства, которые необходимо задать для этого типа кодирования.</span><span class="sxs-lookup"><span data-stu-id="a5102-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="a5102-125">Укажите режим кодирования VBR, задав для свойства **мфпкэй \_ ВБРЕНАБЛЕД** значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="a5102-125">Specify the VBR encoding mode by setting the **MFPKEY\_VBRENABLED** property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="a5102-126">Присвойте параметру **\_ пассесусед мфпкэй** значение 1, так как в этом режиме используется один проход кодирования.</span><span class="sxs-lookup"><span data-stu-id="a5102-126">Set the **MFPKEY\_PASSESUSED** to 1 because this VBR mode uses one encoding pass.</span></span>
-   <span data-ttu-id="a5102-127">Задайте требуемый уровень качества (от 0 до 100), задав **мфпкэй \_ требуемое свойство \_ вбркуалити** .</span><span class="sxs-lookup"><span data-stu-id="a5102-127">Set the desired quality level (from 0 to 100) by setting the **MFPKEY\_DESIRED\_VBRQUALITY** property.</span></span> <span data-ttu-id="a5102-128">На основе качества VBR содержимое не кодируется в какие-либо предопределенные параметры буфера.</span><span class="sxs-lookup"><span data-stu-id="a5102-128">Quality-based VBR does not encode the content to any predefined buffer parameters.</span></span> <span data-ttu-id="a5102-129">Этот уровень качества, который будет поддерживаться для всего потока, независимо от требований к битовой скорости.</span><span class="sxs-lookup"><span data-stu-id="a5102-129">This quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>
-   <span data-ttu-id="a5102-130">Для видеопотоков задайте для параметра средняя скорость потока значение ненулевого значения в атрибуте с [**\_ \_ средним \_ значением скорости MF MT**](mf-mt-avg-bitrate-attribute.md) для типа выходного носителя кодировщика.</span><span class="sxs-lookup"><span data-stu-id="a5102-130">For video streams, set the average bit rate to a nonzero value in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the output media type of the encoder.</span></span> <span data-ttu-id="a5102-131">Точная скорость потока обновляется после завершения сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="a5102-131">The accurate bit rate is updated after the encoding session is complete.</span></span>

<span data-ttu-id="a5102-132">В следующем примере кода показана реализация для Сетенкодингпропертиес.</span><span class="sxs-lookup"><span data-stu-id="a5102-132">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="a5102-133">Эта функция задает свойства кодирования на уровне потока для CBR и VBR.</span><span class="sxs-lookup"><span data-stu-id="a5102-133">This function sets stream level encoding properties for CBR and VBR.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a5102-134">См. также</span><span class="sxs-lookup"><span data-stu-id="a5102-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5102-135">Типы кодирования ASF</span><span class="sxs-lookup"><span data-stu-id="a5102-135">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> </dl>

 

 



