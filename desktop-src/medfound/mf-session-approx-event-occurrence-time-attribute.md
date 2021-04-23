---
description: Приблизительное время, когда сеанс мультимедиа вызвал событие.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: Атрибут MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a31b1970c2c9d86384c12c50777a8cee55e3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712398"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a><span data-ttu-id="04b08-103">\_ \_ \_ \_ Атрибут времени возникновения события MF Session примерно \_</span><span class="sxs-lookup"><span data-stu-id="04b08-103">MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME attribute</span></span>

<span data-ttu-id="04b08-104">Приблизительное время, когда сеанс мультимедиа вызвал событие.</span><span class="sxs-lookup"><span data-stu-id="04b08-104">The approximate time when the Media Session raised an event.</span></span>

## <a name="data-type"></a><span data-ttu-id="04b08-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="04b08-105">Data type</span></span>

<span data-ttu-id="04b08-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="04b08-106">**UINT64**</span></span>

<span data-ttu-id="04b08-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="04b08-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04b08-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04b08-108">Remarks</span></span>

<span data-ttu-id="04b08-109">Некоторые события из сеанса мультимедиа имеют этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="04b08-109">Some events from the Media Session have this attribute.</span></span> <span data-ttu-id="04b08-110">Значение дает приблизительное время показа при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="04b08-110">The value gives the approximate presentation time when the event was raised.</span></span>

<span data-ttu-id="04b08-111">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="04b08-111">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="04b08-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="04b08-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b08-113">Требования</span><span class="sxs-lookup"><span data-stu-id="04b08-113">Requirements</span></span>



| <span data-ttu-id="04b08-114">Требование</span><span class="sxs-lookup"><span data-stu-id="04b08-114">Requirement</span></span> | <span data-ttu-id="04b08-115">Значение</span><span class="sxs-lookup"><span data-stu-id="04b08-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04b08-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04b08-116">Minimum supported client</span></span><br/> | <span data-ttu-id="04b08-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04b08-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="04b08-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04b08-118">Minimum supported server</span></span><br/> | <span data-ttu-id="04b08-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04b08-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="04b08-120">Header</span><span class="sxs-lookup"><span data-stu-id="04b08-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="04b08-121"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="04b08-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b08-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04b08-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b08-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04b08-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="04b08-124">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="04b08-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="04b08-125">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="04b08-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="04b08-126">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="04b08-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




