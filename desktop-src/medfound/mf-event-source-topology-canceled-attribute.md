---
description: Указывает, отменила ли источник Sequencer топологию.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: Атрибут MF_EVENT_SOURCE_TOPOLOGY_CANCELED (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656711"
---
# <a name="mf_event_source_topology_canceled-attribute"></a><span data-ttu-id="29954-103">\_Атрибут " \_ топология источника события MF \_ \_ отменен"</span><span class="sxs-lookup"><span data-stu-id="29954-103">MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED attribute</span></span>

<span data-ttu-id="29954-104">Указывает, отменила ли [источник Sequencer](sequencer-source.md) топологию.</span><span class="sxs-lookup"><span data-stu-id="29954-104">Specifies whether the [Sequencer Source](sequencer-source.md) canceled a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="29954-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="29954-105">Data type</span></span>

<span data-ttu-id="29954-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="29954-106">**UINT32**</span></span>

<span data-ttu-id="29954-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="29954-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29954-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29954-108">Remarks</span></span>

<span data-ttu-id="29954-109">Этот атрибут используется со следующими событиями:</span><span class="sxs-lookup"><span data-stu-id="29954-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="29954-110">миндофпресентатионсегмент</span><span class="sxs-lookup"><span data-stu-id="29954-110">MEEndOfPresentationSegment</span></span>](meendofpresentationsegment.md)
-   [<span data-ttu-id="29954-111">миндофпресентатион</span><span class="sxs-lookup"><span data-stu-id="29954-111">MEEndOfPresentation</span></span>](meendofpresentation.md)

<span data-ttu-id="29954-112">Если этот атрибут имеется и имеет ненулевое значение, это означает, что сегмент презентации завершен, так как источник Sequencer отменил топологию.</span><span class="sxs-lookup"><span data-stu-id="29954-112">If this attribute is present and nonzero, it means that the presentation segment ended because the sequencer source canceled the topology.</span></span> <span data-ttu-id="29954-113">В противном случае сегмент презентации завершается нормально.</span><span class="sxs-lookup"><span data-stu-id="29954-113">Otherwise, the presentation segment ended normally.</span></span>

<span data-ttu-id="29954-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="29954-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="29954-115">Требования</span><span class="sxs-lookup"><span data-stu-id="29954-115">Requirements</span></span>



| <span data-ttu-id="29954-116">Требование</span><span class="sxs-lookup"><span data-stu-id="29954-116">Requirement</span></span> | <span data-ttu-id="29954-117">Значение</span><span class="sxs-lookup"><span data-stu-id="29954-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29954-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29954-118">Minimum supported client</span></span><br/> | <span data-ttu-id="29954-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29954-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="29954-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29954-120">Minimum supported server</span></span><br/> | <span data-ttu-id="29954-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29954-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="29954-122">Header</span><span class="sxs-lookup"><span data-stu-id="29954-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="29954-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="29954-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29954-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29954-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29954-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29954-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="29954-126">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="29954-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="29954-127">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="29954-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="29954-128">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="29954-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="29954-129">События источника Sequencer</span><span class="sxs-lookup"><span data-stu-id="29954-129">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




