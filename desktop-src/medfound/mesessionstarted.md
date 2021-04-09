---
description: 'Возникает, когда метод Имфмедиасессион:: Start завершается асинхронно.'
ms.assetid: 28ed32f0-9b23-4da1-9587-15f490da7bf9
title: Событие Месессионстартед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9510fb5f5dda3d14b916ed40dcba4ca05800b52b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080492"
---
# <a name="mesessionstarted-event"></a><span data-ttu-id="b130b-103">Событие Месессионстартед</span><span class="sxs-lookup"><span data-stu-id="b130b-103">MESessionStarted event</span></span>

<span data-ttu-id="b130b-104">Возникает, когда метод [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="b130b-104">Raised when the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="b130b-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="b130b-105">Event values</span></span>

<span data-ttu-id="b130b-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="b130b-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b130b-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b130b-107">VARTYPE</span></span>              | <span data-ttu-id="b130b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b130b-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b130b-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="b130b-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b130b-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="b130b-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="b130b-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b130b-111">Attributes</span></span>

<span data-ttu-id="b130b-112">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="b130b-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="b130b-113">attribute</span><span class="sxs-lookup"><span data-stu-id="b130b-113">Attribute</span></span>                                                                                               | <span data-ttu-id="b130b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b130b-114">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b130b-115">**\_ \_ \_ смещение времени презентации событий \_ MF**</span><span class="sxs-lookup"><span data-stu-id="b130b-115">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/> | <span data-ttu-id="b130b-116">Смещение между временем презентации и штампами времени источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b130b-116">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b130b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b130b-117">Requirements</span></span>



| <span data-ttu-id="b130b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b130b-118">Requirement</span></span> | <span data-ttu-id="b130b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b130b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b130b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b130b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b130b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b130b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b130b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b130b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b130b-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b130b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b130b-124">Header</span><span class="sxs-lookup"><span data-stu-id="b130b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b130b-125"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b130b-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b130b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b130b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b130b-127">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b130b-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




