---
description: Максимальное число кадров, которое кодировщик H. 264 принимает для ответа на команду.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: Атрибут MF_MT_H264_MAX_CODEC_CONFIG_DELAY (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a835d5b5a37be0c722f313aaf4fe8ed8aa55f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656593"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a><span data-ttu-id="7e7ce-103">\_ \_ \_ \_ \_ Атрибут задержки конфигурации кодека MF MT H264 Single bitrate \_</span><span class="sxs-lookup"><span data-stu-id="7e7ce-103">MF\_MT\_H264\_MAX\_CODEC\_CONFIG\_DELAY attribute</span></span>

<span data-ttu-id="7e7ce-104">Максимальное число кадров, которое кодировщик H. 264 принимает для ответа на команду.</span><span class="sxs-lookup"><span data-stu-id="7e7ce-104">The maximum number of frames the H.264 encoder takes to respond to a command.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e7ce-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7e7ce-105">Data type</span></span>

<span data-ttu-id="7e7ce-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7e7ce-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7e7ce-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="7e7ce-107">Get/set</span></span>

<span data-ttu-id="7e7ce-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7e7ce-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7e7ce-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7e7ce-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="7e7ce-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="7e7ce-110">Applies to</span></span>

[<span data-ttu-id="7e7ce-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="7e7ce-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="7e7ce-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e7ce-112">Remarks</span></span>

<span data-ttu-id="7e7ce-113">Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB.</span><span class="sxs-lookup"><span data-stu-id="7e7ce-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="7e7ce-114">Значение соответствует полю **бмакскодекконфигделай** в дескрипторе формата видео УВК 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="7e7ce-114">The value corresponds to the **bMaxCodecConfigDelay** field in the UVC 1.2 H.264 video format descriptor.</span></span>

<span data-ttu-id="7e7ce-115">Этот атрибут также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="7e7ce-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e7ce-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7e7ce-116">Requirements</span></span>



| <span data-ttu-id="7e7ce-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7e7ce-117">Requirement</span></span> | <span data-ttu-id="7e7ce-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7e7ce-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7ce-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e7ce-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7e7ce-120">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="7e7ce-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="7e7ce-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e7ce-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7e7ce-122">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="7e7ce-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7e7ce-123">Header</span><span class="sxs-lookup"><span data-stu-id="7e7ce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e7ce-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e7ce-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e7ce-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e7ce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7ce-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e7ce-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7e7ce-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7e7ce-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




