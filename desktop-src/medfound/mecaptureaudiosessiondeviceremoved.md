---
description: Отправляется источником записи звука при удалении устройства.
ms.assetid: A249D8B4-15A8-4AD3-8316-2886E5C37825
title: Событие Мекаптуреаудиосессиондевицеремовед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0cf1b9a7536affed5a4665f6f2e364e1f872e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719712"
---
# <a name="mecaptureaudiosessiondeviceremoved-event"></a><span data-ttu-id="1ab27-103">Событие Мекаптуреаудиосессиондевицеремовед</span><span class="sxs-lookup"><span data-stu-id="1ab27-103">MECaptureAudioSessionDeviceRemoved event</span></span>

<span data-ttu-id="1ab27-104">Отправляется источником записи звука при удалении устройства.</span><span class="sxs-lookup"><span data-stu-id="1ab27-104">Sent by an audio capture source when the device is removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="1ab27-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="1ab27-105">Event values</span></span>

<span data-ttu-id="1ab27-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="1ab27-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1ab27-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1ab27-107">VARTYPE</span></span>               | <span data-ttu-id="1ab27-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1ab27-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="1ab27-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="1ab27-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="1ab27-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="1ab27-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1ab27-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ab27-111">Remarks</span></span>

<span data-ttu-id="1ab27-112">Это событие отправляется потоком мультимедиа источника записи звука.</span><span class="sxs-lookup"><span data-stu-id="1ab27-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="1ab27-113">Источник захвата отправляет это событие при получении события [**иаудиосессионевентс:: онсессиондисконнектед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) из сеанса аудио с причиной отключения соединения, равной **дисконнектреасондевицеремовал**.</span><span class="sxs-lookup"><span data-stu-id="1ab27-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonDeviceRemoval**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ab27-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1ab27-114">Requirements</span></span>



| <span data-ttu-id="1ab27-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1ab27-115">Requirement</span></span> | <span data-ttu-id="1ab27-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab27-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab27-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ab27-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1ab27-118">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1ab27-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="1ab27-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ab27-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1ab27-120">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1ab27-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ab27-121">Header</span><span class="sxs-lookup"><span data-stu-id="1ab27-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ab27-122"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ab27-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ab27-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ab27-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab27-124">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ab27-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
