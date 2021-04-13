---
description: Указывает уровень MPEG-2 или H. 264 в типе видеоматериала.
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: Атрибут MF_MT_MPEG2_LEVEL (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111c4b30befb1d4b25a688d25f46f02bcef21541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265363"
---
# <a name="mf_mt_mpeg2_level-attribute"></a><span data-ttu-id="7fea1-103">\_Атрибут уровня "MF MT \_ MPEG2" \_</span><span class="sxs-lookup"><span data-stu-id="7fea1-103">MF\_MT\_MPEG2\_LEVEL attribute</span></span>

<span data-ttu-id="7fea1-104">Указывает уровень MPEG-2 или H. 264 в типе видеоматериала.</span><span class="sxs-lookup"><span data-stu-id="7fea1-104">Specifies the MPEG-2 or H.264 level in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="7fea1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7fea1-105">Data type</span></span>

<span data-ttu-id="7fea1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7fea1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7fea1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fea1-107">Remarks</span></span>

<span data-ttu-id="7fea1-108">Для видео MPEG-2 значение этого атрибута является членом перечисления [**\_ MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) .</span><span class="sxs-lookup"><span data-stu-id="7fea1-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) enumeration.</span></span>

<span data-ttu-id="7fea1-109">Для видео H. 264 значение является членом перечисления [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) .</span><span class="sxs-lookup"><span data-stu-id="7fea1-109">For H.264 video, the value is a member of the [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) enumeration.</span></span>

<span data-ttu-id="7fea1-110">Этот атрибут соответствует элементу **двлевел** структуры [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="7fea1-110">This attribute corresponds to the **dwLevel** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="7fea1-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="7fea1-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fea1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7fea1-112">Requirements</span></span>



| <span data-ttu-id="7fea1-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7fea1-113">Requirement</span></span> | <span data-ttu-id="7fea1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7fea1-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7fea1-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fea1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7fea1-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="7fea1-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7fea1-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fea1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7fea1-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="7fea1-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7fea1-119">Header</span><span class="sxs-lookup"><span data-stu-id="7fea1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fea1-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fea1-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fea1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fea1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fea1-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7fea1-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7fea1-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="7fea1-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7fea1-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7fea1-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7fea1-125">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="7fea1-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7fea1-126">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7fea1-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
