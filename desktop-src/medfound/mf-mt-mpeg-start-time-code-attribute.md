---
description: Код времени запуска Group-of-Pictures (GOP) для типа видеоклипа MPEG-1 или MPEG-2.
ms.assetid: 8313b83c-5a0a-4aaa-bdc8-58a987c329c7
title: Атрибут MF_MT_MPEG_START_TIME_CODE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b19a041dbcd791359d704b407445779927d0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712406"
---
# <a name="mf_mt_mpeg_start_time_code-attribute"></a><span data-ttu-id="c0267-103">\_ \_ \_ \_ Атрибут кода времени начала MF MT MPEG \_</span><span class="sxs-lookup"><span data-stu-id="c0267-103">MF\_MT\_MPEG\_START\_TIME\_CODE attribute</span></span>

<span data-ttu-id="c0267-104">Код времени запуска Group-of-Pictures (GOP) для типа видеоклипа MPEG-1 или MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="c0267-104">Group-of-pictures (GOP) start time code, for an MPEG-1 or MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="c0267-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c0267-105">Data type</span></span>

<span data-ttu-id="c0267-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c0267-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c0267-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0267-107">Remarks</span></span>

<span data-ttu-id="c0267-108">Этот атрибут соответствует элементу **двстарттимекоде** в структурах [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) и [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="c0267-108">This attribute corresponds to the **dwStartTimeCode** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) and [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structures.</span></span>

<span data-ttu-id="c0267-109">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="c0267-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0267-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c0267-110">Requirements</span></span>



| <span data-ttu-id="c0267-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c0267-111">Requirement</span></span> | <span data-ttu-id="c0267-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c0267-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0267-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0267-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c0267-114">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="c0267-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c0267-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0267-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c0267-116">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c0267-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c0267-117">Header</span><span class="sxs-lookup"><span data-stu-id="c0267-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0267-118"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0267-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0267-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0267-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0267-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0267-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c0267-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="c0267-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c0267-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c0267-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c0267-123">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c0267-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c0267-124">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c0267-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="c0267-125">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0267-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 
