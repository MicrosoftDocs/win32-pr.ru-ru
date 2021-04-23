---
description: Минимальная частота кадров, поддерживаемая устройством записи видео, в кадрах в секунду.
ms.assetid: d3725796-f683-4ca1-a37f-22c40fff0b76
title: Атрибут MF_MT_FRAME_RATE_RANGE_MIN (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9692927242eea7ec65b86572db455e610e30c711
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912164"
---
# <a name="mf_mt_frame_rate_range_min-attribute"></a><span data-ttu-id="91bc3-103">\_ \_ \_ \_ Атрибут мин в диапазоне частоты кадров MF MT \_</span><span class="sxs-lookup"><span data-stu-id="91bc3-103">MF\_MT\_FRAME\_RATE\_RANGE\_MIN attribute</span></span>

<span data-ttu-id="91bc3-104">Минимальная частота кадров, поддерживаемая устройством записи видео, в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="91bc3-104">The minimum frame rate that is supported by a video capture device, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="91bc3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="91bc3-105">Data type</span></span>

<span data-ttu-id="91bc3-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="91bc3-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="91bc3-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="91bc3-107">Get/set</span></span>

<span data-ttu-id="91bc3-108">Чтобы получить этот атрибут, вызовите [**мфжетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="91bc3-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="91bc3-109">Чтобы задать этот атрибут, вызовите [**мфсетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="91bc3-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="remarks"></a><span data-ttu-id="91bc3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91bc3-110">Remarks</span></span>

<span data-ttu-id="91bc3-111">Частота кадров выражается в виде коэффициента.</span><span class="sxs-lookup"><span data-stu-id="91bc3-111">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="91bc3-112">Верхние 32 бит значения атрибута содержат числитель, а младшие 32 биты содержат знаменатель.</span><span class="sxs-lookup"><span data-stu-id="91bc3-112">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="91bc3-113">Например, если частота кадров составляет 30 кадров в секунду (кадров/с), то соотношение составляет 30/1.</span><span class="sxs-lookup"><span data-stu-id="91bc3-113">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span>

<span data-ttu-id="91bc3-114">Если устройство записи сообщает о минимальной частоте кадров, источник мультимедиа задает этот атрибут для типа носителя.</span><span class="sxs-lookup"><span data-stu-id="91bc3-114">If the capture device reports a minimum frame rate, the media source sets this attribute on the media type.</span></span> <span data-ttu-id="91bc3-115">Максимальная частота кадров указывается в атрибуте [ \_ \_ \_ \_ \_ максимального диапазона частоты кадров MF MT](mf-mt-frame-rate-range-max.md) .</span><span class="sxs-lookup"><span data-stu-id="91bc3-115">The maximum frame rate is given in the [MF\_MT\_FRAME\_RATE\_RANGE\_MAX](mf-mt-frame-rate-range-max.md) attribute.</span></span> <span data-ttu-id="91bc3-116">На устройстве не гарантируется поддержка каждого приращения в этом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="91bc3-116">The device is not guaranteed to support every increment within this range.</span></span>

<span data-ttu-id="91bc3-117">Чтобы задать частоту кадров устройства, сначала измените значение атрибута [**\_ \_ \_ Частота кадров MF MT**](mf-mt-frame-rate-attribute.md) для типа носителя.</span><span class="sxs-lookup"><span data-stu-id="91bc3-117">To set the device's frame rate, first modify the value of the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="91bc3-118">Затем задайте тип носителя в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="91bc3-118">Then set the media type on the media source.</span></span>

<span data-ttu-id="91bc3-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="91bc3-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="91bc3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="91bc3-120">Requirements</span></span>



| <span data-ttu-id="91bc3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="91bc3-121">Requirement</span></span> | <span data-ttu-id="91bc3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="91bc3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91bc3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91bc3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="91bc3-124">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="91bc3-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="91bc3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91bc3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="91bc3-126">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="91bc3-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="91bc3-127">Header</span><span class="sxs-lookup"><span data-stu-id="91bc3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="91bc3-128"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="91bc3-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91bc3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91bc3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91bc3-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="91bc3-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="91bc3-131">Настройка частоты кадров видеозаписи</span><span class="sxs-lookup"><span data-stu-id="91bc3-131">How to Set the Video Capture Frame Rate</span></span>](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[<span data-ttu-id="91bc3-132">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="91bc3-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="91bc3-133">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="91bc3-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="91bc3-134">\_ \_ \_ \_ максимальный диапазон частот кадров MF MT \_</span><span class="sxs-lookup"><span data-stu-id="91bc3-134">MF\_MT\_FRAME\_RATE\_RANGE\_MAX</span></span>](mf-mt-frame-rate-range-max.md)
</dt> </dl>

 

 




