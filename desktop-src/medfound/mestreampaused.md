---
description: Вызывается потоком мультимедиа, когда метод Имфмедиасаурце::P Аусе завершается асинхронно.
ms.assetid: 8fafb9a1-95a4-44b6-acd6-fb007d515915
title: Событие Местреампаусед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78147c7cdd7cb6e391052111e11ef0ac92b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711215"
---
# <a name="mestreampaused-event"></a><span data-ttu-id="e9ddc-103">Событие Местреампаусед</span><span class="sxs-lookup"><span data-stu-id="e9ddc-103">MEStreamPaused event</span></span>

<span data-ttu-id="e9ddc-104">Вызывается потоком мультимедиа, когда метод [**имфмедиасаурце::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="e9ddc-104">Raised by a media stream when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="e9ddc-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="e9ddc-105">Event values</span></span>

<span data-ttu-id="e9ddc-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="e9ddc-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e9ddc-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e9ddc-107">VARTYPE</span></span>              | <span data-ttu-id="e9ddc-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e9ddc-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e9ddc-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="e9ddc-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e9ddc-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="e9ddc-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e9ddc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9ddc-111">Remarks</span></span>

<span data-ttu-id="e9ddc-112">Каждый активный поток в презентации отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="e9ddc-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ddc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e9ddc-113">Requirements</span></span>



| <span data-ttu-id="e9ddc-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e9ddc-114">Requirement</span></span> | <span data-ttu-id="e9ddc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e9ddc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ddc-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9ddc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ddc-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9ddc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e9ddc-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9ddc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ddc-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9ddc-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9ddc-120">Header</span><span class="sxs-lookup"><span data-stu-id="e9ddc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ddc-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9ddc-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ddc-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9ddc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ddc-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9ddc-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




