---
description: Генерируется модулем подготовки звука при изменении звукового формата по умолчанию для звукового устройства. Модуль подготовки звука теперь недействителен.
ms.assetid: eeef764a-f6d2-4f6e-9af3-acd5fd7bc55c
title: Событие Меаудиосессионформатчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1faddc73622c65d1eb32e0d723f576b9410d978b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897838"
---
# <a name="meaudiosessionformatchanged-event"></a><span data-ttu-id="cd0e8-104">Событие Меаудиосессионформатчанжед</span><span class="sxs-lookup"><span data-stu-id="cd0e8-104">MEAudioSessionFormatChanged event</span></span>

<span data-ttu-id="cd0e8-105">Генерируется модулем подготовки звука при изменении звукового формата по умолчанию для звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-105">Raised by the audio renderer when the default audio format for the audio device changes.</span></span> <span data-ttu-id="cd0e8-106">Модуль подготовки звука теперь недействителен.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="cd0e8-107">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="cd0e8-108">Значения событий</span><span class="sxs-lookup"><span data-stu-id="cd0e8-108">Event values</span></span>

<span data-ttu-id="cd0e8-109">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cd0e8-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cd0e8-110">VARTYPE</span></span>                | <span data-ttu-id="cd0e8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cd0e8-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd0e8-112">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="cd0e8-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="cd0e8-113">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="cd0e8-114">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="cd0e8-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="cd0e8-115">Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="cd0e8-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="cd0e8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd0e8-116">Remarks</span></span>

<span data-ttu-id="cd0e8-117">Это событие отправляется приемником потока модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="cd0e8-118">Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: онсессиондисконнектед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) из сеанса звука пользовательского режима с причиной разрыва соединения, равным **дисконнектреасонформатчанжед**.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the user-mode audio session with the disconnection reason equal to **DisconnectReasonFormatChanged**.</span></span>

<span data-ttu-id="cd0e8-119">Указатель [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , если он задан, неудобен, так как аудиопоток больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd0e8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cd0e8-120">Requirements</span></span>



| <span data-ttu-id="cd0e8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cd0e8-121">Requirement</span></span> | <span data-ttu-id="cd0e8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cd0e8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd0e8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd0e8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cd0e8-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd0e8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cd0e8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd0e8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cd0e8-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd0e8-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd0e8-127">Header</span><span class="sxs-lookup"><span data-stu-id="cd0e8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd0e8-128"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd0e8-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd0e8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd0e8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd0e8-130">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cd0e8-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="cd0e8-131">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="cd0e8-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
