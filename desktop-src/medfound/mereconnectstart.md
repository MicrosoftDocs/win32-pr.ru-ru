---
description: Сигнализирует, что источник мультимедиа пытается повторно подключиться к серверу.
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: Событие Мереконнектстарт (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21944e937f52205416b5e6e2b52d18c3a3c768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155587"
---
# <a name="mereconnectstart-event"></a><span data-ttu-id="c032b-103">Событие Мереконнектстарт</span><span class="sxs-lookup"><span data-stu-id="c032b-103">MEReconnectStart event</span></span>

<span data-ttu-id="c032b-104">Сигнализирует, что источник мультимедиа пытается повторно подключиться к серверу.</span><span class="sxs-lookup"><span data-stu-id="c032b-104">Signals that a media source is attempting to reconnect to the server.</span></span>

<span data-ttu-id="c032b-105">Вызвано медиа-источником в начале попытки повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="c032b-105">Raised by a media source at the start of a reconnection attempt.</span></span> <span data-ttu-id="c032b-106">Источник сети создает это событие, если пытается повторно подключиться к серверу.</span><span class="sxs-lookup"><span data-stu-id="c032b-106">The network source raises this event if it attempts to reconnect to the server.</span></span> <span data-ttu-id="c032b-107">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="c032b-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="c032b-108">Значения событий</span><span class="sxs-lookup"><span data-stu-id="c032b-108">Event values</span></span>

<span data-ttu-id="c032b-109">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="c032b-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c032b-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c032b-110">VARTYPE</span></span>              | <span data-ttu-id="c032b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c032b-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c032b-112">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="c032b-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c032b-113">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="c032b-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="c032b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c032b-114">Requirements</span></span>



| <span data-ttu-id="c032b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c032b-115">Requirement</span></span> | <span data-ttu-id="c032b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c032b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c032b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c032b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c032b-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c032b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c032b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c032b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c032b-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c032b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c032b-121">Header</span><span class="sxs-lookup"><span data-stu-id="c032b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c032b-122"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c032b-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c032b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c032b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c032b-124">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c032b-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




