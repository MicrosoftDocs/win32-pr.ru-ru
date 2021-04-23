---
description: Указывает, требует ли тип видеоклипа принудительное применение защиты от копирования.
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: Атрибут MF_MT_DRM_FLAGS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ef771cb72050b2273d822ce799092ce51e64c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712407"
---
# <a name="mf_mt_drm_flags-attribute"></a><span data-ttu-id="7d8c2-103">\_ \_ \_ Атрибут флагов DRM MF MT</span><span class="sxs-lookup"><span data-stu-id="7d8c2-103">MF\_MT\_DRM\_FLAGS attribute</span></span>

<span data-ttu-id="7d8c2-104">Указывает, требует ли тип видеоклипа принудительное применение защиты от копирования.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-104">Specifies whether a video media type requires the enforcement of copy protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="7d8c2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7d8c2-105">Data type</span></span>

<span data-ttu-id="7d8c2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7d8c2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7d8c2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d8c2-107">Remarks</span></span>

<span data-ttu-id="7d8c2-108">Значение этого атрибута является членом перечисления [**мфвидеодрмфлагс**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) .</span><span class="sxs-lookup"><span data-stu-id="7d8c2-108">The value of this attribute is a member of the [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) enumeration.</span></span>

<span data-ttu-id="7d8c2-109">Этот атрибут обеспечивает указание для приложения.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-109">This attribute provides a hint to the application.</span></span> <span data-ttu-id="7d8c2-110">Он не используется для обеспечения защиты от копирования или для указания механизма защиты от копирования.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-110">It is not used to enforce copy protection or to specify the copy protection mechanism.</span></span>

<span data-ttu-id="7d8c2-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d8c2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7d8c2-112">Requirements</span></span>



| <span data-ttu-id="7d8c2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7d8c2-113">Requirement</span></span> | <span data-ttu-id="7d8c2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7d8c2-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8c2-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d8c2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7d8c2-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="7d8c2-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7d8c2-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d8c2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7d8c2-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="7d8c2-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7d8c2-119">Header</span><span class="sxs-lookup"><span data-stu-id="7d8c2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d8c2-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d8c2-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d8c2-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d8c2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8c2-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7d8c2-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7d8c2-123">MF \_ - \_ защищенный SD</span><span class="sxs-lookup"><span data-stu-id="7d8c2-123">MF\_SD\_PROTECTED</span></span>](mf-sd-protected-attribute.md)
</dt> <dt>

[<span data-ttu-id="7d8c2-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="7d8c2-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7d8c2-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7d8c2-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7d8c2-126">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="7d8c2-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7d8c2-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7d8c2-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




