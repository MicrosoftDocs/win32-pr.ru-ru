---
description: Вызывается источником мультимедиа при перезапуске или при поиске уже активного потока.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Событие Меупдатедстреам (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546162"
---
# <a name="meupdatedstream-event"></a><span data-ttu-id="1d029-103">Событие Меупдатедстреам</span><span class="sxs-lookup"><span data-stu-id="1d029-103">MEUpdatedStream event</span></span>

<span data-ttu-id="1d029-104">Вызывается источником мультимедиа при перезапуске или при поиске уже активного потока.</span><span class="sxs-lookup"><span data-stu-id="1d029-104">Raised by a media source when it restarts or seeks a stream that is already active.</span></span>

<span data-ttu-id="1d029-105">Когда метод [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) вызывается для источника мультимедиа, источник мультимедиа отправляет одно событие для каждого выбранного потока:</span><span class="sxs-lookup"><span data-stu-id="1d029-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="1d029-106">Источник отправляет событие [меневстреам](menewstream.md) , если поток не был выбран в предыдущем вызове [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), или это самый первый вызов для **запуска** в этом источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1d029-106">The source sends the [MENewStream](menewstream.md) event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="1d029-107">Источник отправляет событие Меупдатедстреам, если поток уже был выбран в предыдущем вызове [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="1d029-107">The source sends the MEUpdatedStream event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="1d029-108">Для невыбранных потоков события не отправляются.</span><span class="sxs-lookup"><span data-stu-id="1d029-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="1d029-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="1d029-109">Event values</span></span>

<span data-ttu-id="1d029-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="1d029-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1d029-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1d029-111">VARTYPE</span></span>                | <span data-ttu-id="1d029-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1d029-112">Description</span></span>                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d029-113">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="1d029-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="1d029-114">Указатель на интерфейс [**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) потока.</span><span class="sxs-lookup"><span data-stu-id="1d029-114">Pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1d029-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d029-115">Remarks</span></span>

<span data-ttu-id="1d029-116">При первом вызове метода [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) , в котором поток станет активным, источник мультимедиа отправляет событие [меневстреам](menewstream.md) для потока.</span><span class="sxs-lookup"><span data-stu-id="1d029-116">On the first call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) in which a stream becomes active, the media source sends an [MENewStream](menewstream.md) event for the stream.</span></span> <span data-ttu-id="1d029-117">При последующих вызовах для **запуска** источник мультимедиа отправляет событие меупдатедстреам до тех пор, пока поток не будет выбран.</span><span class="sxs-lookup"><span data-stu-id="1d029-117">On subsequent calls to **Start**, the media source sends an MEUpdatedStream event, until the stream is deselected.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d029-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1d029-118">Requirements</span></span>



| <span data-ttu-id="1d029-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1d029-119">Requirement</span></span> | <span data-ttu-id="1d029-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1d029-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d029-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d029-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1d029-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d029-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1d029-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d029-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1d029-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1d029-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d029-125">Header</span><span class="sxs-lookup"><span data-stu-id="1d029-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d029-126"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d029-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d029-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d029-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d029-128">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d029-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




