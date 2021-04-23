---
description: Генерируется модулем подготовки звука при прерывании сеанса звука в режиме монопольного подключения. Модуль подготовки звука теперь недействителен.
ms.assetid: f89acfe4-14a7-4051-a816-e5e0ba8db80a
title: Событие Меаудиосессионексклусивемодеоверриде (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3732be3fec73e3e948f6093187f32dd46839bea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263320"
---
# <a name="meaudiosessionexclusivemodeoverride-event"></a><span data-ttu-id="3a255-104">Событие Меаудиосессионексклусивемодеоверриде</span><span class="sxs-lookup"><span data-stu-id="3a255-104">MEAudioSessionExclusiveModeOverride event</span></span>

<span data-ttu-id="3a255-105">Генерируется модулем подготовки звука при прерывании сеанса звука в режиме монопольного подключения.</span><span class="sxs-lookup"><span data-stu-id="3a255-105">Raised by the audio renderer when the audio session is preempted by an exclusive-mode connection.</span></span> <span data-ttu-id="3a255-106">Модуль подготовки звука теперь недействителен.</span><span class="sxs-lookup"><span data-stu-id="3a255-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="3a255-107">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="3a255-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="3a255-108">Значения событий</span><span class="sxs-lookup"><span data-stu-id="3a255-108">Event values</span></span>

<span data-ttu-id="3a255-109">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="3a255-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3a255-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3a255-110">VARTYPE</span></span>                | <span data-ttu-id="3a255-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3a255-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a255-112">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="3a255-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="3a255-113">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="3a255-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="3a255-114">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="3a255-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="3a255-115">Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="3a255-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3a255-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a255-116">Remarks</span></span>

<span data-ttu-id="3a255-117">Это событие отправляется приемником потока модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="3a255-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="3a255-118">Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: онсессиондисконнектед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) из сеанса аудио с причиной разрыва соединения, равным дисконнектреасонексклусивемодеоверриде.</span><span class="sxs-lookup"><span data-stu-id="3a255-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to DisconnectReasonExclusiveModeOverride.</span></span>

<span data-ttu-id="3a255-119">Указатель [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , если он задан, неудобен, так как аудиопоток больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3a255-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a255-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3a255-120">Requirements</span></span>



| <span data-ttu-id="3a255-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3a255-121">Requirement</span></span> | <span data-ttu-id="3a255-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3a255-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a255-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a255-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3a255-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a255-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3a255-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a255-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3a255-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a255-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a255-127">Header</span><span class="sxs-lookup"><span data-stu-id="3a255-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a255-128"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a255-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a255-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a255-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a255-130">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a255-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3a255-131">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="3a255-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
