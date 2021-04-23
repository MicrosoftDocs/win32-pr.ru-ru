---
description: 'Возникает, когда источник мультимедиа выполняет поиск в новой должности. Источник мультимедиа вызывает это событие, если источник запущен или приостановлен, а приложение вызывает Имфмедиасаурце:: Start с временем начала, которое не равно текущей позицией.'
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Событие Месаурцесикед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711222"
---
# <a name="mesourceseeked-event"></a><span data-ttu-id="0d821-104">Событие Месаурцесикед</span><span class="sxs-lookup"><span data-stu-id="0d821-104">MESourceSeeked event</span></span>

<span data-ttu-id="0d821-105">Возникает, когда источник мультимедиа выполняет поиск в новой должности.</span><span class="sxs-lookup"><span data-stu-id="0d821-105">Raised when a media source seeks to a new position.</span></span> <span data-ttu-id="0d821-106">Источник мультимедиа вызывает это событие, если источник запущен или приостановлен, а приложение вызывает [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) с временем начала, которое не равно текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="0d821-106">A media source raises this event if the source is running or paused and the application calls [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) with a start time that does not equal the current position.</span></span>

## <a name="event-values"></a><span data-ttu-id="0d821-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="0d821-107">Event values</span></span>

<span data-ttu-id="0d821-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="0d821-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0d821-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0d821-109">VARTYPE</span></span>           | <span data-ttu-id="0d821-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0d821-110">Description</span></span>                                                                |
|-------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="0d821-111">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="0d821-111">VT\_I8</span></span><br/> | <span data-ttu-id="0d821-112">Новая начальная позицией в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="0d821-112">The new starting position, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="0d821-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0d821-113">Requirements</span></span>



| <span data-ttu-id="0d821-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0d821-114">Requirement</span></span> | <span data-ttu-id="0d821-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0d821-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d821-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d821-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0d821-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d821-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0d821-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d821-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0d821-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d821-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0d821-120">Header</span><span class="sxs-lookup"><span data-stu-id="0d821-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d821-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d821-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d821-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d821-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d821-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d821-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




