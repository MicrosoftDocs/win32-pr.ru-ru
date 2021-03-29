---
description: Когда источник мультимедиа запрашивает новый темп воспроизведения, этот атрибут указывает, запрашиваются ли в источнике тонкости. Определение тонкости см. в разделе сведения об управлении скоростью.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: Атрибут MF_EVENT_DO_THINNING (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991235"
---
# <a name="mf_event_do_thinning-attribute"></a><span data-ttu-id="4fed9-104">\_Событие MF \_ — \_ тонкий атрибут</span><span class="sxs-lookup"><span data-stu-id="4fed9-104">MF\_EVENT\_DO\_THINNING attribute</span></span>

<span data-ttu-id="4fed9-105">Когда источник мультимедиа запрашивает новый темп воспроизведения, этот атрибут указывает, запрашиваются ли в источнике тонкости.</span><span class="sxs-lookup"><span data-stu-id="4fed9-105">When a media source requests a new playback rate, this attribute specifies whether the source also requests thinning.</span></span> <span data-ttu-id="4fed9-106">Определение тонкости см. в разделе [сведения об управлении скоростью](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="4fed9-106">For a definition of thinning, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="4fed9-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4fed9-107">Data type</span></span>

<span data-ttu-id="4fed9-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4fed9-108">**UINT32**</span></span>

<span data-ttu-id="4fed9-109">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="4fed9-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fed9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fed9-110">Remarks</span></span>

<span data-ttu-id="4fed9-111">Этот атрибут используется с событием [месаурцератечанжерекуестед](mesourceratechangerequested.md) .</span><span class="sxs-lookup"><span data-stu-id="4fed9-111">This attribute is used with the [MESourceRateChangeRequested](mesourceratechangerequested.md) event.</span></span> <span data-ttu-id="4fed9-112">Если значение равно **true**, источник мультимедиа запрашивает переключение на тонкое воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="4fed9-112">If the value is **TRUE**, the media source is requesting a switch to thinned playback.</span></span>

<span data-ttu-id="4fed9-113">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4fed9-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="4fed9-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="4fed9-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fed9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4fed9-115">Requirements</span></span>



| <span data-ttu-id="4fed9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4fed9-116">Requirement</span></span> | <span data-ttu-id="4fed9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4fed9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fed9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fed9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4fed9-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4fed9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4fed9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fed9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4fed9-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4fed9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4fed9-122">Header</span><span class="sxs-lookup"><span data-stu-id="4fed9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fed9-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fed9-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fed9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fed9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fed9-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4fed9-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4fed9-126">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="4fed9-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="4fed9-127">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="4fed9-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4fed9-128">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4fed9-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




