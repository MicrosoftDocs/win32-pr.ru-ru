---
description: Генерируется модулем подготовки звука при завершении работы системы Windows Audio Server. Модуль подготовки звука теперь недействителен.
ms.assetid: 8e80903c-d6ce-4fa2-87db-552c7fba3c6a
title: Событие Меаудиосессионсервершутдовн (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d819d850df481477b2ea1a5052c18d140a41cdb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719383"
---
# <a name="meaudiosessionservershutdown-event"></a><span data-ttu-id="4cb3f-104">Событие Меаудиосессионсервершутдовн</span><span class="sxs-lookup"><span data-stu-id="4cb3f-104">MEAudioSessionServerShutdown event</span></span>

<span data-ttu-id="4cb3f-105">Генерируется модулем подготовки звука при завершении работы системы Windows Audio Server.</span><span class="sxs-lookup"><span data-stu-id="4cb3f-105">Raised by the audio renderer when the Windows audio server system is shut down.</span></span> <span data-ttu-id="4cb3f-106">Модуль подготовки звука теперь недействителен.</span><span class="sxs-lookup"><span data-stu-id="4cb3f-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="4cb3f-107">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="4cb3f-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="4cb3f-108">Значения событий</span><span class="sxs-lookup"><span data-stu-id="4cb3f-108">Event values</span></span>

<span data-ttu-id="4cb3f-109">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="4cb3f-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4cb3f-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4cb3f-110">VARTYPE</span></span>                | <span data-ttu-id="4cb3f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4cb3f-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb3f-112">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="4cb3f-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="4cb3f-113">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="4cb3f-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="4cb3f-114">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="4cb3f-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="4cb3f-115">Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="4cb3f-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4cb3f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cb3f-116">Remarks</span></span>

<span data-ttu-id="4cb3f-117">Это событие отправляется приемником потока модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="4cb3f-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="4cb3f-118">Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: онсессиондисконнектед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) из сеанса аудио с причиной разрыва соединения, равным **дисконнектреасонсервершутдовн**.</span><span class="sxs-lookup"><span data-stu-id="4cb3f-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonServerShutdown**.</span></span>

<span data-ttu-id="4cb3f-119">Указатель [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , если он задан, неудобен, так как аудиопоток больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="4cb3f-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cb3f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4cb3f-120">Requirements</span></span>



| <span data-ttu-id="4cb3f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4cb3f-121">Requirement</span></span> | <span data-ttu-id="4cb3f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4cb3f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb3f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cb3f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb3f-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cb3f-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4cb3f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cb3f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb3f-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4cb3f-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4cb3f-127">Header</span><span class="sxs-lookup"><span data-stu-id="4cb3f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cb3f-128"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cb3f-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cb3f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cb3f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb3f-130">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4cb3f-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="4cb3f-131">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="4cb3f-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
