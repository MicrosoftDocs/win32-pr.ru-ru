---
description: Вызывается приемником потока, когда тип носителя приемников больше не действителен.
ms.assetid: 9eeb4262-1593-4c5f-9341-ebd328b586e7
title: Событие Местреамсинкформатчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04c62072f69425079753ef4d0a56edcf8d65d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263637"
---
# <a name="mestreamsinkformatchanged-event"></a><span data-ttu-id="ccf6a-103">Событие Местреамсинкформатчанжед</span><span class="sxs-lookup"><span data-stu-id="ccf6a-103">MEStreamSinkFormatChanged event</span></span>

<span data-ttu-id="ccf6a-104">Вызывается приемником потока, когда тип носителя приемника больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="ccf6a-104">Raised by a stream sink when the sink's media type is no longer valid.</span></span>

## <a name="event-values"></a><span data-ttu-id="ccf6a-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="ccf6a-105">Event values</span></span>

<span data-ttu-id="ccf6a-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="ccf6a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ccf6a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ccf6a-107">VARTYPE</span></span>              | <span data-ttu-id="ccf6a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ccf6a-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ccf6a-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="ccf6a-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ccf6a-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="ccf6a-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ccf6a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccf6a-111">Remarks</span></span>

<span data-ttu-id="ccf6a-112">Приемник потока может вызвать это, даже если что-то произошло, что сделает недействительным тип носителя приемника потока.</span><span class="sxs-lookup"><span data-stu-id="ccf6a-112">A stream sink can raise this even if something happens that invalidates the stream sink's media type.</span></span> <span data-ttu-id="ccf6a-113">Например, расширенный обработчик видео (Евр) отправляет это событие при изменении отображения.</span><span class="sxs-lookup"><span data-stu-id="ccf6a-113">For example, the enhanced video renderer (EVR) sends this event when the display changes.</span></span>

<span data-ttu-id="ccf6a-114">Значение **HRESULT** , полученное с помощью [**имфмедиаевент::-Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) , может означать, почему тип мультимедиа больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="ccf6a-114">The **HRESULT** value retrieved by [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) might indicate why the media type is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf6a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ccf6a-115">Requirements</span></span>



| <span data-ttu-id="ccf6a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ccf6a-116">Requirement</span></span> | <span data-ttu-id="ccf6a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ccf6a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf6a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ccf6a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf6a-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccf6a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ccf6a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ccf6a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf6a-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccf6a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ccf6a-122">Header</span><span class="sxs-lookup"><span data-stu-id="ccf6a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccf6a-123"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccf6a-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf6a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccf6a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf6a-125">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ccf6a-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="ccf6a-126">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="ccf6a-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




