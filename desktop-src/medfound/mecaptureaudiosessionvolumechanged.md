---
description: Отправляется источником аудиозаписи при изменении тома.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Событие Мекаптуреаудиосессионволумечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719395"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a><span data-ttu-id="b7330-103">Событие Мекаптуреаудиосессионволумечанжед</span><span class="sxs-lookup"><span data-stu-id="b7330-103">MECaptureAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="b7330-104">Отправляется источником аудиозаписи при изменении тома.</span><span class="sxs-lookup"><span data-stu-id="b7330-104">Sent by an audio capture source when the volume changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="b7330-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="b7330-105">Event values</span></span>

<span data-ttu-id="b7330-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="b7330-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b7330-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b7330-107">VARTYPE</span></span>               | <span data-ttu-id="b7330-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b7330-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="b7330-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="b7330-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="b7330-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="b7330-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b7330-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7330-111">Remarks</span></span>

<span data-ttu-id="b7330-112">Это событие отправляется потоком мультимедиа источника записи звука.</span><span class="sxs-lookup"><span data-stu-id="b7330-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="b7330-113">Источник записи звука отправляет это событие при изменении тома внешним действием, например, если пользователь изменяет том с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="b7330-113">The audio capture source sends this event if an external action changes the volume—for example, if the user changes the volume through the Control Panel.</span></span> <span data-ttu-id="b7330-114">Источник записи не отправляет событие, если приложение изменяет том непосредственно в источнике.</span><span class="sxs-lookup"><span data-stu-id="b7330-114">The capture source does not send the event if the application changes the volume directly on the source.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7330-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b7330-115">Requirements</span></span>



| <span data-ttu-id="b7330-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b7330-116">Requirement</span></span> | <span data-ttu-id="b7330-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b7330-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7330-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7330-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b7330-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b7330-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="b7330-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7330-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b7330-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b7330-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b7330-122">Header</span><span class="sxs-lookup"><span data-stu-id="b7330-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7330-123"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7330-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7330-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7330-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7330-125">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7330-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




