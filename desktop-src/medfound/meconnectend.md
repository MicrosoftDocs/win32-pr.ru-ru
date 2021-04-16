---
description: Порождается сетевым источником после завершения открытия URL-адреса.
ms.assetid: 737aec32-24f4-4825-ad34-8d2fc889bc09
title: Событие Меконнектенд (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9801b1af38f7bf0a0107680d77a399b3927a616e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719394"
---
# <a name="meconnectend-event"></a><span data-ttu-id="6a5be-103">Событие Меконнектенд</span><span class="sxs-lookup"><span data-stu-id="6a5be-103">MEConnectEnd event</span></span>

<span data-ttu-id="6a5be-104">Порождается сетевым источником после завершения открытия URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="6a5be-104">Raised by the network source when it finishes opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="6a5be-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="6a5be-105">Event values</span></span>

<span data-ttu-id="6a5be-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="6a5be-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6a5be-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6a5be-107">VARTYPE</span></span>              | <span data-ttu-id="6a5be-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6a5be-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="6a5be-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="6a5be-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="6a5be-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="6a5be-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6a5be-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a5be-111">Remarks</span></span>

<span data-ttu-id="6a5be-112">Источник сети отправляет это событие непосредственно в приложение через метод [**имфсаурцеопенмонитор:: онсаурцеевент**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) приложения, а не через обычный интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="6a5be-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a5be-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6a5be-113">Requirements</span></span>



| <span data-ttu-id="6a5be-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6a5be-114">Requirement</span></span> | <span data-ttu-id="6a5be-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6a5be-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a5be-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a5be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a5be-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a5be-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6a5be-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a5be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a5be-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a5be-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6a5be-120">Header</span><span class="sxs-lookup"><span data-stu-id="6a5be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a5be-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a5be-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a5be-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a5be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a5be-123">**имфсаурцеопенмонитор**</span><span class="sxs-lookup"><span data-stu-id="6a5be-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="6a5be-124">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a5be-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




