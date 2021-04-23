---
description: Вызывается потоком мультимедиа при запуске или при остановке потока. Дополнительные сведения об сужении см. в разделе сведения об управлении скоростью.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Событие Местреамсинмоде (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701895"
---
# <a name="mestreamthinmode-event"></a><span data-ttu-id="4febb-104">Событие Местреамсинмоде</span><span class="sxs-lookup"><span data-stu-id="4febb-104">MEStreamThinMode event</span></span>

<span data-ttu-id="4febb-105">Вызывается потоком мультимедиа при запуске или при остановке потока.</span><span class="sxs-lookup"><span data-stu-id="4febb-105">Raised by a media stream when it starts or stops thinning the stream.</span></span> <span data-ttu-id="4febb-106">Дополнительные сведения об *сужении* см. в разделе [сведения об управлении скоростью](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="4febb-106">For information about *thinning*, see [About Rate Control](about-rate-control.md).</span></span>

<span data-ttu-id="4febb-107">Это событие можно отправить в ответ на метод [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) или метод [**Имфкуалитядвисе:: сетдропмоде**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .</span><span class="sxs-lookup"><span data-stu-id="4febb-107">This event can be sent in response to the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method or the [**IMFQualityAdvise::SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="4febb-108">Значения событий</span><span class="sxs-lookup"><span data-stu-id="4febb-108">Event values</span></span>

<span data-ttu-id="4febb-109">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="4febb-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4febb-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4febb-110">VARTYPE</span></span></th>
<th><span data-ttu-id="4febb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4febb-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4febb-112">VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="4febb-112">VT_BOOL</span></span><br/></td>
<td><span data-ttu-id="4febb-113">Указывает, началось ли тонкое начало или прекращение.</span><span class="sxs-lookup"><span data-stu-id="4febb-113">Indicates whether thinning has started or stopped.</span></span><br/>
<ul>
<li><span data-ttu-id="4febb-114">VARIANT_TRUE: образцы, доставленные после этого события, будут тоньше.</span><span class="sxs-lookup"><span data-stu-id="4febb-114">VARIANT_TRUE: Samples delivered after this event are thinned.</span></span></li>
<li><span data-ttu-id="4febb-115">VARIANT_FALSE: образцы, доставленные после этого события, не будут тоньше.</span><span class="sxs-lookup"><span data-stu-id="4febb-115">VARIANT_FALSE: Samples delivered after this event are not thinned.</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="4febb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4febb-116">Requirements</span></span>



| <span data-ttu-id="4febb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4febb-117">Requirement</span></span> | <span data-ttu-id="4febb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4febb-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4febb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4febb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4febb-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4febb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4febb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4febb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4febb-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4febb-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4febb-123">Header</span><span class="sxs-lookup"><span data-stu-id="4febb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4febb-124"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4febb-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4febb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4febb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4febb-126">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4febb-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




