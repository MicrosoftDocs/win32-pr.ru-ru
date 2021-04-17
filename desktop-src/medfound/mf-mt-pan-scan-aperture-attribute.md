---
description: Определяет апертуру и сканирование, т. е. 4&\# 215; 3 региона видео, который должен отображаться в режиме панорамирования и сканирования.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: Атрибут MF_MT_PAN_SCAN_APERTURE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692546"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a><span data-ttu-id="f2014-103">\_ \_ \_ Атрибут апертуры развертки MF MT \_</span><span class="sxs-lookup"><span data-stu-id="f2014-103">MF\_MT\_PAN\_SCAN\_APERTURE attribute</span></span>

<span data-ttu-id="f2014-104">Определяет апертуру и сканирование, то есть 4 × 3 региона видео, который должен отображаться в режиме панорамы и сканирования.</span><span class="sxs-lookup"><span data-stu-id="f2014-104">Defines the pan/scan aperture, which is the 4×3 region of video that should be displayed in pan/scan mode.</span></span>

## <a name="data-type"></a><span data-ttu-id="f2014-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f2014-105">Data type</span></span>

<span data-ttu-id="f2014-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="f2014-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="f2014-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2014-107">Remarks</span></span>

<span data-ttu-id="f2014-108">Значение атрибута является структурой [**мфвидеоареа**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="f2014-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="f2014-109">Этот атрибут используется для обрезки широкоэкранных видео до 4:3 пропорций.</span><span class="sxs-lookup"><span data-stu-id="f2014-109">This attribute is used to crop widescreen video to a 4:3 aspect ratio.</span></span> <span data-ttu-id="f2014-110">Апертура/развертка используется только в режиме панорамирования/развертки, который включается путем установки атрибута « [**\_ \_ \_ \_ Включить сканирование MF MT Pan**](mf-mt-pan-scan-enabled-attribute.md) » в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f2014-110">The pan/scan aperture is used only in pan/scan mode, which is enabled by setting the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="f2014-111">Если режим Pan/Scan не включен, используйте апертуру экрана, заданную атрибутом [**\_ \_ \_ \_ апертуры по крайней мере в MF MT**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="f2014-111">If pan/scan mode is not enabled, use the display aperture, specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="f2014-112">Если этот атрибут не задан, то раскадровка панорамы и развертки считается кадром всего видео.</span><span class="sxs-lookup"><span data-stu-id="f2014-112">If this attribute is not set, the pan/scan aperture is assumed to be the entire video frame.</span></span>

<span data-ttu-id="f2014-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="f2014-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2014-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f2014-114">Requirements</span></span>



| <span data-ttu-id="f2014-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f2014-115">Requirement</span></span> | <span data-ttu-id="f2014-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f2014-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2014-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2014-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2014-118">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="f2014-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f2014-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2014-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2014-120">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f2014-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f2014-121">Header</span><span class="sxs-lookup"><span data-stu-id="f2014-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2014-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2014-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2014-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2014-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2014-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2014-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2014-125">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f2014-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2014-126">Пропорции рисунка</span><span class="sxs-lookup"><span data-stu-id="f2014-126">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="f2014-127">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="f2014-127">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="f2014-128">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="f2014-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="f2014-129">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="f2014-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="f2014-130">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="f2014-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f2014-131">**\_ \_ геометрическое \_ Апертура MF**</span><span class="sxs-lookup"><span data-stu-id="f2014-131">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="f2014-132">**\_ \_ Минимальный \_ \_ Апертура экрана MF MT**</span><span class="sxs-lookup"><span data-stu-id="f2014-132">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="f2014-133">**\_ \_ включена проверка панорамы MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f2014-133">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




