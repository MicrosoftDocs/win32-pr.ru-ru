---
description: 'Вызывается потоком мультимедиа после вызова Имфмедиасаурце:: Start, чтобы выполнить поиск в потоке. Поток мультимедиа вызывает это событие, когда источник мультимедиа создает событие Месаурцесикед.'
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Событие Местреамсикед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263638"
---
# <a name="mestreamseeked-event"></a><span data-ttu-id="66543-104">Событие Местреамсикед</span><span class="sxs-lookup"><span data-stu-id="66543-104">MEStreamSeeked event</span></span>

<span data-ttu-id="66543-105">Вызывается потоком мультимедиа после вызова [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) , чтобы выполнить поиск в потоке.</span><span class="sxs-lookup"><span data-stu-id="66543-105">Raised by a media stream after a call to [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causes a seek in the stream.</span></span> <span data-ttu-id="66543-106">Поток мультимедиа вызывает это событие, когда источник мультимедиа создает событие [месаурцесикед](mesourceseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="66543-106">A media stream raises this event when the media source raises the [MESourceSeeked](mesourceseeked.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="66543-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="66543-107">Event values</span></span>

<span data-ttu-id="66543-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="66543-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="66543-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="66543-109">VARTYPE</span></span>           | <span data-ttu-id="66543-110">Описание</span><span class="sxs-lookup"><span data-stu-id="66543-110">Description</span></span>                                                        |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="66543-111">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="66543-111">VT\_I8</span></span><br/> | <span data-ttu-id="66543-112">Новое время начала, в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="66543-112">New starting time, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="66543-113">Требования</span><span class="sxs-lookup"><span data-stu-id="66543-113">Requirements</span></span>



| <span data-ttu-id="66543-114">Требование</span><span class="sxs-lookup"><span data-stu-id="66543-114">Requirement</span></span> | <span data-ttu-id="66543-115">Значение</span><span class="sxs-lookup"><span data-stu-id="66543-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66543-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66543-116">Minimum supported client</span></span><br/> | <span data-ttu-id="66543-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66543-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="66543-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66543-118">Minimum supported server</span></span><br/> | <span data-ttu-id="66543-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66543-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66543-120">Header</span><span class="sxs-lookup"><span data-stu-id="66543-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="66543-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66543-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66543-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66543-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66543-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66543-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




