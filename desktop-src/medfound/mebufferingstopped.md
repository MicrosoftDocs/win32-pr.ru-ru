---
description: Сигнализирует, что источник мультимедиа прекратил буферизацию данных.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: Событие Мебуфферингстоппед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e996ec160f57ec598196b388170741705adb9a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344302"
---
# <a name="mebufferingstopped-event"></a><span data-ttu-id="e791f-103">Событие Мебуфферингстоппед</span><span class="sxs-lookup"><span data-stu-id="e791f-103">MEBufferingStopped event</span></span>

<span data-ttu-id="e791f-104">Сигнализирует, что источник мультимедиа прекратил буферизацию данных.</span><span class="sxs-lookup"><span data-stu-id="e791f-104">Signals that a media source has stopped buffering data.</span></span>

<span data-ttu-id="e791f-105">Источник мультимедиа отправляет его, когда прекращает буферизацию данных после отправки события [мебуфферингстартед](mebufferingstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="e791f-105">A media source sends this when it stops buffering data after sending the [MEBufferingStarted](mebufferingstarted.md) event.</span></span>

<span data-ttu-id="e791f-106">Потоковые потоки, которые реализуют интерфейс [**имфбитестреамбуфферинг**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) , также отправляют это событие.</span><span class="sxs-lookup"><span data-stu-id="e791f-106">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="e791f-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="e791f-107">Event values</span></span>

<span data-ttu-id="e791f-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="e791f-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e791f-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e791f-109">VARTYPE</span></span>              | <span data-ttu-id="e791f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e791f-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e791f-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="e791f-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e791f-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="e791f-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e791f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e791f-113">Remarks</span></span>

<span data-ttu-id="e791f-114">Когда сеанс мультимедиа получает это событие, он перезапускает часы презентации.</span><span class="sxs-lookup"><span data-stu-id="e791f-114">When the Media Session receives this event, it restarts the presentation clock.</span></span> <span data-ttu-id="e791f-115">Сеанс мультимедиа также перенаправляет событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="e791f-115">The Media Session also forwards the event to the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e791f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e791f-116">Requirements</span></span>



| <span data-ttu-id="e791f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e791f-117">Requirement</span></span> | <span data-ttu-id="e791f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e791f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e791f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e791f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e791f-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e791f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e791f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e791f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e791f-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e791f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e791f-123">Header</span><span class="sxs-lookup"><span data-stu-id="e791f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e791f-124"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e791f-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e791f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e791f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e791f-126">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e791f-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




