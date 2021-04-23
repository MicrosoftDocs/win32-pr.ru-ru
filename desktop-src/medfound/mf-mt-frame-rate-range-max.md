---
description: Максимальная частота кадров, поддерживаемая устройством записи видео, в кадрах в секунду.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: Атрибут MF_MT_FRAME_RATE_RANGE_MAX (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991474"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a><span data-ttu-id="4c6a4-103">\_ \_ \_ \_ Атрибут максимального диапазона частот кадров MF MT \_</span><span class="sxs-lookup"><span data-stu-id="4c6a4-103">MF\_MT\_FRAME\_RATE\_RANGE\_MAX attribute</span></span>

<span data-ttu-id="4c6a4-104">Максимальная частота кадров, поддерживаемая устройством записи видео, в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="4c6a4-104">The maximum frame rate that is supported by a video capture device, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="4c6a4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4c6a4-105">Data type</span></span>

<span data-ttu-id="4c6a4-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4c6a4-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="4c6a4-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="4c6a4-107">Get/set</span></span>

<span data-ttu-id="4c6a4-108">Чтобы получить этот атрибут, вызовите [**мфжетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="4c6a4-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="4c6a4-109">Чтобы задать этот атрибут, вызовите [**мфсетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="4c6a4-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c6a4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c6a4-110">Remarks</span></span>

<span data-ttu-id="4c6a4-111">Частота кадров выражается в виде коэффициента.</span><span class="sxs-lookup"><span data-stu-id="4c6a4-111">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="4c6a4-112">Верхние 32 бит значения атрибута содержат числитель, а младшие 32 биты содержат знаменатель.</span><span class="sxs-lookup"><span data-stu-id="4c6a4-112">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="4c6a4-113">Например, если частота кадров составляет 30 кадров в секунду (кадров/с), то соотношение составляет 30/1.</span><span class="sxs-lookup"><span data-stu-id="4c6a4-113">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span>

<span data-ttu-id="4c6a4-114">Если устройство записи сообщает о максимальной частоте кадров, источник мультимедиа задает этот атрибут для типа носителя.</span><span class="sxs-lookup"><span data-stu-id="4c6a4-114">If the capture device reports a maximum frame rate, the media source sets this attribute on the media type.</span></span> <span data-ttu-id="4c6a4-115">Минимальная частота кадров указывается в атрибуте [ \_ \_ \_ \_ \_ мин. частоты кадров MF MT](mf-mt-frame-rate-range-min.md) .</span><span class="sxs-lookup"><span data-stu-id="4c6a4-115">The minimum frame rate is given in the [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attribute.</span></span> <span data-ttu-id="4c6a4-116">На устройстве не гарантируется поддержка каждого приращения в этом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="4c6a4-116">The device is not guaranteed to support every increment within this range.</span></span>

<span data-ttu-id="4c6a4-117">Чтобы задать частоту кадров устройства, сначала измените значение атрибута [**\_ \_ \_ Частота кадров MF MT**](mf-mt-frame-rate-attribute.md) для типа носителя.</span><span class="sxs-lookup"><span data-stu-id="4c6a4-117">To set the device's frame rate, first modify the value of the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="4c6a4-118">Затем задайте тип носителя в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4c6a4-118">Then set the media type on the media source.</span></span>

<span data-ttu-id="4c6a4-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="4c6a4-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c6a4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4c6a4-120">Requirements</span></span>



| <span data-ttu-id="4c6a4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4c6a4-121">Requirement</span></span> | <span data-ttu-id="4c6a4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4c6a4-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c6a4-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c6a4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4c6a4-124">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="4c6a4-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4c6a4-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c6a4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4c6a4-126">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="4c6a4-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4c6a4-127">Header</span><span class="sxs-lookup"><span data-stu-id="4c6a4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c6a4-128"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c6a4-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c6a4-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c6a4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c6a4-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c6a4-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c6a4-131">Настройка частоты кадров видеозаписи</span><span class="sxs-lookup"><span data-stu-id="4c6a4-131">How to Set the Video Capture Frame Rate</span></span>](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[<span data-ttu-id="4c6a4-132">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="4c6a4-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c6a4-133">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="4c6a4-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4c6a4-134">\_ \_ \_ \_ Минимальный диапазон частот кадров MF MT \_</span><span class="sxs-lookup"><span data-stu-id="4c6a4-134">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




