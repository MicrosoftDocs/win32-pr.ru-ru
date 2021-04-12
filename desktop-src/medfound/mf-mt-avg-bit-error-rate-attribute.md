---
description: Частота ошибок данных в битах в секунду для типа видеоклипа.
ms.assetid: 90433ff4-a563-4751-86d9-caac0cc58194
title: Атрибут MF_MT_AVG_BIT_ERROR_RATE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21eb33d1bc1636dd047dbd56ce6b7ad3a683f356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263622"
---
# <a name="mf_mt_avg_bit_error_rate-attribute"></a><span data-ttu-id="19c97-103">\_ \_ \_ Атрибут частоты среднего разряда \_ ошибок \_ MF MT</span><span class="sxs-lookup"><span data-stu-id="19c97-103">MF\_MT\_AVG\_BIT\_ERROR\_RATE attribute</span></span>

<span data-ttu-id="19c97-104">Частота ошибок данных в битах в секунду для типа видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="19c97-104">Data error rate, in bit errors per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="19c97-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="19c97-105">Data type</span></span>

<span data-ttu-id="19c97-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="19c97-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="19c97-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19c97-107">Remarks</span></span>

<span data-ttu-id="19c97-108">Этот атрибут соответствует элементу **двбитерроррате** в структурах [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) и [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="19c97-108">This attribute corresponds to the **dwBitErrorRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="19c97-109">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="19c97-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="19c97-110">Требования</span><span class="sxs-lookup"><span data-stu-id="19c97-110">Requirements</span></span>



| <span data-ttu-id="19c97-111">Требование</span><span class="sxs-lookup"><span data-stu-id="19c97-111">Requirement</span></span> | <span data-ttu-id="19c97-112">Значение</span><span class="sxs-lookup"><span data-stu-id="19c97-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19c97-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19c97-113">Minimum supported client</span></span><br/> | <span data-ttu-id="19c97-114">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="19c97-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="19c97-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19c97-115">Minimum supported server</span></span><br/> | <span data-ttu-id="19c97-116">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="19c97-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="19c97-117">Header</span><span class="sxs-lookup"><span data-stu-id="19c97-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="19c97-118"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="19c97-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19c97-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19c97-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c97-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19c97-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="19c97-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="19c97-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="19c97-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="19c97-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="19c97-123">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="19c97-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="19c97-124">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="19c97-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
