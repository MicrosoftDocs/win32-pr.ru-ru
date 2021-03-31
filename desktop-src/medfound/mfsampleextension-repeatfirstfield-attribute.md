---
description: Указывает, следует ли повторять первое поле в чередовании кадров. Этот атрибут применяется к примерам мультимедиа.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: Атрибут MFSampleExtension_RepeatFirstField (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155366"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a><span data-ttu-id="6d6d5-104">Мфсампликстенсион \_ репеатфирстфиелд, атрибут</span><span class="sxs-lookup"><span data-stu-id="6d6d5-104">MFSampleExtension\_RepeatFirstField attribute</span></span>

<span data-ttu-id="6d6d5-105">Указывает, следует ли повторять первое поле в чередовании кадров.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-105">Specifies whether to repeat the first field in an interlaced frame.</span></span> <span data-ttu-id="6d6d5-106">Этот атрибут применяется к примерам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="6d6d5-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6d6d5-107">Data type</span></span>

<span data-ttu-id="6d6d5-108">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="6d6d5-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6d6d5-109">Get/Set</span><span class="sxs-lookup"><span data-stu-id="6d6d5-109">Get/set</span></span>

<span data-ttu-id="6d6d5-110">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6d6d5-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6d6d5-111">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="6d6d5-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6d6d5-112">Применяется к</span><span class="sxs-lookup"><span data-stu-id="6d6d5-112">Applies to</span></span>

[<span data-ttu-id="6d6d5-113">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="6d6d5-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="6d6d5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d6d5-114">Remarks</span></span>

<span data-ttu-id="6d6d5-115">Если значение равно **false** или атрибут не задан, первое поле не повторяется.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-115">If the value is **FALSE** or the attribute is not set, the first field is not repeated.</span></span> <span data-ttu-id="6d6d5-116">Если значение равно **true**, первое поле повторяется.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-116">If the value is **TRUE**, the first field is repeated.</span></span> <span data-ttu-id="6d6d5-117">Значение **true** допустимо только в том случае, если выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-117">The value **TRUE** is valid only when the following conditions are true:</span></span>

-   <span data-ttu-id="6d6d5-118">Тип мультимедиа смешанный и прогрессивный.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-118">The media type is mixed interlaced and progressive.</span></span> <span data-ttu-id="6d6d5-119">(Атрибут атрибута « [**\_ \_ \_ режим с чередованием» MF MT**](mf-mt-interlace-mode-attribute.md) для типа носителя — **мфвидеоинтерлаце \_ миксединтерлацеорпрогрессиве**.)</span><span class="sxs-lookup"><span data-stu-id="6d6d5-119">(The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute attribute on the media type is **MFVideoInterlace\_MixedInterlaceOrProgressive**.)</span></span>
-   <span data-ttu-id="6d6d5-120">Кадр является прогрессивным, а атрибут [**мфсампликстенсион \_ чередования**](mfsampleextension-interlaced-attribute.md) в образце имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-120">The frame is progressive and the [**MFSampleExtension\_Interlaced**](mfsampleextension-interlaced-attribute.md) attribute on the sample is **TRUE**.</span></span>
-   <span data-ttu-id="6d6d5-121">В образце задан атрибут [**мфсампликстенсион \_ боттомфиелдфирст**](mfsampleextension-bottomfieldfirst-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6d6d5-121">The [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute is set on the sample.</span></span> <span data-ttu-id="6d6d5-122">Значение может быть **true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-122">The value can be **TRUE** or **FALSE**.</span></span> <span data-ttu-id="6d6d5-123">Порядок полей определяется этим атрибутом.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-123">The ordering of the fields is determined by this attribute.</span></span>

<span data-ttu-id="6d6d5-124">Этот атрибут используется для выпадающих 3:2.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-124">This attribute is used for 3:2 pulldown.</span></span> <span data-ttu-id="6d6d5-125">В следующей таблице показан порядок отображения полей.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-125">The following table shows the order in which fields are displayed.</span></span>



| <span data-ttu-id="6d6d5-126">Мфсампликстенсион \_ репеатфирстфиелд</span><span class="sxs-lookup"><span data-stu-id="6d6d5-126">MFSampleExtension\_RepeatFirstField</span></span> | <span data-ttu-id="6d6d5-127">Мфсампликстенсион \_ боттомфиелдфирст</span><span class="sxs-lookup"><span data-stu-id="6d6d5-127">MFSampleExtension\_BottomFieldFirst</span></span> | <span data-ttu-id="6d6d5-128">Порядок полей</span><span class="sxs-lookup"><span data-stu-id="6d6d5-128">Field order</span></span>         |
|-------------------------------------|-------------------------------------|---------------------|
| <span data-ttu-id="6d6d5-129">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6d6d5-129">**TRUE**</span></span>                            | <span data-ttu-id="6d6d5-130">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6d6d5-130">**TRUE**</span></span>                            | <span data-ttu-id="6d6d5-131">Нижние, верхние и нижние</span><span class="sxs-lookup"><span data-stu-id="6d6d5-131">Lower, upper, lower</span></span> |
| <span data-ttu-id="6d6d5-132">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6d6d5-132">**TRUE**</span></span>                            | <span data-ttu-id="6d6d5-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6d6d5-133">**FALSE**</span></span>                           | <span data-ttu-id="6d6d5-134">Верхний, нижний, верхний</span><span class="sxs-lookup"><span data-stu-id="6d6d5-134">Upper, lower, upper</span></span> |
| <span data-ttu-id="6d6d5-135">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6d6d5-135">**FALSE**</span></span>                           | <span data-ttu-id="6d6d5-136">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6d6d5-136">**TRUE**</span></span>                            | <span data-ttu-id="6d6d5-137">Нижний, верхний</span><span class="sxs-lookup"><span data-stu-id="6d6d5-137">Lower, upper</span></span>        |
| <span data-ttu-id="6d6d5-138">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6d6d5-138">**FALSE**</span></span>                           | <span data-ttu-id="6d6d5-139">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6d6d5-139">**FALSE**</span></span>                           | <span data-ttu-id="6d6d5-140">Верхний и нижний</span><span class="sxs-lookup"><span data-stu-id="6d6d5-140">Upper, lower</span></span>        |



 

<span data-ttu-id="6d6d5-141">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="6d6d5-141">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d6d5-142">Требования</span><span class="sxs-lookup"><span data-stu-id="6d6d5-142">Requirements</span></span>



| <span data-ttu-id="6d6d5-143">Требование</span><span class="sxs-lookup"><span data-stu-id="6d6d5-143">Requirement</span></span> | <span data-ttu-id="6d6d5-144">Значение</span><span class="sxs-lookup"><span data-stu-id="6d6d5-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d6d5-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d6d5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6d6d5-146">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="6d6d5-146">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6d6d5-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d6d5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6d6d5-148">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6d6d5-148">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6d6d5-149">Header</span><span class="sxs-lookup"><span data-stu-id="6d6d5-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d6d5-150"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d6d5-150"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d6d5-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d6d5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d6d5-152">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6d6d5-152">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d6d5-153">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="6d6d5-153">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d6d5-154">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="6d6d5-154">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="6d6d5-155">Чередование видео</span><span class="sxs-lookup"><span data-stu-id="6d6d5-155">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




