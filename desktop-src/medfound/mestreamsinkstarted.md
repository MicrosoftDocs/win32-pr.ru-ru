---
description: Вызывается приемником потока при завершении перехода в состояние выполнения.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: Событие Местреамсинкстартед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711563"
---
# <a name="mestreamsinkstarted-event"></a><span data-ttu-id="03b9a-103">Событие Местреамсинкстартед</span><span class="sxs-lookup"><span data-stu-id="03b9a-103">MEStreamSinkStarted event</span></span>

<span data-ttu-id="03b9a-104">Вызывается приемником потока при завершении перехода в состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="03b9a-104">Raised by a stream sink when it completes the transition to the running state.</span></span> <span data-ttu-id="03b9a-105">Переход на выполнение происходит при вызове метода [**имфпресентатионклокк:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) для часов представления приемника.</span><span class="sxs-lookup"><span data-stu-id="03b9a-105">The transition to running occurs when the [**IMFPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) method is called on the sink's presentation clock.</span></span> <span data-ttu-id="03b9a-106">Приемник мультимедиа получает уведомление через его метод [**имфклоккстатесинк:: онклоккстарт**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) или [**Имфклоккстатесинк:: онклоккрестарт**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) .</span><span class="sxs-lookup"><span data-stu-id="03b9a-106">The media sink receives the notification through its [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="03b9a-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="03b9a-107">Event values</span></span>

<span data-ttu-id="03b9a-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="03b9a-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="03b9a-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="03b9a-109">VARTYPE</span></span>              | <span data-ttu-id="03b9a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="03b9a-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="03b9a-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="03b9a-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="03b9a-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="03b9a-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="03b9a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="03b9a-113">Requirements</span></span>



| <span data-ttu-id="03b9a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="03b9a-114">Requirement</span></span> | <span data-ttu-id="03b9a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="03b9a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03b9a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03b9a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="03b9a-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03b9a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="03b9a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03b9a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="03b9a-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="03b9a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="03b9a-120">Header</span><span class="sxs-lookup"><span data-stu-id="03b9a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="03b9a-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03b9a-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03b9a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03b9a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03b9a-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03b9a-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="03b9a-124">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="03b9a-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




