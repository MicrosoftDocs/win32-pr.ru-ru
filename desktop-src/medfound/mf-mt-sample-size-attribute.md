---
description: Задает размер каждого образца в байтах в типе носителя.
ms.assetid: 4c28f73d-ff40-4eb9-a45f-57a60df719c6
title: Атрибут MF_MT_SAMPLE_SIZE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bb897524dac5f73f4d4553f8e77e02ef473f611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683118"
---
# <a name="mf_mt_sample_size-attribute"></a><span data-ttu-id="e3dc5-103">\_ \_ Атрибут размера для примера MF MT \_</span><span class="sxs-lookup"><span data-stu-id="e3dc5-103">MF\_MT\_SAMPLE\_SIZE attribute</span></span>

<span data-ttu-id="e3dc5-104">Задает размер каждого образца в байтах в типе носителя.</span><span class="sxs-lookup"><span data-stu-id="e3dc5-104">Specifies the size of each sample, in bytes, in a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3dc5-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e3dc5-105">Data type</span></span>

<span data-ttu-id="e3dc5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3dc5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e3dc5-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3dc5-107">Remarks</span></span>

<span data-ttu-id="e3dc5-108">Этот атрибут допустим только в том случае, если атрибуту [**\_ \_ \_ \_ SAMPLED size с фиксированным размером MF**](mf-mt-fixed-size-samples-attribute.md) присвоено **значение true**.</span><span class="sxs-lookup"><span data-stu-id="e3dc5-108">This attribute is valid only if the [**MF\_MT\_FIXED\_SIZE\_SAMPLES**](mf-mt-fixed-size-samples-attribute.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="e3dc5-109">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="e3dc5-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3dc5-110">Требования</span><span class="sxs-lookup"><span data-stu-id="e3dc5-110">Requirements</span></span>



| <span data-ttu-id="e3dc5-111">Требование</span><span class="sxs-lookup"><span data-stu-id="e3dc5-111">Requirement</span></span> | <span data-ttu-id="e3dc5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e3dc5-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3dc5-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3dc5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e3dc5-114">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="e3dc5-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e3dc5-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3dc5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e3dc5-116">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="e3dc5-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e3dc5-117">Header</span><span class="sxs-lookup"><span data-stu-id="e3dc5-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3dc5-118"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc5-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3dc5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3dc5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3dc5-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3dc5-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e3dc5-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3dc5-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e3dc5-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e3dc5-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e3dc5-123">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="e3dc5-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="e3dc5-124">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="e3dc5-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




