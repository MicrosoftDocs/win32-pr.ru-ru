---
description: Указывает профиль MPEG-2 или H. 264 в типе видеоматериала.
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: Атрибут MF_MT_MPEG2_PROFILE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911188"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a><span data-ttu-id="447dd-103">\_ \_ Атрибут профиля MF MT MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="447dd-103">MF\_MT\_MPEG2\_PROFILE attribute</span></span>

<span data-ttu-id="447dd-104">Указывает профиль MPEG-2 или H. 264 в типе видеоматериала.</span><span class="sxs-lookup"><span data-stu-id="447dd-104">Specifies the MPEG-2 or H.264 profile in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="447dd-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="447dd-105">Data type</span></span>

<span data-ttu-id="447dd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="447dd-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="447dd-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="447dd-107">Remarks</span></span>

<span data-ttu-id="447dd-108">Для видео MPEG-2 значение этого атрибута является членом перечисления [**\_ MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) .</span><span class="sxs-lookup"><span data-stu-id="447dd-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) enumeration.</span></span>

<span data-ttu-id="447dd-109">Для видео H. 264 значение является членом перечисления [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="447dd-109">For H.264 video, the value is a member of the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span>

<span data-ttu-id="447dd-110">Этот атрибут соответствует элементу **двпрофиле** структуры [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="447dd-110">This attribute corresponds to the **dwProfile** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="447dd-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="447dd-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="447dd-112">Требования</span><span class="sxs-lookup"><span data-stu-id="447dd-112">Requirements</span></span>



| <span data-ttu-id="447dd-113">Требование</span><span class="sxs-lookup"><span data-stu-id="447dd-113">Requirement</span></span> | <span data-ttu-id="447dd-114">Значение</span><span class="sxs-lookup"><span data-stu-id="447dd-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="447dd-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="447dd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="447dd-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="447dd-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="447dd-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="447dd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="447dd-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="447dd-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="447dd-119">Header</span><span class="sxs-lookup"><span data-stu-id="447dd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="447dd-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="447dd-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="447dd-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="447dd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="447dd-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="447dd-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="447dd-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="447dd-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="447dd-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="447dd-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="447dd-125">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="447dd-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="447dd-126">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="447dd-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
