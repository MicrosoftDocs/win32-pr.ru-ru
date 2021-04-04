---
description: Генерируется модулем подготовки звука при изменении отображаемого имени сеанса звука.
ms.assetid: d180b145-88e1-4f85-b001-b76140ca39d8
title: Событие Меаудиосессионнамечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb06244c196ab55bbd93e12ebff6a6a394176cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810810"
---
# <a name="meaudiosessionnamechanged-event"></a><span data-ttu-id="93a55-103">Событие Меаудиосессионнамечанжед</span><span class="sxs-lookup"><span data-stu-id="93a55-103">MEAudioSessionNameChanged event</span></span>

<span data-ttu-id="93a55-104">Генерируется модулем подготовки звука при изменении отображаемого имени сеанса звука.</span><span class="sxs-lookup"><span data-stu-id="93a55-104">Raised by the audio renderer when the audio session display name changes.</span></span>

<span data-ttu-id="93a55-105">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="93a55-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="93a55-106">Значения событий</span><span class="sxs-lookup"><span data-stu-id="93a55-106">Event values</span></span>

<span data-ttu-id="93a55-107">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="93a55-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="93a55-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="93a55-108">VARTYPE</span></span>                | <span data-ttu-id="93a55-109">Описание</span><span class="sxs-lookup"><span data-stu-id="93a55-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a55-110">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="93a55-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="93a55-111">Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="93a55-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="93a55-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93a55-112">Remarks</span></span>

<span data-ttu-id="93a55-113">Это событие отправляется приемником потока модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="93a55-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="93a55-114">Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: ондисплайнамечанжед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) из сеанса аудио.</span><span class="sxs-lookup"><span data-stu-id="93a55-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnDisplayNameChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) event from the audio session.</span></span>

<span data-ttu-id="93a55-115">Чтобы получить новое отображаемое имя, вызовите [**имфаудиополици::**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)lt.</span><span class="sxs-lookup"><span data-stu-id="93a55-115">To get the new display name, call [**IMFAudioPolicy::GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span></span>

## <a name="requirements"></a><span data-ttu-id="93a55-116">Требования</span><span class="sxs-lookup"><span data-stu-id="93a55-116">Requirements</span></span>



| <span data-ttu-id="93a55-117">Требование</span><span class="sxs-lookup"><span data-stu-id="93a55-117">Requirement</span></span> | <span data-ttu-id="93a55-118">Значение</span><span class="sxs-lookup"><span data-stu-id="93a55-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a55-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93a55-119">Minimum supported client</span></span><br/> | <span data-ttu-id="93a55-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93a55-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="93a55-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93a55-121">Minimum supported server</span></span><br/> | <span data-ttu-id="93a55-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93a55-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="93a55-123">Header</span><span class="sxs-lookup"><span data-stu-id="93a55-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="93a55-124"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93a55-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93a55-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93a55-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a55-126">**Имфаудиополици::/DisplayName**</span><span class="sxs-lookup"><span data-stu-id="93a55-126">**IMFAudioPolicy::GetDisplayName**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)
</dt> <dt>

[<span data-ttu-id="93a55-127">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="93a55-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="93a55-128">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="93a55-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
