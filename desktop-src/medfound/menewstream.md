---
description: Вызывается источником мультимедиа при запуске нового потока.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Событие Меневстреам (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692674"
---
# <a name="menewstream-event"></a><span data-ttu-id="27a7d-103">Событие Меневстреам</span><span class="sxs-lookup"><span data-stu-id="27a7d-103">MENewStream event</span></span>

<span data-ttu-id="27a7d-104">Вызывается источником мультимедиа при запуске нового потока.</span><span class="sxs-lookup"><span data-stu-id="27a7d-104">Raised by a media source when it starts a new stream.</span></span>

<span data-ttu-id="27a7d-105">Когда метод [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) вызывается для источника мультимедиа, источник мультимедиа отправляет одно событие для каждого выбранного потока:</span><span class="sxs-lookup"><span data-stu-id="27a7d-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="27a7d-106">Источник отправляет событие Меневстреам, если поток не был выбран в предыдущем вызове [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), или это самый первый вызов для **запуска** в этом источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="27a7d-106">The source sends the MENewStream event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="27a7d-107">Источник отправляет событие [меупдатедстреам](meupdatedstream.md) , если поток уже был выбран в предыдущем вызове [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="27a7d-107">The source sends the [MEUpdatedStream](meupdatedstream.md) event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="27a7d-108">Для невыбранных потоков события не отправляются.</span><span class="sxs-lookup"><span data-stu-id="27a7d-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="27a7d-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="27a7d-109">Event values</span></span>

<span data-ttu-id="27a7d-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="27a7d-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="27a7d-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="27a7d-111">VARTYPE</span></span>                | <span data-ttu-id="27a7d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="27a7d-112">Description</span></span>                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a7d-113">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="27a7d-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="27a7d-114">Содержит указатель на интерфейс [**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) потока.</span><span class="sxs-lookup"><span data-stu-id="27a7d-114">Contains a pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="27a7d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="27a7d-115">Requirements</span></span>



| <span data-ttu-id="27a7d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="27a7d-116">Requirement</span></span> | <span data-ttu-id="27a7d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="27a7d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a7d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27a7d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="27a7d-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27a7d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="27a7d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27a7d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="27a7d-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27a7d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="27a7d-122">Header</span><span class="sxs-lookup"><span data-stu-id="27a7d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="27a7d-123"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27a7d-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27a7d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27a7d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a7d-125">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="27a7d-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




