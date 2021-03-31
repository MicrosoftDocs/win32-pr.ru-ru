---
description: Вызывается приемником потока при завершении перехода в остановленное состояние. Переход на остановленный происходит при вызове метода остановки Имфпресентатионклокк для часов представления приемников.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Событие Местреамсинкстоппед (Мфобжектс. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35313ab3d43c950184a82e403fa6ad0eb5b4ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081108"
---
# <a name="mestreamsinkstopped-event"></a><span data-ttu-id="86cc7-104">Событие Местреамсинкстоппед</span><span class="sxs-lookup"><span data-stu-id="86cc7-104">MEStreamSinkStopped event</span></span>

<span data-ttu-id="86cc7-105">Вызывается приемником потока при завершении перехода в остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="86cc7-105">Raised by a stream sink when it completes the transition to the stopped state.</span></span> <span data-ttu-id="86cc7-106">Переход на остановленный происходит при вызове метода [**имфпресентатионклокк:: остановки**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) в часах представления приемника.</span><span class="sxs-lookup"><span data-stu-id="86cc7-106">The transition to stopped occurs when the [**IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="86cc7-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="86cc7-107">Event values</span></span>

<span data-ttu-id="86cc7-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="86cc7-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="86cc7-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="86cc7-109">VARTYPE</span></span>              | <span data-ttu-id="86cc7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="86cc7-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="86cc7-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="86cc7-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="86cc7-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="86cc7-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="86cc7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="86cc7-113">Requirements</span></span>



| <span data-ttu-id="86cc7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="86cc7-114">Requirement</span></span> | <span data-ttu-id="86cc7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="86cc7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86cc7-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86cc7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="86cc7-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86cc7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="86cc7-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86cc7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="86cc7-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86cc7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86cc7-120">Header</span><span class="sxs-lookup"><span data-stu-id="86cc7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="86cc7-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86cc7-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86cc7-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86cc7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86cc7-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86cc7-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="86cc7-124">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="86cc7-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




