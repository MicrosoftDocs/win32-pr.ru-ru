---
description: Возникает, когда метод Имфмедиасессион::P Аусе завершается асинхронно.
ms.assetid: 72546082-83ec-4481-a24f-e82bd6c88859
title: Событие Месессионпаусед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd3e8ef60426f83203cfffae3a75febfdf7032d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155583"
---
# <a name="mesessionpaused-event"></a><span data-ttu-id="b6538-103">Событие Месессионпаусед</span><span class="sxs-lookup"><span data-stu-id="b6538-103">MESessionPaused event</span></span>

<span data-ttu-id="b6538-104">Возникает, когда метод [**имфмедиасессион::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="b6538-104">Raised when the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="b6538-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="b6538-105">Event values</span></span>

<span data-ttu-id="b6538-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="b6538-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b6538-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b6538-107">VARTYPE</span></span>              | <span data-ttu-id="b6538-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b6538-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b6538-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="b6538-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b6538-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="b6538-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b6538-111">Требования</span><span class="sxs-lookup"><span data-stu-id="b6538-111">Requirements</span></span>



| <span data-ttu-id="b6538-112">Требование</span><span class="sxs-lookup"><span data-stu-id="b6538-112">Requirement</span></span> | <span data-ttu-id="b6538-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b6538-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6538-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6538-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b6538-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6538-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6538-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6538-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b6538-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6538-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6538-118">Header</span><span class="sxs-lookup"><span data-stu-id="b6538-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6538-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6538-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6538-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6538-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6538-121">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6538-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




