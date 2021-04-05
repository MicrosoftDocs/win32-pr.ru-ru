---
description: Время презентации для примера, отображаемого во время очистки.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: Атрибут MF_EVENT_SCRUBSAMPLE_TIME (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7c4fb1a8015367fa3d48edb066cdb135983926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991479"
---
# <a name="mf_event_scrubsample_time-attribute"></a><span data-ttu-id="4dac1-103">\_ \_ Атрибут времени СКРУБСАМПЛЕ события MF \_</span><span class="sxs-lookup"><span data-stu-id="4dac1-103">MF\_EVENT\_SCRUBSAMPLE\_TIME attribute</span></span>

<span data-ttu-id="4dac1-104">Время презентации для примера, отображаемого во время очистки.</span><span class="sxs-lookup"><span data-stu-id="4dac1-104">Presentation time for a sample that was rendered while scrubbing.</span></span>

## <a name="data-type"></a><span data-ttu-id="4dac1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4dac1-105">Data type</span></span>

<span data-ttu-id="4dac1-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4dac1-106">**UINT64**</span></span>

<span data-ttu-id="4dac1-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="4dac1-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dac1-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4dac1-108">Remarks</span></span>

<span data-ttu-id="4dac1-109">Этот атрибут используется с событием [местреамсинкскрубсамплекомплете](mestreamsinkscrubsamplecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="4dac1-109">This attribute is used with the [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) event.</span></span>

<span data-ttu-id="4dac1-110">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="4dac1-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="4dac1-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="4dac1-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dac1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4dac1-112">Requirements</span></span>



| <span data-ttu-id="4dac1-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4dac1-113">Requirement</span></span> | <span data-ttu-id="4dac1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4dac1-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4dac1-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4dac1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4dac1-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4dac1-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4dac1-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4dac1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4dac1-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4dac1-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4dac1-119">Header</span><span class="sxs-lookup"><span data-stu-id="4dac1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dac1-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dac1-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dac1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4dac1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dac1-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4dac1-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4dac1-123">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="4dac1-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="4dac1-124">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="4dac1-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="4dac1-125">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="4dac1-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




