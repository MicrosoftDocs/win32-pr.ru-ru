---
description: Сообщает о событии из приемника мультимедиа, который визуализирует данные мультимедиа.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Событие Мерендереревент (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263645"
---
# <a name="merendererevent-event"></a><span data-ttu-id="05f92-103">Событие Мерендереревент</span><span class="sxs-lookup"><span data-stu-id="05f92-103">MERendererEvent event</span></span>

<span data-ttu-id="05f92-104">Сообщает о событии из приемника мультимедиа, который визуализирует данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="05f92-104">Signals an event from a media sink that renders media data.</span></span>

<span data-ttu-id="05f92-105">[Расширенный модуль обработки видео](enhanced-video-renderer.md) (Евр) отправляет это событие при получении пользовательского события от Евр.</span><span class="sxs-lookup"><span data-stu-id="05f92-105">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) sends this event when it receives a user event from the EVR presenter.</span></span>

## <a name="event-values"></a><span data-ttu-id="05f92-106">Значения событий</span><span class="sxs-lookup"><span data-stu-id="05f92-106">Event values</span></span>

<span data-ttu-id="05f92-107">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="05f92-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="05f92-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="05f92-108">VARTYPE</span></span>           | <span data-ttu-id="05f92-109">Описание</span><span class="sxs-lookup"><span data-stu-id="05f92-109">Description</span></span>                        |
|-------------------|------------------------------------|
| <span data-ttu-id="05f92-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="05f92-110">VT\_I4</span></span><br/> | <span data-ttu-id="05f92-111">Код события.</span><span class="sxs-lookup"><span data-stu-id="05f92-111">Event code.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="05f92-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05f92-112">Remarks</span></span>

<span data-ttu-id="05f92-113">Если выступающий вызывает метод **имедиаевентсинк:: notify** Евр с кодом события в диапазоне EC \_ User или выше, ЕВР отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="05f92-113">If the presenter calls the EVR's **IMediaEventSink::Notify** method with an event code in the range EC\_USER or higher, the EVR sends this event.</span></span> <span data-ttu-id="05f92-114">Данные события — это код события, который был передан методу **Notify** .</span><span class="sxs-lookup"><span data-stu-id="05f92-114">The event data is the event code that was passed to the **Notify** method.</span></span>

<span data-ttu-id="05f92-115">Параметры исходного события (*EventParam1* и *EventParam2* в методе **имедиаевентсинк:: notify** ) игнорируются, поэтому при выступающем параметрам должны быть присвоены значения **null**.</span><span class="sxs-lookup"><span data-stu-id="05f92-115">The original event parameters (*EventParam1* and *EventParam2* in the **IMediaEventSink::Notify** method) are ignored, so the presenter should set these values to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f92-116">Требования</span><span class="sxs-lookup"><span data-stu-id="05f92-116">Requirements</span></span>



| <span data-ttu-id="05f92-117">Требование</span><span class="sxs-lookup"><span data-stu-id="05f92-117">Requirement</span></span> | <span data-ttu-id="05f92-118">Значение</span><span class="sxs-lookup"><span data-stu-id="05f92-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f92-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05f92-119">Minimum supported client</span></span><br/> | <span data-ttu-id="05f92-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05f92-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="05f92-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05f92-121">Minimum supported server</span></span><br/> | <span data-ttu-id="05f92-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05f92-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05f92-123">Header</span><span class="sxs-lookup"><span data-stu-id="05f92-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f92-124"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05f92-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f92-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05f92-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f92-126">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05f92-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




