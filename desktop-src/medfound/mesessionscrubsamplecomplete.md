---
description: Вызывается сеансом мультимедиа при завершении запроса на очистку.
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: Событие Месессионскрубсамплекомплете (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076c2f2978831cc30521fcf49d71c04620c4dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898378"
---
# <a name="mesessionscrubsamplecomplete-event"></a><span data-ttu-id="6e7b8-103">Событие Месессионскрубсамплекомплете</span><span class="sxs-lookup"><span data-stu-id="6e7b8-103">MESessionScrubSampleComplete event</span></span>

<span data-ttu-id="6e7b8-104">Вызывается сеансом мультимедиа при завершении запроса на очистку.</span><span class="sxs-lookup"><span data-stu-id="6e7b8-104">Raised by the Media Session when it completes a scrubbing request.</span></span>

<span data-ttu-id="6e7b8-105">Очистка происходит, когда скорость воспроизведения равна нулю и приложение вызывает [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="6e7b8-105">Scrubbing occurs when the playback rate is zero and the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="6e7b8-106">Это событие возникает после завершения запроса очистки каждым приемником потока.</span><span class="sxs-lookup"><span data-stu-id="6e7b8-106">This event is raised after every stream sink has completed the scrubbing request.</span></span>

## <a name="event-values"></a><span data-ttu-id="6e7b8-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="6e7b8-107">Event values</span></span>

<span data-ttu-id="6e7b8-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="6e7b8-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6e7b8-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6e7b8-109">VARTYPE</span></span>              | <span data-ttu-id="6e7b8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6e7b8-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="6e7b8-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="6e7b8-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="6e7b8-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="6e7b8-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="6e7b8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6e7b8-113">Requirements</span></span>



| <span data-ttu-id="6e7b8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6e7b8-114">Requirement</span></span> | <span data-ttu-id="6e7b8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6e7b8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e7b8-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e7b8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e7b8-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e7b8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6e7b8-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e7b8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e7b8-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e7b8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e7b8-120">Header</span><span class="sxs-lookup"><span data-stu-id="6e7b8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e7b8-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e7b8-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e7b8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e7b8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e7b8-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6e7b8-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="6e7b8-124">местреамсинкскрубсамплекомплете</span><span class="sxs-lookup"><span data-stu-id="6e7b8-124">MEStreamSinkScrubSampleComplete</span></span>](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




