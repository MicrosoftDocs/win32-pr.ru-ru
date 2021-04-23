---
description: Указывает исходный прямоугольник для видеомикшера расширенного обработчика видео (Евр). Исходный прямоугольник — это часть видеокадра, блитс микшер на поверхность назначения.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: Атрибут VIDEO_ZOOM_RECT (Евр. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662680"
---
# <a name="video_zoom_rect-attribute"></a><span data-ttu-id="d9f89-104">\_ \_ Атрибут Rect масштаба видео</span><span class="sxs-lookup"><span data-stu-id="d9f89-104">VIDEO\_ZOOM\_RECT attribute</span></span>

<span data-ttu-id="d9f89-105">Указывает исходный прямоугольник для видеомикшера [расширенного обработчика видео](enhanced-video-renderer.md) (Евр).</span><span class="sxs-lookup"><span data-stu-id="d9f89-105">Specifies the source rectangle for video mixer of the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="d9f89-106">Исходный прямоугольник — это часть видеокадра, блитс микшер на поверхность назначения.</span><span class="sxs-lookup"><span data-stu-id="d9f89-106">The source rectangle is the portion of the video frame that the mixer blits to the destination surface.</span></span>

## <a name="data-type"></a><span data-ttu-id="d9f89-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d9f89-107">Data type</span></span>

<span data-ttu-id="d9f89-108">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="d9f89-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f89-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9f89-109">Remarks</span></span>

<span data-ttu-id="d9f89-110">Значением этого атрибута является структура [**мфвидеонормализедрект**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .</span><span class="sxs-lookup"><span data-stu-id="d9f89-110">The value of this attribute is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="d9f89-111">Исходный прямоугольник определяется относительно нормализованной системы координат, в которой весь кадр видео занимает прямоугольник с координатами {0, 0, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="d9f89-111">The source rectangle is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="d9f89-112">Исходный прямоугольник должен помещаться в кадре видео; координаты исходного прямоугольника имеют диапазон (0... 1).</span><span class="sxs-lookup"><span data-stu-id="d9f89-112">The source rectangle must fit within the video frame; the coordinates of the source rectangle have a range of (0...1).</span></span>

<span data-ttu-id="d9f89-113">Стандартный выступающий Евр задает этот атрибут для микшера.</span><span class="sxs-lookup"><span data-stu-id="d9f89-113">The standard EVR presenter sets this attribute on the mixer.</span></span> <span data-ttu-id="d9f89-114">Чтобы задать атрибут, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d9f89-114">To set the attribute, do the following:</span></span>

1.  <span data-ttu-id="d9f89-115">Вызовите [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в микшере, чтобы получить хранилище атрибутов микшера.</span><span class="sxs-lookup"><span data-stu-id="d9f89-115">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the mixer, to get the mixer's attribute store.</span></span>
2.  <span data-ttu-id="d9f89-116">Вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) , чтобы задать для микшера атрибут **\_ \_ Rect масштаба видео** .</span><span class="sxs-lookup"><span data-stu-id="d9f89-116">Call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) to set the **VIDEO\_ZOOM\_RECT** attribute on the mixer.</span></span> <span data-ttu-id="d9f89-117">Значение является структурой [**мфвидеонормализедрект**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .</span><span class="sxs-lookup"><span data-stu-id="d9f89-117">The value is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="d9f89-118">В пользовательском выступающем Евр можно использовать этот атрибут для реализации метода [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) .</span><span class="sxs-lookup"><span data-stu-id="d9f89-118">In a custom EVR presenter, you can use this attribute to implement the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method.</span></span> <span data-ttu-id="d9f89-119">Дополнительные сведения см. в разделе [прямоугольники источника и назначения](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="d9f89-119">For more information, see [Source and Destination Rectangles](how-to-write-an-evr-presenter.md).</span></span>

<span data-ttu-id="d9f89-120">Константа GUID для этого атрибута экспортируется из стрмиидс. lib.</span><span class="sxs-lookup"><span data-stu-id="d9f89-120">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="d9f89-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="d9f89-121">Examples</span></span>

<span data-ttu-id="d9f89-122">В следующем примере задается исходный прямоугольник в микшере.</span><span class="sxs-lookup"><span data-stu-id="d9f89-122">The following example sets the source rectangle on the mixer.</span></span>


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="d9f89-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d9f89-123">Requirements</span></span>



| <span data-ttu-id="d9f89-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d9f89-124">Requirement</span></span> | <span data-ttu-id="d9f89-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d9f89-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d9f89-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9f89-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d9f89-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9f89-127">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d9f89-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9f89-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d9f89-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d9f89-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d9f89-130">Header</span><span class="sxs-lookup"><span data-stu-id="d9f89-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9f89-131"><dt>Евр. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9f89-131"><dt>Evr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f89-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9f89-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f89-133">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9f89-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9f89-134">Расширенные атрибуты модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="d9f89-134">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9f89-135">Написание выступающего Евр</span><span class="sxs-lookup"><span data-stu-id="d9f89-135">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="d9f89-136">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="d9f89-136">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="d9f89-137">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="d9f89-137">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




