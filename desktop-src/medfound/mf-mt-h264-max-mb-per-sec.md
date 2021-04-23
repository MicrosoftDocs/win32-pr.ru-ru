---
description: Указывает максимальную скорость обработки макроблокк для потока видео H. 264.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: Атрибут MF_MT_H264_MAX_MB_PER_SEC (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692658"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a><span data-ttu-id="5ff00-103">\_ \_ \_ Атрибут с максимальным числом \_ МБ \_ в \_ секунду для H264 Single bitrate MF MT</span><span class="sxs-lookup"><span data-stu-id="5ff00-103">MF\_MT\_H264\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="5ff00-104">Указывает максимальную скорость обработки макроблокк для потока видео H. 264.</span><span class="sxs-lookup"><span data-stu-id="5ff00-104">Specifies the maximum macroblock processing rate for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="5ff00-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5ff00-105">Data type</span></span>

<span data-ttu-id="5ff00-106">**\[ UINT32 \]** сохраняется как **UINT8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5ff00-106">**UINT32\[\]** stored as **UINT8\[\]**</span></span>

## <a name="applies-to"></a><span data-ttu-id="5ff00-107">Применяется к</span><span class="sxs-lookup"><span data-stu-id="5ff00-107">Applies to</span></span>

[<span data-ttu-id="5ff00-108">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="5ff00-108">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="5ff00-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ff00-109">Remarks</span></span>

<span data-ttu-id="5ff00-110">Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB.</span><span class="sxs-lookup"><span data-stu-id="5ff00-110">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="5ff00-111">Значение атрибута является массивом значений UINT32, которые соответствуют следующим полям в дескрипторе формата видео УВК 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="5ff00-111">The value of the attribute is an array of UINT32 values, which correspond to the following fields in the UVC 1.5 H.264 video format descriptor.</span></span>

| <span data-ttu-id="5ff00-112">Элемент массива</span><span class="sxs-lookup"><span data-stu-id="5ff00-112">Array Element</span></span> | <span data-ttu-id="5ff00-113">Поле дескриптора</span><span class="sxs-lookup"><span data-stu-id="5ff00-113">Descriptor Field</span></span>                                           |
|---------------|------------------------------------------------------------|
| <span data-ttu-id="5ff00-114">0</span><span class="sxs-lookup"><span data-stu-id="5ff00-114">0</span></span>             | <span data-ttu-id="5ff00-115">**двмаксмбперсеконересолутионноскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-115">**dwMaxMBperSecOneResolutionNoScalability**</span></span>                |
| <span data-ttu-id="5ff00-116">1</span><span class="sxs-lookup"><span data-stu-id="5ff00-116">1</span></span>             | <span data-ttu-id="5ff00-117">**двмаксмбперсектворесолутионсноскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span></span>               |
| <span data-ttu-id="5ff00-118">2</span><span class="sxs-lookup"><span data-stu-id="5ff00-118">2</span></span>             | <span data-ttu-id="5ff00-119">**двмаксмбперсексриресолутионсноскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span></span>             |
| <span data-ttu-id="5ff00-120">3</span><span class="sxs-lookup"><span data-stu-id="5ff00-120">3</span></span>             | <span data-ttu-id="5ff00-121">**двмаксмбперсекфаурресолутионсноскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-121">**dwMaxMBperSecFourResolutionsNoScalability**</span></span>              |
| <span data-ttu-id="5ff00-122">4</span><span class="sxs-lookup"><span data-stu-id="5ff00-122">4</span></span>             | <span data-ttu-id="5ff00-123">**двмаксмбперсеконересолутионтемпоралскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span></span>          |
| <span data-ttu-id="5ff00-124">5</span><span class="sxs-lookup"><span data-stu-id="5ff00-124">5</span></span>             | <span data-ttu-id="5ff00-125">**двмаксмбперсектворесолутионстемпоралскалаблилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span></span>        |
| <span data-ttu-id="5ff00-126">6</span><span class="sxs-lookup"><span data-stu-id="5ff00-126">6</span></span>             | <span data-ttu-id="5ff00-127">**двмаксмбперсексриресолутионстемпоралскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span></span>       |
| <span data-ttu-id="5ff00-128">7</span><span class="sxs-lookup"><span data-stu-id="5ff00-128">7</span></span>             | <span data-ttu-id="5ff00-129">**двмаксмбперсекфаурресолутионстемпоралскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span></span>        |
| <span data-ttu-id="5ff00-130">8</span><span class="sxs-lookup"><span data-stu-id="5ff00-130">8</span></span>             | <span data-ttu-id="5ff00-131">**двмаксмбперсеконересолутионтемпоралкуалитискалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span></span>   |
| <span data-ttu-id="5ff00-132">9</span><span class="sxs-lookup"><span data-stu-id="5ff00-132">9</span></span>             | <span data-ttu-id="5ff00-133">**двмаксмбперсектворесолутионстемпоралкуалитискалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span></span>  |
| <span data-ttu-id="5ff00-134">10</span><span class="sxs-lookup"><span data-stu-id="5ff00-134">10</span></span>            | <span data-ttu-id="5ff00-135">**двмаксмбперсексриресолутионстемпоралкуалитискалаблити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span></span> |
| <span data-ttu-id="5ff00-136">11</span><span class="sxs-lookup"><span data-stu-id="5ff00-136">11</span></span>            | <span data-ttu-id="5ff00-137">**двмаксмбперсекфаурресолутионстемпоралкуалитискалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span></span> |
| <span data-ttu-id="5ff00-138">12</span><span class="sxs-lookup"><span data-stu-id="5ff00-138">12</span></span>            | <span data-ttu-id="5ff00-139">**двмаксмбперсеконересолутионфуллскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-139">**dwMaxMBperSecOneResolutionFullScalability**</span></span>              |
| <span data-ttu-id="5ff00-140">13</span><span class="sxs-lookup"><span data-stu-id="5ff00-140">13</span></span>            | <span data-ttu-id="5ff00-141">**двмаксмбперсектворесолутионсфуллскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span></span>             |
| <span data-ttu-id="5ff00-142">14</span><span class="sxs-lookup"><span data-stu-id="5ff00-142">14</span></span>            | <span data-ttu-id="5ff00-143">**двмаксмбперсексриресолутионсфуллскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span></span>           |
| <span data-ttu-id="5ff00-144">15</span><span class="sxs-lookup"><span data-stu-id="5ff00-144">15</span></span>            | <span data-ttu-id="5ff00-145">**двмаксмбперсекфаурресолутионсфуллскалабилити**</span><span class="sxs-lookup"><span data-stu-id="5ff00-145">**dwMaxMBperSecFourResolutionsFullScalability**</span></span>            |



 

<span data-ttu-id="5ff00-146">Этот атрибут также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="5ff00-146">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ff00-147">Требования</span><span class="sxs-lookup"><span data-stu-id="5ff00-147">Requirements</span></span>



| <span data-ttu-id="5ff00-148">Требование</span><span class="sxs-lookup"><span data-stu-id="5ff00-148">Requirement</span></span> | <span data-ttu-id="5ff00-149">Значение</span><span class="sxs-lookup"><span data-stu-id="5ff00-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff00-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ff00-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5ff00-151">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="5ff00-151">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="5ff00-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ff00-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5ff00-153">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="5ff00-153">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5ff00-154">Header</span><span class="sxs-lookup"><span data-stu-id="5ff00-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ff00-155"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ff00-155"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ff00-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ff00-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff00-157">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5ff00-157">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5ff00-158">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="5ff00-158">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




