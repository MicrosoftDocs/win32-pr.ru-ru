---
description: 'Вызывается сеансом мультимедиа при изменении частоты воспроизведения. Это событие отправляется после асинхронного завершения метода Имфратеконтрол:: Сетрате.'
ms.assetid: 6bef923f-4083-46e1-9a2e-49a6825467ec
title: Событие Месессионратечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4cbbd8254dfb988c94cf2016164726d578d8906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898381"
---
# <a name="mesessionratechanged-event"></a><span data-ttu-id="ab47a-104">Событие Месессионратечанжед</span><span class="sxs-lookup"><span data-stu-id="ab47a-104">MESessionRateChanged event</span></span>

<span data-ttu-id="ab47a-105">Вызывается сеансом мультимедиа при изменении частоты воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ab47a-105">Raised by the Media Session when the playback rate changes.</span></span> <span data-ttu-id="ab47a-106">Это событие отправляется после асинхронного завершения метода [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) .</span><span class="sxs-lookup"><span data-stu-id="ab47a-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="ab47a-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="ab47a-107">Event values</span></span>

<span data-ttu-id="ab47a-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="ab47a-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ab47a-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ab47a-109">VARTYPE</span></span>           | <span data-ttu-id="ab47a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ab47a-110">Description</span></span>                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab47a-111">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="ab47a-111">VT\_R4</span></span><br/> | <span data-ttu-id="ab47a-112">Новая скорость воспроизведения, выраженная в виде коэффициента обычной скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ab47a-112">The new playback rate, expressed as a ratio of the normal playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ab47a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ab47a-113">Requirements</span></span>



| <span data-ttu-id="ab47a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ab47a-114">Requirement</span></span> | <span data-ttu-id="ab47a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ab47a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab47a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab47a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab47a-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab47a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ab47a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab47a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab47a-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab47a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ab47a-120">Header</span><span class="sxs-lookup"><span data-stu-id="ab47a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab47a-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab47a-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab47a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab47a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab47a-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab47a-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




