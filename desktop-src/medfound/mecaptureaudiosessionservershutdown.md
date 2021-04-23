---
description: Отправляется источником записи звука, когда сеанс записи звука отключается из-за завершения работы сервера аудио.
ms.assetid: 43284B3E-3018-44F3-8D6C-8C3041DCCD3E
title: Событие Мекаптуреаудиосессионсервершутдовн (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad934f6d60868c1db7c5b5b7907ff720312ea439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719596"
---
# <a name="mecaptureaudiosessionservershutdown-event"></a><span data-ttu-id="647da-103">Событие Мекаптуреаудиосессионсервершутдовн</span><span class="sxs-lookup"><span data-stu-id="647da-103">MECaptureAudioSessionServerShutdown event</span></span>

<span data-ttu-id="647da-104">Отправляется источником записи звука, когда сеанс записи звука отключается из-за завершения работы сервера аудио.</span><span class="sxs-lookup"><span data-stu-id="647da-104">Sent by an audio capture source when the capture audio session is disconnected due to the audio server being shutdown.</span></span>

## <a name="event-values"></a><span data-ttu-id="647da-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="647da-105">Event values</span></span>

<span data-ttu-id="647da-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="647da-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="647da-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="647da-107">VARTYPE</span></span>               | <span data-ttu-id="647da-108">Описание</span><span class="sxs-lookup"><span data-stu-id="647da-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="647da-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="647da-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="647da-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="647da-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="647da-111">Требования</span><span class="sxs-lookup"><span data-stu-id="647da-111">Requirements</span></span>



| <span data-ttu-id="647da-112">Требование</span><span class="sxs-lookup"><span data-stu-id="647da-112">Requirement</span></span> | <span data-ttu-id="647da-113">Значение</span><span class="sxs-lookup"><span data-stu-id="647da-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="647da-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="647da-114">Minimum supported client</span></span><br/> | <span data-ttu-id="647da-115">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="647da-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="647da-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="647da-116">Minimum supported server</span></span><br/> | <span data-ttu-id="647da-117">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="647da-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="647da-118">Header</span><span class="sxs-lookup"><span data-stu-id="647da-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="647da-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="647da-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="647da-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="647da-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="647da-121">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="647da-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




