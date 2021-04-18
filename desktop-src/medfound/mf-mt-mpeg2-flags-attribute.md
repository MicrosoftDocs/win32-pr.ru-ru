---
description: Содержит различные флаги для типа мультимедиа MPEG-2.
ms.assetid: 2e1bf3e3-c005-418b-b9fd-1d43c42dad6f
title: Атрибут MF_MT_MPEG2_FLAGS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ef0a0def9c3e5413ec9b9bf7568fcbe9add851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712865"
---
# <a name="mf_mt_mpeg2_flags-attribute"></a><span data-ttu-id="2f6df-103">\_ \_ \_ Атрибут флагов MF MT MPEG2</span><span class="sxs-lookup"><span data-stu-id="2f6df-103">MF\_MT\_MPEG2\_FLAGS attribute</span></span>

<span data-ttu-id="2f6df-104">Содержит различные флаги для типа мультимедиа MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="2f6df-104">Contains miscellaneous flags for an MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="2f6df-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2f6df-105">Data type</span></span>

<span data-ttu-id="2f6df-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2f6df-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2f6df-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f6df-107">Remarks</span></span>

<span data-ttu-id="2f6df-108">Этот атрибут соответствует элементу **dwFlags** структуры [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="2f6df-108">This attribute corresponds to the **dwFlags** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="2f6df-109">Список допустимых флагов см. в документации по **MPEG2VIDEOINFO**.</span><span class="sxs-lookup"><span data-stu-id="2f6df-109">For a list of valid flags, see the documentation for **MPEG2VIDEOINFO**.</span></span>

<span data-ttu-id="2f6df-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="2f6df-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f6df-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2f6df-111">Requirements</span></span>



| <span data-ttu-id="2f6df-112">Требование</span><span class="sxs-lookup"><span data-stu-id="2f6df-112">Requirement</span></span> | <span data-ttu-id="2f6df-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2f6df-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6df-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f6df-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2f6df-115">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="2f6df-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2f6df-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f6df-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2f6df-117">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="2f6df-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2f6df-118">Header</span><span class="sxs-lookup"><span data-stu-id="2f6df-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f6df-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f6df-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f6df-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f6df-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f6df-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f6df-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f6df-122">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="2f6df-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2f6df-123">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2f6df-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2f6df-124">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="2f6df-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2f6df-125">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2f6df-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
