---
description: Вызывается приемником потока, когда поток получил достаточное количество предварительных данных для начала подготовки к просмотру. Это событие вызывается приемниками носителей, поддерживающими интерфейс Имфмедиасинкпреролл.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Событие Местреамсинкпрероллед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312daa90c995ccbbe8667cfa5acdf47975248474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811867"
---
# <a name="mestreamsinkprerolled-event"></a><span data-ttu-id="56497-104">Событие Местреамсинкпрероллед</span><span class="sxs-lookup"><span data-stu-id="56497-104">MEStreamSinkPrerolled event</span></span>

<span data-ttu-id="56497-105">Вызывается приемником потока, когда поток получил достаточное количество предварительных данных для начала подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="56497-105">Raised by a stream sink when the stream has received enough pre-roll data to begin rendering.</span></span> <span data-ttu-id="56497-106">Это событие вызывается приемниками носителей, поддерживающими интерфейс [**имфмедиасинкпреролл**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .</span><span class="sxs-lookup"><span data-stu-id="56497-106">This event is raised by media sinks that support the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="56497-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="56497-107">Event values</span></span>

<span data-ttu-id="56497-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="56497-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="56497-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="56497-109">VARTYPE</span></span>              | <span data-ttu-id="56497-110">Описание</span><span class="sxs-lookup"><span data-stu-id="56497-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="56497-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="56497-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="56497-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="56497-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="56497-113">Требования</span><span class="sxs-lookup"><span data-stu-id="56497-113">Requirements</span></span>



| <span data-ttu-id="56497-114">Требование</span><span class="sxs-lookup"><span data-stu-id="56497-114">Requirement</span></span> | <span data-ttu-id="56497-115">Значение</span><span class="sxs-lookup"><span data-stu-id="56497-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56497-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56497-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56497-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56497-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="56497-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56497-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56497-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="56497-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="56497-120">Header</span><span class="sxs-lookup"><span data-stu-id="56497-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="56497-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56497-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56497-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56497-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56497-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="56497-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="56497-124">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="56497-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




