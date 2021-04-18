---
description: Предоставляет отзыв диспетчеру качества о качестве качества воспроизведения.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Событие Мекуалитинотифи (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544386"
---
# <a name="mequalitynotify-event"></a><span data-ttu-id="14f5a-103">Событие Мекуалитинотифи</span><span class="sxs-lookup"><span data-stu-id="14f5a-103">MEQualityNotify event</span></span>

<span data-ttu-id="14f5a-104">Предоставляет отзыв диспетчеру качества о качестве качества воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="14f5a-104">Provides feedback to the quality manager about playback quality.</span></span>

## <a name="event-values"></a><span data-ttu-id="14f5a-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="14f5a-105">Event values</span></span>

<span data-ttu-id="14f5a-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="14f5a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="14f5a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="14f5a-107">VARTYPE</span></span>           | <span data-ttu-id="14f5a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="14f5a-108">Description</span></span>                         |
|-------------------|-------------------------------------|
| <span data-ttu-id="14f5a-109">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="14f5a-109">VT\_I8</span></span><br/> | <span data-ttu-id="14f5a-110">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="14f5a-110">See Remarks.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="14f5a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14f5a-111">Remarks</span></span>

<span data-ttu-id="14f5a-112">Это событие вызывается некоторыми компонентами конвейера.</span><span class="sxs-lookup"><span data-stu-id="14f5a-112">This event is raised by some pipeline components.</span></span> <span data-ttu-id="14f5a-113">Сеанс мультимедиа перенаправляет событие диспетчеру качества, вызывая метод [**имфкуалитиманажер:: нотификуалитевент**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) .</span><span class="sxs-lookup"><span data-stu-id="14f5a-113">The Media Session forwards the event to the quality manager by calling the [**IMFQualityManager::NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) method.</span></span>

<span data-ttu-id="14f5a-114">Расширенный тип события указывает значение данных события.</span><span class="sxs-lookup"><span data-stu-id="14f5a-114">The event's extended type indicates the meaning of the event data.</span></span>



| <span data-ttu-id="14f5a-115">Расширенный тип</span><span class="sxs-lookup"><span data-stu-id="14f5a-115">Extended type</span></span>                            | <span data-ttu-id="14f5a-116">Данные событий</span><span class="sxs-lookup"><span data-stu-id="14f5a-116">Event data</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f5a-117">\_ \_ уведомление о \_ задержке при обработке уведомления MF \_</span><span class="sxs-lookup"><span data-stu-id="14f5a-117">MF\_QUALITY\_NOTIFY\_PROCESSING\_LATENCY</span></span> | <span data-ttu-id="14f5a-118">Приблизительная задержка обработки, представленная компонентом, в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="14f5a-118">Approximate processing latency introduced by the component, in 100-nanosecond units.</span></span><br/> <span data-ttu-id="14f5a-119">Задержка обработки — это количество задержки, которое компонент вводит в конвейер путем обработки образца.</span><span class="sxs-lookup"><span data-stu-id="14f5a-119">Processing latency is the amount of latency that a component introduces into the pipeline by processing a sample.</span></span> <span data-ttu-id="14f5a-120">В некоторых случаях задержка не может быть получена просто путем просмотра вызовов [**имфкуалитиманажер:: нотифипроцессинпут**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) и [**Имфкуалитиманажер:: нотифипроцессаутпут**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span><span class="sxs-lookup"><span data-stu-id="14f5a-120">In some cases, the latency cannot be derived simply by looking at the calls to [**IMFQualityManager::NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) and [**IMFQualityManager::NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span></span> <span data-ttu-id="14f5a-121">Например, может не быть однозначного соответствия между входными и выходными примерами.</span><span class="sxs-lookup"><span data-stu-id="14f5a-121">For example, there may not be a one-to-one correspondence between input samples and output samples.</span></span> <span data-ttu-id="14f5a-122">В этом случае компонент может отправить событие Мекуалитинотифи с задержкой обработки.</span><span class="sxs-lookup"><span data-stu-id="14f5a-122">In this case, the component might send an MEQualityNotify event with the processing latency.</span></span> <span data-ttu-id="14f5a-123">При изменении задержки обработки компонент может отправить новое событие в любое время во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="14f5a-123">If the processing latency changes, the component can send a new event at any time during streaming.</span></span><br/> |
| <span data-ttu-id="14f5a-124">\_ \_ \_ Задержка ВЫБОРки уведомлений \_ MF</span><span class="sxs-lookup"><span data-stu-id="14f5a-124">MF\_QUALITY\_NOTIFY\_SAMPLE\_LAG</span></span>         | <span data-ttu-id="14f5a-125">Время запаздывания для примера в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="14f5a-125">Lag time for the sample, in 100-nanosecond units.</span></span> <span data-ttu-id="14f5a-126">Если значение положительное, пример был последним.</span><span class="sxs-lookup"><span data-stu-id="14f5a-126">If the value is positive, the sample was late.</span></span> <span data-ttu-id="14f5a-127">Если значение отрицательное, пример был ранним.</span><span class="sxs-lookup"><span data-stu-id="14f5a-127">If the value is negative, the sample was early.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="14f5a-128">Чтобы получить расширенный тип, вызовите метод [**имфмедиаевент:: жетекстендедтипе**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="14f5a-128">To get the extended type, call [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

<span data-ttu-id="14f5a-129">Компоненты конвейера не являются обязательными для отправки этого события.</span><span class="sxs-lookup"><span data-stu-id="14f5a-129">Pipeline components are not required to send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="14f5a-130">Требования</span><span class="sxs-lookup"><span data-stu-id="14f5a-130">Requirements</span></span>



| <span data-ttu-id="14f5a-131">Требование</span><span class="sxs-lookup"><span data-stu-id="14f5a-131">Requirement</span></span> | <span data-ttu-id="14f5a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="14f5a-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f5a-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14f5a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="14f5a-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14f5a-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="14f5a-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14f5a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="14f5a-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14f5a-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="14f5a-137">Header</span><span class="sxs-lookup"><span data-stu-id="14f5a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="14f5a-138"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14f5a-138"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14f5a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14f5a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f5a-140">**имфкуалитиманажер**</span><span class="sxs-lookup"><span data-stu-id="14f5a-140">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[<span data-ttu-id="14f5a-141">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14f5a-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




