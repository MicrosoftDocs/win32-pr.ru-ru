---
description: Определяет геометрическое апертуру для типа видеоклипа.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: Атрибут MF_MT_GEOMETRIC_APERTURE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991473"
---
# <a name="mf_mt_geometric_aperture-attribute"></a><span data-ttu-id="607d4-103">\_ \_ Атрибут геометрического \_ Апертура MF</span><span class="sxs-lookup"><span data-stu-id="607d4-103">MF\_MT\_GEOMETRIC\_APERTURE attribute</span></span>

<span data-ttu-id="607d4-104">Определяет геометрическое апертуру для типа видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="607d4-104">Defines the geometric aperture for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="607d4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="607d4-105">Data type</span></span>

<span data-ttu-id="607d4-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="607d4-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="607d4-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="607d4-107">Remarks</span></span>

<span data-ttu-id="607d4-108">Значением этого атрибута является структура [**мфвидеоареа**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="607d4-108">The value of this attribute is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="607d4-109">Пропорции изображения рассчитываются относительно геометрического апертуры с использованием следующей формулы: пропорции рисунка = (геометрическое значение ширины и геометрического апертуры) x пиксельных пропорций.</span><span class="sxs-lookup"><span data-stu-id="607d4-109">The picture aspect ratio is calculated relative to the geometric aperture, using the following formula: Picture aspect ratio = (geometric aperture width / geometric aperture height) × pixel aspect ratio.</span></span>

<span data-ttu-id="607d4-110">Если этот атрибут не задан, то геометрический апертурой считается весь кадр видео.</span><span class="sxs-lookup"><span data-stu-id="607d4-110">If this attribute is not set, the geometric aperture is assumed to be the entire video frame.</span></span> <span data-ttu-id="607d4-111">Этот атрибут следует задавать только в том случае, если тип носителя описывает стандарт видео с определенной активной областью.</span><span class="sxs-lookup"><span data-stu-id="607d4-111">You should set this attribute only when the media type describes a video standard with a defined active area.</span></span>

<span data-ttu-id="607d4-112">Например, в NTSC-телевидении видеокадр равен 720 × 480 с активной областью 704 x 480 и соотношением пропорций 10:11 в пикселях.</span><span class="sxs-lookup"><span data-stu-id="607d4-112">For example, in NTSC television the video frame is 720 × 480 with an active area of 704 × 480 and a 10:11 pixel aspect ratio.</span></span> <span data-ttu-id="607d4-113">Полученное изображение имеет пропорции (704/480) × (10/11) = 4:3.</span><span class="sxs-lookup"><span data-stu-id="607d4-113">The resulting picture has an aspect ratio of (704/480) × (10/11) = 4:3.</span></span>

> [!Note]  
> <span data-ttu-id="607d4-114">В средстве визуализации по умолчанию для [расширенного обработчика видео](enhanced-video-renderer.md) (Евр) отображается геометрическое Апертура видео, если оно указано.</span><span class="sxs-lookup"><span data-stu-id="607d4-114">The default presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) shows the geometric aperture of the video, if specified.</span></span>

 

<span data-ttu-id="607d4-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="607d4-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="607d4-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="607d4-116">Examples</span></span>


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a><span data-ttu-id="607d4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="607d4-117">Requirements</span></span>



| <span data-ttu-id="607d4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="607d4-118">Requirement</span></span> | <span data-ttu-id="607d4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="607d4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="607d4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="607d4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="607d4-121">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="607d4-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="607d4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="607d4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="607d4-123">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="607d4-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="607d4-124">Header</span><span class="sxs-lookup"><span data-stu-id="607d4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="607d4-125"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="607d4-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="607d4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="607d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607d4-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="607d4-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="607d4-128">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="607d4-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="607d4-129">Пропорции рисунка</span><span class="sxs-lookup"><span data-stu-id="607d4-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="607d4-130">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="607d4-130">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="607d4-131">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="607d4-131">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="607d4-132">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="607d4-132">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="607d4-133">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="607d4-133">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="607d4-134">**\_ \_ Минимальный \_ \_ Апертура экрана MF MT**</span><span class="sxs-lookup"><span data-stu-id="607d4-134">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="607d4-135">**\_ \_ \_ Апертура для поиска MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="607d4-135">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




