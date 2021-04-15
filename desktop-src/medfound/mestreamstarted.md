---
description: Вызывается потоком мультимедиа, когда источник запускается без поиска. Поток мультимедиа вызывает это событие, когда источник мультимедиа создает событие Месаурцестартед.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Событие Местреамстартед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701896"
---
# <a name="mestreamstarted-event"></a><span data-ttu-id="45ba9-104">Событие Местреамстартед</span><span class="sxs-lookup"><span data-stu-id="45ba9-104">MEStreamStarted event</span></span>

<span data-ttu-id="45ba9-105">Вызывается потоком мультимедиа, когда источник запускается без поиска.</span><span class="sxs-lookup"><span data-stu-id="45ba9-105">Raised by a media stream when the source starts without seeking.</span></span> <span data-ttu-id="45ba9-106">Поток мультимедиа вызывает это событие, когда источник мультимедиа создает событие [месаурцестартед](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="45ba9-106">A media stream raises this event when the media source raises the [MESourceStarted](mesourcestarted.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="45ba9-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="45ba9-107">Event values</span></span>

<span data-ttu-id="45ba9-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="45ba9-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="45ba9-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="45ba9-109">VARTYPE</span></span>              | <span data-ttu-id="45ba9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="45ba9-110">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ba9-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="45ba9-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="45ba9-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="45ba9-112">No event data.</span></span><br/> <br/>                                                                          |
| <span data-ttu-id="45ba9-113">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="45ba9-113">VT\_I8</span></span><br/>    | <span data-ttu-id="45ba9-114">Время начала (в 100-наносекундных единицах) относительно меток времени в примерах.</span><span class="sxs-lookup"><span data-stu-id="45ba9-114">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="45ba9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="45ba9-115">Requirements</span></span>



| <span data-ttu-id="45ba9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="45ba9-116">Requirement</span></span> | <span data-ttu-id="45ba9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="45ba9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ba9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45ba9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="45ba9-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45ba9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="45ba9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45ba9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="45ba9-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45ba9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="45ba9-122">Header</span><span class="sxs-lookup"><span data-stu-id="45ba9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="45ba9-123"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45ba9-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45ba9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45ba9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ba9-125">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="45ba9-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




