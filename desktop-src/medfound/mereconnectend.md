---
description: Сигнализирует о том, что источник мультимедиа завершил попытку повторного подключения к серверу.
ms.assetid: 228e069a-a26b-472e-915e-ff9aec5ee9c1
title: Событие Мереконнектенд (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3477abd5d4413faa6b2d965f7ace2d19c48dd786
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544383"
---
# <a name="mereconnectend-event"></a><span data-ttu-id="d22b5-103">Событие Мереконнектенд</span><span class="sxs-lookup"><span data-stu-id="d22b5-103">MEReconnectEnd event</span></span>

<span data-ttu-id="d22b5-104">Сигнализирует о том, что источник мультимедиа завершил попытку повторного подключения к серверу.</span><span class="sxs-lookup"><span data-stu-id="d22b5-104">Signals that a media source has completed an attempt to reconnect to the server.</span></span>

<span data-ttu-id="d22b5-105">Вызвано источником мультимедиа в конце попытки повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="d22b5-105">Raised by a media source at the end of a reconnection attempt.</span></span> <span data-ttu-id="d22b5-106">Источник сети создает это событие, если оно повторно подключается к серверу.</span><span class="sxs-lookup"><span data-stu-id="d22b5-106">The network source raises this event if it reconnects to the server.</span></span> <span data-ttu-id="d22b5-107">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="d22b5-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="d22b5-108">Значения событий</span><span class="sxs-lookup"><span data-stu-id="d22b5-108">Event values</span></span>

<span data-ttu-id="d22b5-109">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="d22b5-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d22b5-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d22b5-110">VARTYPE</span></span>              | <span data-ttu-id="d22b5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d22b5-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d22b5-112">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="d22b5-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d22b5-113">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="d22b5-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="d22b5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d22b5-114">Requirements</span></span>



| <span data-ttu-id="d22b5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d22b5-115">Requirement</span></span> | <span data-ttu-id="d22b5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d22b5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d22b5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d22b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d22b5-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d22b5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d22b5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d22b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d22b5-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d22b5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d22b5-121">Header</span><span class="sxs-lookup"><span data-stu-id="d22b5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d22b5-122"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d22b5-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d22b5-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d22b5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22b5-124">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d22b5-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




