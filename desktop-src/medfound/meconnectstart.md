---
description: Вызывается сетевым источником при открытии URL-адреса.
ms.assetid: 0844ac10-cc5b-4e7f-92df-3a5901c72148
title: Событие Меконнектстарт (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8e45d723a62854c34ba7b297e462d03fed97a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543266"
---
# <a name="meconnectstart-event"></a><span data-ttu-id="78d52-103">Событие Меконнектстарт</span><span class="sxs-lookup"><span data-stu-id="78d52-103">MEConnectStart event</span></span>

<span data-ttu-id="78d52-104">Вызывается сетевым источником при открытии URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="78d52-104">Raised by the network source when it starts opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="78d52-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="78d52-105">Event values</span></span>

<span data-ttu-id="78d52-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="78d52-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="78d52-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="78d52-107">VARTYPE</span></span>              | <span data-ttu-id="78d52-108">Описание</span><span class="sxs-lookup"><span data-stu-id="78d52-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="78d52-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="78d52-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="78d52-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="78d52-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="78d52-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78d52-111">Remarks</span></span>

<span data-ttu-id="78d52-112">Источник сети отправляет это событие непосредственно в приложение через метод [**имфсаурцеопенмонитор:: онсаурцеевент**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) приложения, а не через обычный интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="78d52-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="78d52-113">Требования</span><span class="sxs-lookup"><span data-stu-id="78d52-113">Requirements</span></span>



| <span data-ttu-id="78d52-114">Требование</span><span class="sxs-lookup"><span data-stu-id="78d52-114">Requirement</span></span> | <span data-ttu-id="78d52-115">Значение</span><span class="sxs-lookup"><span data-stu-id="78d52-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78d52-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78d52-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78d52-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78d52-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78d52-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78d52-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78d52-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78d52-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78d52-120">Header</span><span class="sxs-lookup"><span data-stu-id="78d52-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="78d52-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78d52-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78d52-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78d52-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d52-123">**имфсаурцеопенмонитор**</span><span class="sxs-lookup"><span data-stu-id="78d52-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="78d52-124">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="78d52-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




