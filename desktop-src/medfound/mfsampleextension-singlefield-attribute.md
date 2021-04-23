---
description: Указывает, содержит ли образец видео одно поле или два поля с чередованием. Этот атрибут применяется к примерам мультимедиа.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: Атрибут MFSampleExtension_SingleField (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543927"
---
# <a name="mfsampleextension_singlefield-attribute"></a><span data-ttu-id="8db14-104">Мфсампликстенсион \_ синглефиелд, атрибут</span><span class="sxs-lookup"><span data-stu-id="8db14-104">MFSampleExtension\_SingleField attribute</span></span>

<span data-ttu-id="8db14-105">Указывает, содержит ли образец видео одно поле или два поля с чередованием.</span><span class="sxs-lookup"><span data-stu-id="8db14-105">Specifies whether a video sample contains a single field or two interleaved fields.</span></span> <span data-ttu-id="8db14-106">Этот атрибут применяется к примерам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8db14-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="8db14-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8db14-107">Data type</span></span>

<span data-ttu-id="8db14-108">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="8db14-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="8db14-109">Get/Set</span><span class="sxs-lookup"><span data-stu-id="8db14-109">Get/set</span></span>

<span data-ttu-id="8db14-110">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8db14-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8db14-111">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="8db14-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8db14-112">Применяется к</span><span class="sxs-lookup"><span data-stu-id="8db14-112">Applies to</span></span>

[<span data-ttu-id="8db14-113">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="8db14-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="8db14-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8db14-114">Remarks</span></span>

<span data-ttu-id="8db14-115">Если значение равно **true**, пример содержит одно поле.</span><span class="sxs-lookup"><span data-stu-id="8db14-115">If the value is **TRUE**, the sample contains one field.</span></span> <span data-ttu-id="8db14-116">Если значение равно **false** или атрибут не задан, пример содержит полный кадр.</span><span class="sxs-lookup"><span data-stu-id="8db14-116">If the value is **FALSE** or the attribute is not set, the sample contains a complete frame.</span></span> <span data-ttu-id="8db14-117">(Два поля при чередовании или прогрессивный фрейм.)</span><span class="sxs-lookup"><span data-stu-id="8db14-117">(Two fields if interlaced, or a progressive frame.)</span></span>

<span data-ttu-id="8db14-118">Если тип носителя — прогрессивные кадры или поля с чередованием, этот атрибут должен иметь **значение false** или не заполняться.</span><span class="sxs-lookup"><span data-stu-id="8db14-118">If the media type is progressive frames or interleaved fields, this attribute must be **FALSE** or left unset.</span></span>

<span data-ttu-id="8db14-119">Если тип мультимедиа является одним полем, этот атрибут должен иметь **значение true**.</span><span class="sxs-lookup"><span data-stu-id="8db14-119">If the media type is single field, this attribute must be **TRUE**.</span></span> <span data-ttu-id="8db14-120">Задайте атрибут [**мфсампликстенсион \_ боттомфиелдфирст**](mfsampleextension-bottomfieldfirst-attribute.md) в образце, чтобы указать, является ли это верхнее поле или нижнее поле.</span><span class="sxs-lookup"><span data-stu-id="8db14-120">Set the [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute on the sample to indicate whether it is the upper field or the lower field.</span></span>

<span data-ttu-id="8db14-121">В настоящее время расширенный обработчик видео (Евр) не поддерживает содержимое, переключаясь между чередованием кадров и отдельными полями.</span><span class="sxs-lookup"><span data-stu-id="8db14-121">Currently the enhanced video renderer (EVR) does not support content that switches between interlaced frames and single fields.</span></span>

<span data-ttu-id="8db14-122">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="8db14-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8db14-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8db14-123">Requirements</span></span>



| <span data-ttu-id="8db14-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8db14-124">Requirement</span></span> | <span data-ttu-id="8db14-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8db14-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8db14-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8db14-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8db14-127">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="8db14-127">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8db14-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8db14-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8db14-129">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="8db14-129">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8db14-130">Header</span><span class="sxs-lookup"><span data-stu-id="8db14-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8db14-131"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8db14-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8db14-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8db14-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db14-133">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8db14-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8db14-134">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="8db14-134">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="8db14-135">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="8db14-135">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="8db14-136">Чередование видео</span><span class="sxs-lookup"><span data-stu-id="8db14-136">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




