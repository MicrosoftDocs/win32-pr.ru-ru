---
description: Пропорции пикселя для типа видеоклипа.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: Атрибут MF_MT_PIXEL_ASPECT_RATIO (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542159"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a><span data-ttu-id="32fbb-103">\_ \_ \_ Атрибут соотношения сторон MF MT пикселей \_</span><span class="sxs-lookup"><span data-stu-id="32fbb-103">MF\_MT\_PIXEL\_ASPECT\_RATIO attribute</span></span>

<span data-ttu-id="32fbb-104">Пропорции пикселя для типа видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="32fbb-104">Pixel aspect ratio for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="32fbb-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="32fbb-105">Data type</span></span>

<span data-ttu-id="32fbb-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="32fbb-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="32fbb-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32fbb-107">Remarks</span></span>

<span data-ttu-id="32fbb-108">Верхние 32 бит содержат числитель с пропорциями в пикселях, а младшие 32 бита содержат знаменатель.</span><span class="sxs-lookup"><span data-stu-id="32fbb-108">The upper 32 bits contain the numerator of the pixel aspect ratio and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="32fbb-109">Числитель является горизонтальным компонентом пропорций; знаменатель является вертикальным компонентом.</span><span class="sxs-lookup"><span data-stu-id="32fbb-109">The numerator is the horizontal component of the aspect ratio; the denominator is the vertical component.</span></span>

<span data-ttu-id="32fbb-110">Чтобы задать этот атрибут, используйте функцию [**мфсетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="32fbb-110">To set this attribute, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="32fbb-111">Чтобы получить этот атрибут, используйте функцию [**мфжетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="32fbb-111">To get this attribute, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="32fbb-112">Соотношение пиксельных пропорций описывает форму пикселов в отображаемом видеоизображении.</span><span class="sxs-lookup"><span data-stu-id="32fbb-112">The pixel aspect ratio describes the shape of the pixels in the displayed video image.</span></span> <span data-ttu-id="32fbb-113">Установите этот атрибут, если изображение содержит неквадратные пикселы.</span><span class="sxs-lookup"><span data-stu-id="32fbb-113">Set this attribute if the image has non-square pixels.</span></span> <span data-ttu-id="32fbb-114">Для правильной работы на устройстве вывода с квадратными пикселами изображение должно масштабироваться путем обратного пропорций изображения.</span><span class="sxs-lookup"><span data-stu-id="32fbb-114">To display correctly on a display device with square pixels, the image must be scaled by the inverse of the image's pixel aspect ratio.</span></span>

<span data-ttu-id="32fbb-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="32fbb-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="32fbb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="32fbb-116">Requirements</span></span>



| <span data-ttu-id="32fbb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="32fbb-117">Requirement</span></span> | <span data-ttu-id="32fbb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="32fbb-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32fbb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32fbb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="32fbb-120">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="32fbb-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="32fbb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32fbb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="32fbb-122">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="32fbb-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="32fbb-123">Header</span><span class="sxs-lookup"><span data-stu-id="32fbb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="32fbb-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="32fbb-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32fbb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32fbb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32fbb-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="32fbb-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="32fbb-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="32fbb-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="32fbb-128">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="32fbb-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="32fbb-129">Пропорции рисунка</span><span class="sxs-lookup"><span data-stu-id="32fbb-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




