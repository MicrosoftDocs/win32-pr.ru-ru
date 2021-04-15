---
description: Основной тип GUID для типа мультимедиа.
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: Атрибут MF_MT_MAJOR_TYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c4cc02df4f89e261605c91b71ac1c80ba38b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701615"
---
# <a name="mf_mt_major_type-attribute"></a><span data-ttu-id="88d3f-103">\_ \_ Атрибут основного типа MF MT \_</span><span class="sxs-lookup"><span data-stu-id="88d3f-103">MF\_MT\_MAJOR\_TYPE attribute</span></span>

<span data-ttu-id="88d3f-104">Основной тип GUID для типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="88d3f-104">Major type GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="88d3f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="88d3f-105">Data type</span></span>

<span data-ttu-id="88d3f-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="88d3f-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="88d3f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88d3f-107">Remarks</span></span>

<span data-ttu-id="88d3f-108">Основной тип определяет общую категорию данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="88d3f-108">The major type defines the overall category of the media data.</span></span> <span data-ttu-id="88d3f-109">К основным типам относятся видео, звук, сценарий и т. д.</span><span class="sxs-lookup"><span data-stu-id="88d3f-109">Major types include video, audio, script, and so forth.</span></span> <span data-ttu-id="88d3f-110">Список возможных значений см. в разделе [основные типы носителей](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="88d3f-110">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="88d3f-111">Альтернативным способом получения этого атрибута является вызов [**имфмедиатипе:: жетмажортипе**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="88d3f-111">An alternate way to retrieve this attribute is to call [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span></span>

<span data-ttu-id="88d3f-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="88d3f-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="88d3f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="88d3f-113">Requirements</span></span>



| <span data-ttu-id="88d3f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="88d3f-114">Requirement</span></span> | <span data-ttu-id="88d3f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="88d3f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88d3f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88d3f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="88d3f-117">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="88d3f-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="88d3f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88d3f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="88d3f-119">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="88d3f-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="88d3f-120">Header</span><span class="sxs-lookup"><span data-stu-id="88d3f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="88d3f-121"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="88d3f-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88d3f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88d3f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d3f-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="88d3f-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="88d3f-124">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="88d3f-124">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="88d3f-125">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="88d3f-125">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="88d3f-126">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="88d3f-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="88d3f-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="88d3f-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




