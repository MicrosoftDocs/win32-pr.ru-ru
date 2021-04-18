---
description: Определяет отображаемый Апертура, представляющий собой область видеокадра, которая содержит допустимые данные изображения.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: Атрибут MF_MT_MINIMUM_DISPLAY_APERTURE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711155"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a><span data-ttu-id="00e5f-103">\_ \_ Минимальный \_ отображаемый \_ атрибут апертуры MF</span><span class="sxs-lookup"><span data-stu-id="00e5f-103">MF\_MT\_MINIMUM\_DISPLAY\_APERTURE attribute</span></span>

<span data-ttu-id="00e5f-104">Определяет отображаемый Апертура, представляющий собой область видеокадра, которая содержит допустимые данные изображения.</span><span class="sxs-lookup"><span data-stu-id="00e5f-104">Defines the display aperture, which is the region of a video frame that contains valid image data.</span></span>

## <a name="data-type"></a><span data-ttu-id="00e5f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="00e5f-105">Data type</span></span>

<span data-ttu-id="00e5f-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="00e5f-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="00e5f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00e5f-107">Remarks</span></span>

<span data-ttu-id="00e5f-108">Значение атрибута является структурой [**мфвидеоареа**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="00e5f-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="00e5f-109">Минимальный отображаемый Апертура — это область, которая содержит действительную часть сигнала.</span><span class="sxs-lookup"><span data-stu-id="00e5f-109">The minimum display aperture is the region that contains the valid portion of the signal.</span></span> <span data-ttu-id="00e5f-110">Пиксели за пределами апертуры содержат недопустимые данные и не должны отображаться.</span><span class="sxs-lookup"><span data-stu-id="00e5f-110">The pixels outside the aperture contain invalid data and should not be displayed.</span></span>

<span data-ttu-id="00e5f-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="00e5f-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="00e5f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="00e5f-112">Requirements</span></span>



| <span data-ttu-id="00e5f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="00e5f-113">Requirement</span></span> | <span data-ttu-id="00e5f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="00e5f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00e5f-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00e5f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="00e5f-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="00e5f-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="00e5f-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00e5f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="00e5f-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="00e5f-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="00e5f-119">Header</span><span class="sxs-lookup"><span data-stu-id="00e5f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="00e5f-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="00e5f-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00e5f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00e5f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e5f-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00e5f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="00e5f-123">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="00e5f-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="00e5f-124">Пропорции рисунка</span><span class="sxs-lookup"><span data-stu-id="00e5f-124">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="00e5f-125">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="00e5f-125">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="00e5f-126">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="00e5f-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="00e5f-127">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="00e5f-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="00e5f-128">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="00e5f-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="00e5f-129">**\_ \_ геометрическое \_ Апертура MF**</span><span class="sxs-lookup"><span data-stu-id="00e5f-129">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="00e5f-130">**\_ \_ \_ Апертура для поиска MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="00e5f-130">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




