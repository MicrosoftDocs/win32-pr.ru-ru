---
description: Вызывается модулем подготовки звука при изменении параметров группирования для сеанса аудио.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Событие Меаудиосессионграупингпарамчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac115bb30a4c01247da537f3255e9bc40099e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263319"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a><span data-ttu-id="9ec8d-103">Событие Меаудиосессионграупингпарамчанжед</span><span class="sxs-lookup"><span data-stu-id="9ec8d-103">MEAudioSessionGroupingParamChanged event</span></span>

<span data-ttu-id="9ec8d-104">Вызывается модулем подготовки звука при изменении параметров группирования для сеанса аудио.</span><span class="sxs-lookup"><span data-stu-id="9ec8d-104">Raised by the audio renderer when the grouping parameters change for the audio session.</span></span>

<span data-ttu-id="9ec8d-105">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="9ec8d-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="9ec8d-106">Значения событий</span><span class="sxs-lookup"><span data-stu-id="9ec8d-106">Event values</span></span>

<span data-ttu-id="9ec8d-107">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="9ec8d-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9ec8d-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9ec8d-108">VARTYPE</span></span>                | <span data-ttu-id="9ec8d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9ec8d-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec8d-110">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="9ec8d-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="9ec8d-111">Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="9ec8d-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9ec8d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ec8d-112">Remarks</span></span>

<span data-ttu-id="9ec8d-113">Это событие отправляется приемником потока модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="9ec8d-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="9ec8d-114">Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: онграупингпарамчанжед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) из сеанса аудио.</span><span class="sxs-lookup"><span data-stu-id="9ec8d-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) event from the audio session.</span></span>

<span data-ttu-id="9ec8d-115">Чтобы получить новые параметры группирования, вызовите метод [**имфаудиополици:: жетграупингпарам**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span><span class="sxs-lookup"><span data-stu-id="9ec8d-115">To get the new grouping parameters, call [**IMFAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ec8d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9ec8d-116">Requirements</span></span>



| <span data-ttu-id="9ec8d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9ec8d-117">Requirement</span></span> | <span data-ttu-id="9ec8d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9ec8d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec8d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ec8d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec8d-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ec8d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9ec8d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ec8d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec8d-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ec8d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ec8d-123">Header</span><span class="sxs-lookup"><span data-stu-id="9ec8d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ec8d-124"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ec8d-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ec8d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ec8d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec8d-126">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9ec8d-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="9ec8d-127">**Имфаудиополици:: Жетграупингпарам**</span><span class="sxs-lookup"><span data-stu-id="9ec8d-127">**IMFAudioPolicy::GetGroupingParam**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[<span data-ttu-id="9ec8d-128">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="9ec8d-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
