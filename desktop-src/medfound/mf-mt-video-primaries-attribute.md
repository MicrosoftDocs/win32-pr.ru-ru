---
description: Задает первичные цвета для типа видеоклипа.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: Атрибут MF_MT_VIDEO_PRIMARIES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712864"
---
# <a name="mf_mt_video_primaries-attribute"></a><span data-ttu-id="2bdb4-103">\_ \_ \_ Атрибут первичного видео MF MT</span><span class="sxs-lookup"><span data-stu-id="2bdb4-103">MF\_MT\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="2bdb4-104">Задает первичные цвета для типа видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="2bdb4-104">Specifies the color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="2bdb4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2bdb4-105">Data type</span></span>

<span data-ttu-id="2bdb4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2bdb4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2bdb4-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bdb4-107">Remarks</span></span>

<span data-ttu-id="2bdb4-108">Значение этого атрибута является членом перечисления [**мфвидеопримариес**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) .</span><span class="sxs-lookup"><span data-stu-id="2bdb4-108">The value of this attribute is a member of the [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration.</span></span>

<span data-ttu-id="2bdb4-109">Перечисление [**мфвидеопримариес**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) определяет первичные цвета, связанные с определенными распространенными стандартами видео.</span><span class="sxs-lookup"><span data-stu-id="2bdb4-109">The [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration identifies color primaries associated with certain common video standards.</span></span> <span data-ttu-id="2bdb4-110">Если тип мультимедиа использует первичные цвета, которые не определены в перечислении **мфвидеопримариес** , задайте вместо этого атрибута атрибут " [**\_ \_ пользовательские \_ \_ первичные цвета" MF MT**](mf-mt-custom-video-primaries-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2bdb4-110">If the media type uses color primaries that are not identified in the **MFVideoPrimaries** enumeration, set the [**MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES**](mf-mt-custom-video-primaries-attribute.md) attribute instead of this attribute.</span></span>

<span data-ttu-id="2bdb4-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="2bdb4-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bdb4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2bdb4-112">Requirements</span></span>



| <span data-ttu-id="2bdb4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2bdb4-113">Requirement</span></span> | <span data-ttu-id="2bdb4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2bdb4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2bdb4-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2bdb4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2bdb4-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="2bdb4-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2bdb4-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2bdb4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2bdb4-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="2bdb4-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2bdb4-119">Header</span><span class="sxs-lookup"><span data-stu-id="2bdb4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bdb4-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bdb4-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bdb4-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bdb4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bdb4-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2bdb4-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2bdb4-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="2bdb4-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2bdb4-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2bdb4-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2bdb4-125">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="2bdb4-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2bdb4-126">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2bdb4-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="2bdb4-127">Расширенные сведения о цвете</span><span class="sxs-lookup"><span data-stu-id="2bdb4-127">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




