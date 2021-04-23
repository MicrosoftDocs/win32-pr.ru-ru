---
description: Вызывается приемником потока при изменении скорости.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Событие Местреамсинкратечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a26adbdb64ffd5af0896d8aebe0cef474bee9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712413"
---
# <a name="mestreamsinkratechanged-event"></a><span data-ttu-id="97fe9-103">Событие Местреамсинкратечанжед</span><span class="sxs-lookup"><span data-stu-id="97fe9-103">MEStreamSinkRateChanged event</span></span>

<span data-ttu-id="97fe9-104">Вызывается приемником потока при изменении скорости.</span><span class="sxs-lookup"><span data-stu-id="97fe9-104">Raised by a stream sink when the rate has changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="97fe9-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="97fe9-105">Event values</span></span>

<span data-ttu-id="97fe9-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="97fe9-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="97fe9-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="97fe9-107">VARTYPE</span></span>              | <span data-ttu-id="97fe9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="97fe9-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="97fe9-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="97fe9-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="97fe9-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="97fe9-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="97fe9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97fe9-111">Remarks</span></span>

<span data-ttu-id="97fe9-112">Если приемник потока поддерживает изменение частоты, он отправляет это событие после завершения изменения скорости.</span><span class="sxs-lookup"><span data-stu-id="97fe9-112">If a stream sink supports rate changes, it sends this event after the rate change is complete.</span></span> <span data-ttu-id="97fe9-113">Событие отправляется один раз для каждого вызова метода [**имфклоккстатесинк:: онклокксетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) приемника.</span><span class="sxs-lookup"><span data-stu-id="97fe9-113">The event is sent once for each call to the sink's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span> <span data-ttu-id="97fe9-114">Если изменение скорости не прошло успешно, значение состояния события является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="97fe9-114">If the rate change is not successful, the event status value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="97fe9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="97fe9-115">Requirements</span></span>



| <span data-ttu-id="97fe9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="97fe9-116">Requirement</span></span> | <span data-ttu-id="97fe9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="97fe9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97fe9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97fe9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="97fe9-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97fe9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="97fe9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97fe9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="97fe9-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97fe9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97fe9-122">Header</span><span class="sxs-lookup"><span data-stu-id="97fe9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="97fe9-123"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97fe9-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97fe9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97fe9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97fe9-125">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97fe9-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="97fe9-126">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="97fe9-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




