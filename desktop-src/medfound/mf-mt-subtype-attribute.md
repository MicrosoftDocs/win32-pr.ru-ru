---
description: Идентификатор GUID подтипа для типа мультимедиа.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: Атрибут MF_MT_SUBTYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080865"
---
# <a name="mf_mt_subtype-attribute"></a><span data-ttu-id="38a1c-103">\_ \_ Атрибут подтипа MF MT</span><span class="sxs-lookup"><span data-stu-id="38a1c-103">MF\_MT\_SUBTYPE attribute</span></span>

<span data-ttu-id="38a1c-104">Идентификатор GUID подтипа для типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="38a1c-104">Subtype GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="38a1c-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="38a1c-105">Data type</span></span>

<span data-ttu-id="38a1c-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="38a1c-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="38a1c-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38a1c-107">Remarks</span></span>

<span data-ttu-id="38a1c-108">Идентификатор GUID подтипа определяет конкретный тип формата носителя в основном типе.</span><span class="sxs-lookup"><span data-stu-id="38a1c-108">The subtype GUID defines a specific media format type within a major type.</span></span> <span data-ttu-id="38a1c-109">Например, в видео подтипы включают RGB-24, RGB-32, UYVY, АЙУВ и т. д.</span><span class="sxs-lookup"><span data-stu-id="38a1c-109">For example, within video, the subtypes include RGB-24, RGB-32, UYVY, AYUV, and so forth.</span></span> <span data-ttu-id="38a1c-110">В звуке подтипы включают в себя звук PCM, Windows Media Audio 9 и т. д.</span><span class="sxs-lookup"><span data-stu-id="38a1c-110">Within audio, the subtypes include PCM audio, Windows Media Audio 9, and so forth.</span></span>

<span data-ttu-id="38a1c-111">Возможные значения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="38a1c-111">For possible values, see the following topics:</span></span>

-   [<span data-ttu-id="38a1c-112">Идентификаторы GUID для подтипов звука</span><span class="sxs-lookup"><span data-stu-id="38a1c-112">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
-   [<span data-ttu-id="38a1c-113">Идентификаторы GUID для подтипов видео</span><span class="sxs-lookup"><span data-stu-id="38a1c-113">Video Subtype GUIDs</span></span>](video-subtype-guids.md)

<span data-ttu-id="38a1c-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="38a1c-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="38a1c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="38a1c-115">Requirements</span></span>



| <span data-ttu-id="38a1c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="38a1c-116">Requirement</span></span> | <span data-ttu-id="38a1c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="38a1c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="38a1c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38a1c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38a1c-119">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="38a1c-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="38a1c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38a1c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38a1c-121">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="38a1c-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="38a1c-122">Header</span><span class="sxs-lookup"><span data-stu-id="38a1c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="38a1c-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="38a1c-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38a1c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38a1c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a1c-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="38a1c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="38a1c-126">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="38a1c-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="38a1c-127">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="38a1c-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="38a1c-128">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="38a1c-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="38a1c-129">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="38a1c-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




