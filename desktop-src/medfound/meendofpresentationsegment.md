---
description: Вызывается источником Sequencer при завершении сегмента, за которым следует другой сегмент. По завершении последнего сегмента источник Sequencer вызывает событие Миндофпресентатион.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Событие Миндофпресентатионсегмент (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898389"
---
# <a name="meendofpresentationsegment-event"></a><span data-ttu-id="723de-104">Событие Миндофпресентатионсегмент</span><span class="sxs-lookup"><span data-stu-id="723de-104">MEEndOfPresentationSegment event</span></span>

<span data-ttu-id="723de-105">Вызывается источником Sequencer при завершении сегмента, за которым следует другой сегмент.</span><span class="sxs-lookup"><span data-stu-id="723de-105">Raised by the sequencer source when a segment is completed and is followed by another segment.</span></span> <span data-ttu-id="723de-106">По завершении последнего сегмента источник Sequencer вызывает событие [миндофпресентатион](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="723de-106">When the final segment is completed, the sequencer source raises an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

<span data-ttu-id="723de-107">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="723de-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="723de-108">Значения событий</span><span class="sxs-lookup"><span data-stu-id="723de-108">Event values</span></span>

<span data-ttu-id="723de-109">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="723de-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="723de-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="723de-110">VARTYPE</span></span>              | <span data-ttu-id="723de-111">Описание</span><span class="sxs-lookup"><span data-stu-id="723de-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="723de-112">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="723de-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="723de-113">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="723de-113">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="723de-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="723de-114">Attributes</span></span>

<span data-ttu-id="723de-115">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="723de-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="723de-116">attribute</span><span class="sxs-lookup"><span data-stu-id="723de-116">Attribute</span></span>                                                                                               | <span data-ttu-id="723de-117">Описание</span><span class="sxs-lookup"><span data-stu-id="723de-117">Description</span></span>                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="723de-118">**\_ \_ топология источника событий MF \_ \_ отменена**</span><span class="sxs-lookup"><span data-stu-id="723de-118">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="723de-119">Указывает, отменил ли источник Sequencer этот сегмент.</span><span class="sxs-lookup"><span data-stu-id="723de-119">Specifies whether the sequencer source canceled this segment.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="723de-120">Требования</span><span class="sxs-lookup"><span data-stu-id="723de-120">Requirements</span></span>



| <span data-ttu-id="723de-121">Требование</span><span class="sxs-lookup"><span data-stu-id="723de-121">Requirement</span></span> | <span data-ttu-id="723de-122">Значение</span><span class="sxs-lookup"><span data-stu-id="723de-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="723de-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="723de-123">Minimum supported client</span></span><br/> | <span data-ttu-id="723de-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="723de-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="723de-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="723de-125">Minimum supported server</span></span><br/> | <span data-ttu-id="723de-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="723de-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="723de-127">Header</span><span class="sxs-lookup"><span data-stu-id="723de-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="723de-128"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="723de-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="723de-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="723de-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723de-130">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="723de-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="723de-131">Сведения о источнике Sequencer</span><span class="sxs-lookup"><span data-stu-id="723de-131">About the Sequencer Source</span></span>](about-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="723de-132">События источника Sequencer</span><span class="sxs-lookup"><span data-stu-id="723de-132">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




