---
description: Вызывается приемником потока для запроса нового примера носителя из конвейера.
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: Событие Местреамсинкрекуестсампле (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c5afbfa9f0cfe4b320b451e699612a4729c23a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673500"
---
# <a name="mestreamsinkrequestsample-event"></a><span data-ttu-id="1ef17-103">Событие Местреамсинкрекуестсампле</span><span class="sxs-lookup"><span data-stu-id="1ef17-103">MEStreamSinkRequestSample event</span></span>

<span data-ttu-id="1ef17-104">Вызывается приемником потока для запроса нового примера носителя из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1ef17-104">Raised by a stream sink to request a new media sample from the pipeline.</span></span> <span data-ttu-id="1ef17-105">Для каждого события Местреамсинкрекуестсампле конвейер запрашивает данные от следующего вышестоящего компонента.</span><span class="sxs-lookup"><span data-stu-id="1ef17-105">For each MEStreamSinkRequestSample event, the pipeline requests data from the next upstream component.</span></span>

## <a name="event-values"></a><span data-ttu-id="1ef17-106">Значения событий</span><span class="sxs-lookup"><span data-stu-id="1ef17-106">Event values</span></span>

<span data-ttu-id="1ef17-107">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="1ef17-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1ef17-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1ef17-108">VARTYPE</span></span>              | <span data-ttu-id="1ef17-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1ef17-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="1ef17-110">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="1ef17-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="1ef17-111">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="1ef17-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="1ef17-112">Требования</span><span class="sxs-lookup"><span data-stu-id="1ef17-112">Requirements</span></span>



| <span data-ttu-id="1ef17-113">Требование</span><span class="sxs-lookup"><span data-stu-id="1ef17-113">Requirement</span></span> | <span data-ttu-id="1ef17-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1ef17-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef17-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ef17-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef17-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ef17-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1ef17-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ef17-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef17-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ef17-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ef17-119">Header</span><span class="sxs-lookup"><span data-stu-id="1ef17-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ef17-120"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ef17-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ef17-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ef17-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef17-122">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ef17-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="1ef17-123">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="1ef17-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




