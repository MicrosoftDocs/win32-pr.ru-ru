---
description: Содержит заголовок последовательности MPEG-1 или MPEG-2 для типа видеоматериала.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: Атрибут MF_MT_MPEG_SEQUENCE_HEADER (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693302"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a><span data-ttu-id="d1a89-103">\_ \_ \_ Атрибут заголовка последовательного сервера MF MT MPEG \_</span><span class="sxs-lookup"><span data-stu-id="d1a89-103">MF\_MT\_MPEG\_SEQUENCE\_HEADER attribute</span></span>

<span data-ttu-id="d1a89-104">Содержит заголовок последовательности MPEG-1 или MPEG-2 для типа видеоматериала.</span><span class="sxs-lookup"><span data-stu-id="d1a89-104">Contains the MPEG-1 or MPEG-2 sequence header for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="d1a89-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d1a89-105">Data type</span></span>

<span data-ttu-id="d1a89-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="d1a89-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="d1a89-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1a89-107">Remarks</span></span>

<span data-ttu-id="d1a89-108">Этот атрибут соответствует элементу **двсекуенцехеадер** структуры [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) или элементу **бсекуенцехеадер** структуры [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="d1a89-108">This attribute corresponds to the **dwSequenceHeader** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure, or the **bSequenceHeader** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) structure.</span></span>

<span data-ttu-id="d1a89-109">Для видео H264 Single bitrate и H265 BLOB-объект содержит Соединенные [NAL-единицы](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) в формате приложение б, а также их начальные коды.</span><span class="sxs-lookup"><span data-stu-id="d1a89-109">For h264 and h265 video, the blob contains concatenated [NAL units](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) in Annex B format, along with their start codes.</span></span> <span data-ttu-id="d1a89-110">В частности, для H264 Single bitrate видео это SPS & PPS NAL Units.</span><span class="sxs-lookup"><span data-stu-id="d1a89-110">Specifically, for h264 video they are SPS & PPS NAL units.</span></span> <span data-ttu-id="d1a89-111">Для H265 это ВПС, SPS & PPS.</span><span class="sxs-lookup"><span data-stu-id="d1a89-111">For h265 they are VPS, SPS & PPS.</span></span>

<span data-ttu-id="d1a89-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="d1a89-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a89-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d1a89-113">Requirements</span></span>



| <span data-ttu-id="d1a89-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d1a89-114">Requirement</span></span> | <span data-ttu-id="d1a89-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a89-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a89-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1a89-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a89-117">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="d1a89-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d1a89-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1a89-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a89-119">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="d1a89-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d1a89-120">Header</span><span class="sxs-lookup"><span data-stu-id="d1a89-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1a89-121"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1a89-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a89-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1a89-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a89-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1a89-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1a89-124">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="d1a89-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="d1a89-125">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="d1a89-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="d1a89-126">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d1a89-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d1a89-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d1a89-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
