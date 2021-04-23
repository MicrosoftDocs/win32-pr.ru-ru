---
description: Генерируется модулем подготовки звука при удалении звукового устройства. Модуль подготовки звука теперь недействителен.
ms.assetid: a65a3931-e0d6-47ac-b545-9d616e914109
title: Событие Меаудиосессиондевицеремовед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8153eca68d480f092a358c35bfcbad7cedffd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539946"
---
# <a name="meaudiosessiondeviceremoved-event"></a><span data-ttu-id="b8745-104">Событие Меаудиосессиондевицеремовед</span><span class="sxs-lookup"><span data-stu-id="b8745-104">MEAudioSessionDeviceRemoved event</span></span>

<span data-ttu-id="b8745-105">Генерируется модулем подготовки звука при удалении звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="b8745-105">Raised by the audio renderer when the audio device is removed.</span></span> <span data-ttu-id="b8745-106">Модуль подготовки звука теперь недействителен.</span><span class="sxs-lookup"><span data-stu-id="b8745-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="b8745-107">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="b8745-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="b8745-108">Значения событий</span><span class="sxs-lookup"><span data-stu-id="b8745-108">Event values</span></span>

<span data-ttu-id="b8745-109">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="b8745-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b8745-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b8745-110">VARTYPE</span></span>                | <span data-ttu-id="b8745-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b8745-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8745-112">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="b8745-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="b8745-113">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="b8745-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="b8745-114">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="b8745-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="b8745-115">Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="b8745-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b8745-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8745-116">Remarks</span></span>

<span data-ttu-id="b8745-117">Это событие отправляется приемником потока модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="b8745-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="b8745-118">Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: онсессиондисконнектед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) из сеанса аудио с причиной разрыва соединения, равным **дисконнектреасондевицеремовал**.</span><span class="sxs-lookup"><span data-stu-id="b8745-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonDeviceRemoval**.</span></span>

<span data-ttu-id="b8745-119">Указатель [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , если он задан, неудобен, так как аудиопоток больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="b8745-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8745-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b8745-120">Requirements</span></span>



| <span data-ttu-id="b8745-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b8745-121">Requirement</span></span> | <span data-ttu-id="b8745-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b8745-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8745-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8745-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b8745-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8745-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b8745-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8745-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b8745-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8745-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b8745-127">Header</span><span class="sxs-lookup"><span data-stu-id="b8745-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8745-128"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8745-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8745-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8745-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8745-130">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b8745-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="b8745-131">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="b8745-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
