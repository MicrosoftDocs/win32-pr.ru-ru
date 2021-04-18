---
description: Вызывается источником мультимедиа при изменении характеристик источника.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Событие Месаурцечарактеристиксчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711565"
---
# <a name="mesourcecharacteristicschanged-event"></a><span data-ttu-id="abed0-103">Событие Месаурцечарактеристиксчанжед</span><span class="sxs-lookup"><span data-stu-id="abed0-103">MESourceCharacteristicsChanged event</span></span>

<span data-ttu-id="abed0-104">Вызывается источником мультимедиа при изменении характеристик источника.</span><span class="sxs-lookup"><span data-stu-id="abed0-104">Raised by a media source when the source's characteristics change.</span></span>

## <a name="event-values"></a><span data-ttu-id="abed0-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="abed0-105">Event values</span></span>

<span data-ttu-id="abed0-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="abed0-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="abed0-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="abed0-107">VARTYPE</span></span>              | <span data-ttu-id="abed0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="abed0-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="abed0-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="abed0-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="abed0-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="abed0-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="abed0-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="abed0-111">Attributes</span></span>

<span data-ttu-id="abed0-112">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="abed0-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="abed0-113">attribute</span><span class="sxs-lookup"><span data-stu-id="abed0-113">Attribute</span></span>                                                                                                   | <span data-ttu-id="abed0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="abed0-114">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="abed0-115">**\_ \_ характеристики источника события \_ MF**</span><span class="sxs-lookup"><span data-stu-id="abed0-115">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)<br/>          | <span data-ttu-id="abed0-116">Новые характеристики источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="abed0-116">New characteristics of the media source.</span></span><br/> <br/>      |
| [<span data-ttu-id="abed0-117">**\_ \_ \_ старые характеристики источника события \_ MF**</span><span class="sxs-lookup"><span data-stu-id="abed0-117">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)<br/> | <span data-ttu-id="abed0-118">Предыдущие характеристики источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="abed0-118">Previous characteristics of the media source.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="abed0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="abed0-119">Requirements</span></span>



| <span data-ttu-id="abed0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="abed0-120">Requirement</span></span> | <span data-ttu-id="abed0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="abed0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abed0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abed0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="abed0-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abed0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="abed0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abed0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="abed0-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="abed0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="abed0-126">Header</span><span class="sxs-lookup"><span data-stu-id="abed0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="abed0-127"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abed0-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abed0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abed0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abed0-129">**имфмедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="abed0-129">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[<span data-ttu-id="abed0-130">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="abed0-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




