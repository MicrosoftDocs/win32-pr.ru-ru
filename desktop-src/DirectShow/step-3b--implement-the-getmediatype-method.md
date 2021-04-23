---
description: Шаг 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Шаг 3B. Реализация метода Жетмедиатипе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547359"
---
# <a name="step-3b-implement-the-getmediatype-method"></a><span data-ttu-id="d01e6-104">Шаг 3B.</span><span class="sxs-lookup"><span data-stu-id="d01e6-104">Step 3B.</span></span> <span data-ttu-id="d01e6-105">Реализация метода Жетмедиатипе</span><span class="sxs-lookup"><span data-stu-id="d01e6-105">Implement the GetMediaType Method</span></span>

<span data-ttu-id="d01e6-106">Это шаг 3B из руководства [Создание фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d01e6-106">This is step 3B of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="d01e6-107">Этот шаг не является обязательным для фильтров, производных от **ктрансинплацефилтер**.</span><span class="sxs-lookup"><span data-stu-id="d01e6-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="d01e6-108">Метод [**ктрансформфилтер:: жетмедиатипе**](ctransformfilter-getmediatype.md) возвращает один из предпочтительных выходных типов фильтра, на который ссылается номер индекса.</span><span class="sxs-lookup"><span data-stu-id="d01e6-108">The [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method returns one of the filter's preferred output types, referenced by index number.</span></span> <span data-ttu-id="d01e6-109">Этот метод никогда не вызывается, если входной ПИН-код фильтра уже не подключен.</span><span class="sxs-lookup"><span data-stu-id="d01e6-109">This method is never called unless the filter's input pin is already connected.</span></span> <span data-ttu-id="d01e6-110">Таким образом, можно использовать тип мультимедиа из вышестоящего соединения, чтобы определить предпочтительные типы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d01e6-110">Therefore, you can use the media type from the upstream connection to determine the preferred output types.</span></span>

<span data-ttu-id="d01e6-111">Кодировщик обычно предлагает один предпочтительный тип, представляющий целевой формат.</span><span class="sxs-lookup"><span data-stu-id="d01e6-111">An encoder typically offers a single preferred type, representing the target format.</span></span> <span data-ttu-id="d01e6-112">Декодеры обычно поддерживают ряд выходных форматов и предлагают их в порядке убывания качества или эффективности.</span><span class="sxs-lookup"><span data-stu-id="d01e6-112">Decoders generally support a range of output formats, and offer them in order of descending quality or efficiency.</span></span> <span data-ttu-id="d01e6-113">Например, в этом порядке список может быть UYVY, Y211, RGB-24, RGB-565, RGB-555 и RGB-8.</span><span class="sxs-lookup"><span data-stu-id="d01e6-113">For example, the list might be UYVY, Y211, RGB-24, RGB-565, RGB-555, and RGB-8, in that order.</span></span> <span data-ttu-id="d01e6-114">Фильтры эффектов могут потребовать точного соответствия между выходным форматом и форматом входных данных.</span><span class="sxs-lookup"><span data-stu-id="d01e6-114">Effect filters may require an exact match between the output format and the input format.</span></span>

<span data-ttu-id="d01e6-115">В следующем примере возвращается один выходной тип, который создается путем изменения типа входных данных для указания сжатия RLE8:</span><span class="sxs-lookup"><span data-stu-id="d01e6-115">The following example returns a single output type, which is constructed by modifying the input type to specify RLE8 compression:</span></span>


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



<span data-ttu-id="d01e6-116">В этом примере метод вызывает [**Ипин:: коннектионмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) , чтобы получить входной тип из входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d01e6-116">In this example, the method calls [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) to get the input type from the input pin.</span></span> <span data-ttu-id="d01e6-117">Затем он изменяет некоторые поля, чтобы указать формат сжатия следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d01e6-117">Then it changes some of the fields to indicate the compression format, as follows:</span></span>

-   <span data-ttu-id="d01e6-118">Он назначает новый идентификатор GUID подтипа, созданный из кода FOURCC "МРЛЕ", с помощью класса [**фаурккмап**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="d01e6-118">It assigns a new subtype GUID, which is constructed from the FOURCC code 'MRLE', using the [**FOURCCMap**](fourccmap.md) class.</span></span>
-   <span data-ttu-id="d01e6-119">Он вызывает метод [**кмедиатипе:: сетвариаблесизе**](cmediatype-setvariablesize.md) , который устанавливает для флага **бфикседсизесамплес** **значение false** , а элемент **лсамплесизе** — равным нулю, указывая выборки размера переменной.</span><span class="sxs-lookup"><span data-stu-id="d01e6-119">It calls the [**CMediaType::SetVariableSize**](cmediatype-setvariablesize.md) method, which sets the **bFixedSizeSamples** flag to **FALSE** and the **lSampleSize** member to zero, indicating variable-sized samples.</span></span>
-   <span data-ttu-id="d01e6-120">Он вызывает метод [**кмедиатипе:: сеттемпоралкомпрессион**](cmediatype-settemporalcompression.md) со значением **false**, указывающим, что каждый кадр является ключевым кадром.</span><span class="sxs-lookup"><span data-stu-id="d01e6-120">It calls the [**CMediaType::SetTemporalCompression**](cmediatype-settemporalcompression.md) method with the value **FALSE**, indicating that every frame is a key frame.</span></span> <span data-ttu-id="d01e6-121">(Это поле доступно только для информационных целей, поэтому его можно спокойно проигнорировать.)</span><span class="sxs-lookup"><span data-stu-id="d01e6-121">(This field is informational only, so you could safely ignore it.)</span></span>
-   <span data-ttu-id="d01e6-122">Он устанавливает для поля **бикомпрессион** значение BI \_ RLE8.</span><span class="sxs-lookup"><span data-stu-id="d01e6-122">It sets the **biCompression** field to BI\_RLE8.</span></span>
-   <span data-ttu-id="d01e6-123">Он задает для поля **бисизеимаже** размер изображения.</span><span class="sxs-lookup"><span data-stu-id="d01e6-123">It sets the **biSizeImage** field to the image size.</span></span>

<span data-ttu-id="d01e6-124">Далее. [шаг 3c. Реализация метода чекктрансформ](step-3c--implement-the-checktransform-method.md).</span><span class="sxs-lookup"><span data-stu-id="d01e6-124">Next: [Step 3C. Implement the CheckTransform Method](step-3c--implement-the-checktransform-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d01e6-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d01e6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d01e6-126">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="d01e6-126">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



