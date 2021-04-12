---
description: 'Вызывается сеансом мультимедиа, когда метод Имфмедиасессион:: Клеартопологиес завершается асинхронно.'
ms.assetid: 2017d13b-8dc2-48f9-a21e-7b826e174edf
title: Событие Месессионтопологиесклеаред (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551e98607a8d23d9333527337bbd7d038ed0b340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155579"
---
# <a name="mesessiontopologiescleared-event"></a><span data-ttu-id="fb685-103">Событие Месессионтопологиесклеаред</span><span class="sxs-lookup"><span data-stu-id="fb685-103">MESessionTopologiesCleared event</span></span>

<span data-ttu-id="fb685-104">Вызывается сеансом мультимедиа, когда метод [**имфмедиасессион:: клеартопологиес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="fb685-104">Raised by the Media Session when the [**IMFMediaSession::ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="fb685-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="fb685-105">Event values</span></span>

<span data-ttu-id="fb685-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="fb685-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="fb685-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="fb685-107">VARTYPE</span></span>              | <span data-ttu-id="fb685-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fb685-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="fb685-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="fb685-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="fb685-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="fb685-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="fb685-111">Требования</span><span class="sxs-lookup"><span data-stu-id="fb685-111">Requirements</span></span>



| <span data-ttu-id="fb685-112">Требование</span><span class="sxs-lookup"><span data-stu-id="fb685-112">Requirement</span></span> | <span data-ttu-id="fb685-113">Значение</span><span class="sxs-lookup"><span data-stu-id="fb685-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb685-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb685-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fb685-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb685-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fb685-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb685-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fb685-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb685-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fb685-118">Header</span><span class="sxs-lookup"><span data-stu-id="fb685-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb685-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb685-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb685-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb685-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb685-121">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb685-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




