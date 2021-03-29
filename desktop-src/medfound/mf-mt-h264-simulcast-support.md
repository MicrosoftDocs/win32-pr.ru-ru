---
description: Указывает количество конечных точек потоковой передачи и число поддерживаемых потоков для кодировщика УВК H. 264.
ms.assetid: 343EC59E-30E5-4F37-8B05-60EF51717835
title: Атрибут MF_MT_H264_SIMULCAST_SUPPORT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879490c6984186cf45971d2b122f0c2217b0f164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897518"
---
# <a name="mf_mt_h264_simulcast_support-attribute"></a><span data-ttu-id="632fd-103">\_Атрибут поддержки MF MT \_ H264 Single bitrate \_ транслироваться \_</span><span class="sxs-lookup"><span data-stu-id="632fd-103">MF\_MT\_H264\_SIMULCAST\_SUPPORT attribute</span></span>

<span data-ttu-id="632fd-104">Указывает количество конечных точек потоковой передачи и число поддерживаемых потоков для кодировщика УВК H. 264.</span><span class="sxs-lookup"><span data-stu-id="632fd-104">Specifies the number of streaming endpoints and the number of supported streams for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="632fd-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="632fd-105">Data type</span></span>

<span data-ttu-id="632fd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="632fd-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="632fd-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="632fd-107">Get/set</span></span>

<span data-ttu-id="632fd-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="632fd-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="632fd-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="632fd-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="632fd-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="632fd-110">Applies to</span></span>

[<span data-ttu-id="632fd-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="632fd-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="632fd-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="632fd-112">Remarks</span></span>

<span data-ttu-id="632fd-113">Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB.</span><span class="sxs-lookup"><span data-stu-id="632fd-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="632fd-114">Значение соответствует полю **бсимулкастсуппорт** в дескрипторе формата видео УВК 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="632fd-114">The value corresponds to the **bSimulcastSupport** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="632fd-115">Этот атрибут также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="632fd-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="632fd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="632fd-116">Requirements</span></span>



| <span data-ttu-id="632fd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="632fd-117">Requirement</span></span> | <span data-ttu-id="632fd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="632fd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="632fd-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="632fd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="632fd-120">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="632fd-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="632fd-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="632fd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="632fd-122">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="632fd-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="632fd-123">Header</span><span class="sxs-lookup"><span data-stu-id="632fd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="632fd-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="632fd-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="632fd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="632fd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="632fd-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="632fd-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="632fd-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="632fd-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




