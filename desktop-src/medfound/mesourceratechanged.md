---
description: 'Вызывается источником мультимедиа при изменении частоты воспроизведения. Это событие отправляется после асинхронного завершения метода Имфратеконтрол:: Сетрате.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Событие Месаурцератечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154655"
---
# <a name="mesourceratechanged-event"></a><span data-ttu-id="22b2d-104">Событие Месаурцератечанжед</span><span class="sxs-lookup"><span data-stu-id="22b2d-104">MESourceRateChanged event</span></span>

<span data-ttu-id="22b2d-105">Вызывается источником мультимедиа при изменении частоты воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="22b2d-105">Raised by a media source when the playback rate changes.</span></span> <span data-ttu-id="22b2d-106">Это событие отправляется после асинхронного завершения метода [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) .</span><span class="sxs-lookup"><span data-stu-id="22b2d-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="22b2d-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="22b2d-107">Event values</span></span>

<span data-ttu-id="22b2d-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="22b2d-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="22b2d-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="22b2d-109">VARTYPE</span></span>           | <span data-ttu-id="22b2d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="22b2d-110">Description</span></span>                                   |
|-------------------|-----------------------------------------------|
| <span data-ttu-id="22b2d-111">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="22b2d-111">VT\_R4</span></span><br/> | <span data-ttu-id="22b2d-112">Новая скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="22b2d-112">The new playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="22b2d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="22b2d-113">Requirements</span></span>



| <span data-ttu-id="22b2d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="22b2d-114">Requirement</span></span> | <span data-ttu-id="22b2d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="22b2d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b2d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22b2d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="22b2d-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22b2d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="22b2d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22b2d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="22b2d-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="22b2d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="22b2d-120">Header</span><span class="sxs-lookup"><span data-stu-id="22b2d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="22b2d-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22b2d-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22b2d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22b2d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b2d-123">Реализация управления скоростью</span><span class="sxs-lookup"><span data-stu-id="22b2d-123">Implementing Rate Control</span></span>](implementing-rate-control.md)
</dt> <dt>

[<span data-ttu-id="22b2d-124">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="22b2d-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="22b2d-125">Управление скоростью</span><span class="sxs-lookup"><span data-stu-id="22b2d-125">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="22b2d-126">**Имфратеконтрол:: Сетрате**</span><span class="sxs-lookup"><span data-stu-id="22b2d-126">**IMFRateControl::SetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




