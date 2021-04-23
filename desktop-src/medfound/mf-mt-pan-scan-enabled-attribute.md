---
description: Указывает, включен ли режим панорамирования/развертки.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: Атрибут MF_MT_PAN_SCAN_ENABLED (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545031"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a><span data-ttu-id="90c7f-103">\_Атрибут с \_ поддержкой MF Pan \_ Scan \_</span><span class="sxs-lookup"><span data-stu-id="90c7f-103">MF\_MT\_PAN\_SCAN\_ENABLED attribute</span></span>

<span data-ttu-id="90c7f-104">Указывает, включен ли режим панорамирования/развертки.</span><span class="sxs-lookup"><span data-stu-id="90c7f-104">Specifies whether pan/scan mode is enabled.</span></span>

## <a name="data-type"></a><span data-ttu-id="90c7f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="90c7f-105">Data type</span></span>

<span data-ttu-id="90c7f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="90c7f-106">**UINT32**</span></span>

<span data-ttu-id="90c7f-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="90c7f-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90c7f-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90c7f-108">Remarks</span></span>

<span data-ttu-id="90c7f-109">Если этот атрибут имеет **значение true**, должен отображаться только регион сдвига и сканирования видео.</span><span class="sxs-lookup"><span data-stu-id="90c7f-109">If this attribute is **TRUE**, only the pan/scan region of the video should be displayed.</span></span> <span data-ttu-id="90c7f-110">Регион сдвига и сканирования задается атрибутом [**\_ \_ \_ \_ апертуры панорамного просмотра в MF-MT**](mf-mt-pan-scan-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="90c7f-110">The pan/scan region is specified by the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="90c7f-111">Если этот атрибут имеет **значение false** или не задан, отображается весь отображаемый Апертура видео.</span><span class="sxs-lookup"><span data-stu-id="90c7f-111">If this attribute is **FALSE** or not set, the entire display aperture of the video should be displayed.</span></span> <span data-ttu-id="90c7f-112">Отображаемый Апертура определяется с помощью атрибута « [**\_ \_ Минимальный \_ отображаемый \_ Апертура MF MT**](mf-mt-minimum-display-aperture-attribute.md) ».</span><span class="sxs-lookup"><span data-stu-id="90c7f-112">The display aperture is specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="90c7f-113">Если для этого атрибута задано значение **true**, также следует задать для атрибута [**« \_ \_ \_ \_ Апертура панорамного сдвига MF**](mf-mt-pan-scan-aperture-attribute.md) ».</span><span class="sxs-lookup"><span data-stu-id="90c7f-113">If you set this attribute to **TRUE**, also set the value of the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="90c7f-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="90c7f-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="90c7f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="90c7f-115">Requirements</span></span>



| <span data-ttu-id="90c7f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="90c7f-116">Requirement</span></span> | <span data-ttu-id="90c7f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="90c7f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90c7f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90c7f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="90c7f-119">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="90c7f-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="90c7f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90c7f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="90c7f-121">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="90c7f-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="90c7f-122">Header</span><span class="sxs-lookup"><span data-stu-id="90c7f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="90c7f-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="90c7f-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90c7f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90c7f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c7f-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90c7f-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="90c7f-126">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="90c7f-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="90c7f-127">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="90c7f-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="90c7f-128">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="90c7f-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="90c7f-129">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="90c7f-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="90c7f-130">Пропорции рисунка</span><span class="sxs-lookup"><span data-stu-id="90c7f-130">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




