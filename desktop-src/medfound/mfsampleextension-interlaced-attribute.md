---
description: Указывает, находится ли кадр видео с чередованием или с последовательной разверткой.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: Атрибут MFSampleExtension_Interlaced (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719424"
---
# <a name="mfsampleextension_interlaced-attribute"></a><span data-ttu-id="75457-103">Мфсампликстенсион \_ чередующийся атрибут</span><span class="sxs-lookup"><span data-stu-id="75457-103">MFSampleExtension\_Interlaced attribute</span></span>

<span data-ttu-id="75457-104">Указывает, находится ли кадр видео с чередованием или с последовательной разверткой.</span><span class="sxs-lookup"><span data-stu-id="75457-104">Indicates whether a video frame is interlaced or progressive.</span></span> <span data-ttu-id="75457-105">**Значение true** показывает, что кадр является чередованием.</span><span class="sxs-lookup"><span data-stu-id="75457-105">If **TRUE**, the frame is interlaced.</span></span> <span data-ttu-id="75457-106">Если **значение равно false**, кадр является прогрессивным.</span><span class="sxs-lookup"><span data-stu-id="75457-106">If **FALSE**, the frame is progressive.</span></span> <span data-ttu-id="75457-107">Если не задано, тип носителя описывает чересстрочную развертку.</span><span class="sxs-lookup"><span data-stu-id="75457-107">If not set, the media type describes the interlacing.</span></span> <span data-ttu-id="75457-108">Этот атрибут применяется к примерам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="75457-108">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="75457-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="75457-109">Data type</span></span>

<span data-ttu-id="75457-110">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="75457-110">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="75457-111">Get/Set</span><span class="sxs-lookup"><span data-stu-id="75457-111">Get/set</span></span>

<span data-ttu-id="75457-112">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="75457-112">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="75457-113">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="75457-113">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="75457-114">Применяется к</span><span class="sxs-lookup"><span data-stu-id="75457-114">Applies to</span></span>

[<span data-ttu-id="75457-115">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="75457-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="75457-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75457-116">Remarks</span></span>

<span data-ttu-id="75457-117">Для видеосодержимого, содержащего смешанные прогрессивные и чередующиеся кадры, задайте тип мультимедиа с чередованием и используйте этот атрибут в каждом кадре, чтобы указать, является ли кадр прогрессивным или чередованием.</span><span class="sxs-lookup"><span data-stu-id="75457-117">For video content that contains mixed progressive and interlaced frames, set the media type to interlaced and use this attribute on each frame to indicate whether the frame is progressive or interlaced.</span></span>

<span data-ttu-id="75457-118">Для содержимого видео, которое полностью перемещается в чередование, задайте тип мультимедиа с чередованием и опустите этот атрибут или задайте для него **значение true** при каждом выборке.</span><span class="sxs-lookup"><span data-stu-id="75457-118">For video content that is entirely interlaced, set the media type to interlaced and omit this attribute, or set it to **TRUE** on every sample.</span></span>

<span data-ttu-id="75457-119">Для содержимого видео, которое полностью прогрессивно, установите для типа мультимедиа значение прогрессивный и пропустите этот атрибут или задайте для него **значение false** в каждом образце.</span><span class="sxs-lookup"><span data-stu-id="75457-119">For video content that is entirely progressive, set the media type to progressive and omit this attribute, or set it to **FALSE** on every sample.</span></span>

<span data-ttu-id="75457-120">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="75457-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="75457-121">Требования</span><span class="sxs-lookup"><span data-stu-id="75457-121">Requirements</span></span>



| <span data-ttu-id="75457-122">Требование</span><span class="sxs-lookup"><span data-stu-id="75457-122">Requirement</span></span> | <span data-ttu-id="75457-123">Значение</span><span class="sxs-lookup"><span data-stu-id="75457-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75457-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75457-124">Minimum supported client</span></span><br/> | <span data-ttu-id="75457-125">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="75457-125">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="75457-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75457-126">Minimum supported server</span></span><br/> | <span data-ttu-id="75457-127">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="75457-127">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="75457-128">Header</span><span class="sxs-lookup"><span data-stu-id="75457-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="75457-129"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="75457-129"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75457-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75457-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75457-131">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="75457-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="75457-132">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="75457-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="75457-133">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="75457-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="75457-134">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="75457-134">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="75457-135">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="75457-135">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="75457-136">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="75457-136">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="75457-137">Чередование видео</span><span class="sxs-lookup"><span data-stu-id="75457-137">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




