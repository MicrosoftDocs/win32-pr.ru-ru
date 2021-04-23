---
description: Возникает при завершении приобретения лицензии. Дополнительные сведения см. в разделе Мелиценсеаккуиситионстарт.
ms.assetid: f577131b-887a-4912-8278-1165a801c2b3
title: Событие Мелиценсеаккуиситионкомплетед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 545fa012f974637f5d268a7d8257daaf9b393f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656583"
---
# <a name="melicenseacquisitioncompleted-event"></a><span data-ttu-id="c6400-104">Событие Мелиценсеаккуиситионкомплетед</span><span class="sxs-lookup"><span data-stu-id="c6400-104">MELicenseAcquisitionCompleted event</span></span>

<span data-ttu-id="c6400-105">Возникает при завершении приобретения лицензии.</span><span class="sxs-lookup"><span data-stu-id="c6400-105">Raised when license acquisition is complete.</span></span> <span data-ttu-id="c6400-106">Дополнительные сведения см. в разделе [мелиценсеаккуиситионстарт](melicenseacquisitionstart.md).</span><span class="sxs-lookup"><span data-stu-id="c6400-106">For more information, see [MELicenseAcquisitionStart](melicenseacquisitionstart.md).</span></span>

## <a name="event-values"></a><span data-ttu-id="c6400-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="c6400-107">Event values</span></span>

<span data-ttu-id="c6400-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="c6400-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c6400-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c6400-109">VARTYPE</span></span>              | <span data-ttu-id="c6400-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c6400-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c6400-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="c6400-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c6400-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="c6400-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="c6400-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c6400-113">Requirements</span></span>



| <span data-ttu-id="c6400-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c6400-114">Requirement</span></span> | <span data-ttu-id="c6400-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c6400-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6400-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6400-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c6400-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6400-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6400-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6400-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c6400-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6400-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6400-120">Header</span><span class="sxs-lookup"><span data-stu-id="c6400-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6400-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6400-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6400-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6400-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6400-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6400-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




