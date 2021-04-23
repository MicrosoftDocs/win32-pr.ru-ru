---
description: Указывает пользовательские первичные цвета для типа видеоклипа.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: Атрибут MF_MT_CUSTOM_VIDEO_PRIMARIES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703145"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a><span data-ttu-id="cf94f-103">\_ \_ \_ Атрибут пользовательского первичного элемента видео MF MT \_</span><span class="sxs-lookup"><span data-stu-id="cf94f-103">MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="cf94f-104">Указывает пользовательские первичные цвета для типа видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="cf94f-104">Specifies custom color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="cf94f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cf94f-105">Data type</span></span>

<span data-ttu-id="cf94f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cf94f-106">**UINT32**</span></span>

<span data-ttu-id="cf94f-107">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="cf94f-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="cf94f-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf94f-108">Remarks</span></span>

<span data-ttu-id="cf94f-109">Данные атрибута являются [**пользовательской структурой \_ \_ \_ первичного цвета видео**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) .</span><span class="sxs-lookup"><span data-stu-id="cf94f-109">The attribute data is an [**MT\_CUSTOM\_VIDEO\_PRIMARIES**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) structure.</span></span>

<span data-ttu-id="cf94f-110">Этот атрибут определяет фактический цветовой объем содержимого или изображения.</span><span class="sxs-lookup"><span data-stu-id="cf94f-110">This attribute specifies the actual color volume of content or a display.</span></span> <span data-ttu-id="cf94f-111">CEA-861,3/SMPTE ST. 2086 сведения об основных томах хранятся в этом атрибуте декодерами.</span><span class="sxs-lookup"><span data-stu-id="cf94f-111">CEA-861.3 / SMPTE ST.2086 color volume mastering information is stored in this attribute by decoders.</span></span> <span data-ttu-id="cf94f-112">Обратите внимание на то, что этот атрибут не заменяет атрибут [**\_ \_ \_ первичного видео в MF MT**](mf-mt-video-primaries-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="cf94f-112">Note that this attribute does not replace the [**MF\_MT\_VIDEO\_PRIMARIES**](mf-mt-video-primaries-attribute.md)attribute.</span></span> <span data-ttu-id="cf94f-113">Этот атрибут описывает подсказку о цветовой громкости содержимого, тогда как **\_ \_ \_ первичные цвета видео MF MT** описывают цветовые цвета, в которых содержимое фактически закодировано (например, значение 1,0 в каналах R/g/B представления с плавающей запятой).</span><span class="sxs-lookup"><span data-stu-id="cf94f-113">This attribute describes a hint about the color volume of the content, whereas **MF\_MT\_VIDEO\_PRIMARIES** describes the color primaries in which the content is actually coded (e.g: the meaning of 1.0 in the R/G/B channels of a floating point representation).</span></span>

<span data-ttu-id="cf94f-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="cf94f-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf94f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cf94f-115">Requirements</span></span>



| <span data-ttu-id="cf94f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cf94f-116">Requirement</span></span> | <span data-ttu-id="cf94f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cf94f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf94f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf94f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cf94f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf94f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cf94f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf94f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cf94f-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf94f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cf94f-122">Header</span><span class="sxs-lookup"><span data-stu-id="cf94f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf94f-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf94f-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf94f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf94f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf94f-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cf94f-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cf94f-126">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cf94f-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="cf94f-127">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="cf94f-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="cf94f-128">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="cf94f-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="cf94f-129">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="cf94f-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




