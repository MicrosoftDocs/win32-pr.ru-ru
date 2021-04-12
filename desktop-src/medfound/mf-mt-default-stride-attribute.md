---
description: Шаг поверхности по умолчанию для несжатого видеоматериала. STRIDE — это число байтов, необходимое для перехода от одной строки пикселей к следующей.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: Атрибут MF_MT_DEFAULT_STRIDE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263621"
---
# <a name="mf_mt_default_stride-attribute"></a><span data-ttu-id="d44e1-104">MF \_ , \_ по умолчанию, \_ атрибут STRIDE</span><span class="sxs-lookup"><span data-stu-id="d44e1-104">MF\_MT\_DEFAULT\_STRIDE attribute</span></span>

<span data-ttu-id="d44e1-105">Шаг поверхности по умолчанию для несжатого видеоматериала.</span><span class="sxs-lookup"><span data-stu-id="d44e1-105">Default surface stride, for an uncompressed video media type.</span></span> <span data-ttu-id="d44e1-106">STRIDE — это число байтов, необходимое для перехода от одной строки пикселей к следующей.</span><span class="sxs-lookup"><span data-stu-id="d44e1-106">Stride is the number of bytes needed to go from one row of pixels to the next.</span></span>

## <a name="data-type"></a><span data-ttu-id="d44e1-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d44e1-107">Data type</span></span>

<span data-ttu-id="d44e1-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d44e1-108">**UINT32**</span></span>

<span data-ttu-id="d44e1-109">Рассматривать как значение **Int32** .</span><span class="sxs-lookup"><span data-stu-id="d44e1-109">Treat as a **INT32** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d44e1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d44e1-110">Remarks</span></span>

<span data-ttu-id="d44e1-111">Значение атрибута хранится как **UINT32**, но должно быть приведено к значению 32-разрядного целого числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="d44e1-111">The attribute value is stored as a **UINT32**, but should be cast to a 32-bit signed integer value.</span></span> <span data-ttu-id="d44e1-112">Шаг может быть отрицательным.</span><span class="sxs-lookup"><span data-stu-id="d44e1-112">Stride can be negative.</span></span>

<span data-ttu-id="d44e1-113">Шаг имеет положительный значение для нисходящих изображений и отрицательно для изображений в нижней части.</span><span class="sxs-lookup"><span data-stu-id="d44e1-113">Stride is positive for top-down images, and negative for bottom-up images.</span></span>

<span data-ttu-id="d44e1-114">Этот атрибут дает шаг для *непрерывного* представления изображения в памяти; то есть представление без дополнительных байтов заполнения после каждой строки.</span><span class="sxs-lookup"><span data-stu-id="d44e1-114">This attribute gives the stride for a *contiguous* representation of the image in memory; that is, a representation with no additional padding bytes after each row.</span></span> <span data-ttu-id="d44e1-115">Если буфер мультимедиа поддерживает интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , используйте метод [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) , чтобы получить фактический шаг в области, который может включать дополнительные байты заполнения.</span><span class="sxs-lookup"><span data-stu-id="d44e1-115">If a media buffer supports the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method to get the actual stride of the surface, which might include extra padding bytes.</span></span>

<span data-ttu-id="d44e1-116">Дополнительные сведения о параметре STRIDE для поверхности см. в разделе [Шаг с изображением](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="d44e1-116">For more information about surface stride, see [Image Stride](image-stride.md).</span></span>

<span data-ttu-id="d44e1-117">Пример вычисления шага по умолчанию см. в разделе [несжатые Видеобуферы](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="d44e1-117">For an example of how to calculate the default stride, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

<span data-ttu-id="d44e1-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="d44e1-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d44e1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d44e1-119">Requirements</span></span>



| <span data-ttu-id="d44e1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d44e1-120">Requirement</span></span> | <span data-ttu-id="d44e1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d44e1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d44e1-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d44e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d44e1-123">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="d44e1-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d44e1-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d44e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d44e1-125">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="d44e1-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d44e1-126">Header</span><span class="sxs-lookup"><span data-stu-id="d44e1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d44e1-127"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d44e1-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d44e1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d44e1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d44e1-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d44e1-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d44e1-130">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="d44e1-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d44e1-131">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d44e1-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d44e1-132">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d44e1-132">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d44e1-133">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d44e1-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="d44e1-134">Шаг изображения</span><span class="sxs-lookup"><span data-stu-id="d44e1-134">Image Stride</span></span>](image-stride.md)
</dt> </dl>

 

 




