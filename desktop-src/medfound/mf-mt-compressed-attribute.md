---
description: Указывает тип носителя для сжатия данных мультимедиа.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: Атрибут MF_MT_COMPRESSED (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544343"
---
# <a name="mf_mt_compressed-attribute"></a><span data-ttu-id="ba69d-103">\_ \_ Сжатый атрибут (MF MT)</span><span class="sxs-lookup"><span data-stu-id="ba69d-103">MF\_MT\_COMPRESSED attribute</span></span>

<span data-ttu-id="ba69d-104">Указывает тип носителя для сжатия данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ba69d-104">Specifies for a media type whether the media data is compressed.</span></span>

## <a name="data-type"></a><span data-ttu-id="ba69d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ba69d-105">Data type</span></span>

<span data-ttu-id="ba69d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ba69d-106">**UINT32**</span></span>

<span data-ttu-id="ba69d-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="ba69d-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba69d-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba69d-108">Remarks</span></span>

<span data-ttu-id="ba69d-109">Если этот атрибут имеет **значение true**, то тип мультимедиа имеет сжатый формат.</span><span class="sxs-lookup"><span data-stu-id="ba69d-109">If this attribute is **TRUE**, the media type is a compressed format.</span></span> <span data-ttu-id="ba69d-110">В противном случае либо тип носителя не сжат, либо тип сжатия неизвестен.</span><span class="sxs-lookup"><span data-stu-id="ba69d-110">Otherwise, either the media type is uncompressed or the compression type is not known.</span></span>

<span data-ttu-id="ba69d-111">Этот атрибут не обязательно должен иметь значение **true** для всех сжатых форматов, поэтому приложения обычно не полагаются на этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="ba69d-111">This attribute is not guaranteed to be set to **TRUE** for all compressed formats, so applications should generally not rely this attribute.</span></span> <span data-ttu-id="ba69d-112">Самый надежный способ определить, сжимается ли формат, — поддерживать список известных форматов.</span><span class="sxs-lookup"><span data-stu-id="ba69d-112">The most reliable way to determine whether a format is compressed is to maintain a list of known formats.</span></span> <span data-ttu-id="ba69d-113">Если приложение не распознает формат, как указано в атрибуте [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) , он не должен принимать никаких сведений о сжатии формата.</span><span class="sxs-lookup"><span data-stu-id="ba69d-113">If an application does not recognize a format, as specified in the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute, it should not assume anything about the compression of the format.</span></span>

<span data-ttu-id="ba69d-114">Чтобы определить, использует ли формат временное сжатие (это означает, что некоторые примеры вычисляются как разность из предыдущих выборок), проверьте [**\_ \_ \_ \_ независимый атрибут MF MT ALL Samples**](mf-mt-all-samples-independent-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ba69d-114">To determine whether a format uses temporal compression (meaning that some samples are computed as deltas from earlier samples), check the [**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) attribute.</span></span>

<span data-ttu-id="ba69d-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="ba69d-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba69d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ba69d-116">Requirements</span></span>



| <span data-ttu-id="ba69d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ba69d-117">Requirement</span></span> | <span data-ttu-id="ba69d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ba69d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba69d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba69d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ba69d-120">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="ba69d-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ba69d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba69d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ba69d-122">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ba69d-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ba69d-123">Header</span><span class="sxs-lookup"><span data-stu-id="ba69d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba69d-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba69d-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba69d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba69d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba69d-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ba69d-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba69d-127">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="ba69d-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ba69d-128">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ba69d-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ba69d-129">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ba69d-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ba69d-130">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ba69d-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




