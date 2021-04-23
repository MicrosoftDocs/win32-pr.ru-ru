---
description: Задает пропорции выходного прямоугольника для типа видеоклипа.
ms.assetid: d7fec5fb-a1fe-4cc9-aa27-a3af0456ea8d
title: Атрибут MF_MT_PAD_CONTROL_FLAGS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02610b54b84c2470eba19eaa696f633243df347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264753"
---
# <a name="mf_mt_pad_control_flags-attribute"></a><span data-ttu-id="a6ee8-103">\_ \_ \_ Атрибут флагов элемента управления MF MT Pad \_</span><span class="sxs-lookup"><span data-stu-id="a6ee8-103">MF\_MT\_PAD\_CONTROL\_FLAGS attribute</span></span>

<span data-ttu-id="a6ee8-104">Задает пропорции выходного прямоугольника для типа видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-104">Specifies the aspect ratio of the output rectangle for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a6ee8-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a6ee8-105">Data type</span></span>

<span data-ttu-id="a6ee8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a6ee8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a6ee8-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6ee8-107">Remarks</span></span>

<span data-ttu-id="a6ee8-108">Значение этого атрибута является членом перечисления [**мфвидеопадфлагс**](/windows/desktop/api/mfapi/ne-mfapi-mfvideopadflags) .</span><span class="sxs-lookup"><span data-stu-id="a6ee8-108">The value of this attribute is a member of the [**MFVideoPadFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideopadflags) enumeration.</span></span>

<span data-ttu-id="a6ee8-109">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="a6ee8-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ee8-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a6ee8-110">Requirements</span></span>



| <span data-ttu-id="a6ee8-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a6ee8-111">Requirement</span></span> | <span data-ttu-id="a6ee8-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a6ee8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ee8-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6ee8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ee8-114">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="a6ee8-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a6ee8-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6ee8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ee8-116">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="a6ee8-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a6ee8-117">Header</span><span class="sxs-lookup"><span data-stu-id="a6ee8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ee8-118"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6ee8-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ee8-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6ee8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ee8-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6ee8-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6ee8-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="a6ee8-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a6ee8-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a6ee8-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a6ee8-123">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="a6ee8-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a6ee8-124">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="a6ee8-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




