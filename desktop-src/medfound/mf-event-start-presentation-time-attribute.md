---
description: Время начала презентации в единицах измерения 100-наносекундных, измеряемое часами представления.
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: Атрибут MF_EVENT_START_PRESENTATION_TIME (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf6142ce12a7bf921fd26373ea5d10ab384560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081619"
---
# <a name="mf_event_start_presentation_time-attribute"></a><span data-ttu-id="df00b-103">\_ \_ \_ Атрибут времени начала презентации \_ события MF</span><span class="sxs-lookup"><span data-stu-id="df00b-103">MF\_EVENT\_START\_PRESENTATION\_TIME attribute</span></span>

<span data-ttu-id="df00b-104">Время начала презентации в единицах измерения 100-наносекундных, измеряемое часами представления.</span><span class="sxs-lookup"><span data-stu-id="df00b-104">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>

## <a name="data-type"></a><span data-ttu-id="df00b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="df00b-105">Data type</span></span>

<span data-ttu-id="df00b-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="df00b-106">**UINT64**</span></span>

<span data-ttu-id="df00b-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="df00b-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df00b-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df00b-108">Remarks</span></span>

<span data-ttu-id="df00b-109">Этот атрибут используется с событием [месессионнотифипресентатионтиме](mesessionnotifypresentationtime.md) .</span><span class="sxs-lookup"><span data-stu-id="df00b-109">This attribute is used with the [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) event.</span></span>

<span data-ttu-id="df00b-110">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="df00b-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="df00b-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="df00b-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="df00b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="df00b-112">Requirements</span></span>



| <span data-ttu-id="df00b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="df00b-113">Requirement</span></span> | <span data-ttu-id="df00b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="df00b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="df00b-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df00b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="df00b-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df00b-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="df00b-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df00b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="df00b-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df00b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="df00b-119">Header</span><span class="sxs-lookup"><span data-stu-id="df00b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="df00b-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="df00b-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df00b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df00b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df00b-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="df00b-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="df00b-123">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="df00b-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="df00b-124">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="df00b-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="df00b-125">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="df00b-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




