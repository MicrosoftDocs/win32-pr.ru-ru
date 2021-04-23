---
description: Описывает, как чрома был выборке для типа видеоматериала Икбкр.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: Атрибут MF_MT_VIDEO_CHROMA_SITING (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa634cf9a9ca7f5c292eb0cf06c6a1a14c788d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712254"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a><span data-ttu-id="cd633-103">\_ \_ \_ \_ Атрибут чрома заблокировано (MF MT Video)</span><span class="sxs-lookup"><span data-stu-id="cd633-103">MF\_MT\_VIDEO\_CHROMA\_SITING attribute</span></span>

<span data-ttu-id="cd633-104">Описывает, как чрома был выполнен выборку для типа видеоматериалов И'кб'кр.</span><span class="sxs-lookup"><span data-stu-id="cd633-104">Describes how chroma was sampled for a Y'Cb'Cr' video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="cd633-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cd633-105">Data type</span></span>

<span data-ttu-id="cd633-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cd633-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cd633-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd633-107">Remarks</span></span>

<span data-ttu-id="cd633-108">Значение этого атрибута является побитовым оператором **или** для флагов перечисления [**мфвидеочромасубсамплинг**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) .</span><span class="sxs-lookup"><span data-stu-id="cd633-108">The value of this attribute is a bitwise **OR** of flags from the [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) enumeration.</span></span>

<span data-ttu-id="cd633-109">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="cd633-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd633-110">Требования</span><span class="sxs-lookup"><span data-stu-id="cd633-110">Requirements</span></span>



| <span data-ttu-id="cd633-111">Требование</span><span class="sxs-lookup"><span data-stu-id="cd633-111">Requirement</span></span> | <span data-ttu-id="cd633-112">Значение</span><span class="sxs-lookup"><span data-stu-id="cd633-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd633-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd633-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cd633-114">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="cd633-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="cd633-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd633-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cd633-116">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="cd633-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="cd633-117">Header</span><span class="sxs-lookup"><span data-stu-id="cd633-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd633-118"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd633-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd633-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd633-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd633-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cd633-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cd633-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="cd633-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="cd633-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="cd633-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="cd633-123">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="cd633-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="cd633-124">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cd633-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="cd633-125">Расширенные сведения о цвете</span><span class="sxs-lookup"><span data-stu-id="cd633-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




