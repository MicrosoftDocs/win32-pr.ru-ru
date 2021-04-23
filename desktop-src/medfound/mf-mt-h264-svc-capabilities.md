---
description: Указывает возможности SVC для потока видео H. 264.
ms.assetid: B727D9D2-6126-41F8-A27A-743640FE3AE4
title: Атрибут MF_MT_H264_SVC_CAPABILITIES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35a39b5f1727af8399d9d0c56c93d2d9d1486c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810102"
---
# <a name="mf_mt_h264_svc_capabilities-attribute"></a><span data-ttu-id="c02fb-103">\_Атрибут " \_ \_ возможности svc \_ " MF MT H264 Single bitrate</span><span class="sxs-lookup"><span data-stu-id="c02fb-103">MF\_MT\_H264\_SVC\_CAPABILITIES attribute</span></span>

<span data-ttu-id="c02fb-104">Указывает возможности SVC для потока видео H. 264.</span><span class="sxs-lookup"><span data-stu-id="c02fb-104">Specifies the SVC capabilities of an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="c02fb-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c02fb-105">Data type</span></span>

<span data-ttu-id="c02fb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c02fb-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c02fb-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="c02fb-107">Get/set</span></span>

<span data-ttu-id="c02fb-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c02fb-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c02fb-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c02fb-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c02fb-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="c02fb-110">Applies to</span></span>

[<span data-ttu-id="c02fb-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c02fb-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="c02fb-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c02fb-112">Remarks</span></span>

<span data-ttu-id="c02fb-113">Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB.</span><span class="sxs-lookup"><span data-stu-id="c02fb-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="c02fb-114">Значение соответствует полю **бмсвккапабилитиес** в дескрипторе кадра видео УВК 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="c02fb-114">The value corresponds to the **bmSVCCapabilities** field in the UVC 1.5 H.264 video frame descriptor.</span></span>

<span data-ttu-id="c02fb-115">Этот атрибут также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="c02fb-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c02fb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c02fb-116">Requirements</span></span>



| <span data-ttu-id="c02fb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c02fb-117">Requirement</span></span> | <span data-ttu-id="c02fb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c02fb-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c02fb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c02fb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c02fb-120">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="c02fb-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c02fb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c02fb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c02fb-122">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c02fb-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c02fb-123">Header</span><span class="sxs-lookup"><span data-stu-id="c02fb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c02fb-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c02fb-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c02fb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c02fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c02fb-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c02fb-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c02fb-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c02fb-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




