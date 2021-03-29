---
description: Указывает тип носителя, независимо от других выборок в потоке.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: Атрибут MF_MT_ALL_SAMPLES_INDEPENDENT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647235"
---
# <a name="mf_mt_all_samples_independent-attribute"></a><span data-ttu-id="00ac7-103">MF \_ \_ все \_ примеры \_ независимых атрибутов</span><span class="sxs-lookup"><span data-stu-id="00ac7-103">MF\_MT\_ALL\_SAMPLES\_INDEPENDENT attribute</span></span>

<span data-ttu-id="00ac7-104">Указывает тип носителя, независимо от других выборок в потоке.</span><span class="sxs-lookup"><span data-stu-id="00ac7-104">Specifies for a media type whether each sample is independent of the other samples in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="00ac7-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="00ac7-105">Data type</span></span>

<span data-ttu-id="00ac7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="00ac7-106">**UINT32**</span></span>

<span data-ttu-id="00ac7-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="00ac7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00ac7-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00ac7-108">Remarks</span></span>

<span data-ttu-id="00ac7-109">Если этот атрибут имеет **значение false**, некоторые примеры нельзя использовать без ссылки на другие примеры в потоке.</span><span class="sxs-lookup"><span data-stu-id="00ac7-109">If this attribute is **FALSE**, some samples cannot be used without referring to other samples in the stream.</span></span> <span data-ttu-id="00ac7-110">Например, если видеоформат содержит разностные кадры, этот атрибут должен иметь **значение false**.</span><span class="sxs-lookup"><span data-stu-id="00ac7-110">For example, if a video format contains delta frames, this attribute should be **FALSE**.</span></span>

<span data-ttu-id="00ac7-111">Этот атрибут соответствует полю **бтемпоралкомпрессион** в структуре [**\_ \_ типа мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="00ac7-111">This attribute corresponds to the **bTemporalCompression** field in the DirectShow [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="00ac7-112">Задайте для этого атрибута **значение true** для всех несжатых типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="00ac7-112">Set this attribute to **TRUE** for all uncompressed media types.</span></span>

<span data-ttu-id="00ac7-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="00ac7-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="00ac7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="00ac7-114">Requirements</span></span>



| <span data-ttu-id="00ac7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="00ac7-115">Requirement</span></span> | <span data-ttu-id="00ac7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="00ac7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00ac7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00ac7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="00ac7-118">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="00ac7-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="00ac7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00ac7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="00ac7-120">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="00ac7-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="00ac7-121">Header</span><span class="sxs-lookup"><span data-stu-id="00ac7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="00ac7-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="00ac7-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00ac7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00ac7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ac7-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00ac7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="00ac7-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="00ac7-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="00ac7-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="00ac7-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="00ac7-127">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="00ac7-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="00ac7-128">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="00ac7-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
