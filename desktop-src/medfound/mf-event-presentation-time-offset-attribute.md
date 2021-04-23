---
description: Смещение между временем презентации и метками времени источников мультимедиа.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: Атрибут MF_EVENT_PRESENTATION_TIME_OFFSET (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897726"
---
# <a name="mf_event_presentation_time_offset-attribute"></a><span data-ttu-id="5fbca-103">\_ \_ \_ Атрибут смещения времени представления событий MF \_</span><span class="sxs-lookup"><span data-stu-id="5fbca-103">MF\_EVENT\_PRESENTATION\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="5fbca-104">Смещение между временем презентации и штампами времени источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5fbca-104">Offset between the presentation time and the media source's time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="5fbca-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5fbca-105">Data type</span></span>

<span data-ttu-id="5fbca-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="5fbca-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="5fbca-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fbca-107">Remarks</span></span>

<span data-ttu-id="5fbca-108">Смещение вычисляется следующим образом: offset = время представления – источник время.</span><span class="sxs-lookup"><span data-stu-id="5fbca-108">The offset is calculated as follows: offset = presentation time − source time.</span></span> <span data-ttu-id="5fbca-109">Этот атрибут используется со следующими событиями:</span><span class="sxs-lookup"><span data-stu-id="5fbca-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="5fbca-110">месессионнотифипресентатионтиме</span><span class="sxs-lookup"><span data-stu-id="5fbca-110">MESessionNotifyPresentationTime</span></span>](mesessionnotifypresentationtime.md)
-   [<span data-ttu-id="5fbca-111">месессионстартед</span><span class="sxs-lookup"><span data-stu-id="5fbca-111">MESessionStarted</span></span>](mesessionstarted.md)

<span data-ttu-id="5fbca-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="5fbca-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fbca-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5fbca-113">Requirements</span></span>



| <span data-ttu-id="5fbca-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5fbca-114">Requirement</span></span> | <span data-ttu-id="5fbca-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5fbca-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5fbca-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fbca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5fbca-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fbca-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5fbca-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fbca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5fbca-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5fbca-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5fbca-120">Header</span><span class="sxs-lookup"><span data-stu-id="5fbca-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fbca-121"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fbca-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fbca-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fbca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbca-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5fbca-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5fbca-124">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="5fbca-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="5fbca-125">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="5fbca-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="5fbca-126">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="5fbca-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




