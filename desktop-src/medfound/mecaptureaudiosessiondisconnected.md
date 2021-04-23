---
description: Отправляется источником аудиозаписи при отключении дессион, так как пользователь выполнил выход из сеанса служб терминалов Windows (ВТС).
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Событие Мекаптуреаудиосессиондисконнектед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae45ecded4a2a412525da70133845c2487aa604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154882"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a><span data-ttu-id="d93e8-103">Событие Мекаптуреаудиосессиондисконнектед</span><span class="sxs-lookup"><span data-stu-id="d93e8-103">MECaptureAudioSessionDisconnected event</span></span>

<span data-ttu-id="d93e8-104">Отправляется источником аудиозаписи при отключении дессион, так как пользователь выполнил выход из сеанса служб терминалов Windows (ВТС).</span><span class="sxs-lookup"><span data-stu-id="d93e8-104">Sent by an audio capture source when the audio dession is disconnected because the user logged off from a Windows Terminal Services (WTS) session.</span></span>

## <a name="event-values"></a><span data-ttu-id="d93e8-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="d93e8-105">Event values</span></span>

<span data-ttu-id="d93e8-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="d93e8-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d93e8-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d93e8-107">VARTYPE</span></span>               | <span data-ttu-id="d93e8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d93e8-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="d93e8-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="d93e8-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="d93e8-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="d93e8-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d93e8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d93e8-111">Remarks</span></span>

<span data-ttu-id="d93e8-112">Это событие отправляется потоком мультимедиа источника записи звука.</span><span class="sxs-lookup"><span data-stu-id="d93e8-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="d93e8-113">Источник захвата отправляет это событие при получении события [**иаудиосессионевентс:: онсессиондисконнектед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) из сеанса аудио с причиной отключения соединения, равной **дисконнектреасонсессиондисконнектед**.</span><span class="sxs-lookup"><span data-stu-id="d93e8-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonSessionDisconnected**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d93e8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d93e8-114">Requirements</span></span>



| <span data-ttu-id="d93e8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d93e8-115">Requirement</span></span> | <span data-ttu-id="d93e8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d93e8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d93e8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d93e8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d93e8-118">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d93e8-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d93e8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d93e8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d93e8-120">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d93e8-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d93e8-121">Header</span><span class="sxs-lookup"><span data-stu-id="d93e8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d93e8-122"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d93e8-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d93e8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d93e8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d93e8-124">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d93e8-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
