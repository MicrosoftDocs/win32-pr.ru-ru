---
description: Шаг 3C.
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: Шаг 3C. Реализация метода Чекктрансформ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78148701fc54e73a6970d45fde95d70f4cf0df3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272283"
---
# <a name="step-3c-implement-the-checktransform-method"></a><span data-ttu-id="28775-104">Шаг 3C.</span><span class="sxs-lookup"><span data-stu-id="28775-104">Step 3C.</span></span> <span data-ttu-id="28775-105">Реализация метода Чекктрансформ</span><span class="sxs-lookup"><span data-stu-id="28775-105">Implement the CheckTransform Method</span></span>

<span data-ttu-id="28775-106">Это шаг 3C из руководства по созданию [фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="28775-106">This is step 3C of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="28775-107">Этот шаг не является обязательным для фильтров, производных от **ктрансинплацефилтер**.</span><span class="sxs-lookup"><span data-stu-id="28775-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="28775-108">Метод [**ктрансформфилтер:: чекктрансформ**](ctransformfilter-checktransform.md) проверяет, совместим ли предложенный тип выходных данных с текущим типом входных данных.</span><span class="sxs-lookup"><span data-stu-id="28775-108">The [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method checks if a proposed output type is compatible with the current input type.</span></span> <span data-ttu-id="28775-109">Метод также вызывается, если входной ПИН-код переключается после подключения выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="28775-109">The method is also called if the input pin reconnects after the output pin connects.</span></span>

<span data-ttu-id="28775-110">В следующем примере проверяется, является ли формат RLE8 видео. размеры изображения соответствуют входному формату. и записи в палитре одинаковы.</span><span class="sxs-lookup"><span data-stu-id="28775-110">The following example verifies whether the format is RLE8 video; the image dimensions match the input format; and the palette entries are the same.</span></span> <span data-ttu-id="28775-111">Он также отклоняет исходный и целевой прямоугольники, которые не соответствуют размеру изображения.</span><span class="sxs-lookup"><span data-stu-id="28775-111">It also rejects source and target rectangles that do not match the image size.</span></span>


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="28775-112">**Переподключение ПИН-кода**</span><span class="sxs-lookup"><span data-stu-id="28775-112">**Pin Reconnections**</span></span>

<span data-ttu-id="28775-113">Приложения могут отключаться и повторно подключать ПИН-коды.</span><span class="sxs-lookup"><span data-stu-id="28775-113">Applications can disconnect and reconnect pins.</span></span> <span data-ttu-id="28775-114">Предположим, что приложение соединяет оба контакта, отсоединяет входной ПИН-код, а затем повторно подключает входной ПИН-код с помощью нового размера изображения.</span><span class="sxs-lookup"><span data-stu-id="28775-114">Suppose an application connects both pins, disconnects the input pin, and then reconnects the input pin using a new image size.</span></span> <span data-ttu-id="28775-115">В этом случае **чекктрансформ** завершается сбоем, так как измерения изображения больше не совпадают.</span><span class="sxs-lookup"><span data-stu-id="28775-115">In that case, **CheckTransform** fails because the dimensions of the image no longer match.</span></span> <span data-ttu-id="28775-116">Такое поведение имеет смысл, хотя фильтр может попытаться повторно подключить выходной ПИН-код к новому типу носителя.</span><span class="sxs-lookup"><span data-stu-id="28775-116">This behavior is reasonable, although the filter could also try reconnecting the output pin with a new media type.</span></span>

<span data-ttu-id="28775-117">Далее. [Шаг 4. Задайте свойства распределителя](step-4--set-allocator-properties.md).</span><span class="sxs-lookup"><span data-stu-id="28775-117">Next: [Step 4. Set Allocator Properties](step-4--set-allocator-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28775-118">См. также</span><span class="sxs-lookup"><span data-stu-id="28775-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28775-119">Повторное подключение ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="28775-119">Reconnecting Pins</span></span>](reconnecting-pins.md)
</dt> <dt>

[<span data-ttu-id="28775-120">Исходные и целевые прямоугольники в модулях подготовки видео</span><span class="sxs-lookup"><span data-stu-id="28775-120">Source and Target Rectangles in Video Renderers</span></span>](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[<span data-ttu-id="28775-121">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="28775-121">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



