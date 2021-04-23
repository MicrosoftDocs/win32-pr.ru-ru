---
description: Отправляется источником аудиозаписи, когда звуковое устройство открывается другой программой в монопольном режиме.
ms.assetid: E9CC8507-38AB-4049-8DAC-767EC0ECE270
title: Событие Мекаптуреаудиосессионексклусивемодеоверриде (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2051e6073b06f62823b95c80d7d4cfaf21de2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809610"
---
# <a name="mecaptureaudiosessionexclusivemodeoverride-event"></a><span data-ttu-id="4c9e8-103">Событие Мекаптуреаудиосессионексклусивемодеоверриде</span><span class="sxs-lookup"><span data-stu-id="4c9e8-103">MECaptureAudioSessionExclusiveModeOverride event</span></span>

<span data-ttu-id="4c9e8-104">Отправляется источником аудиозаписи, когда звуковое устройство открывается другой программой в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="4c9e8-104">Sent by an audio capture source when another program opens the audio device in exclusive mode.</span></span>

## <a name="event-values"></a><span data-ttu-id="4c9e8-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="4c9e8-105">Event values</span></span>

<span data-ttu-id="4c9e8-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="4c9e8-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4c9e8-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4c9e8-107">VARTYPE</span></span>               | <span data-ttu-id="4c9e8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4c9e8-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="4c9e8-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="4c9e8-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="4c9e8-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="4c9e8-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4c9e8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c9e8-111">Remarks</span></span>

<span data-ttu-id="4c9e8-112">Это событие отправляется потоком мультимедиа источника записи звука.</span><span class="sxs-lookup"><span data-stu-id="4c9e8-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="4c9e8-113">Источник захвата отправляет это событие при получении события [**иаудиосессионевентс:: онсессиондисконнектед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) из сеанса аудио с причиной отключения соединения, равной **дисконнектреасонексклусивемодеоверриде**.</span><span class="sxs-lookup"><span data-stu-id="4c9e8-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonExclusiveModeOverride**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c9e8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4c9e8-114">Requirements</span></span>



| <span data-ttu-id="4c9e8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4c9e8-115">Requirement</span></span> | <span data-ttu-id="4c9e8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4c9e8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9e8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c9e8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4c9e8-118">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4c9e8-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="4c9e8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c9e8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4c9e8-120">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4c9e8-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4c9e8-121">Header</span><span class="sxs-lookup"><span data-stu-id="4c9e8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c9e8-122"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c9e8-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c9e8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c9e8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c9e8-124">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c9e8-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
