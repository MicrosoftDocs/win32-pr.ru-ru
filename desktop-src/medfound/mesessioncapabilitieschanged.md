---
description: Вызывается сеансом мультимедиа при изменении возможностей сеанса.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Событие Месессионкапабилитиесчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711567"
---
# <a name="mesessioncapabilitieschanged-event"></a><span data-ttu-id="95a22-103">Событие Месессионкапабилитиесчанжед</span><span class="sxs-lookup"><span data-stu-id="95a22-103">MESessionCapabilitiesChanged event</span></span>

<span data-ttu-id="95a22-104">Вызывается сеансом мультимедиа при изменении возможностей сеанса.</span><span class="sxs-lookup"><span data-stu-id="95a22-104">Raised by the Media Session when the session capabilities change.</span></span>

## <a name="event-values"></a><span data-ttu-id="95a22-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="95a22-105">Event values</span></span>

<span data-ttu-id="95a22-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="95a22-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="95a22-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="95a22-107">VARTYPE</span></span>              | <span data-ttu-id="95a22-108">Описание</span><span class="sxs-lookup"><span data-stu-id="95a22-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="95a22-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="95a22-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="95a22-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="95a22-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="95a22-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95a22-111">Remarks</span></span>

<span data-ttu-id="95a22-112">Событие содержит следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="95a22-112">The event contains the following attributes.</span></span>



| <span data-ttu-id="95a22-113">attribute</span><span class="sxs-lookup"><span data-stu-id="95a22-113">Attribute</span></span>                                                                     | <span data-ttu-id="95a22-114">Описание</span><span class="sxs-lookup"><span data-stu-id="95a22-114">Description</span></span>                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="95a22-115">**\_сессионкапс событий \_ MF**</span><span class="sxs-lookup"><span data-stu-id="95a22-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)              | <span data-ttu-id="95a22-116">Новые флаги возможностей сеанса.</span><span class="sxs-lookup"><span data-stu-id="95a22-116">New session capabilities flags.</span></span>                  |
| [<span data-ttu-id="95a22-117">**\_Дельта событий MF \_ сессионкапс \_**</span><span class="sxs-lookup"><span data-stu-id="95a22-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md) | <span data-ttu-id="95a22-118">Указывает, какие флаги возможностей изменились.</span><span class="sxs-lookup"><span data-stu-id="95a22-118">Indicates which capabilities flags have changed.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="95a22-119">Требования</span><span class="sxs-lookup"><span data-stu-id="95a22-119">Requirements</span></span>



| <span data-ttu-id="95a22-120">Требование</span><span class="sxs-lookup"><span data-stu-id="95a22-120">Requirement</span></span> | <span data-ttu-id="95a22-121">Значение</span><span class="sxs-lookup"><span data-stu-id="95a22-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95a22-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95a22-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95a22-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95a22-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95a22-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95a22-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95a22-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95a22-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95a22-126">Header</span><span class="sxs-lookup"><span data-stu-id="95a22-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="95a22-127"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95a22-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a22-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95a22-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a22-129">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="95a22-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




