---
description: Отправляется модулем подготовки потоковой передачи звука (САР) при изменении тома или выключения состояния сеанса звука.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Событие Меаудиосессионволумечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719382"
---
# <a name="meaudiosessionvolumechanged-event"></a><span data-ttu-id="4e3b6-103">Событие Меаудиосессионволумечанжед</span><span class="sxs-lookup"><span data-stu-id="4e3b6-103">MEAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="4e3b6-104">Отправляется модулем подготовки потоковой передачи звука (САР) при изменении тома или выключения состояния сеанса звука.</span><span class="sxs-lookup"><span data-stu-id="4e3b6-104">Sent by the streaming audio renderer (SAR) when the volume or mute state of the audio session changes.</span></span>

<span data-ttu-id="4e3b6-105">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="4e3b6-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="4e3b6-106">Значения событий</span><span class="sxs-lookup"><span data-stu-id="4e3b6-106">Event values</span></span>

<span data-ttu-id="4e3b6-107">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="4e3b6-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4e3b6-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4e3b6-108">VARTYPE</span></span>                | <span data-ttu-id="4e3b6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4e3b6-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3b6-110">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="4e3b6-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="4e3b6-111">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="4e3b6-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="4e3b6-112">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="4e3b6-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="4e3b6-113">Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="4e3b6-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4e3b6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e3b6-114">Remarks</span></span>

<span data-ttu-id="4e3b6-115">Это событие вызывается приемником потока в области САР.</span><span class="sxs-lookup"><span data-stu-id="4e3b6-115">This event is raised by the stream sink of the SAR.</span></span> <span data-ttu-id="4e3b6-116">Событие активируется, когда Макао получает событие [**иаудиосессионевентс:: онсимплеволумечанжед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) из сеанса аудио.</span><span class="sxs-lookup"><span data-stu-id="4e3b6-116">The event is triggered when the SAR receives an [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) event from the audio session.</span></span> <span data-ttu-id="4e3b6-117">Чтобы получить новый уровень громкости и выключить его состояние, вызовите [**имфсимплеаудиоволуме:: жетмастерволуме**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) и [**Имфсимплеаудиоволуме:: вкл**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span><span class="sxs-lookup"><span data-stu-id="4e3b6-117">To get the new volume level and mute state, call [**IMFSimpleAudioVolume::GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) and [**IMFSimpleAudioVolume::GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span></span>

<span data-ttu-id="4e3b6-118">Это событие отправляется в том случае, если внешнее действие изменяет том, например, если пользователь изменяет том с помощью программы системного управления громкостью (Сндвол).</span><span class="sxs-lookup"><span data-stu-id="4e3b6-118">The SAR sends this event if an external action changes the volume—for example, if the user changes the volume through the system volume-control program (SndVol).</span></span> <span data-ttu-id="4e3b6-119">САР не отправляет событие, если приложение изменяет том непосредственно в САР.</span><span class="sxs-lookup"><span data-stu-id="4e3b6-119">The SAR does not send the event if the application changes the volume directly on the SAR.</span></span>

<span data-ttu-id="4e3b6-120">Кроме того, Макао не отправляет это событие при изменении громкости канала ([**иаудиосессионевентс:: ончаннелволумечанжед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span><span class="sxs-lookup"><span data-stu-id="4e3b6-120">Also, the SAR does not send this event when the channel volume changes ([**IAudioSessionEvents::OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e3b6-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4e3b6-121">Requirements</span></span>



| <span data-ttu-id="4e3b6-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4e3b6-122">Requirement</span></span> | <span data-ttu-id="4e3b6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4e3b6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3b6-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e3b6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4e3b6-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e3b6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4e3b6-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e3b6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4e3b6-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e3b6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4e3b6-128">Header</span><span class="sxs-lookup"><span data-stu-id="4e3b6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e3b6-129"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e3b6-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e3b6-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e3b6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e3b6-131">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4e3b6-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="4e3b6-132">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="4e3b6-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
