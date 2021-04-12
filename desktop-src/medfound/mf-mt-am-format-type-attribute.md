---
description: Содержит идентификатор GUID формата DirectShow для типа мультимедиа.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Атрибут MF_MT_AM_FORMAT_TYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344572"
---
# <a name="mf_mt_am_format_type-attribute"></a><span data-ttu-id="cc437-103">MF \_ MT \_ , \_ Формат: \_ атрибут типа</span><span class="sxs-lookup"><span data-stu-id="cc437-103">MF\_MT\_AM\_FORMAT\_TYPE attribute</span></span>

<span data-ttu-id="cc437-104">Содержит идентификатор GUID формата DirectShow для типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cc437-104">Contains a DirectShow format GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="cc437-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc437-105">Data type</span></span>

<span data-ttu-id="cc437-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="cc437-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="cc437-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc437-107">Remarks</span></span>

<span data-ttu-id="cc437-108">Этот атрибут может быть задан при преобразовании типа носителя DirectShow в Media Foundation тип носителя.</span><span class="sxs-lookup"><span data-stu-id="cc437-108">This attribute might be set when a DirectShow media type is converted into a Media Foundation media type.</span></span> <span data-ttu-id="cc437-109">Атрибут указывает исходный тип формата DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cc437-109">The attribute indicates the original DirectShow format type.</span></span> <span data-ttu-id="cc437-110">Значение соответствует элементу форматтипе структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="cc437-110">The value corresponds to the formattype member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="cc437-111">Для звукового формата атрибут [**\_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) может содержать исходный блок формата, если тип формата DirectShow не был распознан.</span><span class="sxs-lookup"><span data-stu-id="cc437-111">For an audio format, the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute might contain the original format block, if the DirectShow format type was not recognized.</span></span>

<span data-ttu-id="cc437-112">Не устанавливайте этот атрибут для типа мультимедиа, если только не выполняется преобразование структуры формата DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cc437-112">Do not set this attribute on a media type unless you are converting a DirectShow format structure.</span></span>

<span data-ttu-id="cc437-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="cc437-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc437-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cc437-114">Requirements</span></span>



| <span data-ttu-id="cc437-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cc437-115">Requirement</span></span> | <span data-ttu-id="cc437-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cc437-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cc437-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc437-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc437-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc437-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cc437-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc437-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc437-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc437-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cc437-121">Header</span><span class="sxs-lookup"><span data-stu-id="cc437-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc437-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc437-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc437-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc437-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc437-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc437-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cc437-125">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cc437-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="cc437-126">Преобразования типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cc437-126">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="cc437-127">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="cc437-127">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="cc437-128">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="cc437-128">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="cc437-129">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="cc437-129">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="cc437-130">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="cc437-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="cc437-131">**мфкреатемедиатипефромрепресентатион**</span><span class="sxs-lookup"><span data-stu-id="cc437-131">**MFCreateMediaTypeFromRepresentation**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
