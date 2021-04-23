---
description: Вызывается сеансом мультимедиа, когда он завершает воспроизведение последней презентации в очереди воспроизведения.
ms.assetid: e593e51f-c239-49e9-bba8-c6d8238eff24
title: Событие Месессионендед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447b222be48dccc0f190329ab0bb6d56d09b266e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719452"
---
# <a name="mesessionended-event"></a><span data-ttu-id="12a7a-103">Событие Месессионендед</span><span class="sxs-lookup"><span data-stu-id="12a7a-103">MESessionEnded event</span></span>

<span data-ttu-id="12a7a-104">Вызывается сеансом мультимедиа, когда он завершает воспроизведение последней презентации в очереди воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="12a7a-104">Raised by the Media Session when it has finished playing the last presentation in the playback queue.</span></span>

## <a name="event-values"></a><span data-ttu-id="12a7a-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="12a7a-105">Event values</span></span>

<span data-ttu-id="12a7a-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="12a7a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="12a7a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="12a7a-107">VARTYPE</span></span>              | <span data-ttu-id="12a7a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="12a7a-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="12a7a-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="12a7a-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="12a7a-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="12a7a-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="12a7a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="12a7a-111">Requirements</span></span>



| <span data-ttu-id="12a7a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="12a7a-112">Requirement</span></span> | <span data-ttu-id="12a7a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="12a7a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12a7a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12a7a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="12a7a-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12a7a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12a7a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12a7a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="12a7a-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="12a7a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="12a7a-118">Header</span><span class="sxs-lookup"><span data-stu-id="12a7a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="12a7a-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12a7a-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12a7a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12a7a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a7a-121">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12a7a-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




