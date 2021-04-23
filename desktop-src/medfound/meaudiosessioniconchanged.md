---
description: Вызывается модулем подготовки звука при изменении значка сеанса звука.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Событие Меаудиосессионикончанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719384"
---
# <a name="meaudiosessioniconchanged-event"></a><span data-ttu-id="3ef0c-103">Событие Меаудиосессионикончанжед</span><span class="sxs-lookup"><span data-stu-id="3ef0c-103">MEAudioSessionIconChanged event</span></span>

<span data-ttu-id="3ef0c-104">Вызывается модулем подготовки звука при изменении значка сеанса звука.</span><span class="sxs-lookup"><span data-stu-id="3ef0c-104">Raised by the audio renderer when the audio session icon changes.</span></span>

<span data-ttu-id="3ef0c-105">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="3ef0c-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="3ef0c-106">Значения событий</span><span class="sxs-lookup"><span data-stu-id="3ef0c-106">Event values</span></span>

<span data-ttu-id="3ef0c-107">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="3ef0c-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3ef0c-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3ef0c-108">VARTYPE</span></span>                | <span data-ttu-id="3ef0c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3ef0c-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef0c-110">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="3ef0c-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="3ef0c-111">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="3ef0c-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="3ef0c-112">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="3ef0c-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="3ef0c-113">Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="3ef0c-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3ef0c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ef0c-114">Remarks</span></span>

<span data-ttu-id="3ef0c-115">Это событие отправляется приемником потока модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="3ef0c-115">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="3ef0c-116">Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: ониконпасчанжед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) из сеанса аудио.</span><span class="sxs-lookup"><span data-stu-id="3ef0c-116">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) event from the audio session.</span></span>

<span data-ttu-id="3ef0c-117">Чтобы получить новый значок, вызовите метод [**имфаудиополици:: жетиконпас**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span><span class="sxs-lookup"><span data-stu-id="3ef0c-117">To get the new icon, call [**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef0c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3ef0c-118">Requirements</span></span>



| <span data-ttu-id="3ef0c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3ef0c-119">Requirement</span></span> | <span data-ttu-id="3ef0c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3ef0c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef0c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ef0c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ef0c-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ef0c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3ef0c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ef0c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ef0c-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ef0c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3ef0c-125">Header</span><span class="sxs-lookup"><span data-stu-id="3ef0c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ef0c-126"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ef0c-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ef0c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ef0c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef0c-128">**Имфаудиополици:: Жетиконпас**</span><span class="sxs-lookup"><span data-stu-id="3ef0c-128">**IMFAudioPolicy::GetIconPath**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[<span data-ttu-id="3ef0c-129">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3ef0c-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3ef0c-130">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="3ef0c-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
