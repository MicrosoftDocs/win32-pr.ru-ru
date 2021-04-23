---
description: Содержит время начала, с которого источник мультимедиа перезапускается с текущей позиции.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: Атрибут MF_EVENT_SOURCE_ACTUAL_START (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423825"
---
# <a name="mf_event_source_actual_start-attribute"></a><span data-ttu-id="8af12-103">\_Атрибут "источник события MF — \_ \_ фактическое \_ Начало"</span><span class="sxs-lookup"><span data-stu-id="8af12-103">MF\_EVENT\_SOURCE\_ACTUAL\_START attribute</span></span>

<span data-ttu-id="8af12-104">Содержит время начала, с которого источник мультимедиа перезапускается с текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="8af12-104">Contains the start time at which a media source restarts from its current position.</span></span>

## <a name="data-type"></a><span data-ttu-id="8af12-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8af12-105">Data type</span></span>

<span data-ttu-id="8af12-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="8af12-106">**UINT64**</span></span>

<span data-ttu-id="8af12-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="8af12-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af12-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8af12-108">Remarks</span></span>

<span data-ttu-id="8af12-109">Этот атрибут используется с событием [месаурцестартед](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="8af12-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="8af12-110">Атрибут имеет значение, если данные события пусты (**VT \_ Empty**), что указывает на то, что источник мультимедиа запущен из текущей позицией воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8af12-110">The attribute is relevant when the event data is empty (**VT\_EMPTY**), which indicates that the media source started from the current playback position.</span></span> <span data-ttu-id="8af12-111">В этом случае в атрибуте **\_ \_ \_ \_ Start источника события MF** указан фактическое время начала.</span><span class="sxs-lookup"><span data-stu-id="8af12-111">In that case, the **MF\_EVENT\_SOURCE\_ACTUAL\_START** attribute specifies the actual starting time.</span></span> <span data-ttu-id="8af12-112">Если данные события имеют значение **VT \_ Empty** и этот атрибут не задан, то время начала считается равным нулю.</span><span class="sxs-lookup"><span data-stu-id="8af12-112">If the event data is **VT\_EMPTY** and this attribute is not set, the starting time is assumed to be zero.</span></span>

<span data-ttu-id="8af12-113">Если данные о событии [месаурцестартед](mesourcestarted.md) содержат время начала (**VT \_ i8**), этот атрибут задавать не следует.</span><span class="sxs-lookup"><span data-stu-id="8af12-113">When the [MESourceStarted](mesourcestarted.md) event data contains the start time (**VT\_I8**), this attribute should not be set.</span></span>

<span data-ttu-id="8af12-114">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="8af12-114">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="8af12-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="8af12-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af12-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8af12-116">Requirements</span></span>



| <span data-ttu-id="8af12-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8af12-117">Requirement</span></span> | <span data-ttu-id="8af12-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8af12-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8af12-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8af12-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8af12-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8af12-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8af12-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8af12-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8af12-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8af12-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8af12-123">Header</span><span class="sxs-lookup"><span data-stu-id="8af12-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8af12-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8af12-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af12-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8af12-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af12-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8af12-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8af12-127">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="8af12-127">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="8af12-128">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="8af12-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="8af12-129">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="8af12-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




