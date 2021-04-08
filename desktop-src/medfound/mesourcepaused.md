---
description: Вызывается источником мультимедиа, когда метод Имфмедиасаурце::P Аусе завершается асинхронно.
ms.assetid: cca03d60-47ae-4a11-b29d-81d749e24df9
title: Событие Месаурцепаусед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac346e679eb3a82ca707a14f772f1a79e2a1e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898373"
---
# <a name="mesourcepaused-event"></a><span data-ttu-id="97174-103">Событие Месаурцепаусед</span><span class="sxs-lookup"><span data-stu-id="97174-103">MESourcePaused event</span></span>

<span data-ttu-id="97174-104">Вызывается источником мультимедиа, когда метод [**имфмедиасаурце::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="97174-104">Raised by a media source when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="97174-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="97174-105">Event values</span></span>

<span data-ttu-id="97174-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="97174-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="97174-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="97174-107">VARTYPE</span></span>              | <span data-ttu-id="97174-108">Описание</span><span class="sxs-lookup"><span data-stu-id="97174-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="97174-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="97174-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="97174-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="97174-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="97174-111">Требования</span><span class="sxs-lookup"><span data-stu-id="97174-111">Requirements</span></span>



| <span data-ttu-id="97174-112">Требование</span><span class="sxs-lookup"><span data-stu-id="97174-112">Requirement</span></span> | <span data-ttu-id="97174-113">Значение</span><span class="sxs-lookup"><span data-stu-id="97174-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97174-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97174-114">Minimum supported client</span></span><br/> | <span data-ttu-id="97174-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97174-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="97174-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97174-116">Minimum supported server</span></span><br/> | <span data-ttu-id="97174-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97174-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97174-118">Header</span><span class="sxs-lookup"><span data-stu-id="97174-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="97174-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97174-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97174-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97174-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97174-121">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97174-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




