---
description: Для типа видеоматериала указывает, как трехмерные видеокадры хранятся в памяти.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: Атрибут MF_MT_VIDEO_3D_FORMAT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674192"
---
# <a name="mf_mt_video_3d_format-attribute"></a><span data-ttu-id="980a9-103">\_ \_ \_ Атрибут трехмерного формата видео MF MT \_</span><span class="sxs-lookup"><span data-stu-id="980a9-103">MF\_MT\_VIDEO\_3D\_FORMAT attribute</span></span>

<span data-ttu-id="980a9-104">Для типа видеоматериала указывает, как трехмерные видеокадры хранятся в памяти.</span><span class="sxs-lookup"><span data-stu-id="980a9-104">For a video media type, specifies how 3D video frames are stored in memory.</span></span>

## <a name="data-type"></a><span data-ttu-id="980a9-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="980a9-105">Data type</span></span>

<span data-ttu-id="980a9-106">**MFVideo3DFormat** хранится как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="980a9-106">**MFVideo3DFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="980a9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="980a9-107">Remarks</span></span>

<span data-ttu-id="980a9-108">Значение этого атрибута является членом перечисления [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) .</span><span class="sxs-lookup"><span data-stu-id="980a9-108">The value of this attribute is a member of the [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) enumeration.</span></span> <span data-ttu-id="980a9-109">Атрибут применяется только в том случае, если атрибут [ \_ \_ \_ 3D-видео MF](mf-mt-video-3d.md) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="980a9-109">The attribute applies only if the [MF\_MT\_VIDEO\_3D](mf-mt-video-3d.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="980a9-110">Этот атрибут необходим для несжатых трехмерных видеоформатов.</span><span class="sxs-lookup"><span data-stu-id="980a9-110">This attribute is required for uncompressed 3D video formats.</span></span> <span data-ttu-id="980a9-111">Это необязательно для сжатого трехмерного видео.</span><span class="sxs-lookup"><span data-stu-id="980a9-111">It is optional for compressed 3D video.</span></span> <span data-ttu-id="980a9-112">Источник мультимедиа, который доставляет закодированные кадры, может иметь возможность установить атрибут на основе информации в контейнере файлов.</span><span class="sxs-lookup"><span data-stu-id="980a9-112">A media source that delivers encoded frames might be able to set the attribute, based on information in the file container.</span></span> <span data-ttu-id="980a9-113">В противном случае атрибут должен быть задан декодером в выходном типе носителя декодера.</span><span class="sxs-lookup"><span data-stu-id="980a9-113">Otherwise, the attribute should be set by the decoder in the decoder's output media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="980a9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="980a9-114">Requirements</span></span>



| <span data-ttu-id="980a9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="980a9-115">Requirement</span></span> | <span data-ttu-id="980a9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="980a9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="980a9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="980a9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="980a9-118">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="980a9-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="980a9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="980a9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="980a9-120">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="980a9-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="980a9-121">Header</span><span class="sxs-lookup"><span data-stu-id="980a9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="980a9-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="980a9-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="980a9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="980a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980a9-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="980a9-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




