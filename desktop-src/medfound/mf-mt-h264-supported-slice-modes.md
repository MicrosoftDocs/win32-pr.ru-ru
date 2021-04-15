---
description: Задает поддерживаемые режимы среза для видеопотока H. 264.
ms.assetid: 72DA62EC-A509-4C3B-A51D-7313C176AAA9
title: Атрибут MF_MT_H264_SUPPORTED_SLICE_MODES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9258a2ce2b9bef050fc6ea4468026539ff67f1be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682742"
---
# <a name="mf_mt_h264_supported_slice_modes-attribute"></a><span data-ttu-id="4a460-103">\_ \_ \_ \_ Атрибут режимов среза MF MT H264 Single bitrate поддерживается \_</span><span class="sxs-lookup"><span data-stu-id="4a460-103">MF\_MT\_H264\_SUPPORTED\_SLICE\_MODES attribute</span></span>

<span data-ttu-id="4a460-104">Задает поддерживаемые режимы среза для видеопотока H. 264.</span><span class="sxs-lookup"><span data-stu-id="4a460-104">Specifies the supported slice modes for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a460-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4a460-105">Data type</span></span>

<span data-ttu-id="4a460-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4a460-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4a460-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="4a460-107">Get/set</span></span>

<span data-ttu-id="4a460-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4a460-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4a460-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4a460-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4a460-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="4a460-110">Applies to</span></span>

[<span data-ttu-id="4a460-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="4a460-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="4a460-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a460-112">Remarks</span></span>

<span data-ttu-id="4a460-113">Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB.</span><span class="sxs-lookup"><span data-stu-id="4a460-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="4a460-114">Значение соответствует полю **бмсуппортедслицемодес** в дескрипторе формата видео УВК 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="4a460-114">The value corresponds to the **bmSupportedSliceModes** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="4a460-115">Этот атрибут также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="4a460-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a460-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4a460-116">Requirements</span></span>



| <span data-ttu-id="4a460-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4a460-117">Requirement</span></span> | <span data-ttu-id="4a460-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4a460-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a460-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a460-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4a460-120">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="4a460-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4a460-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a460-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4a460-122">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="4a460-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4a460-123">Header</span><span class="sxs-lookup"><span data-stu-id="4a460-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a460-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a460-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a460-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a460-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a460-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a460-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a460-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="4a460-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




