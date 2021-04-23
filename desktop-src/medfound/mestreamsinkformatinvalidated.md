---
description: Посылается приемником потока, когда нисходящий формат становится недействительным, и его необходимо повторно согласовать.
ms.assetid: 732B3BDD-F394-430F-B895-AF18ED61114D
title: Событие Местреамсинкформатинвалидатед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39c4453c0d5720ffb57f1277946f9cf891ed443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711214"
---
# <a name="mestreamsinkformatinvalidated-event"></a><span data-ttu-id="25e84-103">Событие Местреамсинкформатинвалидатед</span><span class="sxs-lookup"><span data-stu-id="25e84-103">MEStreamSinkFormatInvalidated event</span></span>

<span data-ttu-id="25e84-104">Посылается приемником потока, когда нисходящий формат становится недействительным, и его необходимо повторно согласовать.</span><span class="sxs-lookup"><span data-stu-id="25e84-104">Sent by a stream sink when the downstream format has become invalidated and it needs to be renegotiated.</span></span>

## <a name="event-values"></a><span data-ttu-id="25e84-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="25e84-105">Event values</span></span>

<span data-ttu-id="25e84-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="25e84-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="25e84-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="25e84-107">VARTYPE</span></span>              | <span data-ttu-id="25e84-108">Описание</span><span class="sxs-lookup"><span data-stu-id="25e84-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="25e84-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="25e84-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="25e84-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="25e84-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="25e84-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25e84-111">Remarks</span></span>

<span data-ttu-id="25e84-112">Необходимо повторно отправить данные, помещенные в очередь на приемник, после текущей позиции воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="25e84-112">Data that was queued to the sink, past the current playback position, should be resent.</span></span>

## <a name="requirements"></a><span data-ttu-id="25e84-113">Требования</span><span class="sxs-lookup"><span data-stu-id="25e84-113">Requirements</span></span>



| <span data-ttu-id="25e84-114">Требование</span><span class="sxs-lookup"><span data-stu-id="25e84-114">Requirement</span></span> | <span data-ttu-id="25e84-115">Значение</span><span class="sxs-lookup"><span data-stu-id="25e84-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25e84-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25e84-116">Minimum supported client</span></span><br/> | <span data-ttu-id="25e84-117">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="25e84-117">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                                      |
| <span data-ttu-id="25e84-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25e84-118">Minimum supported server</span></span><br/> | <span data-ttu-id="25e84-119">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="25e84-119">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="25e84-120">Header</span><span class="sxs-lookup"><span data-stu-id="25e84-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="25e84-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25e84-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e84-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25e84-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e84-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25e84-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




