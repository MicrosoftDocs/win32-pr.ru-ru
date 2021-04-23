---
description: Вызывается источником мультимедиа при завершении презентации. Это событие сигнализирует о завершении всех потоков в презентации. Сеанс мультимедиа перенаправляет это событие в приложение.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Событие Миндофпресентатион (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e3a904725908d83afd54bbd64012420075037a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650656"
---
# <a name="meendofpresentation-event"></a><span data-ttu-id="53db5-105">Событие Миндофпресентатион</span><span class="sxs-lookup"><span data-stu-id="53db5-105">MEEndOfPresentation event</span></span>

<span data-ttu-id="53db5-106">Вызывается источником мультимедиа при завершении презентации.</span><span class="sxs-lookup"><span data-stu-id="53db5-106">Raised by a media source when a presentation ends.</span></span> <span data-ttu-id="53db5-107">Это событие сигнализирует о завершении всех потоков в презентации.</span><span class="sxs-lookup"><span data-stu-id="53db5-107">This event signals that all streams in the presentation are complete.</span></span> <span data-ttu-id="53db5-108">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="53db5-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="53db5-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="53db5-109">Event values</span></span>

<span data-ttu-id="53db5-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="53db5-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="53db5-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="53db5-111">VARTYPE</span></span>              | <span data-ttu-id="53db5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="53db5-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="53db5-113">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="53db5-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="53db5-114">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="53db5-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="53db5-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="53db5-115">Attributes</span></span>

<span data-ttu-id="53db5-116">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="53db5-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="53db5-117">attribute</span><span class="sxs-lookup"><span data-stu-id="53db5-117">Attribute</span></span>                                                                                               | <span data-ttu-id="53db5-118">Описание</span><span class="sxs-lookup"><span data-stu-id="53db5-118">Description</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53db5-119">**\_ \_ топология источника событий MF \_ \_ отменена**</span><span class="sxs-lookup"><span data-stu-id="53db5-119">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="53db5-120">Указывает, отменила ли эта презентация источник Sequencer.</span><span class="sxs-lookup"><span data-stu-id="53db5-120">Specifies whether the sequencer source canceled this presentation.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="53db5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="53db5-121">Requirements</span></span>



| <span data-ttu-id="53db5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="53db5-122">Requirement</span></span> | <span data-ttu-id="53db5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="53db5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53db5-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53db5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="53db5-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53db5-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53db5-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53db5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="53db5-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53db5-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53db5-128">Header</span><span class="sxs-lookup"><span data-stu-id="53db5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="53db5-129"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53db5-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53db5-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53db5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53db5-131">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="53db5-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




