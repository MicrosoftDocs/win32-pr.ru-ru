---
description: Вызывается приемником потока при завершении перехода в приостановленное состояние.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: Событие Местреамсинкпаусед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17016285f2b88a1fc266b79f5eee45fea31f824c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702613"
---
# <a name="mestreamsinkpaused-event"></a><span data-ttu-id="95984-103">Событие Местреамсинкпаусед</span><span class="sxs-lookup"><span data-stu-id="95984-103">MEStreamSinkPaused event</span></span>

<span data-ttu-id="95984-104">Вызывается приемником потока при завершении перехода в приостановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="95984-104">Raised by a stream sink when it completes the transition to the paused state.</span></span> <span data-ttu-id="95984-105">Переход на приостановку происходит, когда метод [**имфпресентатионклокк::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) вызывается в часах представления приемника.</span><span class="sxs-lookup"><span data-stu-id="95984-105">The transition to paused occurs when the [**IMFPresentationClock::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="95984-106">Значения событий</span><span class="sxs-lookup"><span data-stu-id="95984-106">Event values</span></span>

<span data-ttu-id="95984-107">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="95984-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="95984-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="95984-108">VARTYPE</span></span>              | <span data-ttu-id="95984-109">Описание</span><span class="sxs-lookup"><span data-stu-id="95984-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="95984-110">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="95984-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="95984-111">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="95984-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="95984-112">Требования</span><span class="sxs-lookup"><span data-stu-id="95984-112">Requirements</span></span>



| <span data-ttu-id="95984-113">Требование</span><span class="sxs-lookup"><span data-stu-id="95984-113">Requirement</span></span> | <span data-ttu-id="95984-114">Значение</span><span class="sxs-lookup"><span data-stu-id="95984-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95984-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95984-115">Minimum supported client</span></span><br/> | <span data-ttu-id="95984-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95984-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95984-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95984-117">Minimum supported server</span></span><br/> | <span data-ttu-id="95984-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95984-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95984-119">Header</span><span class="sxs-lookup"><span data-stu-id="95984-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="95984-120"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95984-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95984-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95984-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95984-122">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="95984-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="95984-123">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="95984-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




