---
description: Указывает для типа носителя, имеет ли выбор фиксированный размер.
ms.assetid: 2d67864a-fd2f-400d-8a1e-e71dc1920593
title: Атрибут MF_MT_FIXED_SIZE_SAMPLES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1bb5bdd4e1330e4744902ed1b37cc55b7a67a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656571"
---
# <a name="mf_mt_fixed_size_samples-attribute"></a><span data-ttu-id="f1dc8-103">\_ \_ \_ Атрибут образцов фиксированного размера MF MT \_</span><span class="sxs-lookup"><span data-stu-id="f1dc8-103">MF\_MT\_FIXED\_SIZE\_SAMPLES attribute</span></span>

<span data-ttu-id="f1dc8-104">Указывает для типа носителя, имеет ли выбор фиксированный размер.</span><span class="sxs-lookup"><span data-stu-id="f1dc8-104">Specifies for a media type whether the samples have a fixed size.</span></span>

## <a name="data-type"></a><span data-ttu-id="f1dc8-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f1dc8-105">Data type</span></span>

<span data-ttu-id="f1dc8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f1dc8-106">**UINT32**</span></span>

<span data-ttu-id="f1dc8-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="f1dc8-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1dc8-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1dc8-108">Remarks</span></span>

<span data-ttu-id="f1dc8-109">Если этот атрибут имеет **значение true**, каждый пример в потоке имеет одинаковый размер (в байтах).</span><span class="sxs-lookup"><span data-stu-id="f1dc8-109">If this attribute is **TRUE**, every sample in the stream is the same size (in bytes).</span></span> <span data-ttu-id="f1dc8-110">В противном случае размер выборки может быть разным.</span><span class="sxs-lookup"><span data-stu-id="f1dc8-110">Otherwise, samples might vary in size.</span></span>

<span data-ttu-id="f1dc8-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="f1dc8-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1dc8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f1dc8-112">Requirements</span></span>



| <span data-ttu-id="f1dc8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f1dc8-113">Requirement</span></span> | <span data-ttu-id="f1dc8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f1dc8-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1dc8-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1dc8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f1dc8-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="f1dc8-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f1dc8-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1dc8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f1dc8-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f1dc8-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f1dc8-119">Header</span><span class="sxs-lookup"><span data-stu-id="f1dc8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1dc8-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1dc8-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1dc8-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1dc8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1dc8-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1dc8-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f1dc8-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="f1dc8-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f1dc8-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f1dc8-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f1dc8-125">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="f1dc8-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f1dc8-126">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f1dc8-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




