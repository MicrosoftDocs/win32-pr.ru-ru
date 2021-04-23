---
description: Шаг 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Шаг 3A. Реализация метода Чеккинпуттипе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674177"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a><span data-ttu-id="cf8f7-104">Шаг 3A.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-104">Step 3A.</span></span> <span data-ttu-id="cf8f7-105">Реализация метода Чеккинпуттипе</span><span class="sxs-lookup"><span data-stu-id="cf8f7-105">Implement the CheckInputType Method</span></span>

<span data-ttu-id="cf8f7-106">Это шаг 3A из руководства по созданию [фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="cf8f7-106">This is step 3A of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="cf8f7-107">Метод [**ктрансформфилтер:: чеккинпуттипе**](ctransformfilter-checkinputtype.md) вызывается, когда вышестоящий фильтр предлагает тип мультимедиа для фильтра преобразования.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-107">The [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method is called when the upstream filter proposes a media type to the transform filter.</span></span> <span data-ttu-id="cf8f7-108">Этот метод принимает указатель на объект [**кмедиатипе**](cmediatype.md) , который является тонкой оболочкой для структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="cf8f7-108">This method takes a pointer to a [**CMediaType**](cmediatype.md) object, which is a thin wrapper for the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="cf8f7-109">В этом методе необходимо проверить каждое соответствующее поле структуры **\_ \_ типа мультимедиа AM** , включая поля в блоке форматирования.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-109">In this method, you should examine every relevant field of the **AM\_MEDIA\_TYPE** structure, including the fields in the format block.</span></span> <span data-ttu-id="cf8f7-110">Можно использовать методы доступа, определенные в **кмедиатипе**, или ссылаться на члены структуры напрямую.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-110">You can use the accessor methods defined in **CMediaType**, or reference the structure members directly.</span></span> <span data-ttu-id="cf8f7-111">Если какое-либо поле недопустимо, возвращается \_ тип VFW E \_ \_ не \_ принят.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-111">If any field is not valid, return VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span> <span data-ttu-id="cf8f7-112">Если весь тип мультимедиа является допустимым, возвращается значение S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-112">If the entire media type is valid, return S\_OK.</span></span>

<span data-ttu-id="cf8f7-113">Например, в фильтре кодировщика RLE тип входных данных должен быть 8-разрядным или 4-битовым несжатым видео RGB.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-113">For example, in the RLE encoder filter, the input type must be 8-bit or 4-bit uncompressed RGB video.</span></span> <span data-ttu-id="cf8f7-114">Нет причин поддерживать другие форматы ввода, например 16-или 24-разрядный RGB, так как фильтр должен преобразовать их в более низкую глубину, а в DirectShow уже есть фильтр [преобразователя цветового пространства](color-space-converter-filter.md) для этой цели.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-114">There is no reason to support other input formats, such as 16- or 24-bit RGB, because the filter would have to convert them to a lower bit depth, and DirectShow already provides a [Color Space Converter](color-space-converter-filter.md) filter for that purpose.</span></span> <span data-ttu-id="cf8f7-115">В следующем примере предполагается, что кодировщик поддерживает 8-разрядное видео, но не 4-разрядное видео:</span><span class="sxs-lookup"><span data-stu-id="cf8f7-115">The following example assumes that the encoder supports 8-bit video but not 4-bit video:</span></span>


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="cf8f7-116">В этом примере метод сначала проверяет основной тип и подтип.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-116">In this example, the method first checks the major type and subtype.</span></span> <span data-ttu-id="cf8f7-117">Затем проверяется тип формата, чтобы блок формата был [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) структурой.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-117">Then it checks the format type, to make sure the format block is a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="cf8f7-118">Фильтр также может поддерживать [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), но в этом случае нет никаких реальных преимуществ.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-118">The filter could also support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), but in this case there would be no real benefit.</span></span> <span data-ttu-id="cf8f7-119">Структура **VIDEOINFOHEADER2** добавляет поддержку чередования и неквадратных пикселей, которые, скорее всего, не будут важны в 8-разрядном видео.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-119">The **VIDEOINFOHEADER2** structure adds support for interlacing and non-square pixels, which are not likely to be relevant in 8-bit video.</span></span>

<span data-ttu-id="cf8f7-120">Если тип формата правильный, пример проверяет элементы **бибиткаунт** и **бикомпрессион** структуры **видеоинфохеадер** , чтобы убедиться в том, что формат имеет 8-битный несжатый RGB.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-120">If the format type is correct, the example checks the **biBitCount** and **biCompression** members of the **VIDEOINFOHEADER** structure, to verify that the format is 8-bit uncompressed RGB.</span></span> <span data-ttu-id="cf8f7-121">Как показано в этом примере, необходимо привести</span><span class="sxs-lookup"><span data-stu-id="cf8f7-121">As this example shows, you must coerce the</span></span>


```C++
pbFormat
```



<span data-ttu-id="cf8f7-122">Указатель на правильную структуру в зависимости от типа формата.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-122">pointer to the correct structure, based on the format type.</span></span> <span data-ttu-id="cf8f7-123">Перед приведением указателя всегда проверяйте тип GUID (**форматтипе**) и размер блока форматирования (**кбформат**).</span><span class="sxs-lookup"><span data-stu-id="cf8f7-123">Always check the format type GUID (**formattype**) and the size of the format block (**cbFormat**) before casting the pointer.</span></span>

<span data-ttu-id="cf8f7-124">В этом примере также проверяется, что число записей палитры совместимо с битовой глубиной, а блок формата достаточно велик для хранения записей палитры.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-124">The example also verifies that the number of palette entries is compatible with the bit depth and the format block is large enough to hold the palette entries.</span></span> <span data-ttu-id="cf8f7-125">Если все эти сведения верны, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-125">If all of this information is correct, the method returns S\_OK.</span></span>

<span data-ttu-id="cf8f7-126">Далее. [Шаг 3b. Реализация метода жетмедиатипе](step-3b--implement-the-getmediatype-method.md).</span><span class="sxs-lookup"><span data-stu-id="cf8f7-126">Next: [Step 3B. Implement the GetMediaType Method](step-3b--implement-the-getmediatype-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf8f7-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cf8f7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf8f7-128">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="cf8f7-128">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



